---
layout: post
title: The Geometry of WKB Method
subtitle: 
date: 2023-09-14
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags: []
---

### A short review of harmonic oscillator

Consider a one-dimensional harmonic oscillator. We have two ways to describe the motion,

1. The Lagrangian formalism. Given the Lagrangian $L=T-V$, where $T$ is the kinetic energy and $V$ the potential, we can obtain the Euler-Lagrange equation (or simply the equation of motion), which is a second order differential equation in $q(t)$, since $q(t)$ takes value in $\mathbb{R}$ we can say that the Euler-Lagrange equation is a *second order equation define on $\mathbb{R}$*. 
2. The Hamiltonian formalism. Given the Hamilton function $H(q,p)$ which is a function of both the (generalized) coordinate $p$ and the corresponding canonical momentum $q$. Then we can obtain a set of first order partial differential equations, collectively called the **Hamilton's equations**. Since $p,q$ live in $\mathbb{R}^{2}$, we can say that now we have *two first-order differential equations on $\mathbb{R}^{2}$*. This $\mathbb{R}^{2}$ is nothing but the phase space of the dynamic system in question. 

The price to pay for going from second order differential equations to the first order equation is having more equations. 

We will focus on the second approach, the Hamiltonian formalism. Hamilton's equation generates us a flow in the phase space, dependent on time $t$.  

We note two features of the Hamiltonian description of a system,

1. The Hamilton function $H(q,p)$ is independent of time. This is most obvious in the Poisson bracket formalism, where the time derivative of a function $\mathcal{O}$ is given by $\left\{ \mathcal{O},H \right\}$.
2. The velocity vector field of the flow generated by the Hamilton function has zero divergence. The velocity vector is
$$
X :=(\dot{q},\dot{p})=\left( \frac{\partial H}{\partial p},-\frac{\partial H}{\partial q} \right)
$$
thus 
$$
\text{div} X = (\partial_ {q},\partial_ {p})\cdot X = 0.
$$
Geometrically this means that the flow preserves the area of a area element. 

- - -

The canonical quantization works as follows. We upgrade $x$ and $p$ into operators,
$$
x\to \hat{x}, \quad  p \to \hat{p} := -i\hbar \partial_ {x}.
$$
The classical Hamiltonian $H(x,p)$ then becomes the Hamiltonian operator, which can be inserted into the Schrodinger equation. This is how we **quantize the equation**. There is also the **quantization of solutions**, roughly speaking. That is, given a system, say the motion of some particle in some potential, the quantum mechanical motion of this particle very much resembles that in the classical case. This is clearer in the case of path integral, the dominant contribution comes always from the classical trajectory. Then, we can make use of this property to study the quantum effects approximately. The error should decrease as $\hbar$ decrease. 

### Some classical mechanics

Recall that a `canonical transformation` is a change of variables, namely generalized coordinates and associated canonical momenta, such that the new variables preserve the form of Hamilton's equations. In other words, if you have a system described by a set of generalized coordinates $q_ {i}$​ and their conjugate momenta $p _ {i}$​, and you transform to a new set of variables $Q_ {i}$​ and $P_ {i}$​, the transformation is canonical if the new variables also satisfy Hamilton's equations but *with potentially a new Hamiltonian*. 


### The WKB method




### Symplectic Manifolds

A symplectic manifold is a pair $(M,\omega)$ where 
- $M$ is a even-dimensional ($2n$) manifold,
- $\omega$ is a **closed**, non-degenerate $2$-form on $M$. This $2$-form is called the symplectic form.

Recall that a $2$-form $\eta$ is degenerate if there exists a non-zero vector $X$ such $\eta(X,Y)=0$ for all vector $Y$. 

These properties ensure that $\omega$ provides a kind of "twisted" volume element on $M$, giving a structure similar to a Riemannian metric but with crucial differences.
