# Tsallis 统计扩展非传统非对称 IRT 的理论、数学与实证可行性评估

## 文献地图、已有先例与真正的方法学缺口

### 结论先行

基于截至 **2026 年 11 月 20 日** 的检索，我没有找到一个已经建立起来的、同行评审的研究传统，系统地把 **Tsallis $q$-指数 / $q$-sigmoid / $q$-Gaussian / 非加性熵** 用作二分 IRT 的项目反应函数并同时研究其**非对称性、拟合倾向 fitting propensity（FP）与反应模式 signature**。现有文献可以分成四个彼此相当分离的群体：第一类是非对称 IRT；第二类是 Tsallis 在认知与行为过程中的应用；第三类是 Tsallis/q-statistics 在神经信号和复杂系统中的应用；第四类是 Tsallis divergence 或 $q$-link 在机器学习与鲁棒统计中的应用。这个交叉处确实存在一个可发表的空白，但“Tsallis + IRT”本身不足以构成贡献；真正可辩护的空白是：

> **在控制参数复杂度、识别性与常规鲁棒替代模型以后，研究一种 Tsallis 诱导的非对称二项响应机制是否产生独特且可检验的 IRF 几何、拟合倾向和反应模式签名，并把 $q$ 与可观察的响应过程机制联系起来。**

Shim 与 Bonifay 的文章非常适合作为这一框架的“母论文”：它把 LPE、RH 和 AO 的差别从“哪个拟合更好”推进到了三个层次——**曲线几何、configural complexity 和 predicted data pattern**；而且明确指出相同参数个数并不意味着相同拟合倾向，甚至相同 FP 也不意味着相同数据模式偏好。fileciteturn1file0 该研究的 LPE 主要改变下尾，AO 主要改变上尾，RH 的非对称更集中在阈值及尾部附近；LPE 和 AO 的总体 FP 接近 2PL，而 RH 的 FP 较低，同时 LPE 更偏好低分与极端总分模式，AO 更偏好较高总分模式。fileciteturn1file2 这正好提供了判断一个 $q$-IRT 是否只是“又一条弯曲曲线”的标准。

非对称 IRT 本身已经相当成熟。Samejima 的 LPEF 早在 2000 年就把指数参数解释为与多步骤、合取式认知加工相关的 item complexity；该文发表于 *Psychometrika*，DOI **10.1007/BF02296149**。后续工作包括 Molenaar 的 heteroscedastic latent trait model，DOI **10.1007/s11336-014-9406-0**，以及 Shim、Bonifay、Wiedermann 的 CLL、NLL 与 cauchit 链接系列。CLL 研究表明非对称链接可以在不引入 3PL 猜测参数的情况下吸收某些极端响应行为；其 DOI 为 **10.3758/s13428-022-01824-5**。citeturn360215search5turn571000search23 2026 年 Feuerstahler 又专门讨论了怎样定义 IRT 中的 asymmetry，说明该领域的理论标准正在提高，而不是仅凭视觉上“有偏斜”即可声称新模型；DOI **10.1111/bmsp.70050**。citeturn571000search20turn571000search25

Shim–Bonifay 使用的 FP 框架也已有坚实的量化心理学先例。Bonifay 与 Cai 的工作指出，模型复杂度不能只数自由参数，因为 functional form 会改变模型拟合随机数据的倾向；Suh、Bonifay 与 Cai 进一步发展了适用于 IRT 的有限信息随机数据生成法，发表于 *Psychometrika* 2025，DOI **10.1017/psy.2025.10017**。citeturn571000search7turn571000search1 同一思想已经扩展到因子模型，并进入 *Psychological Methods*。citeturn571000search3turn571000search16 因此，如果 Tsallis 扩展只能展示 AIC 下降，它相对于这条文献线会显得明显不足；必须回答“**它拟合了什么类型的数据模式，以及为什么**”。

Tsallis 在心理学中的直接应用是有的，但集中在**行为动力学和信息表征**而不是 psychometric measurement。Takahashi 及合作者用 $q$-exponential 描述 delay discounting 与 subjective probability decay，其中 $q$ 被解释为随延迟变化的折扣不一致性或心理时间非线性；例如 *Physica A* 2012，DOI **10.1016/j.physa.2012.07.012**。citeturn731055search3 2014 年关于未来奖励主观概率衰减的研究也使用 $q$-exponential，DOI **10.3390/e16105537**。citeturn731055search0 Hadzibeganovic 与 Cannas 在 *Physica A* 2009 用 Tsallis entropy 构建具有非局部性的神经网络以模拟成人新词学习，DOI **10.1016/j.physa.2008.10.042**。citeturn847307search0turn847307search3 Cognitive Science 中 Crupi 等人的工作把 Tsallis、Rényi 等放进统一的 Sharma–Mittal 信息框架，并用行为数据讨论不同 entropy 模型的心理可解释性，DOI **10.1111/cogs.12613**。citeturn847307search2turn847307search12

