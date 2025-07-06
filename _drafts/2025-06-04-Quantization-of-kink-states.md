---
layout: post
title: Quantization of Kink States
date: 2025-06-04
author: Baiyang Zhang
catalog: true
tags:
---

# Phase space in classical mechanics

The Lagrangian naturally lives on the tangent bundle of the configuration space, while the Hamiltonian lives on the cotangent bundle of the configuration space. 

# Phase space in classical field theory

The phase space is defined to be the set of all classical trajectories *that satisfies the classical equation of motion*. In short, the phase space of classical field theory constitutes of classical solutions. These solutions are locally determined uniquely by the following two types of extra data:

1. Boundary condition (Dirichlet). The initial-time and final-time value of the field;
2. initial value. For scalar fields the EoM is second order in time derivative, so we need both the data of $\phi(\vec{x},t_ {0})$ and the derivative $\dot{\phi}(\vec{x},t_ {0})$, where $\vec{x}$ is the space coordinate and $t_ {0}$ the initial time.

Note that the phase space is not the space of all continuous, or $L^{2}$ field configurations of classical fields, but **trajectories**. 

For now, treat the equation of motion as an initial value problem. It's more convenient for the formalism to define the canonical momentum to replace the time derivative:

$$
\pi(\vec{x},t) := \frac{\partial \mathcal{L}}{\partial \dot{\phi}(\vec{x},t)}.
$$

For a set of real scalar fields, the phase space is thus equivalent to a set of initial data $\left\lbrace \phi_ {r}(\vec{x},t_ {0}),\pi_ {r}(\vec{x},t_ {0}) \right\rbrace$, where $r$ labels other particle properties, such as spin. And since $t_ {0}$ is entirely arbitrary we can just ignore it, writing just $\left\lbrace \phi_ {r}(\vec{x}),\pi_ {r}(\vec{x}) \right\rbrace$. 


- - -

# Appendix 

## Symplectic manifold
 
Let $V$ be a finite-dimensional vector space. Consider a 2-form (sometimes called 2-covector) $\omega$, given a vector $v\in V$, the interior product $i_ {v}\omega$ defines a map $\hat{\omega}:V\to V^\ast$ by $v \mapsto i_ {v}\omega := \omega(v,-)$. If $\hat{\omega}_ {v}$ is invertible (surjective and bijective), then $\omega$ is said to be `non-degenerate`. $\hat{\omega}_ {v}$ being invertible implies that $\text{ker}(\hat{\omega}_ {v})=0$, thus if $i_ {v}\omega$ sends all the vectors $w\in V$ to zero, then $i_ {v}\omega$ is the zero element in $V^\ast$, then since the kernel has only one element zero, $v$ must be zero. $\hat{\omega}_ {v}$ defines a 1-2-1 correspondence between $V$ and $V^\ast$. 

A non-degenerate 2-form is called a `symplectic tensor`, or `symplectic form`. A vector space $V$ endowed with a specific symplectic tensor is called a `symplectic vector space`.

Let $S\subseteq V$ be a subspace, let $S^{\perp}$ be the `symplectic complement` of $S$ w.r.t. the symplectic covector $\omega$:

$$
S^{\perp}:= \left\lbrace v\in V \,\middle\vert\, i_ {v}\omega(S)=0 \right\rbrace .
$$

Unlike orthogonal complements, symplectic completion is not usually exclusive with respect to each other. Although it can be shown using the rank-nullity theorem that $\text{dim}(S)+\text{dim}(S^{\perp})=\text{dim}(V)$, the dimension add up, but it is not necessary that $S \cap S^{\perp}=0$. However, when it is, the subspace $S$ is said to be `symplectic`. 

Given $\omega$ and a $2n$ dimensional vector space $V$, there is always a basis for $V^\ast$ in which $\omega$ has the canonical form:

$$
\omega = \sum_ {i=1}^{n} \alpha^{i}\wedge \beta^{i}.
$$

The corresponding basis, defined by $\left\langle \alpha ^{i} \middle\vert A_ {j} \right\rangle=\delta^{i}_ {j}$  and $\left\langle \beta ^{i} \middle\vert B_ {j} \right\rangle=\delta^{i}_ {j}$, is called a `symplectic basis` for $V$. Every symplectic vector space has a symplectic basis.

Given a 2-covector $\omega$, there is an easy way to see if it is degenerate (hence a symplectic form) or not: $\omega$ is symplectic iff $\omega^{n}:= \omega \wedge\cdots\wedge\omega \neq 0$. 

- - -

Now let's turn to manifolds instead of vector spaces. Let $\omega$ be a 2-form on $2n$ dimensional manifold $M$. $\omega$ is said to be a symplectic form if it is 1) `degenerate` and 2) `closed`. A smooth manifold endowed with a specific choice of symplectic form is called a `symplectic manifold`. A choice of symplectic form is also sometimes called a `symplectic structure`. 

