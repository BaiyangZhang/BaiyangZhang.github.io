---
layout: post
title: Note on Classical Lumps and Their Quantum Descendants
subtitle: 
date: 2024-04-26
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - Duality
  - QFT
  - Notes
---

# Classical lumps
## Solitonic waves

The waves in real world usually dissipate over time. As the energy propagates to infinite far in the form of waves, the energy density goes to zero uniformly in spacetime. The same is true for the solutions of wave equations, except for some singular solutions at least. We give a more rigorous definition for dissipation: a solution of the classical equations of motion is dissipative if 

$$
\lim_{ t \to \infty } \text{max } \mathcal{E}(\mathbf{x},t)=0,
$$

where $\mathcal{E}(\mathbf{x},t)$ is the energy density. 

The interesting thing is that there exists wave functions that allows for non-singular, non-dissipative solutions. In the most striking and simplest case, the solution is time-independent. Somehow, lumps of energy hold themselves together by their own self-interaction. 

- - - 

### Some time-independent example in one space dimension

First some conventions. The metric is taken to be $g = \text{diag}(1,-1,-1,\cdots)$, $i,j, \dots$ denote space dimensions, $a,b, \dots$ denotes internal symmetry. 

Let us consider the simplest relativistic example: theories of a single scalar field in one space and one time dimension, with non-derivative interactions. The dynamics of such a theory are describe by the Lagrangian density

$$
\mathcal{L} = \frac{1}{2} \partial _ {\mu}\phi \partial ^{\mu}\phi - U(\phi).
$$

The energy is given by a Legendre transformation $H = L - p\dot{q}$, we get 

$$
H = \int d x \,  \left[  \frac{1}{2}(\partial _ {0}\phi)^{2}+\frac{1}{2} (\partial _ {1}\phi)^{2}+U(\phi) \right].
$$

We sometimes write the total energy as the sum of kinetic and potential energy,

$$
E = T+V
$$

where $T$ is the term quadratic in *time derivatives*, and $V$ is the term involving no time derivatives. 

- - -

There are two models we will consider here. First let's take a look at the phi-fourth theory. There are two degenerate vacua, corresponding to the two directions of the boundary of the space. The potential energy is 

$$
U = \frac{\lambda}{2} (\phi^{2}-a^{2})^{2}.
$$

The vacuum configuration is clearly given by $\phi = \pm a$ a constant in spacetime. In a different form $a$ is written as $a = \mu^{2} / \lambda$. 

Next let's consider the sine-Gordon potential, 

$$
U = \frac{\alpha}{\beta^{2}} (1-\cos \beta \phi).
$$

The ground states have infinite degeneracy. 

We want to find the time-independent solutions of the equations of motion. We need to find the stationary point of the energy function, which is very similar to finding the stationary point of the action, with one difference: the sign of the potential term. Mathematically, looking for the time-independent solution is the same as looking for the motion of a particle of unit mass in a potential equal to **minus** $U(x)$. 

To emphasize, **we can turn a static problem of finding the time-independent solution that minimizes the Hamiltonian, to a dynamical problem of finding the motion of a particle (of unit mass) in a reversed potential.** The latter allows us to make use of our intuition and imagination, and helps to visualize the solution.

Every motion of the particle in the potential corresponds to a time-independent solution of the field equations, but not all of them are of finite energy. For the energy integral to converge, the energy density must go to zero at space infinity. In terms of the particle problem, this boundary conditions fixes the possible initial and final positions. 

In the example of the phi-fourth theory, the potential takes the form of double-well. The minus version of the potential is of the form double hill. It would be helpful to draw some picture here but I am too lazy, interested readers should just read Coleman's book. The lump solution corresponds to the motion that the particle starts off from one of the hills and rolls over the valley and reaches the other hill and stays there.

By convention, we call the solution for which $\phi$ is monotone increasing `lumps` and those for which it is monotone decreasing `antilumps`.

To find the exact expression of the solution, let's adopt the dynamic picture of a moving particle. The potential is now $-U(x)$ where $x$ is identified with $\phi$ in the static problem. The total energy is conserved to zero during the whole motion, thus 

$$
\frac{1}{2} \left( \frac{dx}{dt} \right)^{2} - U(x) = 0.
$$

We can translate this back into field language by substitution $x\to \phi$ and the solution can be read off instantly in the integral form,

$$
\phi(x) = \pm\int d x \,[2U(\phi(x))]^{1/2}
$$

or 

