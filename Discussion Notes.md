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

C. Tsallis在1988年提出了对传统的Shannon熵（等价于Boltzmann-Gibbs熵）的一种非广延性推广，此后获得了巨大的成功（Tsallis的文章引用量已超过一万一千余次），广泛地用于物理、生物统计、复杂系统、分形几何等等方面。Tsallis统计的推广主要包含两方面的内容：1）在数学上推广了通常的指数函数$e^{ x }$和对数函数$\ln(x)$，引入了额外参数 $q\in\mathbb{R}$ 以表征其对传统函数的偏离程度，定义了q-指数函数$\exp_ {q}(x)$与q-对数函数$\ln _ {q}(x)$；2）在上述函数的基础上，考虑概率分布函数须满足的一般性质（如归一化），定义了Tsallis熵$S_ {q}$， 当 $q\neq 1$ 时Tsallis熵具有非广延性，因此可以解释传统熵无法解释的反常效应，如记忆效应（针对非-马尔科夫过程）、分形效应或长距离相互作用等。

在我们的初步工作中，我们将Tsallis统计与生物统计中常用的逻辑回归方法结合起来，利用q-指数与q-对数函数推广了q-sigmoid函数，以此引入了对线性回归方法的非线性修正（详细可见笔记），通过调整 $q$ 的值来调整非线性修正的贡献。当$q=1$时，sigmoid函数收敛于未修正的版本。初步结论表明，从Yoden指数的变化可以发现，拟合结果对q的取值范围较为敏感，在$q\sim1$附近较大的取值范围内，Tsallis统计的引入显著地改善了拟合优度。