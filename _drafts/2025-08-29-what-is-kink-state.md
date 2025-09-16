---
layout: post
title: What is Kink State?
date: 2025-08-29
author: Baiyang Zhang
catalog: true
tags:
---

# Introduction

In vacuum sector, the zero-occupation state in the Fock representation coincides with the vacuum state, as a result of the following theorem:

**Theorem.** (Haag) In a quantum field theory in which
1. the 3d Euclidean group is implemented by unitary operators $U(a,R)$ under which the fields transform covariantly, e.g. for a scalar field $\phi$ we have $U(a,R)\phi(\vec{x},t)U^{\dagger}(a,R)=\phi(R\vec{x}+\vec{a},t)$;
2. The vacuum is the only Euclidean invariant state,
3. the fields obey ETCCR (equal-time canonical commutation relation) and their representation is a Fock irreducible representation.
Then the vacuum state and the Fock zero-particle state coincide. 

The proof essentially exploits the assumption that the vacuum is the only Euclidean invariant state. This theorem also validates the usage of notation $\left\lvert 0 \right\rangle$ as the free ground state.

Haag's theorem states that a single irreducible Fock representation is incompatible to non-trivial interaction. As a result, unlike in the case of finite degree of freedoms like in quantum mechanics, the total Hamiltonian with non-trivial interaction can not in principal be separated into a free part, which defines the Fock irreducible representation, and a comparatively small interaction, which can be regarded as a perturbation. In fact, as we will see late, at least with the presence of a kink solution, indeed there exists an extra subset of Hilbert space based on the kink state, and during the construction of such states, the data from interaction will inevitably mix with the free Hamiltonian.

Consider a classical source term $J(\vec{x})$ added to a (d+1) Dimensional real-scalar theory $\phi(\vec{x})$. We will work in the Schrodinger picture, where the canonical momentum is written as $\pi(\vec{x})$. The Hamiltonian is defined by 

$$
H = \int d^{d}x \,  \mathcal{N}_ {a,m}\left\lbrace \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi(\vec{x}))^{2} + \frac{m^{2}}{2} \phi^{2}(\vec{x})  + U(\phi) - J(\vec{x})\phi(\vec{x})+\text{c.t.}\right\rbrace ,
$$

where $\text{c.t.}$ stands for the counter terms, $-J\phi$ is the source term, $m$ is the renormalized mass term, $\mathcal{N}_ {a,m}$ is the normal ordering with respect to mass $m$ and annihilation operator $a_ {p}$, which expands the field operator in plane waves:

$$
\begin{align*}
\phi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega_ {p}}} \,  (a_ {p} e^{ i\vec{p}\cdot \vec{x} }+\text{h.c.}), \\
\pi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{\sqrt{\omega_ {p}}}{\sqrt{2}} \,  (-i a_ {p} e^{i\vec{p}\cdot \vec{x} }+\text{h.c.}),
\end{align*}
$$

where $\text{h.c.}$ stands for Hermitian conjugate. 

Not mathematically rigorous, but there are two "definitions" for vacuum state, 1) the zero-occupation state $\left\lvert 0 \right\rangle$ in the Fock representation, namely the state that is annihilated by $a_ {p}$ for all $p$; 2) the lowest energy state $\left\lvert \Omega \right\rangle$, which is the lowest energy state of the total Hamiltonian. When these two descriptions do not coincide, we say the vacuum is polarized. The energy difference is sometimes called the vacuum polarization energy. 

Ignore the counter terms and potential for now, 

$$
H_ {0} = \int d^{d}x \, \mathcal{N}_ {a} \left\lbrace \mathcal{H}_ {0} \right\rbrace ,\quad 
\mathcal{H}_ {0} = \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi)^{2} + \frac{m^{2}}{2} \phi^{2}.
$$

Expanding the fields into normal modes, after some manipulation we have 

$$
H_ {0}= \int \frac{d^{d}p}{(2\pi)^{d}} \, \omega_ {p} a_ {p} ^{\dagger} a_ {p} . 
$$

In other words, $H_ {0}$ is diagonalized by $a$ and $a^{\dagger}$, so there is no vacuum polarization. 

## Vacuum polarization by a classical source

Introducing the source term we have 