在神经科学中，Tsallis entropy 更常见于 EEG/脑信号复杂性，而不是心理测量模型本身。例如 Parkinson 认知下降研究报告基线 EEG Tsallis entropy 与后续认知变化有关。citeturn847307search7turn847307search11 2026 年 APS Open Science 的一项 ADHD/典型儿童 EEG 研究则直接用 $q$-Gaussian 拟合振幅分布，并把 $q$ 解释为复杂性/近临界多尺度动力学的指标；DOI **10.1103/p73j-nq1w**。citeturn731055search7 这类工作可以帮助建立“非扩展性”理论背景，但不能自动移植到 IRT：EEG 多尺度相关并不证明某个测试的条件响应过程服从 Tsallis 机制。

与统计学习最接近的先例是 Amid、Warmuth 与 Srinivasan 的 two-temperature logistic regression，它从 Tsallis divergence 推导 tempered log/exp 损失，且证明了相应 surrogate 的 Bayes consistency；AISTATS 2019。citeturn594194search5 这比单纯把 $e^z$ 换成 $\exp_q(z)$ 的理论基础更强，因为它明确说明了损失、预测分布和 robustness 之间的关系。


综上，这次检索没有发现 Tsallis 已经覆盖了 Shim–Bonifay 所研究的“非对称 IRF + FP + pattern signatures”组合。现有 IRT entropy 研究主要还是 Shannon 型或分类 entropy，例如 Dardick 与 Weiss 的 person-fit entropy，并非 Tsallis nonextensive IRT；DOI **10.1177/0146621617698945**。citeturn731055search4 因而有空白，但应把 novelty 定义得很窄，不能声称“首次把 entropy 用到 IRT”。

## 候选模型、数学性质与最值得推进的单一扩展

Tsallis 基本对象写作

$$
\exp_q(x)=\left[1+(1-q)x\right]_+^{1/(1-q)},
\qquad
\log_q(x)=\frac{x^{1-q}-1}{1-q},
$$

并且 $q\to1$ 时恢复普通 $\exp$ 与 $\log$。Zhang 等采用的两个 $q$-sigmoid 是

$$
S^{(1)}_q(z)
=
\frac{1}{1+\exp_q(-z)},
$$

以及

$$
S^{(2)}_q(z)
=
\frac{\exp_q(z)}
{1+\exp_q(z)}.
$$

上传稿明确保留 ordinary Bernoulli cross-entropy，而没有把目标函数变成 Tsallis cross-entropy。fileciteturn1file1 正式发表版本也作了同样说明。citeturn969710search1

如果把它直接用于 IRT，可写

$$
P(Y_{ij}=1\mid\theta_i)
=
S_q^{(2)}
\!\left(
a_j\theta_i-b_j
\right).
\tag{QIRT}
$$

这在 $q\to1$ 时嵌套 2PL。对内部支持区间

$$
1+(1-q)z>0
$$

有

$$
\frac{dP}{dz}
=
\frac{P(1-P)}
{1+(1-q)z},
$$

所以 $a_j>0$ 且分母为正时保持单调性。二阶导数为

$$
\frac{d^2P}{dz^2}
=
\frac{P(1-P)}
{\left[1+(1-q)z\right]^2}
(q-2P).
$$

因此内点 inflection 满足

$$
P^\star=\frac q2,
\qquad
z^\star=
\log_q\!\left(
\frac{q}{2-q}
\right),
\quad 0<q<2.
$$

这点非常重要：它显示 $q$ 不只是尾部参数，还同时移动**inflection probability 和 inflection location**。与 Shim–Bonifay 三类模型比较，LPE 让 inflection location 随 $\kappa_j$ 移动；RH 通常也移动 inflection；AO 则固定 inflection 的 $\theta$-位置在 $b_j$。fileciteturn0file0 因而一个真正的 $q$-IRT 会有自己独特的几何 signature，而不是 AO 的简单重命名。

但是标准 Tsallis $q$-exponential 带来一个比 LPE/AO 严重得多的问题。若 $q<1$，第二类 $q$-sigmoid 在

$$
z\le -\frac{1}{1-q}
$$

时会达到 **精确的 $P=0$**；而正尾部不是普通指数衰减，而是幂律：

$$
1-P(z)
\asymp
z^{-1/(1-q)}
\qquad
z\rightarrow+\infty.
$$

第一类 $q$-sigmoid 恰好把这种结构反向：一边幂律，另一边在有限 $z$ 达到精确的 $P=1$。这不是传统意义下“更胖尾的 logistic”；它是**一侧有限截断、一侧幂律接近**的高度非对称链接。对于标准正态支持的 $\theta$，这意味着潜变量空间的一部分会被模型宣告为某种响应的条件概率严格为零。对心理测量而言，这是非常强的实质假设。

而且两个 q-sigmoid 的关系在上传稿中存在一个明显的代数问题。文中声称

