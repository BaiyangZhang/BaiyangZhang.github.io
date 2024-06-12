---
layout: post
title: Constructing A Finite Tension Domain Wall in 4D phi-Fourth Model
subtitle: 
date: 2024-06-12
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - "#domainWall"
  - kink
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

we are not interested in the interaction picture but in the Schrodinger picture. It is for a bunch of reasons, one of them is that it is easy to see what the normal-ordering prescription corresponds to in this picture. Schrodinger-picture operators are given as functions of the field $\phi(\vec{x})$ and the canonical momentum density $\pi(\vec{x})$, where $\vec{x}$ is the spatial coordinate, not the Lorentzian spacetime coordinate $x^{\mu}$. We begin with a phi-fourth theory in Schrodinger picture, normal ordered at mass scale $m_ {0}$:

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
\omega_ {p}&= \sqrt{ m^{2}+\vec{p}^{2} },\\
A_ {p}^{\ddagger} &= \frac{A_ {p}^{\dagger}}{2\omega_ {p}}.
\end{align*}
$$

with commutation relation 

$$
[A_ {p_ {1} },A^{\ddagger}_ {p_ {2} }] = (2\pi)^{d}\delta^{d}(p_ {1}-p_ {2}).
$$

In the decomposition, every thing is defined at mass scale $m$. In the paper the creation and annihilation operators are sometime written as $A_ {\vec{p}}^{(0)}$, with an extra naught, it has to do with the definition of normal ordering we choose. If we are normal ordering at some bare mass $m_ {0}$, then we put the superscript $(0)$ to remind us of that. We will go to details later.

- - -

It would be helpful to mention the connection between our convention and that widely adopted in various textbooks. In Schrodinger picture it reads

$$
\phi(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \, \frac{1}{\sqrt{2 \omega_ {p} }} (a_ {p} \, e^{ i\vec{p}\cdot \vec{x} } + a^{\dagger}_ {p}\,e^{ -i\vec{p}\cdot \vec{x} }).
$$

The canonical commutation relation reads

$$
[a_ {p},a^{\dagger}_ {k}] = (2\pi)^{d}\delta^{d}(\vec{p}-\vec{k}).
$$

Comparing to our convention, we have 

$$
\boxed{ 
\begin{align*}
A_ {p} &\equiv \sqrt{ 2\omega_ {p} }\,a_ {p},\quad  A^{\dagger}_ {p} \equiv \sqrt{ 2\omega_ {p} }\,a^{\dagger}_ {p}, \\
A^{\ddagger}_ {p} &:= \frac{A^{\dagger}_ {p}}{2\omega_ {p}} = \frac{a^{\dagger}_ {p}}{\sqrt{ 2\omega_ {p} }}, \\
[A_ {p},A^{\ddagger}_ {k}] &= (2\pi)^{d}\,\delta^{d}(\vec{p}-\vec{k}).
\end{align*}
}
$$

- - -

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

# Normal ordering with mass m

This section is based on Sidney Coleman's [1975 paper](http://users.physik.fu-berlin.de/%7Ekamecke/ps/coleman.pdf) and his lecture note on the aspects of symmetry, the chapter about classical and quantum lumps. In the meanwhile I have adopted notations and convention according to previous chapter. 

In Coleman's 1975 paper mentioned above, he studied the sine-Gordon model

$$
\mathcal{L} = \frac{1}{2} (\partial_ {\mu}\phi)^{2} + \frac{\alpha_ {0}}{\beta^{2}}\cos \beta \phi+\gamma_ {0}, 
$$

where things with a nought are bare (not renormalized), and famously pointed out:

1. As for any theory of a **scalar field** with **nonderivative interaction** in **2 dimensional spacetime**, normal ordering the Hamiltonian alone is enough to cancel all the divergences at any loop order;
2. If the $\beta$-parameter exceeds $8\pi$, the Hamiltonian density is not bounded below. 
3. If $\beta<8\pi$, the model is equivalent to the charge-zero sector of almost-massive Thirring model. 
4. The fermion in the Thirring model is massless if $\beta=4\pi$. 

Turns out there are more details to normal ordering than I thought. In textbooks such that by Peskin&Schroeder, or that by Mark Srednicki, normal ordering is regarded as a simple, even trivial, ad hoc procedure that puts all the creation operators to the left of all the annihilation operators, in order to eliminate the zero point energy of the trivial vacuum. But, as we dig deeper, more details begin to surface. 

- - -

A crucial property of normal ordering is that expectation values of normal-ordered operators vanish in the free theory: 

$$
\left\langle{0}\right\rvert : \mathcal{O} :\left\lvert{0}\right\rangle =0
$$

for any operator $\mathcal{O}$ and free vacuum $\left\lvert{0}\right\rangle$. There are various formulations of this notion [^Polchinski] , such as `creation-annihilation operator normal ordering`, `conformal normal ordering`, `functional integral normal ordering`, etc. In this note we will only talk about familiar creation-annihilation operator normal ordering.

Something that is less mentioned is that, normal ordering involves a mass scale $m$. In most cases, it is rather obvious what $m$ we should choose, that is the mass of the free particle, let's call it free mass. However, in order to tell what the free mass is, we need to what the Hamiltonian is, for example if we can unambiguously separate the Hamiltonian into $\mathcal{H}_ {0}+U(\phi)$, where $\mathcal{H}_ {0}=\pi^{2} / 2+(\partial_ {x}\phi)^{2} /2+m^{2}\phi^{2} /2$, then $m$ is the free mass. Sometimes the situation is not so straightforward, for sometimes it is more convenient to put $m^{2}\phi^{2} /2$ into the interaction part, such as in the case of sine-Gordon model, as a result the free Hamiltonian only contains the kinetic part, and the free particles appears to be massless. In general, given a quadratic term of form $a \phi^{2}$ where $a$ is some real parameter, we can choose how much of it is to be put into the free Hamiltonian part, and the rest goes to the interaction. For example, we can pick a number such as $m=0.511$ MeV and say that $m^{2}\phi^{2}/2$ goes to the free Hamiltonian, such that the free particle has mass $m$, as a result, $(a-\frac{m^{2}}{2})\phi^{2}$ will go to the interaction. This is just a matter of convenience, the observables should not depend on such arbitrary choices.

So, how does all this relate to normal ordering? Normal ordering is a procedure that rearranges creation and annihilation operators. These operators inherently depend on the free mass of the particle. $a^{\dagger}_ {p}$ creates a particle of momentum $\vec{p}$ **with mass $m$**, the energy of the particle is $\sqrt{ \vec{p}^{2}+m^{2} }$. I repeat, **the choice of $m$ depends on what you choose to call the free Hamiltonian, and that choice is somehow arbitrary.** The result of changing $m$ can be absorbed in a redefinition of the theory parameters.

My conjecture is, the field operator $\phi(x)$ itself is independent of the aforementioned choice of mass parameter $m$, while the stuff that do depend on $m$ are

1. creation and annihilation operators $a_ {p,m}$ and $a^{\dagger}_ {p,m}$,
2. the energy $\omega=\sqrt{ \vec{p}^{2}+m^{2} }$, written as $\omega_ {p,m}$ for short and
3. states in Fock space. For example, the free vacuum $\left\lvert{0,m}\right\rangle$ is by definition annihilated by $a_ {p,m}$. Since the states in the Fock space are constructed by applying $a^{\dagger}_ {p,m}$ consecutively, a re-definition of $a^{\dagger}_ {p,m}$ to, say $a^{\dagger}_ {p,\mu}$ will also change the states themselves.

Recall that the field operator can be expanded in terms of these two things, to be specific

$$
\phi(\vec{x}) = \int \frac{d^{d}k}{(2\pi)^{d}}\,  \frac{1}{\sqrt{ 2\omega_ {k,m} }} (a_ {p,m} \, e^{ i\vec{k}\cdot \vec{x} } + a^{\dagger}_ {p,m}\,e^{ -i\vec{k}\cdot \vec{x} })
$$
and the $m$-dependence in $\omega_ {p,m}$, $a_ {p,m}$ and $a^{\dagger}_ {p,m}$ should cancel out so that $\phi(\vec{x})$ itself is $m$-independent.

- - -

We can define the **normal ordering at $m$** by decomposing the Schrodinger picture fields and momenta into creation and annihilation part:

$$
\begin{align*}
\phi^{+}(\vec{x})  &= \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ -i\vec{p}\cdot \vec{x} }  \frac{A^{\dagger}_ {p}}{2\sqrt{ \vec{p}^{2}+m^{2} }},    \\
\phi^{-}(\vec{x}) &=  \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ -i\vec{p}\cdot \vec{x} }  \frac{A_ {-p}}{2\sqrt{ \vec{p}^{2}+m^{2} }}, 
\end{align*}
$$

