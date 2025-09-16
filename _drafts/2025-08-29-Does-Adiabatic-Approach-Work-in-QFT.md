---
layout: post
title: Does-Adiabatic-Approach-Work-in-QFT
date: 2025-08-29
author: Baiyang Zhang
catalog: true
tags:
---
## Coleman's approach

Starting with Coleman's model 2,

$$
H = \int d^{3}x \,  \frac{1}{2}(\pi^{2}+(\partial _ {i}  \phi)^{2})+ \frac{\mu^{2}}{2} \phi^{2} + g\rho(\vec{x})\phi(x)
$$

where $\pi$ is the canonical momentum, and the density function $\rho(\vec{x})$ is a function of space only, independent of time. This means that the interaction doesn't turn off in the far past and far future. The standard lore is to insert an adiabatic switching function $f(t)$, 

$$
H_ {I}(t) = g \int d^{3}x \, \phi(x) \rho(\vec{x})\to  f(t) H_ {I}.
$$

$\phi$ is in the interaction picture, which means that it is the free field. $f(t) =1$ for $-T / 2\leq t\leq T /2$, and $f(t)=0$ for $T< - T /2-\Delta$ and $T > T / 2+\Delta$. It goes to zero during a time interval $\Delta$ smoothly (adiabatically). 

To make sure that 

$$
\lim_ { T \to \infty } \left\langle 0 \right\rvert U\left( T/2, - T/2 \right) \left\lvert 0 \right\rangle=1,
$$

counter terms are needed. 

First, some clarifications on notations. $\left\lvert 0 \right\rangle$ is the free vacuum that is annihilated by the free Hamiltonian, $\left\lvert 0_ {P} \right\rangle$ or $\left\lvert 0 \right\rangle_ {P}$ is the physical vacuum which is an eigenstate of the full Hamiltonian $H$ without the adiabatic function, 

$$
H \left\lvert 0_ {P} \right\rangle = E_ {0} \left\lvert 0_ {P} \right\rangle,
$$

where $E_ {0}$ is the physical ground energy. 

The argument given by Coleman is that, in the far past, when $t < -T / 2-\Delta$, $f(t)=0$ and the ground state is $\left\lvert 0 \right\rangle$, the free ground state or bare ground state. As time goes from $-T / 2-\Delta$ to $-T /2$, we adiabatically turn on the interaction, by the adiabatic theorem, we expect $\left\lvert 0 \right\rangle$ to smoothly go to $\left\lvert 0_ {P} \right\rangle$, perhaps up to some phases. 

