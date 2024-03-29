---
layout: post
title: Perturbative Spontaneous Symmetry Breaking
subtitle: 
date: 2024-03-25
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---


This note is based on Chapter 44 of *Lectures of Sidney Coleman on Quantum Field Theory*. 

# "Spontaneous" symmetry breaking

The word *spontaneous* used to baffle me. It doesn't seem so "spontaneous" in the context of quantum field theory, such as $\phi^{4}$ model. At least not spontaneous enough in comparison with that in the Ising model. In Ising model, starting from high temperature, above Curie temperature to be specific, the ferromagnetic system is in a rotational symmetric phase, all the little spins point to random directions. As the temperature drops, at the Curie temperature the system undergoes a second order phase transition, the system picks a direction and all of a sudden, most of the spins are aligned in that directions,as a result the rotational symmetry is broken, without any external manipulation, hence the word spontaneous. To be more specific, take 2D (spatial) Ising model for example, which is  famously solved by Lars Onsager. We don't choose 1D Ising model because in 1D, spontaneous symmetry breaking doesn't occur due to the lack of a phase transition at finite temperatures, there is a critical dimension under which the free energy is dominated by entropy, so the order phase is not preferred, according to the so-called energy-entropy argument. 

- - -

For a 2D lattice with spins (which can take values +1 or -1, representing up or down magnetic moments) located on each site, the Hamiltonian is given by:

$$
H = -J \sum_ {\langle i, j \rangle} s_ i s_ j - h \sum_ i s_ i 
$$

where $J$ is the exchange interaction energy between neighboring spins. It determines the strength of the interaction and can be positive (favoring alignment) or negative (favoring anti-alignment). The sum $\sum_ {\langle i, j \rangle}$ runs over all nearest-neighbor pairs of lattice sites, ensuring that each pair is counted once. $s_ i$ and $s_ j$ are the spin values at sites $i$ and $j$, respectively. $h$ is the external magnetic field, but for the spontaneous phase transition discussion, we consider $h = 0$.

The free energy (Helmholtz free energy, to be specific) $F$ of the system combines the *internal energy* and the *entropy*. Classically speaking, the free energy describes the work that can be extracted from a system at a constant temperature, but here the physical meaning is that the equilibrium state is such that minimizes the free energy. The free energy in the context of the Ising model can be expressed as:

$$ F = -k_ B T \ln(Z) $$

where $k_ B$ is the Boltzmann constant, $T$ is the temperature, and $Z$ is the partition function of the system, given by the sum over all possible configurations:

$$ Z = \sum_ {\left\lbrace s \right\rbrace } e^{-\beta H(\left\lbrace s \right\rbrace )} $$

where $\beta = \frac{1}{k_ B T}$ and $H(\left\lbrace s \right\rbrace )$ is the Hamiltonian for a particular configuration $\left\lbrace s \right\rbrace$ of spins.

The true ground state must minimize the free energy, the free energy is energy minus temperature times entropy, hence the competition between energy and entropy underlies the phase transition:

- At low temperatures, the system tends to minimize its energy, leading to an ordered phase where spins align (ferromagnetism).
- At high temperatures, the entropy dominates, favoring a disordered state where spins are randomly oriented.

The balance between these two tendencies determines the critical temperature $T_ c$ at which the phase transition occurs.

The critical dimension $d_ c$ of a system is the minimum dimension in which a phase transition can occur at a nonzero temperature. For the Ising model, it is known that $d_ c = 1$ for a lower critical dimension, meaning that there is no phase transition at any nonzero temperature in 1D. In 2D, however, the model does exhibit a phase transition, as shown by Onsager's solution.

Onsager's exact solution for the 2D Ising model on a square lattice without an external field showed that the critical temperature $T_ c$ is given by:

$$ \sinh\left(\frac{2J}{k_ B T_ c}\right) = 1 $$