$$
H_ {0}[J] = \int d^{d}x \, \mathcal{N}_ {a} \left\lbrace \mathcal{H}_ {0}[J] \right\rbrace ,\quad 
\mathcal{H}_ {0}[J] = \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi)^{2} + \frac{m^{2}}{2} \phi^{2}-J\phi.
$$

The source $J(\vec{x})$ can be expanded as 

$$
J(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega _ {p} }} \,  (j_ {p} e^{ i\vec{p}\cdot \vec{x} }+j_ {p} ^\ast e^{ -i\vec{p}\cdot \vec{x} }),
$$

Note that $j_ {p}$ and $j_ {p}^\ast$ are c-number coefficients. In this decomposition we no-longer require $j_ {p}^\ast=j_ {-p}$, but we could always redefine them so that this relation is satisfied. To see it, notice that the Fourier decomposition of $J$ can be written as 

$$
J(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \,  \left[ \frac{1}{\sqrt{2\omega _ {p} }}(j_ {p} +j^\ast _ {-p}) \right] e^{ i\vec{p}\cdot \vec{x} },
$$

so what is important is the combined value of $j_ {p}+j^\ast_ {-p}$. Assume they don't satisfy the condition $j^\ast_ {p} = j_ {-p}$, but $j^\ast_ {p}-j_ {-p}=2z_ {p}$ instead, where $z_ {p}\in\mathbb{C}$. We can redefine $j'_ {p}= j_ {p}-z_ {p}$, $j_ {-p}^{'\ast} = j_ {-p}^{\ast}+z_ {p}$ so that $j'_ {p}=j^{'\ast}_ {-p}$. So we will always assume that the above relation is satisfied.

The source term reads

$$
\int d^{d}x \,  (-J\phi)= - \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\omega _ {p} }\,  (a_ {p} ^{\dagger} j_ {p} +a_ {p} j_ {p}^\ast )
$$

The Hamiltonian with a source now has extra terms involving $j_ {p}$. However it can be diagonalized by completing the squares, we have 

$$
H_ {0}[J] = \int \frac{d^{d}p}{(2\pi)^{d}} \,  \left\lbrace \omega _ {p}  \widetilde{a}_ {p} ^{\dagger}\widetilde{a}_ {p} - \frac{1}{\omega _ {p} ^{3}} j_ {p} ^\ast j_ {p}  \right\rbrace 
$$

where 

$$
\widetilde{a}_ {p} := a_ {p} - \omega _ {p} ^{-2} j_ {p}
$$

is the original annihilation operator shifted by a c-number. A shift in c-number would not affect the commutation relation, thus $\widetilde{a}$ also satisfies the equal-time canonical commutation relation.

The spectrum is shifted by a constant (vacuum polarization energy, VPE)

$$
-\int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\omega^{3}_ {p}}\,  \left\lvert j_ {p} \right\rvert ^{2}
$$

which is well defined as long as $j_ {p}$ decreases fast enough, otherwise we need to introduce an counterterm to cancel the divergence. The Hilbert space now should be chosen as the Fock representation corresponding to $\widetilde{a}_ {p}$, for example the ground state $\left\lvert 0_ {J} \right\rangle$ at the presence of a source term is no longer that annihilated by $a_ {p}$ for all $p$, but rather $\widetilde{a}_ {p}$ for all $p$:

$$
\widetilde{a}_ {p} \left\lvert 0_ {J} \right\rangle =0 \;\forall\;  p.
$$

Since 

$$
\widetilde{a}_ {p} \left\lvert 0_ {J} \right\rangle = 0=\left( a_ {p} -  \frac{j_ {p}}{\omega _ {p} ^{2}} \right) \left\lvert 0_ {J} \right\rangle \implies a_ {p} \left\lvert 0_ {J} \right\rangle = \frac{j_ {p} }{\omega^{2}_ {p} }\left\lvert 0_ {J} \right\rangle,
$$

$\left\lvert 0_ {J} \right\rangle$ is a *coherent state* for the $a$'s, sometimes called a Fock coherent state. 

$\left\lvert 0_ {J} \right\rangle$ can be obtained from $\left\lvert 0 \right\rangle$ via a version of *displacement* operation. To see that, first we need to define the smeared field operator $a(f)$ where $f\in L^{2}(\mathbb{R}^{d})$. Expanding $f(\vec{x})$ similar to the field operator,

$$
f(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega _ {p} }}\, (f _ {p} e^{ i\vec{p}\cdot \vec{x} }+f _ {p} ^{\ast }e^{ -i\vec{p}\cdot \vec{x} })
$$

