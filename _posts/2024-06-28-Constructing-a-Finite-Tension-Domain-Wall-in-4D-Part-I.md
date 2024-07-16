---
layout: post
title: Quantum Domain Wall in 4D Part I
subtitle: 
date: 2024-06-28
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - "#domainWall"
  - kink
---

# Table of Contents

- [1. Coherent state and solitonic state](#1-coherent-state-and-solitonic-state)
- [2. Conventions](#2-conventions)
- [3. Normal ordering with mass m](#3-normal-ordering-with-mass-m)
- [4. Triviality of phi-fourth theory](#4-triviality-of-phi-fourth-theory)
- [5. Perturbative Expansion of the Hamiltonian](#5-perturbative-expansion-of-the-hamiltonian)
- [6. Passive Transformation by $D_ {f}$](#6-passive-transformation-by-d_-f)

# 1. Coherent state and solitonic state

In quantum field theory (QFT), a **coherent state** is a specific type of quantum state that exhibits classical-like behavior. These states are widely used to describe states that most closely resemble classical waves. To understand it, it's best to start with quantum mechanics.

In quantum mechanics, coherent states are eigenstates of the annihilation operator $\hat{a}$. For a harmonic oscillator, a coherent state $\left\lvert{\alpha}\right\rangle$ satisfies:
   $$
   \hat{a} \left\lvert{\alpha}\right\rangle  = \alpha \left\lvert{\alpha}\right\rangle 
   $$

where $\alpha$ is a complex number. Coherent states minimize the Heisenberg uncertainty principle, making them the quantum states most similar to classical oscillations. They exhibit minimal quantum fluctuations, contrary to pathologically defined states such as the eigen state of $\hat{x}$, which maximizes the fluctuation in the momentum space. Also, coherent states form an over-complete basis for the Hilbert space. 

In quantum field theory (QFT), coherent states are often defined with respect to `smeared annihilation operators`. This approach takes into account the fact that field operators are distributions that need to be smeared with test functions to make physical sense. To be specific, the field operators $\hat{\phi}(x)$ and their conjugate momenta $\hat{\pi}(x)$ are functions of spacetime coordinates and are typically distributions. To handle these distributions properly, one introduces smeared field operators:

$$
\hat{\phi}(f) = \int d^dx \, f(x) \hat{\phi}(x)
$$

where $f(x)$ is a smooth test function that **smears** the field operator over spacetime. Similarly, the annihilation operator can be smeared with a test function $g(x)$:

$$
\hat{a}(g) = \int d^dx \, g(x) \hat{a}(x) := \int \frac{d^{d}p}{(2\pi)^{d}} \, \tilde{g}(p) a_ {p},
$$

where $\widetilde{g}(p)$ is the Fourier transform of $g(x)$, and $\hat{a}(x)$ defined by the last integral in momentum space. The eigen equation reads

$$
\hat{a}(g) \left\lvert{\alpha}\right\rangle  = \alpha(g) \left\lvert{\alpha}\right\rangle 
$$

where $\alpha(g)=(\alpha(\vec{x}),g(\vec{x}))$ is the inner product of these two functions.

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

- - -

At the end of section 4.3 in Coleman's note on classical and quantum lumps, he said and I quote

> I do not believe there are any plausible variational computations using coherent states or simple generalizations of them in more than one spatial dimension. It would be nice to have reasonable variational states in this case. A good place to begin exploring would be a super-renormalizable theory in two spatial dimensions. Here, although all divergences are not removed by normal ordering, it is still possible to sum them up in closed form. Thus we have at least a minimal criterion for a reasonable trial state: the expectation value of the Hamiltonian density should not be infinite. Coherent states do not meet this test.

We will see if this is correct in 3+1 dimension. 

# 2. Conventions

we are not interested in the interaction picture but in the Schrodinger picture. It is for a bunch of reasons, one of them is that it is easy to see what the normal-ordering prescription corresponds to in this picture. Schrodinger-picture operators are given as functions of the field $\phi(\vec{x})$ and the canonical momentum density $\pi(\vec{x})$, where $\vec{x}$ is the spatial coordinate, not the Lorentzian spacetime coordinate $x^{\mu}$. We begin with a phi-fourth theory in Schrodinger picture, normal ordered at mass scale $m_ {0}$:

$$
\begin{align*}
\hat{H}(\vec{x}) &= \int d^{3}x: \hat{\mathcal{H}}^{0}(\vec{x}) :_ {m_ {0}} \\
\hat{\mathcal{H}}^{0}(\vec{x}) &= \frac{1}{2}(\pi(\vec{x})^{2}+(\partial_ {i}\phi(\vec{x})^{2}) + \frac{1}{4}(\lambda_ {0}\phi^{4}(\vec{x})-m_ {0}^{2}\phi^{2}(\vec{x}))+A.
\end{align*}
$$

The hat denotes that the vacuum of the Hamiltonian is not obtained at $\phi=0$ yet. To be more specific, the Hamiltonian undergoes spontaneous symmetry breaking, as a result the minimum of the Hamiltonian is obtained at $\phi=v_ {0}$ for some $v_ {0}$. Later we will shift the field operator from $\phi$ to $\phi'$, such that the vacuum is indeed obtained at $\phi'=0$, the Hamiltonian in terms of $\phi'$ will be denoted without the hat. Note the factor $-m_ {0}^{2} /4$ in the mass term, and the last $A$ is a c-number to cancel the zero point energy in the vacuum sector. We also define coupling $g_ {0}$ as 

$$
g_ {0}^{2} := \lambda_ {0}.
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

# 3. Normal ordering with mass m

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

My assumption is, the field operator $\phi(x)$ itself is independent of the aforementioned choice of mass parameter $m$, while the stuff that do depend on $m$ are

1. creation and annihilation operators $a_ {p,m}$ and $a^{\dagger}_ {p,m}$,
2. the energy $\omega=\sqrt{ \vec{p}^{2}+m^{2} }$, we will write it as $\omega_ {p,m}$ explicitly,
3. states in Fock space. For example, the free vacuum $\left\lvert{0,m}\right\rangle$ is by definition annihilated by $a_ {p,m}$. Since the states in the Fock space are constructed by applying $a^{\dagger}_ {p,m}$ consecutively, a re-definition of $a^{\dagger}_ {p,m}$ to, say $a^{\dagger}_ {p,\mu}$ will also change the states themselves.

Recall that the field operator can be expanded in terms of energy and ladder operators, 

$$
\phi(\vec{x}) = \int \frac{d^{d}k}{(2\pi)^{d}}\,  \frac{1}{\sqrt{ 2\omega_ {k,m} }} (a_ {k,m} \, e^{ i\vec{k}\cdot \vec{x} } + a^{\dagger}_ {k,m}\,e^{ -i\vec{k}\cdot \vec{x} })
$$

and the $m$-dependence in $\omega_ {k,m}$, $a_ {k,m}$ and $a^{\dagger}_ {k,m}$ should cancel out so that $\phi(\vec{x})$ itself is $m$-independent.

- - -

We can define the **normal ordering at $m$** by decomposing the Schrodinger picture fields and momenta into creation and annihilation part:

$$
\begin{align*}
\phi^{+}(\vec{x})  &= \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ -i\vec{p}\cdot \vec{x} }  A^{\ddagger}_ {p,m} \\
\phi^{-}(\vec{x}) &=  \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ i\vec{p}\cdot \vec{x} }  \frac{A_ {p,m}}{2\omega_ {p,m}}, 
\end{align*}
$$

similarly for the canonical momenta

$$
\pi^{\pm }(\vec{x})  = \pm   i\sqrt{ -\nabla^{2}+m^{2} }\phi^{\pm }(\vec{x}) ,
$$

which implies

$$
\begin{align*}
\pi^{-}&= - \frac{i}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ i\vec{p}\cdot \vec{x} } A_ {p,m}    ,\\
\pi^{+} &= i \int \frac{d^{3}p}{(2\pi)^{3}} \, e^{ -i\vec{p}\cdot \vec{x} } \omega_ {p,m}A^{\ddagger}_ {p,m}  .
\end{align*}
$$

It is easy to verify that 

$$
\begin{align*}
\phi(\vec{x}) &=  \phi^{+}(\vec{x})  + \phi^{-}(\vec{x}) , \\
\pi(\vec{x}) &=  \pi^{+}(\vec{x})  + \pi^{-}(\vec{x}) . 
\end{align*}
$$

We can arrange a sting of field operators using the Wick's theorem, which says that a string of product of field operators can be rewritten as the sum of all the possible contractions of operators, all of them normal ordered. For example, 

$$
\phi(\vec{x})\phi(\vec{x}) = :\phi(\vec{x})\phi(\vec{x}): + \text{ contraction}\left\lbrace \phi(\vec{x})\phi(\vec{x}) \right\rbrace  .
$$

The contraction is where different choice of $m$ generates different results. Let's write the contraction at $m$ as $C_ {m}\left\lbrace \cdots \right\rbrace$, we have 

$$
\boxed{ 
\begin{align*}
\phi^{2}(\vec{x}) &= :\phi^{2}(\vec{x}):_ {m} + C_ {m}\left\lbrace \phi^{2}(\vec{x}) \right\rbrace , \\
C_ {m}\left\lbrace \phi^{2}(\vec{x}) \right\rbrace &= [\phi^{-},\phi^{+}] = \int \frac{d^3p}{(2\pi)^{3}} \, \frac{1}{2\omega_ {p,m}}. 
\end{align*}
}
$$

Recall that $\phi^{2}$ is $m$-independent, while the normal ordering and the contraction are $m$-dependent. This gives us a means to connect normal ordering at different mass $m$ and $m_ {0}$, since 

$$
\phi^{2}(\vec{x}) = :\phi^{2}(\vec{x}):_ {m} + C_ {m}(\phi^{2}(\vec{x})) = :\phi^{2}(\vec{x}):_ {m_ {0}} + C_ {m_ {0}}(\phi^{2}(\vec{x})),
$$

which implies that 

$$
\begin{align*}
:\phi^{2}(\vec{x}):_ {m_ {0}} &= :\phi^{2}(\vec{x}):_ {m} + C_ {m}-C_ {m_ {0}} \\ 
&= :\phi^{2}(\vec{x}):_ {m} + \frac{1}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, \left( \frac{1}{\omega_ {p,m}} - \frac{1}{\omega_ {p,m_ {0}}} \right) .
\end{align*}
$$

where $C_ {m}$ is short for $C_ {m}(\phi^{2})$, a short-handed notation we will use extensively for the rest of the note. $C_ {m}$ is a c-number, usually given by a divergent integral.

Similarly, 

$$
\boxed{ 
(\partial_ {i}\phi)^{2} = :(\partial_ {i}\phi)^{2} : +  \int \frac{d^{3}p}{(2\pi)^{3}} \,\left( \frac{\vec{p}^{2}}{2\omega_ {p,m}} \right)
}
$$

and

$$
\boxed{ 
\pi^{2}(\vec{x}) =  :\pi^{2}(\vec{x}):_ {m} + \frac{1}{2}\int \frac{d^{3}p}{(2\pi)^{3}} \, \omega_ {p,m}.
}
$$

Let's look at another example which is slightly more complicated, that is the normal ordering of four field operators $\phi^{4}(\vec{x})$,

$$
\begin{align*}
\phi^{4}(\vec{x}) &= :\phi^{4}(\vec{x})+\text{all contractions}:_ {m} \\ 
&= :\phi^{4}(\vec{x})+6C_ {m}\phi^{2}(\vec{x})+3C^{2}_ {m}:_ {m}
\end{align*}
$$

where the factor $6$ comes from $6$ distinct ways to contract two fields out of four, and the factor $3$ comes from 3 distinct ways to contract all the fields. Take $6C_ {m}\phi^{2}$ for example, it (including the combinatoric factors) can be conveniently written as

$$
\frac{1}{2} C_ {m} \frac{d^{2}}{d\phi^{2}} \phi^{4} = 6 C_ {m} \phi^{2},
$$

where the factor of $\frac{1}{2}$ is to cancel the double counting of any contraction. Similarly, for the full contraction, we can write it as 

$$
\frac{1}{2}\left( \frac{1}{2}C_ {m} \frac{d^{2}}{d\phi^{2}} \right)^{2} \phi^{4} = 3C_ {m}^{2}.
$$

The symmetry factors need some explanation. Each $C_ {m}$ comes with a symmetry factor $1/2$, since $C_ {m}$ is the contraction of $\phi^{2}$, which is always double counted. There are two pairs of contraction out of four $\phi$'s, hence the extra symmetry factor $1/2$. 

If there were six $\phi$'s to contract, the total contraction of $\phi^{6}(\vec{x})$ comprises of three pairs of $C_ {m}$. We can calculate the total contraction using 

$$
\frac{1}{3!}\left( \frac{1}{2}C_ {m} \frac{d^{2}}{d\phi^{2}}  \right)^{3} \phi^{6}(\vec{x}) = 15 C_ {m}^{3}.
$$

The symmetry factor $1/n!$ reminds us of the Taylor expansion of exponents. We can assemble all the contractions together in a neat formula. In general, given any polynomial function $U(\phi)$ of $\phi$, we have 

$$
\boxed{ 
U(\phi) = :\exp \left\lbrace \frac{1}{2}C_ {m} \frac{d^{2}}{d\phi^{2}} \right\rbrace U(\phi):_ {m}.
}
$$

Note it is the double derivative $d^{2}/d\phi^{2}$, not single derivative $d/d(\phi^{2})$. 

- - -

For a free theory of mass $m$, and for any source function $J(x)$, we have 

$$
\begin{align*}
\exp \left\lbrace i \int \, J(x)\phi(x) d^{2}x  \right\rbrace  &=\; :\exp \left\lbrace i \int d^{2}x   \, J(x)\phi(x)  \right\rbrace:_ {m} \\
&\;\;\;\;\;\times \exp \left\lbrace -\frac{1}{2}\int d^{2}x  d^{2}y J(x) \, \Delta(x-y)J(y)  \right\rbrace 
\end{align*}
$$

where $\Delta(x-y)$ is the Wightman function. If we go to interaction picture and adopt time ordering, the Wightman functions become Feynman propagators.

- - -

For the sake of completeness, we compare the normal ordering of $\phi^{2}(\vec{x})$, $\pi^{2}$, $(\partial_ {i}\phi)^{2}$ and $\phi^{4}$ at different mass, namely $m$ and $m_ {0}$. The result is given below. 

$$
\begin{align*}
:\phi^{2}(\vec{x}):_ {m_ {0}} &=  :\phi^{2}(\vec{x}):_ {m} + I , \\
:\pi^{2}(\vec{x}):_ {m_ {0}} &= :\pi^{2}(\vec{x}):_ {m} + \frac{1}{2}\int \frac{d^{3}p}{(2\pi)^{3}} \, (\omega_ {p,m}-\omega_ {p,m_ {0}}), \\
:( \vec{\nabla}\phi )\cdot(\vec{\nabla}\phi):_ {m_ {0}} &= :( \vec{\nabla}\phi )\cdot(\vec{\nabla}\phi):_ {m} +  \int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{\vec{p}^{2}}{2} \left( \frac{1}{\omega_ {p,m}}-\frac{1}{\omega_ {p,m_ {0}}} \right) , \\
:\phi^{4}(\vec{x}):_ {m_ {0}} &= :\phi^{4}(\vec{x}):_ {m} + 6 I :\phi^{2}:_ {m} +3I^{2}, \\
I &=  C_ {m}-C_ {m_ {0}} = \frac{1}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{1}{\omega_ {p,m}}-\frac{1}{\omega_ {p,m_ {0}}} \right).
\end{align*}
$$

Recall that the **defining expression** for the Hamiltonian density reads

$$
\begin{align*}
\hat{H}(\vec{x}) &= \int d^{3}x \,  :\hat{\mathcal{H}}^{0}(\vec{x}):_ {m_ {0}} = \int d^{3}x \, :\hat{\mathcal{H}}:_ {m} , \\
\hat{\mathcal{H}}^{0}(\vec{x}) &= \frac{1}{2}\pi^{2}(\vec{x})+\frac{1}{2} (\partial_ {i}\phi)^{2} - \frac{m_ {0}^{2}}{4} \phi^{2}(\vec{x}) + \frac{\lambda_ {0}}{4} \phi^{4}(\vec{x}) + A,
\end{align*}
$$

We want to normal order it to get rid of the infinite zero point energy. The thing is, there are two obvious options for the mass scale at which the normal ordering is done: the bare mass $m_ {0}$ and the "physical" mass $m$. At $m_ {0}$ we have 

$$
\begin{align*}
\hat{\mathcal{H}}^{0}(\vec{x}) &= :\hat{\mathcal{H}}^{0}(\vec{x}):_ {m_ {0}}  + \frac{3}{2}\lambda_ {0} C_ {m_ {0}} :\phi^{2}(\vec{x}):_ {m_ {0}} + \frac{3}{4} \lambda_ {0} C_ {m_ {0}}^{2} - \frac{m_ {0}^{2}}{4}C_ {m_ {0}} \\
  &\;\;\;\; + \frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,   \frac{2\vec{p}^{2}+m_ {0}^{2}}{\omega_ {p,m_ {0}}}  .
\end{align*} 
$$

We can also rewrite it into normal ordering at $m$:

$$
\begin{align*}
  :\hat{\mathcal{H}}^{0}(\vec{x}):_ {m_ {0}} &= :\hat{\mathcal{H}}^{0}(\vec{x}):_ {m} + \frac{3}{2}\lambda_ {0} I :\phi^{2}(\vec{x}):_ {m} + \frac{3}{4} \lambda_ {0} I^{2} - \frac{m_ {0}^{2}}{4}I \\
  &\;\;\;\; + \frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{2\vec{p}^{2}+m^{2}}{\omega_ {p,m}} - \frac{2\vec{p}^{2}+m_ {0}^{2}}{\omega_ {p,m_ {0}}}  \right) .
\end{align*} 
$$

Since, by definition, $:\hat{\mathcal{H}}:_ {m}=:\hat{\mathcal{H}}^{0}:_ {m_ {0}}$, we have 

$$
\begin{align*}
\hat{\mathcal{H}}(\vec{x})&= \hat{\mathcal{H}}^{0}(\vec{x}) + \frac{3}{2}\lambda_ {0} I \phi^{2}(\vec{x}) + \frac{3}{4} \lambda_ {0} I^{2} - \frac{m_ {0}^{2}}{4}I \\
  &\;\;\;\; + \frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{2\vec{p}^{2}+m^{2}}{\omega_ {p,m}} - \frac{2\vec{p}^{2}+m_ {0}^{2}}{\omega_ {p,m_ {0}}}  \right) 
\end{align*}
$$


[^Polchinski]: J. Polchinski, String Theory. Vol. 1: An Introduction to the Bosonic String. Cambridge Univ. Pr., UK, 1998.

# 4. Triviality of phi-fourth theory

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
# 5. Perturbative Expansion of the Hamiltonian

Since we want to cancel divergences in a perturbative manner, that is, order-by-order in (renormalized) coupling $\lambda$. When $\Lambda$ is involved, we should count the order with respect to $\lambda$ first, treating terms such as $\lambda \Lambda,\,\lambda \Lambda^{2}, \cdots\lambda \Lambda^{n}$ all as $\mathcal{O}(\lambda)$, and group things of the same order together. Only then do we take the limit $\Lambda\to\infty$, and cancel the divergences. 

For the rest of this note, unless explicitly said otherwise, $\lambda$ stants for the *renormalized coupling* and $\lambda_ {0}$ the bare coupling.

I copy the Hamiltonian here:

$$
\begin{align*}
\hat{H}(\vec{x}) &= \int d^{3}x \, :\left\lbrace   \hat{\mathcal{H}}^{0}(\vec{x}) + \frac{3}{2}\lambda_ {0} I \phi^{2}(\vec{x}) + \frac{3}{4} \lambda_ {0} I^{2} - \frac{1}{4}I\,m_ {0}^{2} \right\rbrace :_ {m} \\
  &\;\;\;\; +  \int d^{3}x \,\frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{2\vec{p}^{2}+m^{2}}{\omega_ {p,m}} - \frac{2\vec{p}^{2}+m_ {0}^{2}}{\omega_ {p,m_ {0}}}  \right) .
