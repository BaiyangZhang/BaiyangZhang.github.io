---
layout: post
title:
date:
author: Baiyang Zhang
catalog: true
tags:
---

$$
I(x) =\int_ {-\infty}^{\infty} dp \,    p^{2} (1+p^{2})^{x} \text{csch}^{2}(p)
$$

where $\text{csch}$ is the hyperbolic function 

$$
\text{csch}(x) = \frac{1}{\sinh(x)} , \quad \sinh(x)= \frac{e^{ x }-e^{ -x }}{2}.
$$

- - -


I was trying to turn the integral

$$
I =\int_ {-\infty}^{\infty} dp \,    p^{2} (1+p^{2})^{3/2} \text{csch}^{2}(p)
$$

into a function $I(x)$ of $x$ and look for the differential equations the $I(x)$ satisfies. For example, if define

$$
I(x) := I(x) =\int_ {-\infty}^{\infty} dp \,    p^{2} (1+p^{2})^{x} \text{csch}^{2}(p)
$$

and we can find the differential equation for $I(x)$, since we know the value of $I(0)$, there is a chance to workout $I\left( \frac{3}{2} \right)$. But I failed, the recursive relation 

$$
I^{(n)}(x) = \int_ {-\infty}^{\infty} dp \,  p^{2} (1+p^{2})^{x} \ln^{n}(1+p^{2}) \text{csch}^{2}(p)
$$

doesn't lead to anywhere... I tried different ways to insert $x$ into $I$ such as 

$$
\int_ {-\infty}^{\infty} dp \, p^{2} (1+p^{2})^{3/2} \text{csch}^{2}(xp),\quad  \int_ {-\infty}^{\infty} dp \,  (1+p^{2})^{3/2} \left( \frac{p}{\text{csch}(p)} \right)^{x},\cdots
$$

but none of them seem to work.