Then we define the smeared ladder operators as 

$$
\boxed{ 
\begin{align*}
a^{\dagger}(f) :=& \int \frac{d^{d}p}{(2\pi)^{d}} \, f_ {p} a^{\dagger}_ {p}, \\
a(f) :=& \int \frac{d^{d}p}{(2\pi)^{d}} \, f_ {p}^\ast  a_ {p}.
\end{align*}
}
$$

Note $f_ {p}^\ast$ in the definition of $a(f)$. This definition might seem a bit weird at the beginning, but it has the benefit of notation-wise consistency: $a^{\dagger}(f)$ is indeed the hermitian conjugate of $a(f)$, $a^{\dagger}(f) = (a(f))^{\dagger}$. 

The commutation relation:

$$
\boxed{
[a(f),a^{\dagger}(g)] = \int \frac{d^{d}p}{(2\pi)^{d}} \,  f_ {p} ^\ast g_ {p} ,
} 
$$

particularly we have 

$$
\boxed{
[a(f),a^{\dagger}(f)] = \int \frac{d^{d}p}{(2\pi)^{d}} \, \left\lvert f_ {p}  \right\rvert ^{2}. 
} 
$$

Often times the smeared ladder operator are defined by the Fourier transformation of $f(\vec{x})$: (as adopted in the book by `Franco Strocchi`)

$$
a(f) := \int \frac{d^{d}p}{(2\pi)^{d}} \,   \widetilde{f}(\vec{p}) a_ {p} ,\quad  \widetilde{f}(\vec{p}) := \int d^{d}x \,  f(\vec{x}) e^{ -i \vec{p}\cdot \vec{x} }
$$

and similarly define the smeared creation operator $a^{\dagger}(f)$ 

$$
a^{\dagger}(f) := \int \frac{d^{d}p}{(2\pi)^{d}} \,   \widetilde{f}(\vec{p}) a^{\dagger}_ {p} 
$$

Then  $a^{\dagger}(f) \neq(a(f))^{\dagger}$. Direct evaluation shows that with the above convention $(a(f))^{\dagger}=a^{\dagger}(f_ {r})$ where $f_ {r}(\vec{x}):=f(-\vec{x})$ is the reflected function of $f$. That's why we won't use this convention here.

Define the smeared canonical operator against $f$ as 

$$
\pi(f) := \int d^{d}x \,  \pi(\vec{x}) f(\vec{x}),
$$

we have 

$$
-i \pi(f) = a^{\dagger}(f) - a(f).
$$

- - -

By the Baker-Campbell-Hausdorff formula, we have 

$$
e^{ -a^{\dagger}(f) } a_ {p} e^{ a^{\dagger}(f) } = a_ {p} +f_ {p} ,
$$

thus

$$
a_ {p} e^{ a^{\dagger}(f) }\left\lvert 0 \right\rangle = f_ {p}  e^{ a^{\dagger}(f) }\left\lvert 0 \right\rangle.
$$

However $e^{ a^{\dagger}(f) }$ is not a unitary operator, which means that when acting on a state it can change the norm of the state. To make it a unitary operator while preserving the desired properties, we can define a new operator:

$$
\mathcal{D}_ {f}:= e^{ -i\pi(f) } = e^{ a^{\dagger}(f) - a(f) }.
$$

$\mathcal{D}_ {f}$ is a unitary operator that satisfies 

$$
\mathcal{D}_ {f}^{\dagger} a_ {p}  \mathcal{D}_ {f} = a_ {p} + f_ {p}.
$$

$\mathcal{D}_ {f}$ can be used to create $\left\lvert 0_ {J} \right\rangle$ from $\left\lvert 0 \right\rangle$: 

$$
 \left\lvert 0_ {J} \right\rangle = \mathcal{D}_ {J'} \left\lvert 0 \right\rangle, 
$$

where 

$$
J'(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega _ {p} }} \, (j'_ {p} e^{ i\vec{p}\cdot \vec{x} }+\text{h.c.}), \quad  j'_ {p} := \frac{j_ {p} }{\omega _ {p} ^{2}}. 
$$

- - -