\end{align*}
$$

p.s. **Jarah's version is written differently**, 

$$
\begin{align*}
\hat{H}(\vec{x})   &=\int d^{3}x \, :\left\lbrace   \hat{\mathcal{H}}^{0}(\vec{x}) + \frac{3}{2}\lambda_ {0} I \phi^{2}(\vec{x}) + \frac{3}{4} \lambda_ {0} I^{2} - \frac{3}{4}I\,m_ {0}^{2} \right\rbrace :_ {m} \\
  &\;\;\;\; +  \int d^{3}x \,\frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \frac{(\omega_ {p,m}-\omega_ {p,m_ {0}})^{2}}{\omega_ {p,m}} ,
  \end{align*}
$$

which is equivalent to our expression. 

A simple Taylor expansion shows that 

$$
\omega_ {p,m} = \omega_ {p,m_ {0}} + \frac{1}{2} \frac{\delta m^{2}}{\omega_ {p,m_ {0}}} + \mathcal{O}(\delta m^{4}),
$$

thus 

$$
\omega_ {p,m} - \omega_ {p,m_ {0}} \sim \mathcal{O}(\lambda) 
$$

since $\delta m^{2}=(\cdots)\lambda+(\cdots)\lambda^{2}+\cdots$. Similarly, 

$$
\begin{align*}
I &= \frac{1}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{1}{\omega_ {p,m}}-\frac{1}{\omega_ {p,m_ {0}}} \right) \\
&= \frac{1}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, \left( - \frac{\delta m^{2}}{2 \omega^{3}_ {p,m_ {0}}} +\cdots \right)\\
&= -\frac{\delta m^{2}}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,   \frac{1}{\omega^{3}_ {p,m_ {0}} }   + \cdots\\
&\sim \mathcal{O}(\lambda)
\end{align*}
$$

