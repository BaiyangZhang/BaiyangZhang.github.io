---
layout: post
title: A Passive Perspective of Linearized Soliton Perturbation Theory
date: 2025-01-02
author: Baiyang Zhang
catalog: true
tags:
  - kink
---

# The model

## Unnecessary mathematical preliminaries

*This section can be skipped.*

An `algebra` over a field $k$ is a vector space $A$ over $k$, equipped with an additional structure: a bilinear multiplication $\cdot: A \times A \to A$ that makes $A$ a ring (not necessarily commutative). That is, $A$ has:

- Addition $+$ and scalar multiplication $\cdot$, making $A$ a $k$-vector space,
- A bilinear multiplication satisfying associativity.

More formally, an algebra $A$ is a vector space over field $k$ together with a map:


$$
\mu: A \times A \to A, \quad (a, b) \mapsto ab
$$

that satisfies the ring axioms and is $k$-bilinear, meaning:

$$
(ab + c)d = ab \cdot d + c \cdot d, \quad a(b + c)d = ab \cdot d + ac \cdot d
$$

for all $a, b, c, d \in A$. Examples of Algebras include Matrix algebra (the space of $n \times n$ matrices over a field $k$, with matrix addition and multiplication), Polynomial algebra and Function algebra. 

An algebra $A$ is said to be `unital` if it contains a multiplicative unit $1$. 

- - -

Denote by $\mathcal{E}$ a complex Hilbert space, with inner product $\left\langle - \middle\vert- \right\rangle$, and $\mathcal{B}(\mathcal{E})$ the set of all bounded operators. In is a Banach algebra with the `operator norm`, which is defined as

$$
\left\lVert A \right\rVert = \text{sup}\, \left\lVert Av \right\rVert \quad  \;\forall\;  \left\lVert v \right\rVert =1.
$$

Let $\xi_ {1},\xi_ {2} \in\mathcal{E}$. For $a\in \mathcal{B}(\mathcal{E})$, the adjoint operator $a^{\ast}$ is defined by 

$$
\left\langle a^{\ast }\xi_ {1} \middle\vert\xi_ {2} \right\rangle  = \left\langle \xi_ {1} \middle\vert a \xi_ {2} \right\rangle .
$$

The adjoint operation is an `involution`, i.e. it is anti-linear (meaning $(\lambda a)^{\ast}=\overline{\lambda} a^{\ast}$, where $\overline{\lambda}$ is the complex conjugate of $\lambda$) and satisfies $(ab)^{\ast}=b^{\ast}a^{\ast}$.

For it to be a $\mathbb{C}^{\ast}$-algebra, it must satisfy the $\mathbb{C}^{\ast}$-identity

$$
\left\lVert a^{\ast }a \right\rVert = \lVert a \rVert ^{2}.
$$

If the $\mathbb{C}^{\ast}$-algebra is Cauchy-complete under the operator norm, then it is said to be a concrete $\mathbb{C}^{\ast}$-algebra. By default all the $\mathbb{C}^{\ast}$-algebras we talk about will be concrete, so we will ignore it.

- - -

A `module` over an algebra $A$ is a generalization of a vector space, where the scalars used for multiplication come from the algebra $A$ rather than a field. Te be precise, an $A$-module $M$ is an abelian group (under addition) together with a multiplication map:

$$
A \times M \to M, \quad (a, m) \mapsto a \cdot m
$$

satisfying the following conditions for all $a, b \in A$, $m, n \in M$, and $\lambda \in k$:

1. Distributivity: $(a + b) \cdot m = a \cdot m + b \cdot m$,
2. $a \cdot (m + n) = a \cdot m + a \cdot n$,
3. $(\lambda a) \cdot m = \lambda (a \cdot m)$,
4. $(ab) \cdot m = a \cdot (b \cdot m)$.

Roughly speaking, a vector space is just a module over a field. A module over a commutative algebra $A$ can be thought of as a generalization of a vector space where scalars come from $A$ instead of $k$.

Examples of modules over algebras include Module over matrix algebras, Polynomial modules, etc.

A module is said to be `simple` if it does not have nonzero proper submodule.

---