This solution demonstrated that a spontaneous magnetization (order) emerges below $T_ c$ and disappears above $T_ c$, marking a second-order phase transition characterized by a continuous change in the order parameter (magnetization).

The calculation of the critical properties, such as the critical exponents that describe how physical quantities diverge near $T_ c$, is more intricate and relies on sophisticated mathematical techniques, including renormalization group analyses, which go beyond the scope of this note.

- - -

In the contest of quantum field theory, spontaneous symmetry breaking occurs when the most stable state (or states) of a system, namely its ground state or vacuum state, does not share the symmetry of the system's Lagrangian (or Hamiltonian). This can happen even though the governing equations or Lagrangian of the system remain symmetric. The system "chooses" a state that breaks some of the symmetry of the Lagrangian.

The Higgs mechanism is a well-known example of spontaneous symmetry breaking in QFT. The potential of the Higgs field is symmetric, resembling a "Mexican hat" or "sombrero," but the lowest energy state (the ground state) is not at the symmetric center (where the field value is zero) but rather at some nonzero value along the "brim" of the hat. This asymmetric ground state breaks the symmetry of the potential.

The "spontaneous" aspect is that there's no external force or parameter explicitly breaking the symmetry; it's the intrinsic dynamics of the field settling into a minimum energy state that breaks the symmetry. Spontaneous in the context of QFT is not in the dynamical sense, as it is in Ising model.

# Degenerate Vacua

In a simple quantum system, you might expect a unique ground state. However, in systems where spontaneous symmetry breaking occurs, there can be multiple degenerate ground states, all having the same energy but different physical configurations.

All the vacua together form the manifold of vacuum of the Lagrangian, where the basis are just different vacua states, continuous or not. The thing is, there is more than one set of basis for the vacuum states. Let $\left\lvert{0,\alpha}\right\rangle$ be degenerate vacuum states label by some $\alpha$, then any linear combination, properly normalized, is another vacuum state, call it $\left\lvert{0,\beta}\right\rangle$, then we can use the *Gram-Schmidt procedure* to construct another set of orthonormal basis. Among the infinite sets of basis, there do exists good sets and bad ones. But before defining what is a good vacuum, we must first define what is a quasi-local operator.

Recall that operators correspond to observable quantities or actions that can be performed on the field, and "quasilocal" operators are those whose effects are confined to a limited region of space. Take the scalar field theory for example, let $\phi(x)$ be field operator, they are local since it is defined on a point. A *quasilocal operator* $A$ is something can be constructed from $\phi$ via

$$
A = \int d^{d}x \,   f(x_ {1},\cdots,x_ {n}) \phi(x_ {1})\cdots\phi(x_ {n})
$$
where $f(x_ {1},\cdots,x_ {n})$ is a function with finite support (support is the closure of the points where $f$ is nonzero).


Now coming back to vacua. There is a basis where all the vacua are *globally independent*, where one vacua can not be transformed into another using some local (or quasi-local, as Coleman called it) operator. Such a basis is called **good** vacuum states. For a set of good vacua, different vacuum states are not just distinct but are fundamentally separate in the sense that you cannot use a simple, localized operation to move from one to another. By construction, the vev of any quasilocal operators between two distinct good vacua is zero, 

**Theroem 1** There exists a basis for the vacuum states $\left\lvert{0,\alpha}\right\rangle$, so called good vacuum states, such that for any quasilocal operator $A$, we have 

$$
\left\langle{0,\alpha}\right\rvert A\left\lvert{0,\alpha'}\right\rangle =0.
$$

We'll neglect the proof of the theorem here, just mention that it involves translational invariance of vacuum states, causality, and some cluster decomposition-ish argument.

The significance of the theorem is this: it doesn’t matter if you say there’s one vacuum or many; there are always good vacua. It shows that, even if we don’t know anything about spontaneous symmetry breaking, and we’ve chosen a bad set of vacua, by a systematic constructive procedure we can always find a good choice of bases for the vacuum subspace, such that no local operator can connect one vacuum to another.

- - -

In the 