The last term in the Hamiltonian density reads

$$
\frac{1}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \left( \frac{2\vec{p}^{2}+m^{2}}{\omega_ {p,m}} - \frac{2\vec{p}^{2}+m_ {0}^{2}}{\omega_ {p,m_ {0}}}  \right) = \frac{m_ {0}^{2}\delta m^{2}}{8} \int \frac{d^{3}p}{(2\pi)^{3}} \,  \frac{1}{\omega^{3}_ {p,m_ {0}}} +\cdots.
$$

There is another constant term that is of order $\lambda$: 

$$
- \frac{1}{4}I\,m_ {0}^{2}  = \frac{m_ {0}^{2}\,\delta m^{2}}{16}\int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{1}{\omega^{3}_ {p,m_ {0}}} +\cdots.
$$

This is too bad, since I had hoped that the above equation will cancel the above above equation. But we can rearrange the terms proportional to $m_ {0}^{2}$ such that the integrals cancel each other and leaves us only one single term: $-\frac{3}{4} Im_ {0}^{2}$.

The term $\frac{3}{2}\lambda_ {0} I \phi^{2}(\vec{x})$ needs some extra work. It seems to be of order $\lambda_ {0}I\sim \mathcal{O}(\lambda^{2})$, however, often times we need to replace the field operator $\phi$ by $\left\langle \phi \right\rangle+\phi'$, where $\left\langle \phi \right\rangle$ is the expectation valued for $\phi$ under certain circumstances, and it is usually of order $\left\langle \phi \right\rangle\sim 1 / g$ where $g\equiv \sqrt{ \lambda }$. Thus this quadratic term is actually of order $\mathcal{O}(\lambda)$ and we need to keep it.

