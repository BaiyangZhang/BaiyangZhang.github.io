---
layout: post
title: Note on the kink mass correction in 3D
subtitle: 
date: 2024-01-02
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---

# The model 

We will establish the model and notations in this section. First, some nomenclatures.

`Shape modes`: In theories with a kink solution, the equation of motion in the background of the kink typically has discrete, bounded solutions. They are called `shape modes`. They are localized around the kink. Shape modes represent small fluctuations or deformations of the kink's shape. Unlike the continuum of delocalized modes that represent free particle states, the shape modes are confined to the vicinity of the kink, with discrete energy levels. 

`Oscillons`: They are localized, non-solitonic, and semi-stable field configurations that oscillate in time. They are interesting because they represent a form of quasi-stable, localized energy concentration that can persist for long times, even though they are not topologically protected like solitons or kinks. Oscillons are found in various nonlinear field theories and have been studied in different contexts, including cosmology and condensed matter physics. Their persistence and behaviors under various conditions are subjects of ongoing research in theoretical physics. However, it is believed that quantum correction will make oscillons rapidly decay into a pair of fundamental particles. 

`The Unruh effect`: The Unruh effect is a prediction in quantum field theory, stating that an observer accelerating through a vacuum will perceive a thermal bath of particles, whereas an inertial observer would see none. This effect arises from the realization that *the concept of a vacuum state (or empty space) is observer-dependent*. For an accelerating observer, what appears as empty space to an inertial observer is seen as a warm gas of particles. This effect, named after physicist William Unruh, highlights the interplay between quantum theory and relativity, especially in contexts like black hole physics.

In the frame work of the linearized soliton perturbation theory, we can systematically study the quantum corrections to both static and time-dependent solitonic solutions.

- - -

Firstly, we work in the Schrodinger picture where the operator are time-independent while the wave functions (vectors in Hilbert space) are time dependent. Secondly, we will start with the Hamiltonian formalism where the canonical momentum, $\pi$, is considered as a fundamental ingredient, rather than the time derivative of $\phi$, the field of the Lagrangian. 

In $2+1$ dimension, the Hamiltonian $H$ is  the integral of the Hamiltonian density $\mathcal{H}$ over the 2D manifold of space alone, 
$$
H = \int_ {M} dx^{2}\, \mathcal{H}(\phi,\pi),\quad  \mathcal{H}=\frac{1}{2}\pi^{2}(x)+\frac{1}{2} (\partial_ i \phi)^{2} + \frac{1}{\lambda}V(\sqrt{ \lambda }\phi(x)) 
$$

**Dimensional analysis.** In Lagrangian formalism, $[S]=\hbar$ where $S$ is the action, and $S = \int d^d x \, \mathcal{L}$, where $\mathcal{L}$ is the Lagrangian (density) and $d$ is the space-time dimension. Note that we are working with a partly "natural" units, where $c=1$ but $\hbar \neq 1$. Since $c=1$ we still have $[x] = [t]$, but no-longer do we have $[t]=-[E]$ since this is a result of $[\hbar]=ET=1$. If we want to write the dimension of everything in terms of $E$ and $\hbar$, we can define
$$
[x] = [t] = T = \frac{\hbar}{E}.
$$
## A digression to $\hbar$-expansion

To appreciate the importance of $\hbar$, just recall that in canonical quantization $[x,p]=i\hbar$, $\hbar$ enters explicitly in the commutation relation, providing the fundamental basis of quantum theory. This is also true in the case of quantum field theory. Furthermore, at each order of an expansion in $\hbar$, the physical symmetries (Lorentz invariance, $U(1)$ symmetry, etc.) must be satisfied, otherwise there will be some special value of $\hbar$ only at which the symmetries are preserved, which is just strange. 

In the unit where $c=1$, the Planck's constant $\hbar$ has the unit of action, or rather the action has the unit of $[\hbar]=ET$, where $E$ is the energy scale and $T$ the time. It turns out that there are more than one way to assign $\hbar$-dependence for quantities such as the mass $m$, the coupling $g,\lambda$ etc. A criterion for the "right" choice is that, at $\hbar\to 0$ limit, the quantum theory agrees with the classical theory. As an example, take a look at the harmonic oscillator,  