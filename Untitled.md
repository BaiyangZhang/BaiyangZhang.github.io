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

<<<<<<< HEAD
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
=======
I googled this paper and it is about quantum Hall effect, not cosmology? 



$$
\int_ {-\infty}^{\infty} dp \,  p^{2}(1+p^{2})^{\frac{3}{2}} \text{csch}^{2}
$$

by expanding $(1+p^{2})^{3/2}$, but the result is some crazy alternating series

$$
\frac{\pi ^2}{3}+\frac{\pi ^4}{10}+\frac{\pi ^6}{56}-\frac{\pi ^8}{240}+\frac{5 \pi ^{10}}{2816}+\frac{691 \pi ^{12}}{199680}-\frac{21 \pi ^{14}}{2048}+\cdots
$$

not even an asymptotic series. Bob Dingle has a book on asymptotic methods of special functions but doesn't seem to help either.

- - -



>>>>>>> f9089cb7320c4e949c04c85a5c2ce48eb47a8379