Putting everything together. At the leading order of $\lambda$ we have 

$$
\begin{align*}
\hat{H}(\vec{x}) &= \int d^{3}x \, \left\lbrace   :\hat{\mathcal{H}}^{0}(\vec{x}) + \frac{3}{2}\lambda_ {0} I \phi^{2}(\vec{x}) - \frac{3}{4} I m_ {0}^{2}  :_ {m}  \right\rbrace 
\end{align*}
$$

Then we write the bare parameters in terms of renormalized ones (recall that $g:= \sqrt{ \lambda }$ for both bare and renormalized parameters), at order $\mathcal{O}(\lambda)$ we have 

$$
\begin{align*}
\hat{H}(\vec{x}) &\supset \int d^{3}x \, : \frac{1}{2}\pi^{2}+\frac{1}{2}(\partial_ {i}\phi)^{2} - \frac{m^{2}}{4}\phi^{2}+\frac{g^{2}}{4}\phi^{4}:_ {m}  \\
 &\;\;\;\; + \int d^{3}x \, : \frac{\delta m^{2}}{4}\phi^{2}-\frac{1}{2}g \delta g\phi^{4}+\frac{3}{2}g^{2}I\phi^{2}-\frac{3}{4}m^{2}I +A :_ {m}.
\end{align*}
$$