$$
S_q^{(1)}(z)=S_{1-q}^{(2)}(z).
$$

fileciteturn1file1

但由

$$
\exp_q(-z)
=
\frac{1}
{\exp_{2-q}(z)}
$$

直接得到

$$
\boxed{
S_q^{(1)}(z)
=
S_{\,2-q}^{(2)}(z)
}
$$

而不是 $1-q$。这不是记号偏好，而是参数对偶的实际错误。它还说明两个所谓“different kinds”在数学上本质上是同一个族的 $q\leftrightarrow2-q$ 重参数化，至少在共同定义域上如此。这个问题如果用于 Psychometrika/BJMSP 稿件，必须主动指出而不是继承。

第一类的二阶导数也给出

$$
P^\star=1-\frac q2,
$$

恰好与上述 $2-q$ 对偶一致。这进一步验证了该关系。

Zhang 等还把 $q>1$ 时的 $\beta$-factor singularity 作为主要数值问题，并建议限制 $q<1$。fileciteturn1file4 但“$q<1$ 后 $q$-sigmoid 在所有点都是 $C^\infty$”这一类说法并不普遍成立。因为靠近 cutoff 时函数本质上含有

$$
(x_+)^\alpha,\qquad
\alpha=\frac{1}{1-q}.
$$

一般只有有限阶光滑性；例如 $\alpha=10$ 时最多跨界连续到有限阶，而不是 $C^\infty$。所以把 $q<1$ 描述成完全消除了 regularity 问题是不严谨的。

也可以把 Tsallis 放在别的地方，但每条路的科学意义不同：

| Tsallis 进入位置 | 数学意义 | 优点 | 主要问题 |
|---|---|---|---|
| $q$-sigmoid / $q$-logit IRF | 改变条件响应函数 | 直接对应 Shim–Bonifay 非对称框架 | cutoff、识别、和普通链接灵活性竞争 |
| $q$-Gaussian $g(\theta)$ | 改 latent population | 容纳厚尾 latent trait | $q>1$ 时基本等价于 Student-$t$，新颖性弱 |
| $q$-Gaussian response-process error | 改潜在误差 CDF | 类似 probit/cauchit 逻辑 | 需要定义可识别的 threshold model |
| Tsallis score/divergence | 改估计准则而非 IRF | 可获得原则性的 robustness | 不再直接产生 asymmetry |
| $q$-deform LPE/RH/AO | 同时保留 $\kappa_j$ 和 $q$ | 极灵活 | 极易 shape-confounding，Reviewer #2 会攻击 |
| hierarchical $q$ | 描述群体/测试层异质性 | 可能有机制解释 | 数据需求巨大、识别困难 |

这里最需要强调的是 $q$-Gaussian。最大 Tsallis entropy 在二阶约束下产生的 $q$-Gaussian，在 $q>1$ 的常见参数化中与 Student-$t$ 是重参数化关系；例如

$$
q=1+\frac{2}{\nu+1}
$$

对应自由度 $\nu$ 的 $t$ 分布，而 $q=2$ 对应 Cauchy。这一关系在早期 Physica A 工作中已经明确，DOI **10.1016/S0378-4371(96)00395-0**。citeturn694129search1 所以如果只是把

$$
\theta_i\sim N(0,1)
$$

改成

$$
\theta_i\sim q\text{-Gaussian},
$$

Reviewer #2 很容易说：“这就是 Student-$t$ latent distribution 换了物理学记号。”这项扩展单独不足以支撑顶刊方法论文。

Tsallis score 反而在统计学上更有原则。proper scoring rules 可作为估计准则，严格 propriety 是概率校准的重要基础；Gneiting 与 Raftery 给出了系统理论，DOI **10.1198/016214506000001437**。citeturn594194search0turn594194search8 Tsallis score 与 density-power divergence 也有成熟的鲁棒估计文献；Basu 等人的经典 density-power divergence 论文 DOI **10.1093/biomet/85.3.549**，其 tuning parameter 在效率与 robustness 之间连续权衡。citeturn594194search3 后续 logistic/polytomous regression 也已有系统推导。citeturn594194search4turn594194search6

因此，我建议不要把论文发展成“Tsallis everything”。**最值得推进的单一主模型**是一个保守版本：

$$
\boxed{
P_{ij}
=
S_q^{(2)}
(a_j\theta_i-b_j),
\quad
q \text{ 为测试级或群体级公共参数},
\quad
0<q<2,
}
$$

简称 **global-$q$ asymmetric IRT**，而不是 item-specific $q_j$。

原因是：如果每题都有 $q_j$，它会与 $a_j,b_j$ 以及 LPE/AO 的 $\kappa_j$ 产生严重 confounding；global $q$ 至少把 $q$ 定义成**整个响应系统共享的 deformation index**。若 empirical evidence 支持 global $q\neq1$，第二阶段研究再考虑 hierarchical

$$
q_j
=
q_0+\delta_j,\qquad
\delta_j\sim N(0,\tau_q^2).
$$