similarly for the canonical momenta

$$
\pi^{\pm }(\vec{x})  = \pm   i\sqrt{ -\nabla^{2}+m^{2} }\phi^{\pm }(\vec{x}) .
$$

It is easy to verify that 

$$
\begin{align*}
\phi(\vec{x}) &=  \phi^{+}(\vec{x})  + \phi^{-}(\vec{x}) , \\
\pi(\vec{x}) &=  \pi^{+}(\vec{x})  + \pi^{-}(\vec{x}) , 
\end{align*}

$$

We can arrange a sting of field operators using the Wick's theorem, which states that any product of field operators can be rewritten as the sum of all possible ways of contracting pairs of operators, plus the normal ordered product of the operators. For example, 

$$
\phi(\vec{x})\phi(\vec{x}) = :\phi(\vec{x})\phi(\vec{x}): + \text{ contraction}(\phi(\vec{x})\phi(\vec{x})) .
$$

The contraction is where different choice of $m$ generates different results. Let's write the contraction at $m$ as $C_ {m}\left\lbrace \cdots \right\rbrace$, we have 

$$
\begin{align*}
\phi^{2}(\vec{x}) &= :\phi^{2}(\vec{x}):_ {m} + 
\end{align*}
$$




For a free theory of mass $m$, and for any source function $J(x)$, we have 

$$
\begin{align*}
\exp \left\lbrace i \int \, J(x)\phi(x) d^{2}x  \right\rbrace  &=\; :\exp \left\lbrace i \int d^{2}x   \, J(x)\phi(x)  \right\rbrace:_ {m} \\
&\;\;\;\;\;\times \exp \left\lbrace -\frac{1}{2}\int d^{2}x  d^{2}y J(x) \, \Delta(x-y)J(y)  \right\rbrace 
\end{align*}
$$

where $\Delta(x-y)$ is the Wightman function. If we go to interaction picture and adopt time ordering, the Wightman functions become Feynman propagators.





[^Polchinski]: J. Polchinski, String Theory. Vol. 1: An Introduction to the Bosonic String. Cambridge Univ. Pr., UK, 1998.

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