We have neglected higher order terms, for example a term $3g\delta g\sim \mathcal{O}(g^{4}) \sim\mathcal{O}(\lambda^{2})$ was dropped from the expression.
# 6. Passive Transformation by $D_ {f}$

In order to find the approximate Hilbert state with correct vacuum expectation value of $\phi$, we introduce the displacement operator. Given a function $f(\vec{x})$, the associated displacement operator is defined as 

$$
\mathcal{D}_ {f} := \exp \left\lbrace -i\pi(f) \right\rbrace , \quad \pi(f):=\int d^{3}x \,  f(\vec{x})\pi(\vec{x}).
$$

$\pi(f)$ is the **smeared** canonical momentum operator. This definition is similar to the space translation operator

$$
T_ {\vec{x}} = \exp \left\lbrace -i\hat{P}\cdot \vec{x} \right\rbrace .
$$

The translation operator changes the position, while the displacement operator changes the vev of the field operator itself. To be more specific, 

$$
\begin{align*}
T_ {\vec{x}}\, \phi(\vec{y})\, T_ {\vec{x}}^{\dagger} &= \phi(\vec{y}-\vec{x}),\\
\mathcal{D}_ {f} ^{\dagger} \, \phi(\vec{x})\, \mathcal{D}_ {f} &= \phi(\vec{x})+f(\vec{x}).
\end{align*}
$$

