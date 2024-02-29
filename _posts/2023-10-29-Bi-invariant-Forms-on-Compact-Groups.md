---
layout: post
title: Bi-invariant Forms on Compact Groups
subtitle: 
date: 2023-10-29
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - geometry
  - differentialForms
  - frankel
---
*Disclaimer: Nothing in this note is original.*

## Bi-invariant Forms on Compact Groups

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

The Cartan 3-form plays an especially important role. Since $\Omega(X)=X$ for all $X\in{\frak g}$, we have
$$
(\Omega \wedge \Omega)(X,Y) = \Omega(X)\otimes \Omega(Y) - \Omega(Y)\otimes \Omega(X)=[X,Y],
$$
When $G$ is compact we have
$$
\Omega^{3}(X,Y,Z) = 3\mathrm{Tr}\,([X,Y]Z).
$$

- - -

**Bi-invariant Riemannian Metrics**

Let $\left\langle -,- \right\rangle$ be the scalar product in ${\frak g}$ that is Ad invariant. The existence of an invariant scalar product is closely related to the concept of compactness for Lie groups. If a Lie group is compact, then it is possible to average any bilinear form on the Lie algebra over the group to obtain an invariant scalar product. This averaging process relies on the existence of a normalized Haar measure, which exists for compact groups. However, if the Lie group is not compact, such a Haar measure does not exist in general, and hence the averaging process cannot be carried out in the same way. As a result, there is no guarantee that a non-compact Lie group will have an invariant scalar product on its Lie algebra. That said, it is possible for non-compact Lie groups to have invariant scalar products on their Lie algebras, but this is not guaranteed, and it depends on the specific properties of the group and its algebra. 

**Theorem.** There is a bi-invariant Riemannian metric on every compact Lie group

**Theorem.** In any bi-invariant metric on a group, the geodesics are the 1-parameter subgroups and their translates.

As a result, in a group with a bi-variant Riemann metric, a geodesic through $e$ with tangent velocity $X$ is given by $e^{ tX }$. 

One says that a Riemannian manifold $M^{n}$ is `geodesically complete` if every geodesic starting anywhere $C(0)\cdot e^{ tX }$ exists for all real value of $t$. It is a fact that if $M$ is compact then it is automatically geodesically complete. Furthermore

**Hopf-Rinow Theorem.** If $M^{n}$ is geodesically complete, then any pair of points on $G$ can be joined with a geodesic of minimal length.

For a proof of these facts see Milnor’s book.

In a compact group $G$ we may introduce a bi-invariant metric, and then the 1- parameter subgroups are geodesics. Thus

**Theorem.** Every point in a compact connected Lie group G lies on at least one 1-parameter subgroup. 

- - -

There is a theorem saying that, in a *bi-invariant metric* on a *compact* connected Lie group $G$, the bi-invariant forms coincide with the harmonic forms.

We will skip the proof here, just mention that it will make use of the fact that the Hodge dual $\star$ commutes with left and right translations $R_ {g\ast}, L_ {g\ast}$. 

**Bi-invariant forms are harmonic in the bi-invariant metric!**

- - -

The `center` of a group $G$ is the *subgroup* $Z$ of elements that commute with all the elements of the group. For example, the center of $U(N)$ is $e^{ i\theta }\mathbb{1}_ {N}$, the center of $SU(N)$ is the $n$ scalars $\lambda$ such that $\lambda^{i}=1,\;i=1,\dots,N$.

**Weyl’s Theorem.** Let $G$ be a compact connected group. Then the first Betti number vanishes, $b_ {1}(G) = 0$, iff the center of $G$ does not contain any $1$-parameter subgroup.

In particular, $b_ {1}=0$ for $SU(N)$ but not for $U(N)$. 

The following plays an important role in gauge theories,

**Cartan's Theorem.** If $G$ is a *compact*, *nonabelian* Lie group, then the Cartan $3$-form
$$
\Omega_ {3} = \mathrm{Tr}\,(g^{-1} dg g^{-1}  dg g^{-1}  dg)
$$
is a non-trivial harmonic form. In particular $b_ {3}(G)\neq 0$. 

## The Geometry of a Lie Group

Let $G$ be a Lie group endowed with a bi-invariant metric (which exist on every compact Lie group). Let $\mathbf{X},\mathbf{Y},\mathbf{Z},\dots$ be left-invariant vector fields. In a compact Lie group, geodesics are also 1-parameter subgroups and vise versa, so 
$$
\nabla_ {\mathbf{X}}\mathbf{X}=0.
$$
Like wise, 
$$
\nabla_ {\mathbf{X}+\mathbf{Y}}(\mathbf{X}+\mathbf{Y}) \implies 2\nabla_ {\mathbf{X}}\mathbf{Y}=[\mathbf{X},\mathbf{Y}].
$$

The center of a Lie algebra ${\frak g}$ is defined to be the elements $\mathbf{X}$ of ${\frak g}$ such that $[\mathbf{X},\mathbf{Y}]=0$ for all $\mathbf{Y}\in{\frak g}$. 

**Weyl’s Theorem.** Let $G$ be a compact Lie group with bi-invariant metric. Suppose that the center of $G$ is trivial, then $G$ is compact and has a finite fundamental group $\pi_ {1}(G)$. 

