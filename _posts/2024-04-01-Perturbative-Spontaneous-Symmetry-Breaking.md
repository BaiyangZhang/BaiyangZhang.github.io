---
layout: post
title: Perturbative Spontaneous Symmetry Breaking
subtitle: 
date: 2024-04-01
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

In the following we will need to make use of quantum effective action $\Gamma[\varphi]$, for details on this topic see my other note [here](https://www.mathlimbo.net/blog/2024/Coleman-Weinberg-Potential/). 

As explained by Coleman, 

>...(using perturbation theory), but with the effective action $\Gamma[\overline{\phi}]$ substituted for the classical action $S[\phi]$. Instead of trying to find minima by finding the stationary points of the classical action, I **find ground states by looking at the stationary points of the effective action**; instead of finding effective coupling constants and masses by expanding about the minima of the classical action, I **find 1PI Green’s functions by expanding about the minima of the effective action**. It’s exactly the same game in the quantum and classical theories.

Sometimes Coleman talks about classical vev of $\phi$ and quantum vev of $\phi$. By his definition, the classical vev of $\phi$, i.e. $\left\langle \phi \right\rangle$ classical, usually denoted as just $\left\langle \phi \right\rangle$, is the vev of $\phi$ without loop corrections, the quantum one, usually denoted as $\overline{\phi}$, is that with loop corrections. In any cases, $\left\langle \phi \right\rangle$ is supposedly a constant in spacetime. This means that both classical and quantum vacuum preserves the translational symmetry.

In solitonic quantum field theory we constantly deal with ground states that are not translations symmetric. Regarding the possibility of SSB of spontaneous translational symmetry breaking, Coleman comment

>There’s no reason why translation invariance should not be spontaneously broken in a theory that describes the real world. It occurs in statistical mechanics, for example, where the phenomenon is called `crystallization`. There, *instead of changing the square of the mass to cause the manifest symmetry to break spontaneously, one changes the temperature*. Let’s take a typical material such as iron, and imagine an iron universe, spatially infinite. If the temperature is above a certain point, the ground state (in the sense of statistical mechanics) is spatially homogeneous; it’s iron vapor. We lower the temperature below the freezing point of iron, and the ground state becomes an infinite iron crystal, which does not have spatial homogeneity. If we now consider the rotation of a crystal somewhere in the frozen iron, how it rotates depends on its position relative to a central lattice point. That’s an example of spontaneous symmetry breakdown of translational invariance.

Note that **spontaneous symmetry breaking does not affect the renormalization**, SSB is essentially a shift of field, has nothing to do with regularization and renormalization. A SSB model has exactly the same counter terms as the original one. Thus we could renormalize first and shift the field later. This is useful in $\phi^{4}$ model with spontaneous symmetry breaking, since the original theory has no $\phi^{3}$ terms but the symmetry broken theory has, so naturally one could ask, do we need a counter term for $\phi^{3}$ interaction, like Mark Srednicki did in his textbook? The answer is no since such a counter term is not needed in the original theory. Then what about the divergence introduced by $\phi^{3}$ theory? Well, if we had done everything correctly, it should be taken care of by itself, by some destined cancellation. Like Coleman said,

>After we do the shift, of course, a $\phi^{3}$ interaction will appear in the effective action, but we still don’t need a $\phi^{3}$ counterterm, because we’ve already gotten rid of all infinities in computing $\Gamma$ before we’ve made the shift. The shift is a purely algebraic operation without a single integration over internal momenta, and therefore cannot possibly introduce new ultraviolet infinities.

Say we are doing renormalization in the original theory. What are the renormalization conditions? We have MS, $\overline{\text{MS}}$, Pauli-Villas, mass-shell, lattice, Momentum Subtraction, etc. It is not a good idea to adopt the mass shell renormalization since in the original theory $m^{2}<0$. Then we could choose a tentative renormalization condition, then adjust it in the kink sector so that the renormalized parameters are physical. The vev of field $\overline{\phi}$ will depend on the renormalization condition, but different condition will describe the same physics.

Recall that the effective action $\Gamma[\overline{\phi}]$ is made of 1PI diagrams, where $\overline{\phi}(x)$ itself serves as the external legs, just like the source term $J(x)$ with classical action $S$. We have assumed the $\overline{\phi}$ is a const in spacetime, which translates to zero momentum after we Fourier transform it to the momentum space. So we only need to consider the case where the external legs has zero momenta. Next let's dive into calculation.

- - -

Let $V(\overline{\phi})$ be the `effective action` of $\overline{\phi}$, which if you recall is the quantum vev of $\phi$. For the details of effective action see my other note mentioned at the beginning of this note, here we only present the definition,

$$
\Gamma[\overline{\phi}] =: -V(\overline{\phi}) \cdot \text{Vol}^{d},
$$

where $\text{Vol}^{d}$ is the total space of the $d$-dimensional spacetime manifold. 

The connection between $\Gamma[\overline{\phi}]$ and $S[\overline{\phi}]$ is that, at tree level, that is if you forget about quantum corrections, $\Gamma$ is equal go $S$. When the quantum corrections are included, since $\Gamma$ is exact (incorporates all the quantum effects in path integral) at tree level, we have 

$$
 Z[J] = \lim_ { \hbar \to 0 } \int \mathcal{D}\phi \,  \exp \left\lbrace \frac{i}{\hbar}\left( \Gamma[\phi]+\int  J\phi  \right) \right\rbrace  = \exp \left\lbrace i\Gamma[\overline{\phi}]+\int dJ\overline{\phi} \,   \right\rbrace ,
$$

it is understood that the last equality is up to multiplicative constants. Also note that in the last expression it is not just any $\phi$, but $\overline{\phi}$ that satisfies certain functional equation, which is exactly the $\overline{\phi}$ we have been using.

However we also have

$$
Z[J] = \int \mathcal{D}\phi \, \exp \left\lbrace \frac{i}{\hbar}\left( S[\phi] +\int J\phi  \right) \right\rbrace   = \exp \left\lbrace iS[\left\langle \phi \right\rangle ] + \text{loops} \right\rbrace 
$$

where loops are a result of the fluctuations about the classical field configuration $\left\langle \phi \right\rangle$. Thus we have 

$$
\Gamma[\overline{\phi}] = S[\left\langle \phi \right\rangle] + \text{loops}= S[\overline{\phi}] + \text{loops},
$$

since a swap between $\overline{\phi}$ and $\left\langle \phi \right\rangle$ introduces loop corrections only. But so far let's stick with $S[\left\langle \phi \right\rangle]$ instead of $S[\overline{\phi}]$, since $\left\langle \phi \right\rangle$ is the quantum vev thus unknown, while $\left\langle \phi \right\rangle$ is the classical vev thus easily known, one just need to solve for the equation of motion. 

Write the action in terms of the Lagrangian we have 

$$
\Gamma[\overline{\phi}] = \int d^{d}x \, \mathcal{L}(\left\langle \phi \right\rangle ) + \text{loops}.
$$

We have

$$
\mathcal{L} = \frac{1}{2} (\partial \phi)^{2}  - U(\phi) + \mathcal{L}_ {\text{ct}},
$$

where $U$ is the classical potential and $\mathcal{L}_ {\text{ct}}$ are the counter terms. Then, since $\overline{\phi}$ is constant we have 

$$
V(\overline{\phi}) = U(\left\langle \phi \right\rangle ) + \text{loops},
$$

where loop contribution is of form $\hbar(\text{1-loops})+h^{2}(\text{2-loops})+\cdots$. Note that $V(\overline{\phi})$ is not a functional but rather a function of $\overline{\phi}$, it is the negative of the constant density of $\Gamma[\overline{\phi}]$. Since $\Gamma$ generates all the 1PI diagrams, $V(\overline{\phi})$ represents the collection of all the 1PI diagrams with all the external momenta equal to zero and with the $(2\pi)^{d}\delta^{d}(0)$ from overall energy-momentum conservation divided out. That's just the Fourier space equivalent of the integral $\int d^dx$. 

As Coleman explained in his lecture notes,

>The rule for computing $V[\overline{\phi}]$ is very simple. You don’t have to worry about any external momentum. You just have external lines each carrying zero momentum. Sum up all those graphs to one loop or two loops or however many loops you’re going to do.

## Calculating the Effective Potential

With a general renormalizable potential, we start with the Lagrangian that reads

$$
\mathcal{L} = \frac{1}{2} (\partial \phi)^{2} -U(\phi)+\mathcal{L}_ {\text{ct}}.
$$

If there is a mass term it goes to $U$. As a result, the propagator is 

$$
\frac{i}{k^{2}+i\epsilon}.
$$

Recall that calculating $\Gamma[\overline{\phi}]$ means calculating the 1PI diagrams with external legs amputated and replaced by a factor of $\overline{\phi}$. Why are they amputated? We know that when calculating the S-matrix the external legs are also truncated due to the LSZ theorem, but here there is no LSZ theorem so why does it happen? The reason is mostly that 1PI diagrams are used to represent the interaction vertices or the "effective vertices" in the theory, rather than full scattering processes. In the context of effective theory you usually don't hear things like asymptotic states, scattering matrix, things that you must discuss when talking about S-matrix. The 1PI diagrams contribute to the n-point functions, which are essentially the building blocks of the full scattering amplitudes. These vertex functions describe how particles interact at a point, disregarding the propagation of particles to and from this point. In the renormalization process, 1PI diagrams are essential because they contain the divergences that need to be renormalized. The external propagators do not need to be renormalized in the same way, so they are not included in the 1PI diagrams. The renormalization of the theory focuses on the interactions themselves, which are represented by the 1PI diagrams without the external propagators. For details please refer to note here