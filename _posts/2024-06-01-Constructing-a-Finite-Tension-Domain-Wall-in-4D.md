---
layout: post
title: Constructing A Finite Tension Domain Wall in 4D phi-Fourth Model
subtitle: 
date: 2024-06-01
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

# Conventions

We begin with a phi-fourth theory in Schrodinger picture, normal ordered at mass scale $m_ {0}$:

$$
\begin{align*}
H &= \int d^{3}x: \hat{\mathcal{H}}^{0}(\vec{x}) :_ {m_ {0}} \\
\hat{\mathcal{H}}^{0}(\vec{x}) &= \frac{1}{2}(\pi(\vec{x})^{2}+(\partial_ {i}\phi(\vec{x})\partial_ {i}\phi(\vec{x}))) + \frac{1}{4}(\lambda_ {0}\phi^{4}(\vec{x})-m_ {0}^{2}\phi^{2}(\vec{x}))+A.
\end{align*}
$$

Note the factor $-m_ {0}^{2} /4$ in the mass term, and the last $A$ is a c-number to cancel the zero point energy in the vacuum sector. We also define coupling $g_ {0}$ as 

$$
g_ {0}^{2} := \lambda_ {0}^{2}.
$$

In the Schrodinger picture, the field operator and canonical momentum operator can be decomposed as 

$$
\begin{align*}
\phi(\vec{x})&= \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ -i\vec{p}\cdot \vec{x} } \left( A_ {p}^{\ddagger}+\frac{A_ {-p}}{2\omega_ {p}} \right),  \\
\pi(\vec{x})&= i \int \frac{d^{3}p}{(2\pi)^{3}} \,  e^{ -i\vec{p}\cdot \vec{x} } \left( \omega_ {p} A_ {p}^{\ddagger}-\frac{A_ {-p}}{2} \right) .
\end{align*}
$$

and 

$$
\begin{align*}
\omega_ {p}&= \sqrt{ m_ {0}^{2}+\vec{p}^{2} },\\
A_ {p}^{\ddagger} &= \frac{A_ {p}^{\dagger}}{2\omega_ {p}}.
\end{align*}
$$

In the decomposition, every thing is defined at mass scale $m_ {0}$. In the paper the creation and annihilation operators are written as $A_ {\vec{p}}^{(0)}$, I have simplified the notation a little.

The renormalized quantities are define as 

$$
m^{2}=m_ {0}^{2} + \delta m^{2}, \quad  \sqrt{ \lambda } = \sqrt{ \lambda_ {0} } + \delta \sqrt{ \lambda }. 
$$

or equivalently 

$$
g = g_ {0} + \delta g.
$$

We also define $v$ to be the vev of field in some physical vacuum,

$$
v = \frac{m}{\sqrt{ 2\lambda }} + \delta v.
$$

Perturbative expansion:

$$
\begin{align*}
\delta m^{2}&\sim \mathcal{O}(\lambda)\sim \mathcal{O}(g^{2}),   \\
\delta g &\sim \mathcal{O}(g^{3}),\\
H &= \sum_ {i=01}^{\infty} H_ {i},\quad  H_ {i} \sim \mathcal{O}(g^{i-2}) , \\
A &= \sum_ {i=0}^{\infty}A_ {i}, \quad  A_ {i} \sim \mathcal{O}(g^{i-2}) , \\
\delta v &= \sum_ {i=1}^{\infty} \delta v_ {i} ,\quad  v_ {i} \sim \mathcal{O}(g^{i}) \\
\left\lvert{\Psi}\right\rangle  &= \sum_ {i}^{\infty} \left\lvert{\Psi_ {i}}\right\rangle , \quad  \left\lvert{\Psi}\right\rangle _ {i} \sim \mathcal{O}(g^{i})
\end{align*}
$$








- - -

# Triviality of phi-fourth theory

Renormalization is the process by which the parameters of a quantum field theory (like the mass and coupling constant) are adjusted to account for the effects of interactions at different energy scales. This involves introducing a cutoff $\Lambda$ to regulate divergences and then taking the limit $\Lambda \to \infty$.

Triviality in this context means that, as you take the ultraviolet (UV) cutoff $\Lambda \to \infty$, the renormalized coupling constant $\lambda$ tends to zero, making the interacting theory effectively a free (non-interacting) theory. This happens despite having a non-zero bare coupling constant $\lambda_ 0$.

When performing calculations in QFT, the bare field $\phi_ 0$ and the renormalized field $\phi$ are related by a wave function renormalization factor $Z$:

$$ 
\phi_ 0 = Z^{1/2} \phi. 
$$

As $\Lambda \to \infty$, this factor $Z$ becomes large, effectively rescaling the field. Similarly, the bare coupling constant $\lambda_ 0$ and the renormalized coupling constant $\lambda$ are related by:

$$ 
\lambda_ 0 = \frac{\lambda}{Z^2}. 
$$

As $\Lambda \to \infty$, if $Z \to \infty$ (which is the case for $\phi^4$ theory in 4D), the renormalized coupling $\lambda$ must go to zero to keep $\lambda_ 0$ fixed.

In summary, saying that $\phi^4$ theory is "trivial" means that, after accounting for the effects of renormalization, the theory becomes non-interacting as the UV cutoff is taken to infinity. This implies that any interacting $\phi^4$ theory in four dimensions cannot remain interacting at all energy scales and instead becomes a free theory at very high energies. This phenomenon is an important aspect of understanding the limitations and behaviors of quantum field theories in different dimensions.