---
layout: post
title: Constructing A Finite Tension Domain Wall in 4D phi-Fourth Model
subtitle: 
date: 2024-05-23
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - "#domainWall"
---


# Coherent state and solitonic state

In quantum field theory (QFT), a **coherent state** is a specific type of quantum state that exhibits classical-like behavior. These states are widely used to describe states that most closely resemble classical waves.

In quantum mechanics, coherent states are eigenstates of the annihilation operator $\hat{a}$. For a harmonic oscillator, a coherent state $\left\lvert{\alpha}\right\rangle$ satisfies:
   $$
   \hat{a} \left\lvert{\alpha}\right\rangle  = \alpha \left\lvert{\alpha}\right\rangle 
   $$

where $\alpha$ is a complex number. Coherent states minimize the Heisenberg uncertainty principle, making them the quantum states most similar to classical oscillations. They exhibit minimal quantum fluctuations, contrary to pathologically defined states such as the eigen state of $\hat{x}$, which maximizes the fluctuation in the momentum space. Also, coherent states form an over-complete basis for the Hilbert space. The number of particles (e.g., photons) in a coherent state follows a Poisson distribution.

In quantum field theory (QFT), coherent states are often defined with respect to `smeared annihilation operators`. This approach takes into account the fact that field operators are distributions that need to be smeared with test functions to make physical sense. To be more specific, the field operators $\hat{\phi}(x)$ and their conjugate momenta $\hat{\pi}(x)$ are functions of spacetime coordinates and are typically distributions. To handle these distributions properly, one introduces smeared field operators:

$$
\hat{\phi}(f) = \int d^dx \, f(x) \hat{\phi}(x)
$$

where $f(x)$ is a smooth test function that **smears** the field operator over spacetime. Similarly, the annihilation operator can be smeared with a test function $g(x)$:

$$
\hat{a}(g) = \int d^4x \, g(x) \hat{a}(x)
$$

Here, $\hat{a}(x)$ is the local annihilation operator at point $x$, and $\hat{a}(g)$ is the smeared annihilation operator. The eigen equation reads

$$
\hat{a}(g) \left\lvert{\alpha}\right\rangle  = \alpha(g) \left\lvert{\alpha}\right\rangle 
$$

where $\alpha(g)$ is a complex function representing the eigenvalue associated with the test function $g(x)$. This definition ensures that coherent states retain their classical-like properties while respecting the distributional nature of field operators in QFT.

Consider a free scalar field $\hat{\phi}(x)$ in 4D. The field can be expanded in terms of creation and annihilation operators:

$$
\hat{\phi}(x) = \int \frac{d^3k}{(2\pi)^{3/2}} \frac{1}{\sqrt{2\omega_ k}} \left( \hat{a}_ k e^{-ik \cdot x} + \hat{a}_ k^\dagger e^{ik \cdot x} \right)
$$

where $\hat{a}_ k$ and $\hat{a}_ k^\dagger$ are the annihilation and creation operators for mode $k$.

A coherent state $\left\lvert{\alpha}\right\rangle$ for this field is an eigenstate of the smeared annihilation operator:

$$
\hat{a}(g) \left\lvert{\alpha}\right\rangle  = \alpha(g) \left\lvert{\alpha}\right\rangle 
$$

where the smeared annihilation operator is given by:

$$
\hat{a}(g) = \int \frac{d^3k}{(2\pi)^{3/2}} \frac{1}{\sqrt{2\omega_ k}} \tilde{g}(k) \hat{a}_ k
$$

and $\tilde{g}(k)$ is the Fourier transform of the test function $g(x)$.

In some theories, especially those involving non-linear sigma models and certain gauge theories, solitons can be seen as coherent states of the underlying field theory. This correspondence helps in understanding the non-perturbative aspects of the field theory.


