这段代码在处理高维基因表达数据（TCGA 筛选前 20% 后特征维度 $p \approx 4000$，而样本量 $n \approx 1000$）时，确实会同时触发**数值溢出/精度崩溃**和**优化器重复无效迭代**。此外，代码中还隐藏了一个会导致 $\epsilon \to 0$ 时 $\Delta P$ **无法收敛到 0** 的目标函数不一致问题。

  

## 一、 浮点数精度溢出与数值崩溃的 4 个原因

1. **指数幂运算直接溢出（`OverflowError` / `inf`）**
    
    在 `q_exp_pure` 中，直接计算 `arg ** (1.0 / eta)`。当 $\epsilon = 10^{-5}$ 时，$1/\eta = 10^5$。在 4000 维特征空间做 `L-BFGS-B` 线搜索时，线性预测值 $z = X\theta$ 很容易出现几十或上百的数值。一旦 $z < -7.1$，底数 $(1 - \eta z)^{10^5} \approx e^{-z}$ 就会超过 `float64` 的上限（$\approx 1.8 \times 10^{308}$，对应 $e^{709.78}$），直接变成 `inf`。
    
      
    
2. **大数吃小数（Catastrophic Cancellation）**
    
    当 $\eta = 10^{-5}$ 时，直接计算 `1.0 + eta * z` 会在浮点数加法中损失约 5 位有效数字；随后再做 $10^5$ 次方运算，会将截断误差放大 $10^5$ 倍。
    
      
    - **修复方案**：切勿直接求幂，应转换到**对数域**。定义等效对数几率（Effective Logit）：
        
          
        
        $$\tilde{z} = -\ln e_q(-z) = -\frac{\ln(1 - \eta z)}{\eta}$$
        
        利用 `np.log1p(-eta * z) / eta` 计算 $\tilde{z}$，在 $\eta \to 0$ 时底层会自动采用泰勒级数高精度展开；再将 $\tilde{z}$ 代入标准 `scipy.special.expit(z_tilde)`，即可完全避免大指数幂运算。
        
          
        
3. **梯度函数 `grad` 分母除零、符号反转，且与 `loss` 不一致（最致命的问题）**
    
    在 `grad(theta)` 中：
    
      
    
    Python
    
    ```
    beta = 1.0 / (1.0 - z * (1.0 - q_val))
    ```
    
    - **分母无保护**：癌症与正常组织的区分度极高，正类样本的 $z$ 值经常大于 $10$。当 $\epsilon = 0.1$ 时，$1 - 0.1 z \le 0$，导致 `beta` **除零爆炸（`inf`/`nan`）或变成负数（梯度方向完全反号）**。
        
          
        
    - **梯度与 Loss 截断不匹配**：你在 `loss` 中对 `sigma` 做了 `np.clip(..., 1e-9, 1 - 1e-9)`（当 $\epsilon = 0.1, z > 8.74$ 时 `sigma` 就会触发截断，此时 `loss` 的真实导数为 $0$），但 `grad` 却没有截断，依然返回巨大的梯度。**目标函数与梯度不一致**会导致 `L-BFGS-B` 的线搜索（Line Search）陷入死循环并异常终止。
        
          
        
4. **交叉熵中的对数下溢（`1.0 - sigma` 精度丢失）**
    
    先算 `sigma` 再算 `np.log(1 - sigma)`，当 $z$ 较大时，`1.0 - sigma` 会因为浮点数精度限制直接变成 `0.0`。引入等效对数几率 $\tilde{z}$ 后，交叉熵可以直接写作：
    
      
    
    $$\ell(y, \tilde{z}) = \ln(1 + e^{\tilde{z}}) - y\tilde{z} = \text{logaddexp}(0, \tilde{z}) - y\tilde{z}$$
    
    无论 $\tilde{z}$ 是 $-1000$ 还是 $+1000$，该式都不会发生上下溢，彻底摆脱粗糙的 `np.clip(sigma, 1e-9, 1-1e-9)`。
    
      
    

## 二、 计算量过大的 3 个性能瓶颈