The statement is that, we can use the unitary $\mathcal{D}_ {f}$ to translate the basis of the Hilbert space. 

I find it helpful to use $T_ {\vec{x}}$ as an example to understand the properties of $\mathcal{D}_ {f}$. Let $\left\lvert{\psi}\right\rangle$ be any state in quantum mechanics, what is the resulting state of $T_ {\vec{x}}$ acting on it? $T_ {\vec{x}}\left\lvert{\psi}\right\rangle$ has two interpretations, the passive view and the active view. In the passive view, the translation operator is seen as a change in the coordinate system or reference frame rather than a change in the physical state itself. The state of the system remains unchanged, but the coordinates used to describe it are shifted. In the active view, the translation operator actively shifts the physical state of the system by a displacement. The coordinates remain fixed, but the state or the field configuration changes. The same goes for the displacement operator $\mathcal{D}_ {f}$, given any state (quantum field theory now, no longer quantum mechanics) $\left\lvert{\Psi}\right\rangle$, $\mathcal{D}_ {f}\left\lvert{\Psi}\right\rangle$ can be seen as either a new state (active perspective), or the same state but in different basis (passive perspective). When discussing kink states and trivial vacuum states in the future, it seems best to consider $\mathcal{D}_ {f}$ passively. This approach allows us to discuss the same states in different bases, or frames. We'll delve into the details shortly. However, before diving into quantum field theory, I would like to first address the nature of quantum states in quantum mechanics.

---

Quantum mechanics is defined over the spatial coordinates $\vec{x}$. The position eigenstates $\left\lvert{\vec{x}}\right\rangle$ form a complete basis of the Hilbert space. However, $\left\lvert{\vec{x}}\right\rangle$ is represented by a Dirac $\delta$-function, which does not belong to the Hilbert space of $L^{2}(\mathbb{R}^{d})$, where $d$ is the dimension of the space, as usually. It is a challenge to mathematical rigor of quantum mechanics. 

Recall that the Hilbert space $L^{2}(\mathbb{R}^{d})$ consists of all square-integrable functions defined on $\mathbb{R}^{d}$, with an inner product $\left\langle f,g \right\rangle=\int dx \, f^{\ast}g$. This inner product also defines a norm, and with norm we can talk about Cauchy completeness. The space $L^{2}$ is indeed Cauchy complete, since we do not require functions in it to be smooth. The Cauchy completeness makes it a Hilbert space, not a pre-Hilbert space. 

To deal with mathematical objects such as the Dirac $\delta$-function, quantum mechanics often uses the concept of `rigged Hilbert space`, also known as a `Gelfand triplet`. A rigged Hilbert space involves three components:

1. Schwartz space $\mathcal{S}$, the space of **rapidly decreasing smooth** functions. It is a dense subspace of the Hilbert space that we talk about in the next paragraph. By working with $\mathcal{S}$, we can rigorously define unbounded operators and their domains. States here are smooth and decays faster than any polynomial, making them suitable for rigorous operator definitions.
2. Hilbert space $L^{2}$. The Schwartz space $\mathcal{S}$ is a dense subset of $L^{2}$. Here is where all the quantum states reside. These states are normalizable and have finite norm. 
3. Dual space $\mathcal{S}^{\ast}$. It includes functionals, also called generalized states. The Dirac delta function represents the position eigenstate, while plane waves represent momentum eigenstates, we can't fit them into the Hilbert space $L^{2}$, here is where these pathological states reside.

