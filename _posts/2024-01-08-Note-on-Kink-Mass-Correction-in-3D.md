---
layout: post
title: Note on the kink mass correction in 3D
subtitle: 
date: 2024-01-08
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---

# The model 

We will establish the model and notations in this section. First, some nomenclatures.

`Shape modes`: In theories with a kink solution, the equation of motion in the background of the kink typically has discrete, bounded solutions. They are called `shape modes`. They are localized around the kink. Shape modes represent small fluctuations or deformations of the kink's shape. Unlike the continuum of delocalized modes that represent free particle states, the shape modes are confined to the vicinity of the kink, with discrete energy levels. 

`Oscillons`: They are localized, non-solitonic, and semi-stable field configurations that oscillate in time. They are interesting because they represent a form of partial stable, localized energy concentration that can persist for long times, even though they are not topologically protected like solitons or kinks. Oscillons are found in various nonlinear field theories and have been studied in different contexts, including cosmology and condensed matter physics. Their persistence and behaviors under various conditions are subjects of ongoing research in theoretical physics. However, it is believed that quantum correction will make oscillons rapidly decay into a pair of fundamental particles. 

`The Unruh effect`: The Unruh effect is a prediction in quantum field theory, stating that an observer accelerating through a vacuum will perceive a thermal bath of particles, whereas an inertial observer would see none. This effect arises from the realization that *the concept of a vacuum state (or empty space) is observer-dependent*. For an accelerating observer, what appears as empty space to an inertial observer is seen as a warm gas of particles. This effect, named after physicist William Unruh, highlights the interplay between quantum theory and relativity, especially in contexts like black hole physics.

In the frame work of the linearized soliton perturbation theory, we can systematically study the quantum corrections to both static and time-dependent solitonic solutions.

- - -

Firstly, we work in the Schrodinger picture where the operator are time-independent while the wave functions (vectors in Hilbert space) are time dependent. Secondly, we will start with the Hamiltonian formalism where the canonical momentum, $\pi$, is considered as a fundamental ingredient, rather than the time derivative of $\phi$, the field of the Lagrangian. 

In $2+1$ dimension, the Hamiltonian $H$ is  the integral of the Hamiltonian density $\mathcal{H}$ over the 2D manifold of space alone, 
$$
H = \int_ {M} d^{2}x\, \mathcal{H}(\phi,\pi),\quad  \mathcal{H}=\frac{1}{2}\pi^{2}(x)+\frac{1}{2} (\partial_ i \phi)^{2} + \frac{1}{\lambda}V(\sqrt{ \lambda }\phi(x)) 
$$

**Dimensional analysis.** In Lagrangian formalism, $[S]=[\hbar]$ where $S$ is the action, and $S = \int d^d x \, \mathcal{L}$, where $\mathcal{L}$ is the Lagrangian (density) and $d$ is the space-time dimension. Note that right now we are working with a partially "natural" units, where $c=1$ but $\hbar \neq 1$. Since $c=1$ we still have $[x] = [t]$, namely $L=T$ ($L$ is length and $T$ is time), but no longer do we have $T=E^{-1}$ since this is a result of $[\hbar]=ET=1$ (recall that $\hbar \omega=E$, meaning $[\hbar \omega]=E$, and $\omega$ is the frequency with dimension $1 / T$ ). 

Let $d$ be the dimension of spacetime, in the partial natural unit we have
$$
\int d^{d}x \, \mathcal{L}\sim \hbar \implies [\mathcal{L}]=[\hbar] L^{-d}
$$
Take a specific term, say $(\partial \phi)^{2}$, to continue the analysis,
$$
[(\partial \phi)^{2}] = L^{-2} [\phi^{2}] = [\mathcal{L}] = [\hbar]L^{-d} \implies [\phi^{2}]=[\hbar] L^{2-d}
$$
which is 
$$
[\phi] = [\sqrt{ \hbar }] \, L^{1-d / 2}.\tag{1}
$$
This agrees with the convention that field operator $\phi$ scales as $\sqrt{ \hbar }$. Furthermore, this scaling property does not depend on the spacetime dimension $d$, it holds for any spacetime dimension.

I don't think the $\hbar$-dependence given by Eq. (1) is unique, apparently there exist other possibilities, we can move $\hbar$ around in the Lagrangian, just to make sure that the action altogether is of dimension $\hbar$. However it seems that $\phi\sim \hbar^{1/2}$ is indeed the most convenient option. Another way to see the advantage of this choice is from the action,
$$
S \sim \hbar \sim \int d^{4}x \, (m^{2} \phi^{2}+(\partial \phi)^{2} +U(\phi)),
$$
then
$$
\int d^{4}x \, \left[ m^{2} \xi^{2}+(\partial \xi)^{2} + U(\xi) \right] \sim 1,   \quad \xi:= \frac{\phi}{\sqrt{ \hbar }} . 
$$
In this way, we can absorb $\hbar$ into the definition of $\phi$, this is similar to absorbing the coupling $g$ into the field definition in gauge theory. We now *define* $\xi$ to be *independent* of $\hbar$. 

