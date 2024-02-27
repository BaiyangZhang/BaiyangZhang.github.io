---
layout: post
title: Kink in Quantum Field Theory, A Broad Outline
subtitle: 
date: 2024-02-25
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---

Since the details of calculation can be found in other notes, here I will only talk about the broad outline. I will use as few as formula as possible. 

We does it mean to *quantize* the kink? It is similar to what we mean by *quantizing the free theory*? Generally speaking, there exist two different but equivalent methods, the canonical quantization and path integral quantization. Regarding the canonical quantization, 

1. given a classical field theory, we first need to identify the equation of motion and its set of solutions, namely eigen functions. 
2. Expand the fields in these eigenfunctions, this is how we diagonalize the Hamiltonian.  
3. Introduce the canonical quantization relation. 

In textbooks we always start from some simple model for scalar fields $\phi$, based on which the above steps are illustrated. The vacuum of the field theory is conveniently chose as $\phi=0$. In a sense, we are expanding the field in the background of $0$, namely the vacuum of the model. Then to quantize the kink simply means we change the background about which we expand the scalar field, from zero to the specific kink solution. 

Using the picture of path integral things are much more obvious. Here, to consider the quantum correction to a kink solution is to include the quantum effects of fluctuation about the classical kink solution. 

The quantization we described above is akin to the familiar second quantization. Further, if one would like to describe the creation and annihilation of kinks themselves by suitable kink creation and annihilation operators, this would be what people call the *third quantization*.

It turns out that quantum corrections always reduces the kink energy. 

- - -

We will adopt perturbative methods to study the quantization of kinks. As we all know, perturbation stops working at strong coupling, $\lambda \gg 1$. What happens to $\mathcal{Z}_ {2}$ and sine-Gordon kinks when the coupling is large? From the classical kink solution we know that the mass of a kink is proportional to $1 / \lambda$, so the kink mass decreases as $\lambda$ increases. Eventually kinks will be even lighter than mesons. At large $\lambda$ we know much more in sine-Gordon model than $\mathcal{Z}_ {2}$ model. In sine-Gordon, we have a dual theory, namely the massive Thirring model. 

# Quantization procedure

The broad outline is as following. 

1. Consider the 2D QFT model with compact spatial dimension of size $L$. Let $\phi$ be the degree of freedom. We could adopt either periodic or anti-periodic boundary condition. Eventually we will take $L \to \infty$, but for now it is large but finite. 
2. Consider small quantum fluctuation $\psi$ about the kink ground $\phi_ {k}$, namely $\psi = \phi - \phi_ {k}$. 
3. Linearize the equation for the fluctuation field $\psi$ (not the original field). Find the solutions, also known as `eigenmodes` or `normal modes`. Expand the fluctuation field $\psi$ in normal modes.
4. `Quantization.` Each normal mode corresponds to a quantum harmonic oscillator, with zero point fluctuations. Sum up the zero point energies of all the normal modes. This is the quantum correction we were looking for, but without appropriate renormalization procedure the sum is divergent. 
5. `Renormalization` must be performed. This is the subtle part. The zero point energy of the trivial vacuum (without kink background) must be subtracted from the zero point energy of the kink, since we want the energy of the trivial vacuum to be zero. Also, the energy must be expressed in terms of renormalized parameters. 

As we turn on the potential slowly, some of the low-lying modes in the trivial box become the bound states of the kink.

Notice that in the trivial vacuum, the solutions to the equation of motion, a.k.a. the scattering states, are plane waves. They are eigenfunctions to both energy and momentum operator; in the presence of a kink, however, the scattering states are now normal modes, which are eigenstates of energy operator but *not eigenstates to momentum operator*.

To consistently compare the energy difference between trivial vacuum sector (just vacuum sector from now on) and kink sector, we need to carefully match discrete modes (thanks to finite box size $L$) in these two.

$\mathcal{Z}_ {2}$ kink has two bound states, sine-Gordon has only one, the translational zero mode. The leading order correction to kink mass are quite close in these two cases. 

# Introduce the particles 

As in the second quantization of a free quantum field theory, particle creation and annihilation operators are introduced for each of the excitation modes of the kink. This is straightforward, except for the zero mode. The final result is a quantum theory with both kinks and particles, which are sometimes referred to as mesons. 

The distinctive aspect of the zero mode in second quantization is associated with its time dependence and the reality of its eigenfunction, in contrast to the complex nature of the remaining eigenfunctions. To be more specific, the time dependence of the eigenfunction is $e^{ i\omega t}$, since zero mode has zero energy, the time dependence is trivial. A real eigenfunction means that in the normal mode expansion, instead of 

$$
a_ {k}  f _ {k} + a_ {k}^{\dagger} f_ {k}^\ast
$$

we have a single term, say

$$
c_ {0} F,\quad  F \text{ is the zero mode eigenfunction}
$$

and $c_ {0}^{\dagger}=c_ {0}$. It is classical since it commutes with everything (that is $c_ {0}$ itself and all the other ladder operators). 

# Sign of the leading order correction

In both $\mathcal{Z}_ {2}$ and sine-Gordon models, the leading order quantum correction reduces the energy of the kink. A argument by Coleman in his private communication show that this observation holds quite true in 1+1 dimension, with boson only. 