$$
x = \pm\int_ {\phi_ {0}}^{\phi} d\phi \,  [2U(\phi')]^{- 1/2}.
$$


Note that the solutions enjoys the translation symmetry, meaning the center of the lump can be translated to anywhere. 

These equation also enables us to simplify the expression for the energy of a lump, thanks to the fact that a lump satisfies the equation of motion. 

For phi-fourth theory, we find for the form of the lump

$$
\phi = a \tanh(\mu x).
$$

The energy of the lump is given by 

$$
E = \frac{4\mu^{3}}{3\lambda}.
$$

The lumps of $\phi^{4}$ theory is frequently called `kinks` in the literature.

For the sine-Gordon theory, we find 

$$
\phi = \frac{4}{\beta} \tan^{-1} \exp(\alpha^{1/2}x)
$$

where which branch of the inverse tangent we choose determines which two zeros we move between. The energy of the lump is 

$$
E = \frac{8\alpha^{1/2}}{\beta^{2}}.
$$

The lumps of sine-Gordon theory are frequently called `solitons` in the literature. In both cases the antilumps are obtained simply by multiplying by minus one.

A few words on the stability of the kink solution. We know that the equation of motion in the kink background has solutions called normal modes, each with a eigen value corresponding to the energy. The kink is stable under fluctuation if all the eigen values are non-negative, otherwise the perturbation in the direction of the negative-eigenvalue normal mode would decrease the energy indefinitely, hence making the kink unstable. Hence, if we can prove that there exists no normal modes with negative eigen values, we can prove that the kink is stable. To do this, we need two ingredients:  zero mode and the node theorem. Zero mode is a result of translation symmetry of the model, or rather the breaking of it. Zero mode is a constant solution with no nodes, and the node theorem says that for 1-dimensional Schrodinger equation, the lowest wave function has zero node, the first excitation wave function has one nodes, etc. Then the zero mode is the lowest energy state, with energy zero! Hence there exists no negative eigen value.

A kink in $\phi^{4}$ theory can be very well regarded as a almost-localized classical particle, with one major difference: the condition for patching adjacent kink solutions together must be ...kink-antikink-kink..., otherwise it would not be a solution to the equation of motion. 


## With gauge field

Let $\phi$ be a vector of scalar field with gauge group $G$ and gauge field $A$. The covariant derivative and field strength are defined in the usual way, you can pick your favorite convention. Let $\phi=\phi_ {0}$, $A =0$ be the ground state. Due to the gauge invariance (or more precisely, gauge redundancy), there might exist a subset $H$ of $G$ such that it leaves $\phi=\phi_ {0},A=0$ unchanged. It is usually written as $H<G$, then for any $h\in H$ we have $h\phi_ {0}=\phi_ {0}$, $H$ is the little group of $\phi_ {0}$, $\phi_ {0}$ is the fixed point of $H$. If we study the fluctuation near $\phi_ {0}$, we find that the gauge fields associated with the generators of $H$ remains massless. The vacuum manifold would be the coset space $G/H$, for reasons that I have no time to explain here. This is under the assumption that the vacuum manifold is connected and on which the gauge group acts transitively. This excludes both the case of accidental degeneracy and existence of ordinary (non-gauge) symmetry. Accidental degeneracy refers to a situation where two or more energy levels have the same energy not due to an obvious symmetry of the system, but rather due to a more subtle or hidden symmetry, or as a result of a specific mathematical coincidence, such as the accidental degeneracy in the hydrogen atom. This differs from the usual degeneracy associated with the symmetries of the system's Hamiltonian, such as those arising from rotational or translational invariance. 

We can wrap the vacuum manifold, namely the coset space, around the space boundary, this gives a homotopy group. This homotopy group classifies topologically different field configurations the theory admits. 

The rest of Coleman's lecture goes to a involved discussion of homotopy groups and short exact sequence, we will not note it here. Instead, we will directly dive into the quantum lumps. But before going there, I can't resist to say that Sidney Coleman's illustration of the map 

$$
\pi_ {2}(G) \to \pi_ {1}(H)
$$

is brilliant! I strongly recommend section 3.7 to everyone. I've learnt about homotopy groups from other places, mostly from a pure mathematical perspective, and I've learnt how to use the short exact sequence to evaluate the homotopy group, but Coleman's introduction is more intuitive and straightforward. It serves as a pretty good supplement to short exact sequence argument. Coleman's section 3.7 can be regarded as a special case of Theorem. 22.27 in Frankel's textbook.

- - -

# Quantum lumps
## Power expansion of the time-independent lumps

The quantization of kink is a fascinating topic. We start from the classical solution and consider the small perturbations about it, order by order. 

Consider the sine-Gordon Lagrangian:

$$
\boxed{ 
\mathcal{L} = \frac{1}{2} (\partial \phi)^{2} + \frac{\alpha}{\beta^{2}} (\cos \beta \phi-1),
}
$$

where under the $\cos$ function, $\beta$ cancels the dimension of $\phi$ and renders $\beta \phi$ dimensionless. 

We can rescale field such that the parameter $\beta$ factors out of the Lagrangian. Since $\beta \phi$ appears together under $\cos$ function, let's define 

$$
\tilde{\phi} := \phi \beta
$$

then the Lagrangian in term it reads

$$
\mathcal{L} = \frac{1}{\beta^{2}} \left[ \frac{1}{2}(\partial \tilde{\phi})^{2}+\alpha(\cos \tilde{\phi}-1) \right].
$$

If you write down the equation of motion corresponding to the above Lagrangian, you'll find that 