主论文中不要同时加入 $\kappa_j$。否则你的稿子会从“解释一个新的全局非扩展响应机制”退化成“再增加一个 shape parameter”。

估计上建议使用两条平行路线：普通 marginal maximum likelihood 作为主分析，

$$
L(\Theta)
=
\prod_i
\int
\prod_j
P_{ij}(\theta)^{y_{ij}}
[1-P_{ij}(\theta)]^{1-y_{ij}}
g(\theta)\,d\theta,
$$

以及 Tsallis-score robust estimation 作为**敏感性分析而不是同一个主模型的一部分**。这能清楚地区分“$q$ 改 IRF”和“$q$ 改 loss”两个概念。

## Reviewer #2：为什么不是 Student-$t$、Huber、AO 或普通灵活链接

真正危险的问题不是“Tsallis 能不能拟合”，而是：

> **为什么一个心理测量学家需要相信非扩展统计力学，而不是相信‘数据有点厚尾/偏斜’？**

目前文献并不能支持“IRT 数据天然是 nonextensive system”这样的强论断。Tsallis 在物理学中的典型理论理由是长程相互作用、多尺度结构、非遍历、记忆与非平衡状态；在认知领域已有少数模型把 $q$ 与心理时间非线性、非局部神经网络或多尺度 EEG 结构联系起来。citeturn731055search3turn847307search0turn731055search7 但是**局部独立的一维 IRT 条件模型本身恰恰假设在给定 $\theta$ 后各题响应近似独立**。所以如果你的理论论述一边宣称 long-range interactions，一边仍采用普通 local independence，

$$
P(\mathbf Y_i\mid\theta_i)
=
\prod_jP(Y_{ij}\mid\theta_i),
$$

Reviewer #2 会指出逻辑张力。

要让 nonextensivity 有实质意义，你需要给出至少一种可检验的机制，例如：

$$
q-1
\propto
\text{residual dependence strength},
$$

或者

$$
q-1
\propto
\text{between-person heterogeneity in latent response temperature},
$$

或者从一个明确的 random-effects / superstatistical mixture 推导出 $q$-response law。否则 $q$ 只是一个 curvature knob。

与现有替代方案相比，Tsallis 的负担很重：

**3PL/4PL。** 如果数据异常来自有限的 guessing/slipping asymptotes，

$$
P_j(\theta)
=
c_j+(d_j-c_j)
\operatorname{logit}^{-1}(a_j\theta-b_j),
$$

它们直接对机制参数化。q-sigmoid 的 finite cutoff 或 power-law tail 并不会自动比 guessing/slipping 更容易解释。

**CLL/NLL/AO/LPE。** 这些已经专门针对非对称链接，而且 Shim–Bonifay 显示它们具有不同 tail signatures。fileciteturn0file0 一个 $q$-模型必须证明它产生的 pattern signature 不是 AO/LPE 的近似复制。特别是 q-sigmoid 的“一侧 cutoff + 一侧 power-law”很可能是它最有辨识力的预测，应围绕这一点设计实验。

**cauchit 和 Student-$t$ 链接/latent distribution。** q-Gaussian 在 $q>1$ 时与 Student-$t$ 密切等价，因此仅凭 heavy tails 不能说明 Tsallis 独特。citeturn694129search1turn694129search0

**skew-normal / skew-probit。** 如果真正需要的是偏度而不是 power-law/cutoff，则 skew families 通常更自然。Molenaar 早已在 psychometric context 同时讨论 heteroscedasticity 与 skewed latent trait。citeturn571000search31

**Huber / bisquare / contaminated likelihood。** 如果问题是 aberrant responses，直接鲁棒化估计已经有 IRT 文献；2025 年的 GRM robust latent trait estimator 就用 Huber 和 bisquare weights，并在污染数据下研究偏差与标准误。citeturn360215search4turn360215search6 如果你的 q 模型只在 contamination condition 下表现更好，却不能在 clean condition 下保持 calibration，那么 Reviewer #2 会认为它只是比较复杂的 robust estimator。

**mixture IRT、testlet/local dependence、network models。** 如果所谓“非扩展性”来自群体混合或局部相关，那么直接把这些结构建模通常更透明。把它们压缩进一个 $q$ 中只有在你能证明某种 coarse-graining 或 superstatistics 近似时才具有理论优势。

**semiparametric / filtered monotonic polynomial IRF。** Feuerstahler 已展示可以在维持单调性的同时用 polynomial metric transformation 获得很大函数形状自由度，DOI **10.1007/s11336-018-9642-9**。citeturn571000search19 因而“我们的 IRF 更灵活”不是足够的贡献。

所以 Tsallis 真正可能提供、而上述方法不直接提供的东西只有两个：

其一是一个具有明确解析形式的 **power-law / finite-support asymmetry family**，其 tail exponent 与 $q$ 一一对应；

