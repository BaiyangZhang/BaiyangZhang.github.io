---
layout: post
title: Classical correspondence of displacement operation
date: 2025-06-04
author: Baiyang Zhang
catalog: true
tags:
---

# Phase space in classical field theory

The phase space is defined to be the set of all classical trajectories *that satisfies the classical equation of motion*. They are locally determined uniquely by the following two types of extra data:

1. Boundary condition (Dirichlet). The initial-time and final-time value of the field;
2. initial value. For scalar fields the EoM is second order in time derivative, so we need both the data of $\phi(\vec{x},t_ {0})$ and the derivative $\dot{\phi}(\vec{x},t_ {0})$, where $\vec{x}$ is the space coordinate and $t_ {0}$ the initial time.

Note that the phase space is not the space of all continuous, or $L^{2}$ field configurations of classical fields, but **trajectories**. 

For now, treat the equation of motion as an initial value problem. It's more convenient for the formalism to define the canonical momentum to replace the time derivative:

$$
\pi(\vec{x},t) := \frac{\partial \mathcal{L}}{\partial \dot{\phi}(\vec{x},t)}.
$$

For a set of real scalar fields, the phase space is thus equivalent to a set of initial data $\left\lbrace \phi_ {r}(\vec{x},t_ {0}),\pi_ {r}(\vec{x},t_ {0}) \right\rbrace$, where $r$ labels other particle properties, such as spin. And since $t_ {0}$ is entirely arbitrary we can just ignore it, writing just $\left\lbrace \phi_ {r}(\vec{x}),\pi_ {r}(\vec{x}) \right\rbrace$. 