Having fixed the $\hbar$-dependence of $\phi$, we can substitute it to the potential $U$, for example the $\phi^{4}$ model to determine the $\hbar$ dependence of the coupling,
$$
[S]\sim\int d^{d}x \, \lambda \phi^{4} \sim L^{d} [\lambda][\hbar^{2}] L^{4-2d} = L^{4-d}[\hbar^{2}][\lambda],
$$
on the other hand we already know that $S\sim \hbar$ so
$$
L^{4-d}[\hbar^{2}][\lambda] = [\hbar] \implies [\lambda \hbar] = L^{d-4}. 
$$
If we choose $L$ to be the fundamental unit instead of energy $E$, it is clear the $\lambda \hbar$ is independent of $\hbar$. Plus, we see that $d=4$ is special.

For the sake of completeness, let's consider the mass term in the Lagrangian. Similar to what we have for the kinetic term, 
$$
[m^{2} \phi^{2}] = E^{2}\, [\phi^{2}] = [\mathcal{L}] = [\hbar]\,L^{-d} \implies [\phi] = [\sqrt{ \hbar }]L^{-d/2}E^{-1} .
\tag{2}
$$

**Dimension and measurement**

If two things are of the same dimension, for example, say
$$
[A] \sim [a] = L
$$
where $\sim$ means having the same dimension. Then we can use one of them as the unit to measure the other, say, use $a$ as the "ruler" to measure $A$, the result $\widetilde{A} :=A / a$ is a dimensionless number. 

Suppose $[\phi]=[\hbar]^{1/2}$, another way to say the same ting is $\phi \sim \sqrt{ \hbar }$, note that the tilde does not imply any relation between the *values* of $\phi$ and $\sqrt{ \hbar }$, it only means that they have the same dimension. The point is, since they have the same dimension, we can use one of them to measure the other, for example we can define
$$
\tilde{\phi} = \phi / \sqrt{ \hbar }
$$
which is a dimensionless number. Since $\hbar$ scales the "quantumness", the more classical the world is, the smaller $\hbar$ (and $\sqrt{ \hbar }$), hence the bigger numeric value of $\tilde{\phi}$. 

- - -

In the partial natural units, I'd like to think there are two fundamental "rulers" to measure all the quantities, such as mass, coupling, field, etc. One of them is the unit of energy, for example $\text{MeV}$, the other is $\hbar$ whose dimension is $ET$. To measure the length of something, we can use $\frac{\hbar}{\text{MeV}}$ as unit. The advantage of the partial natural unit is that it makes explicit the $\hbar$ factor, revealing the direct relations between quantities with $\hbar$, which is the scale of quantumness, this enables us to discern the importance of various quantities in the classical limit, making the analysis regarding semi-classical more straightforward. 
## Digression to $\hbar$-expansion

To appreciate the importance of $\hbar$, just recall that in canonical quantization $[x,p]=i\hbar$, $\hbar$ enters explicitly in the commutation relation, providing the fundamental basis of quantum theory. This is also true in the case of quantum field theory. Furthermore, at each order of an expansion in $\hbar$, the physical symmetries (Lorentz invariance, $U(1)$ symmetry, etc.) must be satisfied, otherwise there will be some special value of $\hbar$ only at which the symmetries are preserved, which is just strange. 

In the unit where $c=1$, the Planck's constant $\hbar$ has the unit of action, or rather the action has the unit of $[\hbar]=ET$, where $E$ is the energy scale and $T$ the time. It turns out that there are more than one way to assign $\hbar$-dependence for quantities such as the mass $m$, the coupling $g,\lambda$ etc. A criterion for the "right" choice is that, at $\hbar\to 0$ limit, the quantum theory agrees with the classical theory. As an example, Stanley Brodsky and Paul Hoyer in their [paper](https://arxiv.org/pdf/1009.2313.pdf) used the quantum mechanical harmonic oscillator as an example in Eq.(1). The gist is that, you can rescale $x$ to $x / \sqrt{ \hbar }$, then the propagator is formally independent of $\hbar$. However, this will change how we view distance, in the $\hbar\to 0$ limit, for a fixed distance $L$, the "length" measure will increase as $1 / \sqrt{ \hbar }$, hence we are going to smaller and smaller area. 