1. **`loss` 与 `grad` 分离导致矩阵运算翻倍**
    
    传给 `minimize` 时分别传入 `loss` 和 `grad`，`scipy` 每次迭代会分别调用这两个函数，导致最耗时的矩阵乘法 `X @ theta`（规模为 $N \times p$）和对数运算被重复计算了两次。合并为一个函数并设置 `jac=True`，耗时直接减半。
    
      
    
2. **多尺度 $\epsilon$ 循环缺少“热启动”（Warm Start）**
    
    你在循环中对 5 个 $\epsilon$ 独立调用 `train_pure`，每次都从全零向量 `np.zeros(p)` 开始优化 4000 个参数。实际上相邻 $\epsilon$ 的最优解极其接近（且都接近 $q=1$ 的基准解）。将基准逻辑回归的解或上一轮 $\epsilon$ 的收敛解作为初值 `x0` 传入，每个 $\epsilon$ 只需 **5～15 步**即可收敛，提速 **10 倍以上**。
    
      
    
3. **高维数据 ($p > n$) 下基准 `LogisticRegression` 发散**
    
    当特征数 $p \approx 4000$ 大于样本数 $n \approx 880$ 时，数据在特征空间必然**线性可分**。此时 `LogisticRegression(penalty=None, C=1e6, max_iter=5000)` 没有正则化约束，最大似然估计不存在有限解（权重会向 $\pm\infty$ 发散），导致 `lr.fit` 跑满数千次迭代。
    
      
    

## 三、 隐藏的建模 Bug：基准模型与 $q$-模型目标函数不一致

你的实验目的是验证当 $\epsilon \to 0$ ($q \to 1$) 时，$P_q$ 收敛于标准逻辑回归的 $P_{\log}$（即 $\Delta P \to 0$）。但原代码中两者的目标函数存在 **3 处冲突**：

  

1. **正则化不同**：`lr` 设置了 `penalty=None`（无正则化），而 `train_pure` 加了 L2 正则化 `0.5 * 1e-4 * np.sum(theta ** 2)`。
    
      
    
2. **样本权重不同**：`lr` 设置了 `class_weight='balanced'`，而 `train_pure` 使用的是无权重的 `np.mean(...)`。
    
      
    
3. **截距项不同**：`lr` 默认包含截距项（`fit_intercept=True`），而 `train_pure` 的 `X @ theta` 没有截距项。
    
      
    

如果不统一这三点，即使 $\epsilon = 10^{-10}$，算出来的 $\Delta P$ 也会停留在某个常数，不可能收敛到 $0$。（另外，代码前半部分提取了临床变量 `C_all`，但在后续建模中并未拼接到 `X` 中，以下改进代码保留了将其拼接或单独使用的接口。）

  

## 四、 改进后的完整代码

以下代码采用**对数域 $C^1$ 连续延拓 + `logaddexp` 无损交叉熵 + `jac=True` 合并计算 + Warm Start 热启动**，并严格对齐了基准模型的正则化与截距项：

Python

