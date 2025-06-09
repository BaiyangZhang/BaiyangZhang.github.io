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

