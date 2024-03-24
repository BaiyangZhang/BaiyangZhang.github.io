---
layout: post
title: Introduction to Higher Form Symmetry
subtitle: Lecture 3
date: 2023-12-21
author: Baiyang Zhang
header-img: img/lib3.jpg
catalog: true
tags:
  - higherFormSymmetry
  - generalizedSymmetry
---

For conventions used in this note, see my other blog [here](https://www.mathlimbo.net/blog/2022/Conventions-and-Formula/). 

In lecture 2 we talked about classic symmetry and their re-interpretation in the language of differential (exterior) form. We have made the connection between the so-called symmetry defect operator (SDO) and a charged, point (0-dimensional) operator. In this note we try to generalized this concept to charged operators defined on manifolds of dimension more than zero, such as a line or a surface, etc. 

Let's start with the ordinary symmetry once again on a $D$-dimensional manifold. We first upgraded the global symmetry parametrized by $\epsilon$ to a local symmetry parametrized by $\epsilon(x)$, and write the action variation as

$$
\delta S = \int d^{D}x \, J^{\mu}\partial_ {\mu}\epsilon(x)
\tag{1}
$$

under $e^{ iQ_ {\Sigma} }$ the charged operators with non-trivial linking $\text{Link}(\Sigma,x)$ transform as 

$$
\phi(x) \to \epsilon(x) \Delta \phi(x).
$$

In our convention, $\Delta$ stands for a small but finite change while $\epsilon(x)$ stands for an infinitesimal parameter. Eq. (1) can be regarded as the definition of the Noether current $J^{\mu}$, which tells us how much the action changed under the transformation in question. But, being a symmetry of the system, of course the action must remains unchanged under the transformation, thus we have the Noether current 

$$
\partial_ {\mu}J^{\mu} = 0 \Longleftrightarrow d\star J=0.
$$

In terms of differential forms, function $\epsilon(x)$ is a $0$-form and constant function $\epsilon$ is a closed form. The variation of action reads

$$
\delta S = \int_ {M^{(D)}} (\star J)\wedge d\epsilon,
\tag{2}
$$

where $\star J$ is a $(D-1)$-form, $d \epsilon$ is a $1$-form (since $\epsilon$ is a zero form), hence their wedge product is a $D$-form, something can be integrated over $D$-dimensional manifold $M$ (whose boundary is $\Sigma$). 

- - -

The advantage of Eq. (2) is that it can be generalized to higher forms. Assume now the symmetry is parametrized by a $1$-form $\xi = \xi_ {\mu}dx^{\mu}$. Then $d \xi$ is a 2-form, as a result $\star J$ is a $(D-2)$-form thus $J$ is a $2$-form. The conservation law becomes

$$
d \star J = 0 \to \partial_ {\mu} J^{\mu \nu}=0.
$$

Since $(D-2)$-form can be integrated over a $(D-2)$ manifold, we can define the charge operator as 

$$
Q(\Sigma_ {D-2}):= \int_ {\Sigma} \,  \star J.
$$