For a symplectic manifold, $\omega^{n}$ is a $2n$ dimensional non-vanishing form, it naturally defines an orientation on $M$, hence every symplectic manifold is orientable. A diffeomorphism that is compatible with the symplectic structure is called a `symplectomorphism`. The study of properties of symplectic manifolds that are invariant under symplectomorphisms is known as `symplectic geometry` or `symplectic topology`.

- - -

The most important symplectic manifolds are the total spaces of cotangent bundles. They carry the so-called canonical symplectic structure. Let $E\to M$ be a cotangent bundle, namely $E_ {p}=T_ {p}^\ast M$, where $E_ {p}$ is the shorthand notation for the fiber at $p$, $\pi ^{-1}(p)$. Let $\pi:E\to M$ be the projection map. The pullback map $(d\pi)^\ast$ can take on a 1-form in $T^\ast M$, and pull it back on $T^\ast E$. Given a point on $E=(p,\varphi)$, where $p\in M$ and $\phi \in E_ {p}$. Since $\phi \in E_ {p}=T_ {p}^\ast M$, we can also regard $\varphi$ as a 1-form in the cotangent space of $T_ {p}^\ast M$, Then we can pull it back use $(d\pi)^\ast$, this defines the `tautological` 1-form,

$$
\tau:=\pi^\ast_{p,\varphi} \varphi.
$$

$\tau$ and $\varphi$ only differ in the vector space they act on, $\tau$ is in a sense tautological to $\varphi$, hence the name. The `canonical symplectic form` is defined as 

$$
\omega := - d \tau.
$$

Let $(x^{i},\xi_ {i})$ be the natural coordinates on $T^\ast M$ that is associated with coordinate $(x^{i})$, then we have $\tau=\pi ^\ast (\xi_ {i}dx^{i})=\xi_ {i}dx^{i}$, and

$$
-d\tau=-d(\xi_ {i}dx^{i}) = - d(\xi_ {i})\wedge dx^{i} = \sum_ {i}dx^{i}\wedge d\xi_ {i}.
$$

- - -

Given a function $f\in C^{\infty}(M)$ on manifold $M$, Let $\omega(-,-)$ be the symplectic form that takes two vectors and spits out a real number. $\omega$ allows us to define a vector field from $f$. 

We know that $df$ is a one-form, hence by definition $df(-)$ takes a vector $V$ and spits out a real number, $df(V)\in\mathbb{R}$. Given $V$, the symplectic 2-form maps another vector $W$ to real number, $\omega(V,W)\in\mathbb{R}$. Thus we have two ways to map $V$ to a real number:

$$
\begin{align*}
df(-):& \quad  TM \to  \mathbb{R}  \\
\omega(W,-) :&  \quad TM \to  \mathbb{R}

\end{align*}
$$

Hence we can connect $W$ and $f$ by asking the above two kinds of maps to give the same result (for all vectors) everywhere on $M$. This defines a vector $X$ from $f$, called the `Hamiltonian vector field` of $f$, usually denoted $X_ {f}$:

$$
\omega(X_ {f}, V) := df(V)\quad  \;\forall\; V\in  TM.
$$

It can be written as 

$$
X_ {f} \lrcorner\, \omega := df.
$$

Given a vector field, we can talk about the integral curve associated with it. Turns out, the integral curve are such that on which $f$ is a constant! 

Choose the coordinate system (so-called Darboux coordinates) such that the symplectic form can be written as 

$$
\omega =\sum_ {i} dx^{i}\wedge  dy_ {i},
$$

then 

$$
df = \frac{ \partial f }{ \partial x^{i} }  dx^{i} + \frac{ \partial f }{ \partial y_ {i} } dy_ {i},
$$

by comparing the coefficients we find that 

$$
 X_ {f} = \frac{ \partial f }{ \partial y_ {i} } \frac{ \partial  }{ \partial x^{i} } -\frac{ \partial f }{ \partial x^{i} } \frac{ \partial  }{ \partial y_ {i} } .
$$

In general, a symplectic manifold $(M,\omega)$ together with a smooth Hamiltonian function $H$ is called a Hamiltonian system. The Hamiltonian vector $X_ {H}$ generates a flow, called the Hamiltonian flow. The integral curve of $X_ {H}$ is called the orbits or trajectories of the system. Let $\gamma(t)$ be a Hamiltonian flow, in Darboux coordinates $\gamma(t)=x(t),y(t)$ satisfy the equations of motion:

$$
\dot{x} = \frac{ \partial H }{ \partial y_ {i} } , \quad \dot{y}=-\frac{ \partial H }{ \partial x^{i} } .
$$





