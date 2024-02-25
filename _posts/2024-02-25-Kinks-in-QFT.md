---
layout: post
title: Kink in Quantum Field Theory, a Broad Outline
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