**Definition.** `Endomorphism algebra`. If $V$ is a $k$-vector space, then $\text{End}(V)$ is an algebra formed of the the set of all linear maps from $V$ to $V$ itself (endomorphisms), where the multiplication of two elements is given by composition. 

For example, let $V$ be $\mathbb{R}^{n}$, then the endomorphism algebra $\text{End}(V)$ is the $n\times n$ real matrices. 

**Definition.** `Algebra representation`. Let $A$ be a $k$-algebra, a representation of $A$ is a homomorphism between algebras that maps $A$ to $\text{End}(V)$ for some $k$-module $V$. 

In human's language, to define a representation of an abstract algebra, we first choose a module that the algebra act on, then define how exactly each element of the algebra acts on $V$. 

- - -

An introduction of category theory can be found in my blogs [here](https://www.mathlimbo.net/blog/2023/Basic-Category-Theory-Lecture-1/) and [here](https://www.mathlimbo.net/blog/2023/Basic-Category-Theory-Lecture-2/). A blog explicitly devoted to Yoneda lemma which is sometime useful in dealing with gauge theory can be found [here](https://www.mathlimbo.net/blog/2024/Yoneda-Lemma/), but I doubt we will need it in this note.


## Problems with interaction picture

*This section can be entirely skipped for readers who are not interested in Haag's theorem.*

Recall how we quantize a classical theory with interactions. First, 


There are some fundamental issues regarding the good old interaction picture that I haven't figured out, and I mean the so-called Haag's theorem, or more accurately Haag-Hall-Wightman (HHW) theorem, which roughly says that interaction picture is inconsistent, even in the case of neutral free scalar field with different masses. **It claims that the set of assumptions required to construct the interaction picture is only consistent when there is no interaction.** It also claims that **non-Fock representations have an important rule to play in QFT** (Earman and Fraser, 2006). Our work on kinks will provide an concrete example of that. 

- - -

Quantum theories, no matter quantum field theory or quantum field theory are described by a bunch of canonical commutation relations (here we only consider bosonic case), such as $[x,p]=i\hbar$ or $[\phi(\vec{x}),\pi(\vec{y})]=(2\pi)^{d}\delta^{d}(\vec{x}-\vec{y})$. In quantum mechanics we have finite sets of independent CCR's (canonical commutation relation), while in quantum field theory we have an finite set of them. Things usually get quite messy when going from finite to infinity, properties that hold in the finite case may not hold for infinite case, for example a sum of finite positive numbers are always positive, but a sum of infinite positive numbers may not be positive anymore. The same thing happens with going from quantum mechanics to quantum field theory. 

Given the CCR's, we need to find the associated Hilbert space, or the `representation` of CCR. This Hilbert space, or representation should be irreducible, other wise we can separate the theory into two different fields. Regarding quantum mechanics, which is a finite dimensional CCR system, the `Stone-von Neumann theorem` tells us that the irreducible representation of 




The vacuum state can be specified in two ways: (1) it is the minimal energy state; (2) it is the unique state annihilated by particle number operator $a^{\dagger}a$. If these two specification don't coincide, the vacuum is said to be `polarized`. As we will see later, **the presence of a kink will polarize the trivial vacuum**. **Vacuum polarization lies at the core of HHW theorem, any interacting quantum field operator, or free fields of different masses, polarizes the vacuum**. 



## The Hamiltonian

We will work in Schrodinger picture, where operators are dependent on position only. Why don't we work with the good old interaction picture? We will only consider real scalar field $\phi$, in Schrodinger picture, a generic operator $\mathcal{O}(\phi(\vec{x},\pi(\vec{x})))$ is given as a function of the field $\phi(\vec{x})$ and the canonical momentum density $\pi(\vec{x})$, where $\vec{x}$ is the spatial coordinate, not the Lorentzian spacetime coordinate $x^{\mu}$. 

We begin with a phi-fourth theory in Schrodinger picture, normal ordered at mass scale $m_ {0}$:

$$
\begin{align*}
\hat{H}(\vec{x}) &= \int d^{3}x: \hat{\mathcal{H}}^{0}(\vec{x}) :_ {m_ {0}} \\
\hat{\mathcal{H}}^{0}(\vec{x}) &= \frac{1}{2}(\pi(\vec{x})^{2}+(\partial_ {i}\phi(\vec{x})^{2}) + \frac{1}{4}(\lambda_ {0}\phi^{4}(\vec{x})-m_ {0}^{2}\phi^{2}(\vec{x}))+A.
\end{align*}
$$

We use the convention that parameter with a naught subscript represents bare parameters, $\hat{H}$ is the Hamiltonian before the spontaneous symmetry breaking (SSB) while $H$ is the Hamiltonian after SSB. To be more specific, the Hamiltonian undergoes spontaneous symmetry breaking since the minimum of the Hamiltonian is obtained at $\phi=v_ {0}$ for some $v_ {0}$. Later we will shift the field operator from $\phi$ to $\phi'$, such that the vacuum is indeed obtained at $\phi'=0$, the Hamiltonian in terms of $\phi'$ will be denoted without hat. Note the factor $-m_ {0}^{2} /4$ in the mass term, we have $\frac{1}{4}$ instead of $\frac{1}{2}$ so that in the symmetry broken phase the particle has a canonical mass term. The last $A$ in the Hamiltonian is a c-number that cancels the zero point energy in the vacuum sector. We also define coupling $g_ {0}$ as 

$$
g_ {0}^{2} := \lambda_ {0}.
$$

In the Schrodinger picture, the field operator and canonical momentum operator can be decomposed in terms of plane waves as usual,

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
\delta m^{2}& =\sum_ {i=1}^{\infty} \delta m^{2}_ {i} , \quad  \delta m^{2}_ {i}\sim  \mathcal{O}(g^{i+1}),   \\
\delta g &= \sum_ {i=1}^{\infty} \delta g_ {i}, \quad \delta g_ {i}  \sim \mathcal{O}(g^{i+2}),\\
H &= \sum_ {i=0}^{\infty} H_ {i},\quad  H_ {i} \sim \mathcal{O}(g^{i-2}) , \\
A &= \sum_ {i=0}^{\infty}A_ {i}, \quad  A_ {i} \sim \mathcal{O}(g^{i-2}) , \\
\delta v &= \sum_ {i=1}^{\infty} \delta v_ {i} ,\quad  \delta v_ {i} \sim \mathcal{O}(g^{i}), \\
\left\lvert{\Psi}\right\rangle  &= \sum_ {i=0}^{\infty} \left\lvert{\Psi_ {i}}\right\rangle , \quad  \left\lvert{\Psi}\right\rangle _ {i} \sim \mathcal{O}(g^{i}), \\
I &\sim \mathcal{O}(g^{2}).
\end{align*}
$$

Where $I$ is some variable which will be define later, I put it here for the sake of completeness.

## Normal ordering with mass m

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

## Triviality of phi-fourth theory

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
## Perturbative Expansion of the Hamiltonian

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


# Loop expansion, semi-classical expansion and coupling expansion


To appreciate the importance of $\hbar$, just recall that in canonical quantization $[x,p]=i\hbar$, $\hbar$ enters explicitly in the commutation relation, providing the fundamental basis of quantum theory. This is also true in the case of quantum field theory. Furthermore, at each order of an expansion in $\hbar$, the physical symmetries (Lorentz invariance, $U(1)$ symmetry, etc.) must be satisfied, otherwise there will be some special value of $\hbar$ only at which the symmetries are preserved, which is just strange. 

In the unit where $c=1$, the Planck's constant $\hbar$ has the unit of action, or rather the action has the unit of $[\hbar]=ET$, where $E$ is the energy scale and $T$ the time. The textbook proof of the equivalence between *loop expansion* and *semi-classical expansion*, i.e. $\hbar$-expansion usually goes as follows. First write the partition function (with the source term) with $\hbar$:

$$
Z[J(x)] = \int \mathcal{D}\phi \, \exp \left\lbrace \frac{i}{\hbar} \int d^{d}x \, (\mathcal{L}+\hbar J \phi)  \right\rbrace  ,
$$

where $J=J(x)$ is the source term. Note that the source term has an $\hbar$ multiplied with it. Splitting the Lagrangian into free and interacting part (depends on the choice), we can extract out the interaction and put it in the front of the free partition function:

$$
Z[J] = \exp \left\lbrace \frac{i}{\hbar}\mathcal{L}_ {\text{int}}\left( \frac{1}{i} \frac{\delta}{\delta J} \right) \right\rbrace  Z_ {0}[J],
$$

where $\mathcal{L}_ {\text{int}}$ is the interacting Lagrangian and 

$$
Z_ {0}[J] = \int \mathcal{D}\phi \, \exp \left\lbrace \frac{i}{\hbar}\int d^{d}x\, (\mathcal{L}_ {0}+ \hbar J\phi)  \right\rbrace
$$

is the free partition function with the source. It can be integrated out in the closed form (for the level of rigorous for a physicist) to give

$$
Z_ {0}[J] = N \exp \left\lbrace - \frac{i}{2}\hbar \int d^{d}x d^{d}y \, J(x) \Delta_ {F}(x-y)J(y)   \right\rbrace,
$$

where $\Delta_ {F}$ is the Feynman propagator. It shows that each propagator contributes a factor of $\hbar$. 

Now, since each diagrammatic vertex is a result of a functional derivative $\frac{i}{\hbar }\mathcal{L}_ {\text{int}}\left( \frac{\delta}{\delta J} \right)$, each vertex contributes a factor of $\frac{1}{\hbar}$. Then, using some relations between the numbers of loops, propagators and vertices (it depends on the specific model), and **amputate the external legs**, it can usually be shown that: a general graph with $L$ loops is proportional to $\hbar^{L-1}$. Thus an expansion in the number of loops is also an expansion in powers of $\hbar$. 

- - -

It turns out that there are more than one way to assign $\hbar$-dependence for quantities such as the mass $m$, the coupling $g,\lambda$ etc. A criterion for the "right" choice is that, at $\hbar\to 0$ limit, the quantum theory agrees with the classical theory. As an example, Stanley Brodsky and Paul Hoyer in their [paper](https://arxiv.org/pdf/1009.2313.pdf) used the quantum mechanical harmonic oscillator as an example in Eq.(1). The gist is that, you can rescale $x$ to $x / \sqrt{ \hbar }$, then the propagator is formally independent of $\hbar$. However, this will change how we view distance, in the $\hbar\to 0$ limit, for a fixed distance $L$, the "length" measure will increase as $1 / \sqrt{ \hbar }$, hence we are going to smaller and smaller area. 

It is generally understood that each loop contribution to amplitudes is associated with one factor of $\hbar$. However, to fully define the $\hbar\to 0$ limit one need to specify the $\hbar$ dependence of various quantities in the Lagrangian as mentioned before, such as the field operator, the mass, the coupling, etc. This is not as straightforward as one might think, for $\hbar$ not only appears in the action $iS / \hbar$ but also appears in the Lagrangian. In Brodsky's paper mentioned above, the authors proposed a way to establish the $\hbar$ dependence such that the loop and $\hbar$ expansions are equivalent. We will go to more details in the following.

**First, regard $\hbar$ as a constant of nature with certain dimension, use $\hbar$ to make terms in the Lagrangian dimensionless.**

Again let's work with the assumption that $c = \epsilon_ {0} = 1$. Require $[S]=\hbar$, and $\alpha_ {s} = g^{2} / 4\pi \hbar$ is dimensionless, the latter implies that $[g]=\sqrt{ \hbar }=\sqrt{ ET }=\sqrt{ EL }$. From the self-energy of gluons $G_ {\mu \nu}G^{\mu \nu}$ where $G = \partial A - \partial A +ig / \hbar [A,A]$ we have  

$$
[A] = \sqrt{ \frac{E}{L} }.
$$

Similarly, in scalar QED model the classical electric charge $e$ and mass $m$ are divided by $\hbar$,

$$
S_ {\text{sQED} } = \int d^{4}x \, \left\lbrace \left\lvert D\phi \right\rvert ^{2}-\frac{m^{2} }{\hbar^{2} }\left\lvert \phi \right\rvert ^{2} \right\rbrace , \quad  D = \partial +i \frac{e}{\hbar }A.
$$

The boson field dimension 

$$
[\phi]=[A]= \sqrt{ \frac{E}{L} }.
$$

Fermion fields are more complicated, since they have no classical counterparts, their dimensions are convention-dependent. We will deal with fermions in a different note perhaps.

**Second step is to specify $\hbar$ dependence of all quantities appearing in the action.**

The choice made by Brodsky and Hoyer is as following:

$$
\widetilde{A}:= \frac{A}{\sqrt{ \hbar } },\quad \tilde{\phi}:= \frac{\phi}{\sqrt{ \hbar } }
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





# Changing to a new field operator

In the context of Lagrangian formalism and path integral, the perturbation method is relatively straightforward. For example, consider scalar $\phi^{4}$ theory with spontaneous symmetry breaking,

$$
\mathcal{L} = \frac{1}{2} (\partial_ {\mu}\phi)^{2} + \frac{1}{4} m^{2} + \frac{\lambda}{4}\phi^{4}.
$$
 
After the spontaneous symmetry breaking the vacuum is shifted from $\phi=0$ to $\phi= m / \sqrt{2\lambda}$. Now, we want to study the quantum fluctuation of real scalar field $\phi$ in the back ground of $\frac{m}{\sqrt{2}\lambda}$, what we do is we redefine the field operator as $\phi\to \frac{m }{\sqrt{ 2\lambda  }}+\phi'$, so that the new vacuum is obtained at $\phi'$ equals zero. We can now treat $\phi'$ as the fundamental quantum field. The small fluctuation about $\frac{m }{\sqrt{ 2\lambda  }}$ gives us the quantum effects via the partition function

$$
Z[J] = \int D\phi' \, \exp \left\lbrace iS[\phi']+i \int \phi' J   \right\rbrace ,
$$

but only about $\phi'\sim 0$. This partition function is perturbative about $\phi'=0$. 

- - -

How can we do the same thing but with Hamiltonian formalism? Anything that can be done with one formalism can equally be done in the other, it is just a matter of convenience. 

The problem is, in Hamiltonian formalism and working with $\hat{\mathcal{H}}$, perturbation methods are just not applicable, because the expectation value $\left\langle \phi \right\rangle := \left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle$ is by no means a small quantity, in fact $\left\langle \phi \right\rangle$ scales as $1 / \sqrt{ \lambda  }$, it actually blows up as $\lambda \to 0$. Then, similar to the Lagrangian case, we need to find some new field operator $\phi'$ such that $\left\langle \phi' \right\rangle=0$, then we can study the effects of fluctuation of $\left\langle \phi' \right\rangle$ perturbative in $\left\lvert{0^{+}}\right\rangle$ state. Turns out, $\phi'$ is connected to $\phi$ by a unitary transformation, and in the case at hand the unitary operator turns out to be the displacement operator $\mathcal{D}_ {v }$, where $v $ is some parameter to be determined. Note that we have replaced the arbitrary function $f(\vec{x})$ with a constant function $v$. We will explain it in the following.

Recall the defining property of displacement operator, $\mathcal{D}_ {f}^{\dagger}\phi \mathcal{D}_ {f}=\phi+f$. Thus if we let 

$$
\boxed{ 
v  = -\frac{m }{\sqrt{ 2\lambda  }}
}
$$

then (at least at leading order)

$$
\left\langle{0^{+}}\right\rvert \mathcal{D}_ {v }^{\dagger} \phi \mathcal{D}_ {v }\left\lvert{0^{+}}\right\rangle  
= \left\langle{0^{+}}\right\rvert \phi+v \left\lvert{0^{+}}\right\rangle  
= \frac{m }{\sqrt{ 2\lambda  }}-\frac{m }{\sqrt{ 2\lambda  }}=0,
$$

hence

$$
\boxed{ 
0=\left\langle{0^{+}}\right\rvert \phi'\left\lvert{0^{+}}\right\rangle, \quad  \phi':= \mathcal{D}_ {v }^{\dagger}\phi \mathcal{D}_ {v }.
}
$$

It inspires us to define a new Hamiltonian exactly in the same fashion, 

$$
\boxed{ 
\mathcal{H} := \mathcal{D}_ {v }^{\dagger} \hat{\mathcal{H}} \mathcal{D}_ {v }.
}
$$

We are interested in the spectrum of the Hamiltonian. The good news is that, a unitary transformation preserves the spectrum! Now, in order to study the quantum correction, instead of working with $\hat{H}$, $\phi$ and $\left\lvert{0^{+}}\right\rangle$ where perturbative methods fail, we can work with $H, \phi'$ and $\left\lvert{0^{+}}\right\rangle$ where $\phi'$ can be dealt with perturbatively. 

**Remarks.** Generally speaking, let $\mathcal{O}$ be any operator and $\left\lvert{\psi}\right\rangle$ its eigenstate. If $\mathcal{O}'=\mathcal{D}^{\dagger}\mathcal{O} \mathcal{D}$ is the unitary transformation of $\mathcal{O}$, then its eigenstate is $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$, not $\left\lvert{\psi}\right\rangle$. It may seem weird to some people to team up $\mathcal{O}'$ and $\left\lvert{\psi}\right\rangle$, not $\mathcal{O}'$ and $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$. In fact, it is exactly the point of our method! If we pair $\mathcal{O}'$ with $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$ it would be a trivial transform compare to working with $\mathcal{O}$ and $\left\lvert{\psi}\right\rangle$, we will not get anything new! Paring up $\mathcal{O}'$ and $\left\lvert{\psi}\right\rangle$ makes it possible for perturbation methods. However, since $\left\lvert{\psi}\right\rangle$ is not the eigen state of $\mathcal{O}'$, it indeed raise some problems, the first and foremost is that now $\mathcal{O}'$ is probably not diagonalized in $\left\lvert{\psi}\right\rangle$, we need to find a way to diagonalized it. In our current case, since the displacement operator only shifts the operators by a constant, it actually preserves the diagonalization, meaning if $\hat{\mathcal{H}}$ is diagonalized in $\left\lvert{\psi}\right\rangle$'s then $\mathcal{D}^{\dagger} \hat{\mathcal{H}}\mathcal{D}$ is also diagonalized in $\left\lvert{\psi}\right\rangle$'s. But for a generic $\mathcal{D}_ {f}$ with non-trivial $f$, this will no longer be true. That would be the topic for the other half the the note, after we introduce the kink solution. 

A comparison between displacement operator method to the case of regular functions might be helpful. 

|                                                                         Functions                                                                          |                                                                                                                                                                      QFT                                                                                                                                                                      |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                            A functions $f(x)$, a neighborhood about a special locus $x_ 0$ where the interesting things happen.                            |                                                                           A Hilbert space, a quantum state  $\left\lvert{\Psi}\right\rangle$ of interest represented by a functional $\left\langle \Psi(x),- \right\rangle$, and some operator $\mathcal{O}(\phi)$.                                                                           |
|                                             We want to study the function $f(x )$ about $x_ 0$ perturbatively,                                             |                                                                                                                We want to study the $\left\langle{\Psi}\right\rvert\mathcal{O}\left\lvert{\Psi}\right\rangle$ perturbatively,                                                                                                                 |
|                             but $x_ 0$ is not a small quantity so Maclaurin expansion (Taylor expansion at the origin) fails.                              |                                                                                                      but $\left\langle{\Psi}\right\rvert\phi \left\lvert{\Psi}\right\rangle=:f(x)$ is too large for $\phi$ to be treated perturbatively.                                                                                                      |
| **In a passive perspective, we shift the origin** to $x_ 0$, then small deviation from $x_ 0$ can now be studied using Maclaurin expansion perturbatively. | In a passive perspective, we shift the operators, especially the field operator $\phi$ since it is usually the building block of other operators. The expectation value of the new, shifted operator $\phi'$ should be zero, $\left\langle{\Psi}\right\rvert \phi'\left\lvert{\Psi}\right\rangle =0$. Now we can treat $\phi$ perturbatively. |
|              We are using a new, shifted coordinate system $\left\lbrace \overline{x} \right\rbrace$ to study the same old functions $f(x)$.               |                                                                                                  We are using shifted operators $\mathcal{D}^{\dagger}\mathcal{O}\mathcal{D}$ to study the same old states $\left\lvert{\Psi}\right\rangle$.                                                                                                  |

In summary, now $\mathcal{H}=\mathcal{D}^{\dagger}_ {v}\hat{\mathcal{H}}\mathcal{D}_ {v}$ is a operator-valued function of $\phi' = \mathcal{D}_ {v}^{\dagger} \phi \mathcal{D}_ {v}$, and $\phi'$ can be dealt with perturbatively.

- - -

#