The Euclidean symmetry $E(\vec{a},R)$ is implemented by a unitary operator $U(\vec{a},R)$, where $\vec{a}$ is the translation vector and $R$ the rotation. Euclidean group is a semidirect product of translation $T(\vec{a})$ and rotation $R$, $E=T\rtimes R$. Let's focus on translation for now. 

Under translation the field operator transforms as $T(\vec{a})\phi(\vec{x})T^{-1}(\vec{a})=\phi(\vec{x}+\vec{a})$, hence the original ladder operator transforms as $T(\vec{a})a_ {p}T^{-1}(\vec{a})=a_ {p} e^{ i\vec{p}\cdot \vec{a} }$, i.e. $a_ {p}$ acquires a phase under translation. Similarly for $j_ {p}$. Since $\widetilde{a}=a-{j}/{\omega^{2}_ {p}}$, we have $T(\vec{a})\,\widetilde{a}_ {p}\,T^{-1}(\vec{a})=\widetilde{a}_ {p}e^{ i\vec{p}\cdot \vec{a} }$.

Since the source term explicitly breaks the Euclidean symmetry, a natural question is how does $T(\vec{a})$ acting on $\left\lvert 0_ {J} \right\rangle$ affects it? Does $\left\lvert 0_ {J} \right\rangle$ just acquires a phase as well? Direct calculation shows that 

$$
T(\vec{a}) \left\lvert 0_ {J} \right\rangle = e^{ i\vec{p}\cdot \vec{a} }\left\lvert 0_ {J} \right\rangle.
$$

- - -

An important question is, can the polarized (or displaced) vacuum $\left\lvert 0_ {J} \right\rangle$ be expanded in original Fock states? Starting from the simplest case, let's try to calculate the superposition between vacuum states with and without source:

$$
\begin{align*}
\left\langle 0 \middle\vert 0_ {J} \right\rangle  =& \left\langle 0 \right\rvert\exp \left\lbrace -i\pi(J') \right\rbrace \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert \exp \left\lbrace a^{\dagger}(J') - a(J') \right\rbrace \left\lvert 0 \right\rangle\\
=& \left\langle 0 \right\rvert \sum_ {n\in \mathbb{N}} \frac{1}{n!}(a^{\dagger}(J')-a(J')^{n})\left\lvert 0 \right\rangle,
\end{align*}
$$

where the $n$-th term can be calculated via Wick's theorem,

$$
\text{string of }a,a^{\dagger} = \mathcal{N}_ {a}\left\lbrace \text{all possible contractions} \right\rbrace.
$$

The vev is nonzero only for $n$ even, 

$$
\left\langle 0 \right\rvert(a^{\dagger}(f)-a(f))^{n} \left\lvert 0 \right\rangle= [a(f),a(f)^{\dagger}] (n-1)!! = (n-1)!! S_ {f} ^{n}
$$

where 

$$
S_ {f} :=- \int \frac{d^{d}p}{(2\pi)^{d}} \, \left\lvert f_ {p}  \right\rvert ^{2} .
$$

Hence,

$$
\left\langle 0 \middle\vert 0_ {J} \right\rangle  = \sum_ {n\in 2\mathbb{N}} \frac{(n-1)!!}{n!} (S_ {J'})^{n} = e^{ S_ {J'}^{2}/2 }.
$$

where 

$$
S_ {J'} =- \int \frac{d^{d}p}{(2\pi)^{d}} \,  \frac{\left\lvert j_ {p}\right\rvert ^{2}}{\omega _ {p} ^{4}}.
$$

However, without a cutoff, the integral in the definition of $S_ {j'}$ might be divergent. For example, consider a delta-function source, $J(\vec{x})=\delta(\vec{x})$, then $j_ {p}\sim \sqrt{\omega _ {p}}$ and $S_ {j'}=-\infty$ for $d\geq 3$. To be continued.






# The setups

A passive perspective is adopted in this note, meaning that states are all independent of the frames chosen, a change a frame will unitarily change the field operator, which is used as a perturbative "probe" for various states. 


# Appendix

The Parseval's identity with our convention: for a real $L^{2}$ function $f(\vec{x})$,

$$
\int d^{d}x \, f(\vec{x})^{2}  = \int \frac{d^{d}p}{(2\pi)^{d}} \, \frac{2}{\omega _ {p} }\left\lvert f_ {p}  \right\rvert ^{2}. 
$$