其二是一个如果有微观模型支持的话，可以把 item-level response law 与**多尺度、异质温度、nonergodic dynamics** 联系起来的 deformation index。

如果这两点都做不到，建议不要以“nonextensive statistical mechanics”作为核心理论宣称，而应更克制地称作 **q-deformed asymmetric link family inspired by Tsallis statistics**。

Zhang 等文章尤其不能作为“理论已经验证”的依据。首先，它最终使用的是普通 cross-entropy，不是 Tsallis entropy objective。fileciteturn1file9 其次，它的 simulation 只有 $n=100,p=50$ 的核心设置和大约 $q\in[0.9,1.1]$ 的有限搜索，并报告最优值通常非常接近 $q=1$。citeturn969710search1 这反而说明性能改善可能来自轻微 link tuning，而不是强 nonextensive regime。

另外，该文把普通 logistic regression 描述成“假设 input data follow an exponential distribution”的说法在统计上是不正确的：logistic regression 对协变量 $X$ 的边缘分布并没有这种要求；模型假设的是条件均值通过 logit link 与线性预测子相连。该表述出现在正式文章的 discussion 摘要中。citeturn969710search1 这削弱了它用“非指数型输入分布”来动机化 Tsallis link 的逻辑。

它的 robustness 主张也需要谨慎。加入 Gaussian white noise 并观察分类指标稳定，并不能建立对 label contamination、leverage points、adversarial covariate outliers 或 model misspecification 的一般 robustness。相比之下，density-power divergence 文献明确通过 influence-function 与效率/robustness trade-off 建立理论。citeturn594194search3turn594194search7

最后，用普通 Bernoulli log loss训练 $q$-sigmoid 时，**log loss 本身仍是 proper score**；只要链接在相关参数区间是一一映射且模型正确指定，条件概率估计可以保持 Fisher consistency。但 q-sigmoid 的 cutoff 导致全实轴上不再严格一一对应，而且如果同时估计 $q$ 和 slope/intercept，parametric Fisher consistency 还需要重新证明。Zhang 等引用 Fisher consistency 的一般概念，但没有给出针对其 joint-$q$ estimator 的完整识别与一致性证明。fileciteturn1file9 这一缺口在 IRT 论文中必须补上。

## 理论推导、识别性与对 Shim–Bonifay 分析框架的扩展

投稿 Psychometrika 或 BJMSP 前，理论部分至少要完整解决以下问题。

首先是 **score 与 information**。对一般 Bernoulli IRF $P_j(\theta)$，

