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

BPS equation for $\phi^{4}$ theory:

$$
\phi' = \sqrt{ 2V } \implies \phi'= \pm \frac{\sqrt{ \lambda }}{\sqrt{ 2 }}\left( \phi^{2}-\frac{m^{2}}{\lambda} \right).
$$

Eventually the plus sign gives the anti-kink equation, while the minus sign gives the kink equation. But for the sake of notation simplicity, let's carry on with plus sign. After some arrangement and put things under integral, we get 

$$
\int d\phi \,  \sqrt{ \frac{2}{\lambda} } \frac{1}{\phi^{2}-m^{2} / \lambda} = \int  \,   dx
$$

define 

$$
t:= \frac{\sqrt{ \lambda }}{m} \phi
$$

we have 

$$
\int d(x+c)  = \frac{\sqrt{ 2 }}{m} \int  \,  dt \frac{1}{t^{2}-1},
$$

where $c$ is the constant of integral. The lower limit of $t$-integral is arbitrary as long as it's not zero, since we are only interested in the differentials. Perform the integral This gives us 

$$
x+c = - \frac{\sqrt{ 2 }}{m} \mathrm{arctanh}\,\left( \frac{\sqrt{ \lambda }}{m}\phi \right)
$$

which is 

$$
\phi = \frac{m}{\sqrt{ \lambda }} \tanh\left( -\frac{m}{\sqrt{ 2 }}(x+c) \right).
$$