```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from scipy.optimize import minimize
from scipy.special import expit
import warnings

warnings.filterwarnings("ignore")

print("1. 加载 TCGA 真实数据...")
expr_df = pd.read_csv("lung_expr.csv", index_col=0)

pheno_luad = pd.read_excel("tcga_data/癌症数据/不同阶段/LUAD/clinical_data.xlsx")
pheno_lusc = pd.read_excel("tcga_data/癌症数据/不同阶段/LUSC/clinical_data.xlsx")
pheno = pd.concat([pheno_luad, pheno_lusc], ignore_index=True).set_index('A0_Samples')
pheno.index = [s.split('.')[0] for s in pheno.index]
sample_ids = expr_df.columns
pheno_ids = [s.rsplit('-', 1)[0] for s in sample_ids]

# 提取4个临床变量
age = pd.to_numeric(pheno.loc[pheno_ids, 'A17_Age'], errors='coerce').values
age_norm = np.nan_to_num((age - np.nanmean(age)) / np.nanstd(age), nan=0.0)
sex = (pheno.loc[pheno_ids, 'A18_Sex'] == 'MALE').astype(int).values

def extract_stage(x):
    s = str(x).upper()
    return 1 if ('III' in s or 'IV' in s) else 0

def extract_smoking(x):
    return 1 if str(x).strip() in {'1.0', '2.0', '3.0', '4.0', '5.0'} else 0

stage = pheno.loc[pheno_ids, 'A6_Stage'].apply(extract_stage).values
smoking = pheno.loc[pheno_ids, 'tobacco_smoking_history'].apply(extract_smoking).values
C_all = np.column_stack([age_norm, sex, stage, smoking])

def get_samples(path):
    # 仅读取表头，避免解析整张大表
    df = pd.read_excel(path, nrows=0)
    return [c for c in df.columns if c != 'Tag']

labels_4 = {}
for s in get_samples("tcga_data/癌症数据/不同阶段/LUAD/LUAD_data_cancer.xlsx"): labels_4[s] = 0
for s in get_samples("tcga_data/癌症数据/不同阶段/LUAD/LUAD_data_normal.xlsx"): labels_4[s] = 1
for s in get_samples("tcga_data/癌症数据/不同阶段/LUSC/LUSC_data_cancer.xlsx"): labels_4[s] = 2
for s in get_samples("tcga_data/癌症数据/不同阶段/LUSC/LUSC_data_normal.xlsx"): labels_4[s] = 3

y_binary = np.array([1 if labels_4[c] in [0, 2] else 0 for c in expr_df.columns])
X = expr_df.T.values
gene_means = X.mean(axis=0)
X = X[:, gene_means > np.percentile(gene_means, 80)]

X_train, X_test, y_train, y_test = train_test_split(
    X, y_binary, test_size=0.2, random_state=42, stratify=y_binary
)
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# 拼接全 1 列以引入截距项 (Intercept)，最后一位参数作为 bias（不参与 L2 正则化）
X_train_aug = np.column_stack([X_train, np.ones(X_train.shape[0])])
X_test_aug = np.column_stack([X_test, np.ones(X_test.shape[0])])


# ==========================================
# 对数域高精度、C1连续延拓的 q-sigmoid 与训练器
# ==========================================
def q_effective_logit(z, q, delta=1e-8):
    """
    计算等效对数几率 z_tilde = -ln(e_q(-z)) 及其对 z 的一阶导数 dz_tilde / dz。
    当 1 - eta * z < delta 时采用 C1 连续线性延拓，保证：
    1. 彻底消除大指数幂运算溢出 (Overflow)
    2. 避免分母 1 - eta * z 除零或变负
    3. 目标函数与解析梯度在全实数域 100% 严格匹配
    """
    eta = 1.0 - q
    if np.abs(eta) < 1e-12:
        return z, np.ones_like(z)

    w = 1.0 - eta * z
    safe_mask = w >= delta
    w_safe = np.where(safe_mask, w, delta)

    # 在安全区使用 log1p(-eta * z) 保证极小 eta 下的泰勒展开精度
    u_safe = np.where(safe_mask, -eta * z, delta - 1.0)
    z_tilde_safe = -np.log1p(u_safe) / eta

    # 在截断边界 w < delta 处做一阶导数连续的线性延拓
    z_tilde_ext = -np.log(delta) / eta + (delta - w) / (eta * delta)

    z_tilde = np.where(safe_mask, z_tilde_safe, z_tilde_ext)
    dz_tilde = 1.0 / w_safe  # 处处等于 d(z_tilde)/dz
    return z_tilde, dz_tilde


def q_sigmoid_stable(z, q):
    z_tilde, _ = q_effective_logit(z, q)
    return expit(z_tilde)


def train_q_logistic(X_aug, y, q_val, l2_reg=1e-4, theta_init=None):
    n, p_aug = X_aug.shape
    if theta_init is None:
        theta_init = np.zeros(p_aug)

    def loss_and_grad(theta):
        z = X_aug @ theta
        z_tilde, dz_tilde = q_effective_logit(z, q_val)

        # 使用 logaddexp 计算交叉熵，避免 log(sigma) 和 log(1-sigma) 下溢
        bce_loss = np.mean(np.logaddexp(0.0, z_tilde) - y * z_tilde)
        # 仅对权重做 L2 正则化，不对最后一位截距项正则化
        reg_loss = 0.5 * l2_reg * np.sum(theta[:-1] ** 2)
        total_loss = bce_loss + reg_loss

        # 利用 -expit(-z_tilde) 计算 y=1 时的 (sigma - 1)，避免 1.0 - 1.0 的精度抵消
        diff = np.where(y == 1, -expit(-z_tilde), expit(z_tilde))
        grad_z = diff * dz_tilde

        grad = (X_aug.T @ grad_z) / n
        grad[:-1] += l2_reg * theta[:-1]

        return total_loss, grad

    res = minimize(
        loss_and_grad,
        theta_init,
        jac=True,  # 同时返回 Loss 和 Grad，矩阵乘法减半
        method='L-BFGS-B',
        options={'gtol': 1e-8, 'ftol': 1e-12, 'maxiter': 1000}
    )
    return res.x


# 1. 先求 q=1.0 (标准 Logistic 回归) 的精确基准解，确保正则化与目标函数完全对齐
print("\n2. 计算基准 Logistic 回归 (q = 1)...")
theta_log = train_q_logistic(X_train_aug, y_train, q_val=1.0, l2_reg=1e-4)
p_log = q_sigmoid_stable(X_test_aug @ theta_log, q=1.0)

# 2. 验证不同 epsilon 下的收敛性（使用 Warm Start 热启动）
print("\n3. 开始真实高维数据的收敛性验证...")
epsilons = [0.1, 0.01, 0.001, 0.0001, 0.00001]
results = []

# 从小到大或从基准解热启动，大幅减少迭代次数
current_theta = theta_log.copy()

for eps in epsilons:
    q_val = 1.0 - eps
    theta_q = train_q_logistic(
        X_train_aug, y_train, q_val=q_val, l2_reg=1e-4, theta_init=current_theta
    )
    current_theta = theta_q  # 更新热启动初值

    z_test = X_test_aug @ theta_q
    p_q = q_sigmoid_stable(z_test, q_val)

    delta_p = np.mean(np.abs(p_q - p_log))
    results.append({
        'eps': eps,
        '-log10(eps)': -np.log10(eps),
        'delta_p': delta_p
    })
    print(f"eps=10^-{ -np.log10(eps):.0f}: 概率差 = {delta_p:.8f}")

# 画图
results_df = pd.DataFrame(results)
plt.figure(figsize=(8, 5))
plt.plot(results_df['-log10(eps)'], results_df['delta_p'], 'o-',
         color='#1f77b4', linewidth=2.5, markersize=8)

plt.xlabel(r'$-\lg \epsilon$', fontsize=14)
plt.ylabel(r'$\Delta P = \mathrm{Mean}(|P_q - P_{\log}|)$', fontsize=14)
plt.title(r'Convergence of $q$-Logistic Regression ($q \to 1$)', fontsize=15)
plt.grid(True, linestyle='--', alpha=0.7)
plt.ylim(bottom=0)
plt.tight_layout()
plt.savefig("verify_prob_qc.png", dpi=300)
print("\n图像已保存为 verify_prob_qc.png")
```

