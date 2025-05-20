---
layout: post
title: Note on Domain Wall Tension from Spectral method
date: 2025-05-13
author: Baiyang Zhang
catalog: true
tags:
---

The spectral method makes direct contact between perturbative and non-perturbative treatments of quantum field theory. Although studying field configurations corresponding to strong potentials that cannot be treated perturbatively, one is able to implement standard perturbative renormalization conditions.

In the monograph *LNP777*, the authors claim:

>The spectral techniques we present provide a complete, self-contained approach to the calculation of one-loop quantum corrections, which reveals the fundamental connections between quantum field theory and ordinary quantum mechanics.

As demonstrated by Rebhan and Nieuwenhuizen NPB 508(1997) 449.10, integrating the unregulated integral by parts introduces such finite ambiguities, corresponding physically to the difference between holding the number of modes fixed and holding the energy cutoff fixed when subtracting the divergent sums. Such ambiguities are intolerable in a treatment that is to make predictive statements about physical systems, such as the stability of solitons or the energy density in the vacuum

# The model

The Lagrangian:

$$
\mathcal{L} = \frac{1}{2} (\partial \phi)^{2} -U(\phi),
$$

where the potential for sine-Gordon and phi-4 are respectively

$$
U_ {\text{sG}} := \frac{\mu^{4}}{\lambda}\left[ 1-\cos\left( \frac{\sqrt{\lambda}\phi}{\mu} \right) \right],\quad  U_ {\text{kink}}:= \frac{\lambda}{8}\left[ \phi^{2}-\frac{\mu^{2}}{\lambda} \right]^{2}.
$$

The field decomposition:

$$
\phi = \phi_ {cl}(\vec{x}) + \eta_ {k}(\vec{x})e^{ -i \omega t }.
$$

define $g:=\sqrt{\lambda}$. 