The relationship can be written as 

$$
\mathcal{S} \subset L^{2} \subset \mathcal{S}^{\ast }.
$$

Actually, I don't think it makes a lot of sense to regard $\left\lvert{\vec{x}}\right\rangle$ as a physical state, since in real life, due to the uncertainty principal, a particle will never be localized at a specific point. Instead, the position always smears about a certain region, so is its momentum. The role of $\left\lvert{\vec{x}}\right\rangle$ is more of giving us the value of the wave function at position $\vec{x}$, in other words, what naturally appears is the dual version $\left\langle{\vec{x}}\right\rvert$ of $\left\lvert{\vec{x}}\right\rangle$. $\left\langle{\vec{x}}\right\rvert$ can be regarded as map that takes a state in the Hilbert space of quantum states, and spits out a complex number:

$$
\begin{align*}
\left\langle{\vec{x}}\right\rvert : \quad  \mathcal{H} &\to \mathbb{C} \\
\left\lvert{\psi}\right\rangle  &\mapsto \psi(\vec{x}),
\end{align*}
$$

where $\mathcal{H}$ is not the Hamiltonian but the Hilbert space of quantum states. 

For a state $\left\lvert{\psi}\right\rangle$ to be a physical state, it should be sensible to talk about 

$$
\left\langle{\psi}\right\rvert \mathcal{O} \left\lvert{\psi}\right\rangle ,\quad  \mathcal{O}\text{ is an observable.}
$$

$\left\lvert{\vec{x}}\right\rangle$ fails this requirement since $\left\langle{\vec{x}}\right\rvert \hat{x} \left\lvert{\vec{x}}\right\rangle=\infty$, this is another reason to say that $\left\lvert{\vec{x}}\right\rangle$ is not a physical state. 

- - -

We distinguish two concepts, `states` and `wave function`. In quantum mechanics, they are sometimes used interchangeably, but they have distinct meanings. A quantum state contains all the information about the system. It can be described in different representations, depending on what information we want to know. For example, if we want to know information about the position, we go to the physical space representation expanded by $\left\lvert{\vec{x}}\right\rangle$. Quantum states can be represented as vectors in a Hilbert space, and there exists pure and mixed states. On the other hand, the wave function is a specific representation of a quantum state in the position (or sometimes momentum) basis. It is a complex-valued function that gives the probability amplitude of finding a particle in a particular position in space. The wave function of a state $\left\lvert{\psi}\right\rangle$ is denoted by $\psi(x)$, where $x$ is the position. 

In the passive perspective, a state before and after spatial translation is the same state, they just have different wave functions, because in order to get the wave function we need two things: bases and a state, even though the state is unchanged but the bases are changed now, thus the final expression is also changed.

- - -

Coming back to the passive perspective regarding the displacement operator $\mathcal{D}_ {f}$ acting on a state, for example the kink state $\left\lvert{K}\right\rangle$. We regard $\mathcal{D}_ {f}\left\lvert{K}\right\rangle$ (or is it $D_ {f}^{\dagger}\left\lvert{K}\right\rangle$? I don't remember, anyways the argument works the same) as the same state as $\left\lvert{K}\right\rangle$, but "shifted". In the case of quantum mechanics, the things that get shifted are wave functions; in quantum field theory, it should be **wave functional**, the quantum field theoretical counterpart of wave functions. Let's dive into the details.

Consider a scalar field theory. The "coordinate" for such a theory would not be $\vec{x},\vec{y}$ but field configurations $\phi(\vec{x})$. Instead of the position of a single particle, we now consider the entire configuration of the field $\phi(x)$ at a particular time. The wave functional $\Psi[\phi]$ describes the quantum state of the entire field configuration $\phi(x)$ at a given time.  Recall how the quantization is done in quantum mechanics: classically a particle occupies a specific position $\vec{x}(t)$ at any given time $t$, after quantization, instead of $\vec{x}(t)$ we have a wave function $\psi$ that maps each $\vec{x}$ to a complex number. This is just to say that the wave function is a function of spacetime. Similarly, in QFT, let $\Psi[\phi]$ be a functional, then by definition it assigns a complex number to each field configuration $\phi(\vec{x})$,

$$
\Psi: \phi(\vec{x}) \mapsto \mathbb{C}.
$$

Similar to $\left\lvert{\vec{x}}\right\rangle$ is the eigen state of $\hat{x}$, $\hat{x}\left\lvert{\vec{x}}\right\rangle=\vec{x}$, we can construct the eigen state of field operator $\hat{\phi}$ by 

$$
\hat{\phi}(\vec{x})\left\lvert{\phi}\right\rangle  = \phi(\vec{x})\left\lvert{\phi}\right\rangle ,
$$

Any wave functional can be given as a superposition of such eigen states. Let $\left\lvert{\Psi}\right\rangle$ be a well-behaved wave functions, it can be formally written as 

$$
\left\lvert{\Psi}\right\rangle  = \int D\phi(\vec{x}) \, \Psi[\phi(\bullet)] \left\lvert{\phi(\bullet)}\right\rangle  ,
$$

where the bullet in $\phi(\bullet)$ indicates a spatial coordinate, it is here to remind us that $\phi$ is a function, but I don't want to waste another Latin letter. 

Given the quantum state $\left\lvert{\Psi}\right\rangle$, the wave functional corresponding to this state is given by

$$
\Psi [\phi(\bullet)] = \left\langle \phi \middle\vert \Psi \right\rangle \in \mathbb{C}.
$$

As a consistency check, let's see if we can reproduce the result $\left\langle{\Psi}\right\rvert\hat{\phi}(\vec{x}) \left\lvert{\Psi}\right\rangle=\psi(\vec{x})$ for some classical field $\psi(\vec{x})$. We have 

$$
\begin{align*}
\left\langle{\Psi}\right\rvert \hat{\phi}(\vec{x})\left\lvert{\Psi}\right\rangle &= 
\int D\varphi \,  \Psi ^\ast [\varphi]\left\langle{\varphi}\right\rvert\,  \hat{\phi}(\vec{x})\,\int D\varphi' \, \Psi[\varphi']\left\lvert{\varphi'}\right\rangle   \\
&= \int D\varphi \,  \Psi^\ast [\varphi] D\varphi' \, \Psi[\varphi']\left\langle{\varphi}\right\rvert\,  \varphi'(\vec{x})\left\lvert{\varphi'}\right\rangle   \\
&= \int D\varphi \,  \Psi^\ast [\varphi] D\varphi' \, \Psi[\varphi'] \varphi'(\vec{x}) \delta(\varphi-\varphi') \\
&= \int D\varphi \,  \Psi^\ast [\varphi]\, \Psi[\varphi] \varphi(\vec{x}) \\
&= \int D\varphi \,  \left\lvert \Psi[\varphi] \right\rvert^{2}  \varphi(\vec{x}),
\end{align*}
$$

