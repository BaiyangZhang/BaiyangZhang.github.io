---
layout: post
title: Discussion Notes
subtitle: 
date: 2024-04-01
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---

**Question 1:** 为什么Ncs是整数时，能量最低，即真空态？

**Response 1:** 我只知道当规范场是pure gauge，即$A=U(i\partial)U^{\dagger}, U\in SU(2)$的情况下，$N_ {\text{CS}}$刻画在时空边界上规范场的绕数，因此是整数；此时，根据pure gauge的定义，能量也最小。当规范场不是pure gauge时，好像没有理由相信$N_ {CS}$是个整数。。。所以我想可能得解释是:$N_ {\text{CS}}\in\mathbb{Z}$时，规范场属于pure gauge，因此能量最低。


- - -

**Question 2:** 不同Ncs的真空态能否通过规范变换，得到相同的一个真空态？

**Response 2:** 规范变换可以写成$A\to U(A+i\partial)U^{\dagger}$，所谓规范变换的拓扑性质指的是$U\cong\mathbb{S}^{3}$的拓扑性质。规范变换大概分两种：

1. small gauge transformations：指拓扑平凡的规范变换，和单位元（也就是不作任何变换的变换）可以平滑变换；
2. large gauge transformations：指拓扑非平凡的规范变换，无法平滑过渡到单位元。

不同CS数的真空可以通过large gauge transform互相变换(其媒介我记得就是Sphaleron)，不能通过small gauge transform得到。这方面David Tong的gauge theory讲义里讲得比较详细。

话又说回来,能通过large gauge transformation互相转化的两个真空（对应不同的CS number），在物理上并不等价，他们对应不同的希尔伯特态。在经典层面上，但凡差一个规范变换，无论large还是small，都是等价的；但是在量子化的过程中，对应不同CS number的真空在路径积分中有其各自独立的贡献，不能简单地看作同一个真空。比如$\theta$真空就是个例子。small gauge transformation对应着坐标变换（这一点用principal bundle的语言描述最直观），因此不影响物理观测量，这也是为什么small gauge transformation不能有anomaly。而large gauge transformation要更深刻一点，有其拓扑内涵，由其联系起来的不同真空在量子场论中都需要考虑。

- - -

**Question 3:** 随着宇宙演化，零温时，宇宙的不同区域会不会同时处于具有不同Ncs的真空态？

**Response 3:** 这个我不太了解，但是据我所知，只有当discrete symmetry自发破却的时候才会产生cosmic domain wall, 比如$\phi^{4}$ model的$\mathbb{Z}_ {2}$ 对称性，所以我怀疑在宇宙冷却的过程中，应该不会产生Chern-Simons domain wall。不过这方面我不是熟悉，那些专门做cosmic string的人肯定懂得更多，我说的仅供参考。有空的时候我也看看相关文献。

- - -

**Question 4:** 如果不同区域具有不同真空态，是否会导致类似domain wall的结构，能否被宇宙天文观测允许，或者与粒子物理的矛盾？

**Response 4:** 如果不同区域有不同的真空态，确实会形成相应的domain wall（membrane）。比如，某个discrete symmetry如果自发性破缺，就有可能导致cosmic domain wall的形成。我和jarah Evslin、Andy Royston在Kink上的工作，也是为了理解domain wall的量子化问题，以期日后用在cosmic domain wall的计算中。暂时我只是了解一些$\mathbb{Z}_ {2}$ domain wall在宇宙学中的应用。以$\mathbb{Z}_ {2}$ domain wall为例，它有些很有趣的观测性质，比如可以用来解释CMB的各向异性。据我所知，宇宙天文观测会对domain mall的物理参数（比如tension、thickness等）给出种种限制，就像物理实验限制了中微子的质量上限，但是似乎没什么矛盾的地方。就$\mathbb{Z}_ {2}$ Kink和相应的domain wall而言，在粒子物理中也没有和实验矛盾的地方，因为它们都属于基本粒子的群体性质(collective property)，出现在有效理论中，和标准模型并不冲突。弱电理论中的domain wall我就不了解了，不过既然弱电理论没什么问题，包含其中的domain wall应该也不会有矛盾。


Let $U$ be a subspace of $M$, namely $U\subset M$. Let $\phi$ be a coordinate system,

$$
\phi: U\to \mathbb{R} (abd) \left( \frac{a}{b} \right) \frac{ \partial y }{ \partial x }  
$$