$$
I_j(\theta)
=
\frac{\{P_j'(\theta)\}^2}
{P_j(\theta)[1-P_j(\theta)]}.
$$

对于 proposed q-IRT，

$$
P_j'(\theta)
=
a_j
\frac{P_j(1-P_j)}
{1+(1-q)z_j},
$$

从而

$$
I_j(\theta)
=
a_j^2
\frac{P_j(\theta)[1-P_j(\theta)]}
{\{1+(1-q)z_j\}^2}.
$$

这和 logistic 2PL 的

$$
I_j^{2PL}
=
a_j^2P_j(1-P_j)
$$

相比多出一个位置依赖的 deformation factor。因此 $q$ 同时改变 slope 和 information allocation，而不仅仅改变 IRF skewness。这个性质应成为理论论文的核心之一。

Shim–Bonifay 用 $P'(\theta)$ 当作 pseudo-information，因为标准 Fisher information 混合了 slope 和 probability 后会模糊方向性。fileciteturn0file0 对 q-IRT 可完全复用其策略，定义以 $c_j$ 为参考中心的概率非对称指数

$$
A_P(x)
=
P(c_j+x)+P(c_j-x)-1,
$$

以及导数非对称指数

$$
A_D(x)
=
P'(c_j+x)-P'(c_j-x),
$$

但 $c_j$ 不应机械设为 $b_j$。因为 q-IRT 的 inflection point 并非 $b_j$，应分别报告：

$$
c_{50,j}:\quad P_j(c_{50,j})=.5,
$$

与

$$
c_{\mathrm{inf},j}
=
\frac{b_j+z^\star}{a_j}.
$$

这种“threshold center 与 curvature center 分离”的现象本身就是一个可比较的 signature。

其次是 **local identifiability**。至少应研究每题或总体参数的 Jacobian/Hessian：

$$
\mathcal J
=
\left(
\frac{\partial P_{ij}}
{\partial a_j},
\frac{\partial P_{ij}}
{\partial b_j},
\frac{\partial P_{ij}}
{\partial q}
\right),
$$

并检查在 $q=1$ 附近是否近共线。因为小幅 $q-1$ 的影响可能被 $a_j$ 和 $b_j$ 的重新缩放吸收。如果 condition number 在 $q\approx1$ 时非常大，统计上就会出现“理论上 nested、实证上难识别”的弱识别问题。

第三是 **boundary/nesting**。标准模型位于 $q=1$ 的内部还是边界取决于你的参数空间设计。若令

$$
q\in(0,2),
$$

则 $q=1$ 是内部点，可以研究标准 likelihood-ratio/Wald/score 渐近；但 cutoff 所造成的 support dependence 可能破坏普通 regularity，需要单独证明。若为了数值安全把参数硬限制为 $q<1$，则 2PL 的 $q=1$ 变成边界值，常规 $\chi^2_1$ LRT 不再自动成立，必须用 parametric bootstrap 或推导 mixture limit。

第四是 **latent distribution identification**。若同时设

$$
\theta_i\sim q_\theta\text{-Gaussian}
$$

以及

$$
P_{ij}=S_{q_R}(a_j\theta_i-b_j),
$$

你就有两个 q：

$$
q_\theta,\qquad q_R.
$$

这非常容易把“人口厚尾”和“条件响应尾部”混在一起。原则上可以通过大量 items 与丰富 difficulty design 区分，但有限测试下往往会有巨大 posterior correlation。因此第一篇稿件应该固定

$$
\theta\sim N(0,1)
$$

作为 identification convention，再把 Student-$t$/q-Gaussian latent density 当作 misspecification sensitivity condition，而不是同时自由估计。

第五是 **FP 完整复制**。Shim–Bonifay 使用五个二分项目、simplex sampling 的 5000 个数据集、以 univariate/bivariate margins 为基础的 $Y^2/N$，并比较 ECDF、Euler regions 与 model-winning pattern signatures。fileciteturn1file2 新论文应先一比一复刻：

$$
\{2PL,LPE,RH,AO,QIRT\}
$$

在同样的五题空间、同样的先验强度标定、同样的优化容忍度下比较。由于原论文已提醒不同模型上相同 prior variance 不代表相同的 response-curve regularization，而且 RH 的 FP 对 prior variance 特别敏感，fileciteturn1file5 你的 q prior 应按**IRF 变化幅度**而不是参数原始尺度进行 calibration。例如选择先验使

$$
E_{\pi(q)}
\left[
\int
\{P_q(\theta)-P_{2PL}(\theta)\}^2
w(\theta)d\theta
\right]
$$

与 LPE/AO 的对应 prior-induced deformation 匹配。

第六是 **pattern signature 预测必须事前提出**。对第二类 $q$-sigmoid 且 $q<1$，低端存在有限 cutoff、高端 power-law 接近 1，因此合理的先验预测是：它相对于 logistic 会极强压制某些“低 $\theta$ 却正答”的模式，同时在高端比普通 logistic 更慢地趋近 1。也就是说，它很可能偏好与 AO 不完全相同的高分但非满分模式。这种模式应该在跑 simulation 前就写成 preregistered prediction；否则看完 pattern heatmap 再解释 $q$ 很容易显得 post hoc。

最后，convergence failure 本身必须作为 outcome，而不能把失败数据删掉。至少报告

$$
\Pr(\text{converged}),
\quad
\Pr(\text{boundary }q),
\quad
\Pr(\text{Hessian PD}),
\quad
\Pr(\text{finite SE}),
$$

并用 intention-to-fit 方式把失败率纳入 FP 比较。一个靠频繁失败来获得“较低 fitting propensity”的模型并不是更简单。

## Monte Carlo、经验数据与模型比较设计

目标期刊需要的不只是“多个 N 下 bias 小”。模拟应围绕四个问题展开：**能否识别、何时胜过基线、错设时是否安全、以及 $q\neq1$ 的证据是否可校准**。

推荐基础 factorial design 如下：

| 因素 | 建议水平 |
|---|---|
| $N$ | 250, 500, 1000, 2000, 5000 |
| items $J$ | 10, 20, 40, 80 |
| true $q$ | 0.80, 0.90, 0.97, 1.00, 1.03, 1.10, 1.20 |
| discrimination | $a_j$ 约 0.5–2.0 |
| difficulty | 集中、均匀覆盖 $[-2.5,2.5]$、偏向高端/低端三种设计 |
| latent $g(\theta)$ | Normal、skew-normal、Student-$t_5$、two-class mixture |
| local dependence | 0、弱 testlet、强 testlet |
| contamination | 0%、2%、5%、10% random/rapid-guess responses |
| missingness | MCAR 0/10%，MAR 10/25% |
| DIF | 无、少数 item slope/difficulty DIF |
| true generating model | 2PL、LPE、RH、AO、CLL/NLL/cauchit、QIRT |

Replication 数不应武断地统一设为 1000，而应按 Monte Carlo error 反推。若目标是估计 Type I error $0.05$ 并希望 Monte Carlo 标准误约为 $0.003$，

$$
SE_{MC}
=
\sqrt{\frac{0.05(0.95)}{R}},
$$

得到 $R\approx5278$。所以 inferential calibration 条件建议 **5000–10,000 replications**；纯 bias/RMSE 条件如果标准误稳定，1000–2000 通常足够。这样 Reviewer 能看到 replication count 与精度目标之间的关系，而不是“行业惯例”。

参数恢复至少报告

$$
\mathrm{Bias}(\hat q),\quad
\mathrm{RMSE}(\hat q),\quad
\mathrm{Bias}(\hat a_j),\quad
\mathrm{Bias}(\hat b_j),
$$

以及 95% interval coverage、平均 interval width、empirical SD/mean SE ratio。最关键的图不是 q 的 RMSE，而是 $(q,a,b)$ 估计相关矩阵，因为这直接检验 confounding。

在 $q=1$ 时研究检验：

$$
H_0:q=1
$$

的 Type I error；在 $q=.97,.95,.90,\ldots$ 下研究 power。若 support/nonregularity 使 Wald/LRT 失准，应直接转向 parametric bootstrap likelihood-ratio test。

predictive evaluation 应至少包括：

$$
\text{log score}
=
-\sum y\log \hat p +(1-y)\log(1-\hat p),
$$

$$
\text{Brier}
=
\frac1{NJ}
\sum(y-\hat p)^2,
$$

calibration curves、reliability slope/intercept，以及 out-of-sample response-pattern log predictive density。Proper scoring rule 理论支持 log score 和 Brier 作为概率预测评价，而不是只报告分类准确率。citeturn594194search0

模型比较方面，AIC/BIC 可以报告，但不能成为核心证据。因为 Shim–Bonifay 的研究主题本身就在说明“相同参数个数的模型可以有不同 configural complexity”。citeturn571000search0turn571000search7 因此建议证据层级是：

$$
\text{out-of-sample log score}
>
\text{LOO/K-fold}
>
\text{posterior predictive checks}
>
\text{FP/pattern signature}
>
\text{AIC/BIC}.
$$

WAIC/PSIS-LOO 若采用 Bayesian estimation，可以用于 prediction，但必须检查 Pareto-$k$ diagnostics；对于潜变量模型，leave-one-person-out 与 leave-one-response-out 回答的是不同科学问题。前者检验新受试者泛化，后者更多检验 item-response reconstruction。不要把它们混为一谈。

Bayes factor 只有在 q prior 明确且 nesting regular 时才推荐。由于 $q$ 的 prior width 会极大影响边际似然，若没有很强的理论 prior，Bayes factor 很可能变成“先验敏感性结果”。对本项目，K-fold/LOO 加 predictive log score 更可靠。

经验研究建议至少两个 dataset，而且要**事前存在可观察理由**怀疑 ordinary symmetric IRT 不够。一个教育测试可以有多步骤推理、高/低 difficulty 覆盖以及可能的 guessing；一个 personality/clinical screening 数据可以有极端响应与群体异质性。不要只挑“q 模型显著胜出”的数据。经验数据应先检查：

$$
\text{score mass at extremes},
\quad
\text{item-level empirical asymmetry},
\quad
\text{residual dependence},
\quad
\text{testlet effects},
\quad
\text{response-time evidence}.
$$

如果 $q\neq1$ 只在 residual dependence 很强的数据上出现，而加入 testlet factor 后 $q\to1$，这反而是非常有价值的结果：说明 q 原先是在吸收 local dependence，而不是发现新的 nonextensive response law。

一个更强的经验设计是同时使用 response time。已有 psychometric models 能联合建模 response accuracy 与 RT，并用 response-process information 解释潜变量。citeturn571000search13turn571000search29 如果异常 $q$ 项目同时显示长尾 RT、rapid guessing、策略切换或 fatigue，这比单纯的 item score histogram 更容易把 q 解释成过程参数。

## 论文可发表性的判断与潜在致命问题

**BJMSP：可行性最高。** Shim–Bonifay 本身发表于该刊，而 BJMSP 的 scope 明确包括新的心理过程模型、心理数据分析方法、模型批评与估计算法。citeturn395729search7 如果你的稿件把重点放在“q-deformation 作为一种新的 asymmetric response mechanism，并用 asymmetry/FP/pattern signature 做结构比较”，与该刊的近期方法学轨迹高度一致。我的判断是：**有中等偏高的可发表潜力**，条件是数学问题全部解决，而且不要把论文包装成未经证实的“心理系统服从非扩展热力学”。

**Psychometrika：可行，但门槛明显更高。** 该刊已经发表 FP 方法、monotonic polynomial IRF、heteroscedastic IRT、entropy-based score scaling 等高度数学化工作。citeturn571000search1turn571000search19turn395729search2 想进 Psychometrika，至少需要一个完整定理链：monotonicity、identifiability、nesting、regularity、score/information、渐近性质，以及可靠的估计算法。仅“定义 $q$-IRT + simulation + 实证”不够。若能证明 global-$q$ model 的 identifiable parameterization，并给出 q≈1 附近局部几何与 inferential theory，我会把它视为真正有竞争力。

**Psychological Methods：当前版本不如前两者匹配。** 该刊确实发表 fitting propensity 以及模型复杂度工作。citeturn571000search3turn571000search22 但要达到该刊的广泛方法影响力，论文不能只是一个 niche asymmetric IRT link。更合适的 PM 路线是把研究提升为“**deformed links, robust scoring, and configural complexity as a general framework for binary latent-variable models**”，并覆盖 IRT、binary factor model 与 possibly logistic latent regression。这样影响面才足够。

最可能的 Reviewer #2 objections 是：  
1. $q$ 与普通 shape parameter 有什么本质区别？  
2. q-Gaussian 不就是 Student-$t$？  
3. 为什么不是 AO/LPE/cauchit/skew-probit？  
4. nonextensivity 的心理机制在哪里？  
5. q-sigmoid finite cutoff 是否不合理？  
6. $q$ 与 $a,b$ 是否可识别？  
7. 为什么不用 Huber 或 density-power divergence？  
8. 更好的 fit 是否只是更高 FP？  
9. $q$ 是否只是吸收 local dependence / mixture heterogeneity？  
10. q-sigmoid 所谓 robustness 是否有正式 influence-function 或 contamination theory？

真正的**fatal flaws**有四个。第一，使用 Zhang 文中的 $S_q^{(1)}=S_{1-q}^{(2)}$ 错误而不纠正；第二，在没有机制证据时把 $q\neq1$ 解释成“心理系统非扩展”；第三，让每个 item 都自由估计 $q_j$ 而不做局部识别分析；第四，只与 2PL 比较而不包括 LPE、AO、RH、CLL/cauchit、Student-$t$/robust alternatives。

相反，**minimum viable contribution** 很清晰：

> 建立一个参数数目受控的 global-$q$ asymmetric IRT family；证明其几何和统计性质；揭示其一侧有限截断/另一侧 power-law 所产生的独特 asymmetry 与 pattern signature；并证明在与 LPE、RH、AO 具有相似或更低 fitting propensity 的条件下，它只在具有特定数据结构时提供真正的 predictive gain。

这是足够明确、也足够可证伪的核心 claim。

## 推荐稿件结构、标题与最终判断

推荐标题：

**A $q$-Deformed Item Response Model: Asymmetry, Identifiability, Fitting Propensity, and Response-Pattern Signatures**

如果希望更克制、减少“物理学包装”的阻力：

**A Tsallis-Inspired Asymmetric Link for Item Response Theory: Geometry, Complexity, and Predictive Signatures**

核心论点不要写成“Tsallis statistics improves IRT”。应写成：

> **Tsallis $q$-deformation induces a mathematically distinctive asymmetric response family characterized by finite-support behavior on one side and power-law convergence on the other. Whether this flexibility represents substantive response dynamics can be evaluated—and potentially falsified—through item-level geometry, fitting propensity, response-pattern signatures, and out-of-sample prediction.**

推荐文章结构是：Introduction and gap；q-deformed binary response family；Mathematical properties and identification；Comparison with LPE/RH/AO and conventional robust alternatives；FP and pattern-signature study；Monte Carlo recovery/inference；Empirical applications；Discussion on mechanism versus flexible approximation。

代码应至少公开：数据生成、quadrature/MML 或 Bayesian estimation、所有 optimization starts、convergence classification、FP simplex sampler、Euler-region construction、pattern signature computation、Monte Carlo seeds，以及 reproduction scripts。Shim–Bonifay 自身公开了 annotated code，这提高了后续工作的可复现性基准。fileciteturn1file3

最终可行性判断是：

**把 Tsallis 当成“新的物理理论解释 IRT”——目前证据不足，不建议。**

**把 $q$-Gaussian latent trait 当成主要创新——不够新，因为与 Student-$t$ 高度重合。**

**把 Tsallis entropy loss 当成唯一创新——可以成为鲁棒 IRT 论文，但会偏离 Shim–Bonifay 的非对称主题。**

**把一个严格分析过的 global-$q$ asymmetric IRF 放进 Shim–Bonifay 的 asymmetry–FP–pattern-signature 框架，并让 mechanistic interpretation 接受直接竞争模型检验——这是最有潜力的方案。**

在三个目标期刊中，我会按当前构想排序为：

$$
\boxed{\text{BJMSP}>\text{Psychometrika}>\text{Psychological Methods}}
$$

但如果补出强识别/渐近理论，Psychometrika 可以升到第一；如果把框架扩展到多种 binary latent-variable models，而不是只做 IRT，Psychological Methods 的吸引力会显著上升。

最重要的研究策略不是证明“$q$ 有用”，而是设计出一种研究，使结果即使最终得到

$$
\hat q\approx1
$$

仍然值得发表：因为那将严格表明，在控制了 LPE/AO/RH、latent heavy tails、robust loss、mixture heterogeneity 与 local dependence 之后，Tsallis deformation 并没有额外的心理测量学内容。一个能产生这种否定结论、同时又把“为什么”讲清楚的研究，反而最符合 Psychometrika/BJMSP 对方法论文的标准。