It is generally understood that each loop contribution to amplitudes is associated with one factor of $\hbar$. However, to fully define the $\hbar\to 0$ limit one need to specify the $\hbar$ dependence of various quantities in the Lagrangian as mentioned before, such as the field operator, the mass, the coupling, etc. This is not as straightforward as one might think, for $\hbar$ not only appears in the action $iS / \hbar$ but also appears in the Lagrangian. In Brodsky's paper mentioned above, the authors proposed a way to establish the $\hbar$ dependence such that the loop and $\hbar$ expansions are equivalent. We will go to more details in the following.

**First, regard $\hbar$ as a constant of nature with certain dimension, use $\hbar$ to make terms in the Lagrangian dimensionless.**

Again, let's work with the assumption that $c = \epsilon_ {0} = 1$. Require $[S]=\hbar$, and $\alpha_ {s} = g^{2} / 4\pi \hbar$ is dimensionless, the latter implies that $[g]=\sqrt{ \hbar }=\sqrt{ ET }=\sqrt{ EL }$. From the self-energy of gluons $G_ {\mu \nu}G^{\mu \nu}$ where $G = \partial A - \partial A +ig / \hbar [A,A]$ we have  
$$
[A] = \sqrt{ \frac{E}{L} }.
$$
For the same reasons, in the scalar QED the classical electric charge $e$ and mass $m$ are divided by $\hbar$,
$$
S_ {\text{sQED}} = \int d^{4}x \, \left\lbrace \left\lvert D\phi \right\rvert ^{2}-\frac{m^{2}}{\hbar^{2}}\left\lvert \phi \right\rvert ^{2} \right\rbrace , \quad  D = \partial +i \frac{e}{\hbar }A.
$$
The boson field dimension 
$$
[\phi]=[A]= \sqrt{ \frac{E}{L} }.
$$
Fermion fields are more complicated, since they have no classical counterparts, their dimensions are convention-dependent. We will deal with fermions in a different note perhaps.

**Second step is to specify $\hbar$ dependence of all quantities appearing in the action.**

The choice made by Brodsky and Hoyer is as following:
$$
\widetilde{A}:= \frac{A}{\sqrt{ \hbar }},\quad \tilde{\phi}:= \frac{\phi}{\sqrt{ \hbar }}
$$
where $\widetilde{A},\tilde{\phi}$ are $\hbar$-independent. Similarly, define the following $\hbar$-independent quantities
$$
\widetilde{g}:= \frac{g}{\hbar},\quad  \widetilde{e}:= \frac{e}{\hbar},\quad  \widetilde{m}:= \frac{m}{\hbar}.
$$
Then one can write the Lagrangian in terms of these $\hbar$-independent quantities to check the $\hbar$ dependence explicitly. It turns out that, at least in the simple models discussion in the paper, $\hbar$ always appears in the combination 
$$
\widetilde{g}\sqrt{ \hbar } \quad \text{and}\quad \widetilde{e}\sqrt{ \hbar }
$$
that is, with the coupling. Hence loop correction of $\mathcal{O}(g^{2},e^{2})$ will be of order $\hbar$. 

This derivation is equivalent to the standard one of, for example, Mark Srednicki's textbook, which  associates a factor $\hbar$ to each propagator and $h^{-1}$ with each vertex, and assume the parameters appearing in the action to be independent of $\hbar$. 

Fore more details please refer to Brodsky and Hoyer's paper mentioned above. 
## Back to kinks in 3D

In R. Jackiw's [1976 paper](https://www.sciencedirect.com/science/article/abs/pii/037015737690048X), he made three assumption:
1. The energy (mass) is finite;
2. The energy is locally minimum, meaning the soliton is stable;
3. The potential $U$ depends on a coupling constant $\lambda$ according to the scaling law
$$
U(\phi;\lambda) = \frac{1}{\lambda}U(\sqrt{ \lambda }\,\phi;1).
$$
The choice is such that all the $\lambda$ dependence are now moved to the pre-factor $1 / \lambda$. As for $\hbar$-expansion, we take the scheme such that $\hbar$-expansion agrees with $\lambda$-expansion, namely each loop brings in a factor of $\hbar$. 

Let the Hamiltonian be 
$$
H = \int d^{2}x \, : \mathcal{H} :_ {a},\quad \mathcal{H}(x) = \frac{\pi^{2}}{2} + \frac{(\partial_ {x}\phi(x))^{2}}{2} + \frac{1}{\lambda} V\left(\sqrt{ \lambda}\,  \phi(x) \right).    
$$