and recall that $\left\lvert \Psi[\varphi] \right\rvert^{2}$ is the probability of finding $\varphi$ in $\Psi$, thus indeed we have 

$$
\int D\varphi \,  \left\lvert \Psi[\varphi] \right\rvert^{2}  \varphi(\vec{x}) = \left\langle \hat{\phi}(\vec{x}) \right\rangle =: \psi(\vec{x}).
$$

Time evolution is generated by the Hamiltonian, yielding a functional Schrodinger equation:

$$
i\hbar \left\lvert{\Psi[\phi]}\right\rangle  = \hat{H}\left\lvert{\Psi[\phi]}\right\rangle ,
$$

- - -

For the ground state (or vacuum state) of the free scalar field, the wave functional $\Psi_0[\phi]$ has a Gaussian form, it is basically an infinite lattice of harmonic oscillators. It can be written as:

$$
\Psi_0[\phi] = N \exp \left( -\frac{1}{2} \int d^3x \, d^3y \, \phi(x) K(x,y) \phi(y) \right)
$$

where $N$ is a normalization constant, and $K(x,y)$ is a kernel that depends on the mass $m$ of the scalar field and the spatial separation $|x - y|$.

For a free scalar field, $K(x,y)$ can be written in terms of the Fourier transform:

$$
K(x,y) = \int \frac{d^3k}{(2\pi)^3} \, \omega_k \, e^{i k \cdot (x - y)}
$$

with $\omega_k = \sqrt{k^2 + m^2}$.

The wave functional $\Psi_0[\phi]$ provides the probability amplitude for the field configuration $\phi(x)$. The exponential form indicates that the ground state is a Gaussian distribution centered around $\phi(x) = 0$, reflecting the fact that the vacuum state has no preferred field configuration (zero field on average).

For more information please refer to this [post](https://physics.stackexchange.com/questions/746099/schroedinger-equation-for-wave-functional-qft).

- - -

Now we can talk about passive perspective of the action of the displacement operator $D_ {f}$, in a more rigorous way. $\mathcal{D}_ {f}$ will increase the basis $\left\lvert{\varphi}\right\rangle$ by $f(\vec{x})$, 

$$
\mathcal{D}_ {f}\left\lvert{\varphi(\vec{x})}\right\rangle  = \left\lvert{\varphi(\vec{x})+f(\vec{x})}\right\rangle .
$$

Then, as you can verify, we have 

$$
\left\langle{\Psi}\right\rvert \mathcal{D}_ {f}^{\dagger} \hat{\phi}(\vec{x}) \mathcal{D}_ {f}\left\lvert{\Psi}\right\rangle  = \psi(\vec{x})+f(\vec{x}),
$$

as we showed before. We can regard $\mathcal{D}_ {f}\left\lvert{\Psi}\right\rangle$ as the same state as $\left\lvert{\Psi}\right\rangle$, just measured with different basis: instead of $\left\langle \varphi \middle\vert \Psi \right\rangle$, we have $\left\langle \varphi+f \middle\vert \Psi \right\rangle$. 

In the following notes, we will talk about the spontaneous symmetry breaking, and enter the main part of the projcet. 

