---
layout: post
title: Bi-invariant Forms on Compact Groups
subtitle: 
date: 2023-10-24
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Minkowski
  - Frankel
---
*Disclaimer: Nothing in this note is original.*

Recall that a form or vector field on $G$ is said to be bi-invariant if it is both left and right invariant. 

**Theorem.** if $\alpha$ is a bi-invariant $p$-form, then $p$ is closed,
$$
d \alpha=0.
$$
Recall that the Maurer-Cartan form is defined as 
$$
\Omega := g^{-1} dg
$$

The Maurer-Cartan form is a $\mathfrak{g}$-valued 1-form defined on a Lie group $G$, where $\mathfrak{g}$ is the Lie algebra of $G$. The Maurer-Cartan form encodes the local structure of the Lie group, and it is used to translate between the geometry of the Lie group and the algebra of its Lie algebra.

 If $G$ is a Lie group and $g \in G$, the Maurer-Cartan form $\Omega$ at $g$ is a linear map from the tangent space $T_gG$ of $G$ at $g$ to the Lie algebra $\mathfrak{g}$ of $G$:

$$
\Omega_g : T_gG \rightarrow \mathfrak{g}.
$$

Now, let $v$ be a $\mathfrak{g}$-valued vector field on $G$. Then the action of the Maurer-Cartan form on $v$ is given by
$$
\Omega(v) : G \rightarrow \mathfrak{g},
$$$$
g \mapsto \Omega_g(v_g),
$$
where $v_g$ is the value of the vector field $v$ at $g \in G$.

The Maurer-Cartan form has the property that it is left-invariant, i.e., for any $g, h \in G$, we have
$$
\Omega_{gh} = \mathrm{Ad}(h^{-1}) \cdot \Omega_g,
$$
where $\mathrm{Ad}$ is the adjoint representation of the Lie group $G$. This reflects the relationship between the geometry of the Lie group and the algebraic structure of its Lie algebra.

we can also define the `Cartan p-form`
$$
\Omega_ {p} := \mathrm{Tr}\, \Omega^{p} =\mathrm{Tr}\,\left\{ \Omega \wedge \dots \wedge \Omega \right\} .
$$
Cartan p-forms are scalar forms with very special properties, 1) they are bi-invariant hence closed, 2) $\Omega_ {2p}=0$ automatically. We will neglect the proof here. 

