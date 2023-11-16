---
layout: post
title: Curvature and Winding Number
subtitle: 
date: 2023-11-15
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Minkowski
  - Frankel
---

*Disclaimer: Nothing in this note is original.*

We will assume that the Yang-Mills potential $\omega_ {U}$ in patch $U$ has no singularity. 

Let $\theta$ be the two-form curvature, we have the following observation for any vector bundle over all base manifolds,
$$
\theta \wedge \theta = (d\omega+\omega \wedge \omega)\wedge (d\omega+\omega \wedge \omega) ,
$$
using 
$$
\mathrm{Tr}\,(\omega \wedge \omega \wedge d\omega) = \mathrm{Tr}\,(d\omega \wedge \omega \wedge \omega)
$$
and 
$$
\mathrm{Tr}\,(\omega \wedge \omega \wedge \omega \wedge \omega)=0
$$
we have eventually
$$
\mathrm{Tr}\,(\theta \wedge \theta) = d\, \mathrm{Tr}\,\left( \omega \wedge d\omega+\frac{2}{3}\omega \wedge \omega \wedge \omega \right)
$$
thus $\mathrm{Tr}\,(\theta \wedge\theta)$ is *locally exact*, it is locally the differential of a $3$-form, called the `Chern-Simons` $3$-form. $\omega$ is not usually globally defined. 

Coming back to the case of instanton, outside the instanton the curvature vanishes but the connection does not, hence we have
$$
\int_ {U} \,  \mathrm{Tr}\,(\theta \wedge \theta) = \int_ {\partial U = \mathbb{S}^{3}} \,  \left( -\frac{1}{3} \right)\mathrm{Tr}\,(\omega \wedge \omega \wedge \omega).
$$
This allows us to write the winding number in terms of curvature, by applying some kind of Stokes theorem
$$
\frac{1}{24\pi^{2}}\int_ {\mathbb{S}^{3}} \,  \mathrm{Tr}\,(\omega_ {U}\wedge \omega_ {U}\wedge \omega_ {U})
= - \frac{1}{8\pi^{2}} \int_ {\mathbb{R}^{4}} \, \mathrm{Tr}\,(\theta \wedge \theta).
$$

Note that $\theta \wedge\theta$ is *not* the Lagrangian, which is $\mathrm{Tr}\,(\theta \wedge\star \theta)$.  We have
$$
\theta \wedge \theta = (\theta \wedge \theta)_ {0123}\,dt\wedge dx\wedge dy\wedge dz\propto \epsilon^{ijkl}F_ {ij}F_ {kl}
$$
while
$$
\theta \wedge \star \theta \propto F_ {ij}F^{ij}.
$$

### The Chern form for a $U(n)$ bundle

The topological significance of $\mathrm{Tr}\,(\theta \wedge\theta)$, generalizing Poincare’s theorem for closed surfaces (which says the sum of indices times multiplicity equal to the Euler characteristic), is developed by 
$$
\bigwedge^k V 
$$


