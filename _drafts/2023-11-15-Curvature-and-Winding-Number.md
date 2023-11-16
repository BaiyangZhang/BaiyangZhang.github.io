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

The topological significance of $\mathrm{Tr}\,(\theta \wedge\theta)$, generalizing Poincare’s theorem for closed surfaces (which says the sum of indices times multiplicity equal to the Euler characteristic), is developed by Chern. $\mathrm{Tr}\,(\theta \wedge\theta)$ is but one of a whole family of significant integrands, called the Chern forms. But before going into details, let's review what is `exterior power space` shortly.

Given a vector space $V$ over a field $F$ (like the real numbers $\mathbb{R}$), the exterior algebra is an algebraic structure that extends the concept of scalars and vectors to higher-dimensional analogs. It is denoted as $\bigwedge V$. The $k$-th `exterior power` of $V$, denoted as $\Lambda^k(V)$ or $\wedge$, is a vector space that consists of all alternating $k$-linear forms on $V$. These are essentially objects that can be thought of as $k$-dimensional oriented volumes. For example, in $\Lambda^1(V)$, elements are just vectors (1-dimensional volumes), while in $\Lambda^2(V)$, elements can be interpreted as oriented areas, and so on.

3. **Exterior Differential Forms**: An exterior differential form of degree $k$ (or a $k$-form) on a differentiable manifold $M$ is a smooth section of the $k$-th exterior power of the cotangent bundle of $M$. In simpler terms, a $k$-form is a mathematical object that can be integrated over $k$-dimensional submanifolds of $M$. These forms are crucial in defining integrals over manifolds and in the formulation of Stokes' theorem.

4. **Relationship**: The exterior power space $\Lambda^k(V)$ provides the algebraic structure that underlies the concept of $k$-forms. When you consider a manifold $M$ with a tangent space at each point that is a vector space $V$, the exterior power $\Lambda^k(T^*M)$ (where $T^*M$ is the cotangent bundle of $M$) is the space in which exterior differential forms live. This means that each $k$-form is an element of $\Lambda^k(T^*M)$ at each point of $M$.

5. **Applications**: Exterior differential forms and their associated exterior powers are used in various areas of mathematics and physics, including the formulation of Maxwell's equations in electromagnetism, the general theory of relativity, and in the study of symplectic manifolds in Hamiltonian mechanics.

In summary, the exterior power space provides the foundational algebraic structure for the study of exterior differential forms, which are key tools in differential geometry and related fields.
$$
\bigwedge^k V 
$$