The extra phase can be eliminated by a counter term, $H_ {I} \to H_ {I} +a$. The counter term also makes the interacting ground state energy to be zero. Using Wick diagram (by Coleman's definition, Feynman diagram is for computing the S-matrix, Wick diagram is for computing operators), it can be shown that $\left\langle 0 \right\rvert S\left\lvert 0 \right\rangle=0$. The classic source we introduced at the beginning of the note can not produce any on-shell mesons since $\widetilde{\rho}(p)=0$ for on-shell $p^{\mu}$. $\rho(\vec{x})$ can only transfer momentum, not energy.

- - -

The ground state is more interesting than the S-matrix. In the $T\to\infty$ limit, the ground state energy reads

$$
E_ {0} = - \frac{g^{2}}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{\left\lvert \widetilde{\rho}(\vec{p}) \right\rvert ^{2}}{\left\lvert \vec{p} \right\rvert^{2}+\mu^{2} } 
$$

where $\widetilde{\rho}$ is the Fourier transformation of $\rho(\vec{x})$, the specific convention can be found in a different blog of mine.

The minus sign means that, adding the interaction $g\rho \phi$ to the free Hamiltonian will decrease the energy. This is a general result, adding an extra term $V$ that has zero vev to the Hamiltonian $H_ {0}$ will always decrease the energy. That is because, let $\left\lvert E_ {0} \right\rangle$ be the ground state of $H_ {0}$, adding $V$ will make $\left\lvert E_ {0} \right\rangle$ a t rial state, the new ground state will be something else $\left\lvert E_ {0}' \right\rangle$. $E_ {0}'$ must be smaller than $E_ {0}$ otherwise it won't be a ground state.

Coleman also calculated the ground state wave function, an expansion of the physical vacuum $\left\lvert 0_ {P} \right\rangle$ in terms into the basis states $\left\lvert \vec{p}_ {1},\cdots,\vec{p}_ {n} \right\rangle$, eigenstates of the free Hamiltonian $H_ {0}$. By the asymptotic assumption, 

$$
\left\lvert 0_ {P} \right\rangle = U(\infty,-\infty) \left\lvert 0 \right\rangle.
$$

Choose the adiabatic function to be 

$$
f(t) = \begin{cases}
e^{ \epsilon t }  & t<0 , \\
0  &  t\geq 0 .
\end{cases}
$$

The final result is 

$$
\left\langle \vec{p}_ {1},\cdots, \vec{p}_ {n} \right\rvert U_ {I}(\infty,-\infty)\left\lvert 0 \right\rangle = e^{ 1/2 (-\alpha+i\beta) } h^\ast (\vec{p}_ {1})\cdots h^\ast (\vec{p}_ {n}),
$$

where 

$$
\begin{align*}
h(\vec{p}) =& \frac{-ig\widetilde{\rho}(\vec{p})\widetilde{f}(\omega _ {p} )}{(2\pi)^{3/2}\sqrt{2\omega_ {p}}}, \widetilde{f}(\omega _ {p} ) \to  \frac{i}{\omega _ {p} },\\
\alpha =& \int d^{3}p \, \left\lvert h(\vec{p}) \right\rvert   \to  g^{2} \int \frac{d^{3}p}{(2\pi)^{3}2\omega _ {p} ^{3}} \, \left\lvert \widetilde{\rho}(\vec{p}) \right\rvert ^{2}. 
\end{align*}
$$

The Fourier transform for $f(t)$ is that 

$$
\widetilde{f}(\omega _ {p} ) = \int dt \, e^{ -i\omega _ {p} t }f(t) = \frac{i}{\omega _ {p} } ,
$$

where we have discarded an $\epsilon$ term.

If $f(t)=1$, then $\widetilde{f}(\omega _ {p})=\delta(\omega _ {p})2\pi$, and $h(\vec{p})\equiv {0}$. Also, if $\rho(\vec{x})=\delta(\vec{x})$, namely for point particles, then $\alpha$ blows up. Physically, $\alpha=\left\langle N \right\rangle$, the expected number of bare mesons.

Next we use a different method to see if the adiabatic assumption really works.

## A different method

Let's try to diagonalize the Hamiltonian directly.

Go to the Schrodinger picture where fields are function of $\vec{x}$ only. Introduce the normal ordering, the Hamiltonian is defined by 

$$
H = \int d^{3}x \,  \mathcal{N}_ {a,m}\left\lbrace \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi(\vec{x}))^{2} + \frac{\mu^{2}}{2} \phi^{2}(\vec{x})  + U(\phi) + g \rho(\vec{x})\phi(\vec{x})\right\rbrace ,
$$

where $\mathcal{N}_ {a,m}$ is the normal ordering with respect to mass $\mu$ and annihilation operator $a_ {p}$, which expands the field operator in plane waves:

$$
\begin{align*}
\phi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega_ {p}}} \,  (a_ {p} e^{ i\vec{p}\cdot \vec{x} }+\text{h.c.}), \\
\pi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{\sqrt{\omega_ {p}}}{\sqrt{2}} \,  (-i a_ {p} e^{i\vec{p}\cdot \vec{x} }+\text{h.c.}),
\end{align*}
$$

where $d=3$ in our case and $\text{h.c.}$ stands for Hermitian conjugate. 

Recall that there are two "definitions" for vacuum state, 1) the zero-occupation state $\left\lvert 0 \right\rangle$ in the Fock representation, namely the state that is annihilated by $a_ {p}$ for all $\vec{p}$; 2) the lowest energy state $\left\lvert \Omega \right\rangle$, which is the lowest energy state of the total Hamiltonian. When these two descriptions do not coincide, we say the vacuum is polarized. The energy difference is sometimes called the vacuum polarization energy. 

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








# Appendix

The canonical momentum in Schrodinger picture:

$$
\pi(\vec{x}) = -\int \frac{d^{3}p}{(2\pi)^{3}} \, \sqrt{\frac{\omega _ {p} }{2}}(a_ {p}e^{ i\vec{p}\cdot \vec{x} } -a^{\dagger}_ {p} e^{ -i\vec{p}\cdot \vec{x} }) .
$$

The CCR (canonical commutation relation) reads

$$
\begin{align*}
[a_ {k} ,a^{\dagger}_ {p} ] =& (2\pi)^{3} \delta^{3}(\vec{k}-\vec{p}), \\
[\phi(\vec{x}),\pi(\vec{y},)] =& i\delta^{3}(\vec{x}-\vec{y}).
\end{align*}
$$

The Parseval's identity with our convention: for a real $L^{2}$ function $f(\vec{x})$,

$$
\int d^{d}x \, f(\vec{x})^{2}  = \int \frac{d^{d}p}{(2\pi)^{d}} \, \frac{2}{\omega _ {p} }\left\lvert f_ {p}  \right\rvert ^{2}. 
$$