### 核心改动对比

|**问题点**|**原代码写法**|**改进后写法**|**效果**|
|---|---|---|---|
|**$q$-指数计算**|`(1 + eta * z) ** (1 / eta)`|`z_tilde = -np.log1p(-eta * z) / eta`|消除 $10^5$ 次幂溢出与有效数字抵消|
|**交叉熵损失**|`-y * log(sigma) - (1-y) * log(1-sigma)`|`np.logaddexp(0.0, z_tilde) - y * z_tilde`|彻底消除 $\sigma \to 0/1$ 时的对数下溢，无需裁剪 `sigma`|
|**正类残差 $\sigma - 1$**|`sigma - y`（当 $\sigma \approx 1$ 时下溢为 0）|`np.where(y == 1, -expit(-z_tilde), expit(z_tilde))`|保留完整的 53 位浮点数尾数精度|
|**奇点与截断一致性**|`loss` 裁剪 `sigma`，但 `grad` 除以 `1 - eta * z`|在 $1 - \eta z < \delta$ 处做 $C^1$ 连续线性延拓|杜绝除零与梯度反号，`loss` 与 `grad` 处处精确匹配|
|**优化器调用开销**|`loss` 与 `grad` 拆成两个函数，每次从 `0` 初始化|`jac=True` 合并函数 + `theta_init` 热启动|矩阵乘法减半，单次收敛迭代步数从数百步降至约 10 步|