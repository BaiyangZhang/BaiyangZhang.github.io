---
layout: post
title: Does Adiabatic Assumption Work?
date: 2025-09-21
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

The extra phase can be eliminated by a counter term, $H_ {I} \to H_ {I} +a$. The counter term also makes the interacting ground state energy to be zero. Using Wick diagram (by Coleman's definition, Feynman diagram is for computing the S-matrix, Wick diagram is for computing operators), it can be shown that $\left\langle 0 \right\rvert S\left\lvert 0 \right\rangle=0$. The classic source we introduced at the beginning of the note can not produce any on-shell mesons since $\tilde{\rho}(p)=0$ for on-shell $p^{\mu}$. $\rho(\vec{x})$ can only transfer momentum, not energy.

- - -

The ground state is more interesting than the S-matrix. In the $T\to\infty$ limit, the ground state energy reads

$$
E_ {0} = - \frac{g^{2}}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{\left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2}}{\left\lvert \vec{p} \right\rvert^{2}+\mu^{2} } 
$$

where $\tilde{\rho}$ is the Fourier transformation of $\rho(\vec{x})$, the specific convention can be found in a different blog of mine.

The minus sign means that, adding the interaction $g\rho \phi$ to the free Hamiltonian will decrease the energy. This is a general result, adding an extra term $V$ that has zero vev to the Hamiltonian $H_ {0}$ will always decrease the energy. That is because, let $\left\lvert E_ {0} \right\rangle$ be the ground state of $H_ {0}$, adding $V$ will make $\left\lvert E_ {0} \right\rangle$ a trial state, the new ground state will be something else $\left\lvert E_ {0}' \right\rangle$. $E_ {0}'$ must be smaller than $E_ {0}$ otherwise it won't be a ground state.

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
h(\vec{p}) =& \frac{-ig\tilde{\rho}(\vec{p})\tilde{f}(\omega _ {p} )}{(2\pi)^{3/2}\sqrt{2\omega_ {p}}}, \tilde{f}(\omega _ {p} ) \to  \frac{i}{\omega _ {p} },\\
\alpha =& \int d^{3}p \, \left\lvert h(\vec{p}) \right\rvert   \to  g^{2} \int \frac{d^{3}p}{(2\pi)^{3}2\omega _ {p} ^{3}} \, \left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2}. 
\end{align*}
$$

The Fourier transform for $f(t)$ is that 

$$
\tilde{f}(\omega _ {p} ) = \int dt \, e^{ -i\omega _ {p} t }f(t) = \frac{i}{\omega _ {p} } ,
$$

where we have discarded an $\epsilon$ term.

If $f(t)=1$, then $\tilde{f}(\omega _ {p})=\delta(\omega _ {p})2\pi$, and $h(\vec{p})\equiv {0}$. Also, if $\rho(\vec{x})=\delta(\vec{x})$, namely for point particles, then $\alpha$ blows up. Physically, $\alpha=\left\langle N \right\rangle$, the expected number of bare mesons.

Next we use a different method to see if the adiabatic assumption really works.

## A different method

Let's try to diagonalize the Hamiltonian directly.

Go to the Schrodinger picture where fields are function of $\vec{x}$ only. Introduce the normal ordering, the Hamiltonian is defined by 

$$
H = \int d^{3}x \,  \mathcal{N}_ {a,\mu}\left\lbrace \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi(\vec{x}))^{2} + \frac{\mu^{2}}{2} \phi^{2}(\vec{x})  + U(\phi) + g \rho(\vec{x})\phi(\vec{x})\right\rbrace ,
$$

where $\mathcal{N}_ {a,\mu}$ is the normal ordering with respect to mass $\mu$ and annihilation operator $a_ {p}$, which expands the field operator in plane waves:

$$
\begin{align*}
\phi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega_ {p}}} \,  (a_ {p} e^{ i\vec{p}\cdot \vec{x} }+\text{h.c.}), \\
\pi(\vec{x}) &= \int \frac{d^{d}p}{(2\pi)^{d}} \frac{\sqrt{\omega_ {p}}}{\sqrt{2}} \,  (-i a_ {p} e^{i\vec{p}\cdot \vec{x} }+\text{h.c.}),
\end{align*}
$$

in our case $d=3$ and $\text{h.c.}$ stands for Hermitian conjugate. 

Recall that there are two "definitions" for vacuum state, 1) the zero-occupation state $\left\lvert 0 \right\rangle$ in the Fock representation, namely the state that is annihilated by $a_ {p}$ for all $\vec{p}$; 2) the lowest energy state $\left\lvert \Omega \right\rangle$, which is the lowest energy state of the total Hamiltonian. When these two descriptions do not coincide, we say the vacuum is polarized. The energy difference is sometimes called the vacuum polarization energy. 

We have Ignored the counter terms. The free Hamiltonian reads

$$
H_ {0} = \int d^{d}x \, \mathcal{N}_ {a} \left\lbrace \mathcal{H}_ {0} \right\rbrace ,\quad 
\mathcal{H}_ {0} = \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi)^{2} + \frac{\mu^{2}}{2} \phi^{2}.
$$

Expanding the fields into normal modes, after some manipulation we have 

$$
H_ {0}= \int \frac{d^{d}p}{(2\pi)^{d}} \, \omega_ {p} a_ {p} ^{\dagger} a_ {p} . 
$$

In other words, $H_ {0}$ is diagonalized by $a$ and $a^{\dagger}$, so there is no vacuum polarization. 

Include the source term, we have 

$$
H = \int d^{d}x \, \mathcal{N}_ {a} \left\lbrace \mathcal{H} \right\rbrace ,\quad 
\mathcal{H} = \frac{1}{2}\pi^{2}(\vec{x}) + \frac{1}{2}(\nabla \phi)^{2} + \frac{\mu^{2}}{2} \phi^{2}+g\rho\phi.
$$

The source $\rho(\vec{x})$ has Fourier transform 

$$
\rho(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}} \, \tilde{\rho}(\vec{p}) e^{ i\vec{p}\cdot \vec{x} },\quad  \tilde{\rho}(\vec{p})= (j_ {p} +j^\ast _ {-p}) .
$$

Note that $j_ {p}$ and $j_ {p}^\ast$ are c-number coefficients, since $\rho$ is assumed to be a classical source. In this decomposition it is not mandatory that $j_ {p}^\ast=j_ {-p}$, but we could always shift them so that this relation is satisfied. To see it, notice that since $\rho$ is real, we have $\tilde{\rho}(\vec{p})=\tilde{\rho}^\ast(-\vec{p})$, which implies that the combined value of $j_ {p}+j^\ast_ {-p}$ satisfy the relation that under $p\leftrightarrow-p$ it requires a complex conjugate. This condition is trivially satisfied no matter if $j_ {p}=j_ {-p}^\ast$ or not. Assume they don't satisfy the condition $j^\ast_ {p} = j_ {-p}$, but $j^\ast_ {p}-j_ {-p}=2z_ {p}$ instead, where $z_ {p}\in\mathbb{C}$. We can redefine $j'_ {p}= j_ {p}-z_ {p}$, $j_ {-p}^{'\ast} = j_ {-p}^{\ast}+z_ {p}$ so that $j'_ {p}=j^{'\ast}_ {-p}$. Without loss of generality, we can always assume that the above relation is satisfied. In the following we will assume that $j_ {p}=j^\ast_ {-p}$.

The source term reads

$$
\int d^{d}x \,  (g\rho\phi)=  g\int \frac{d^{d}p}{(2\pi)^{d}} \frac{1}{\sqrt{2\omega _ {p}}}\, ( a_ {p} \tilde{\rho}(\vec{p})^\ast + a_ {p} ^{\dagger} \tilde{\rho}(\vec{p}) ).
$$

The Hamiltonian with a source now has extra terms involving $\tilde{\rho}(\vec{p})$. It can be diagonalized by completing the squares, we get

$$
H = \int \frac{d^{d}p}{(2\pi)^{d}} \,  \left\lbrace \omega _ {p}  \tilde{a}_ {p} ^{\dagger}\tilde{a}_ {p} - \frac{g^{2}}{2\omega _ {p} ^{2}} \left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2}  \right\rbrace 
$$

where 

$$
\tilde{a}_ {p} := a_ {p} + \frac{g}{\omega _ {p} \sqrt{2\omega _ {p} }}\tilde{\rho}(\vec{p}).
$$

The minus sign of the second term in the above-above equation agrees with the fact the the introduced source term should decrease the energy. $\tilde{a}_ {p}$ is the "free" annihilation operator shifted by a c-number. A shift in c-number would not affect the commutation relation, hence $\tilde{a}$ also satisfies the equal-time canonical commutation relation. The energy of the new ground state with source is

$$
E_ {0}= - \frac{g^{2}}{2} \int \frac{d^{d}p}{(2\pi)^{d}} \, \frac{1}{\omega _ {p} ^{2}} \left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2},
$$

Exactly in agreement with Coleman's result, which is well defined as long as the integral over $\tilde{\rho}$ squared is finite, otherwise we need to introduce an counterterm to cancel the divergence. Which is not mentioned by Coleman at all is that, now the Hilbert space should be chosen as the Fock representation corresponding to $\tilde{a}_ {p}$, for example the ground state $\left\lvert 0_ {\rho} \right\rangle$ at the presence of a source term is no longer that annihilated by $a_ {p}$ for all $p$, but rather $\tilde{a}_ {p}$ for all $p$:

$$
\tilde{a}_ {p} \left\lvert 0_ {\rho} \right\rangle =0 \quad \forall\;  p.
$$

Since 

$$
\tilde{a}_ {p} \left\lvert 0_ {\rho} \right\rangle = 0=\left( a_ {p} + \frac{g}{\omega _ {p} \sqrt{2\omega _ {p} }}\tilde{\rho}(\vec{p}) \right) \left\lvert 0_ {\rho} \right\rangle \implies 
\boxed{ a_ {p} \left\lvert 0_ {\rho} \right\rangle =  -\frac{g}{\omega _ {p} \sqrt{2\omega _ {p} }}\tilde{\rho}(\vec{p}) \left\lvert 0_ {\rho} \right\rangle},
$$

$\left\lvert 0_ {\rho} \right\rangle$ is a *coherent state* from the perspective of the original annihilation operator $a$'s, it is sometimes called a `Fock coherent state`. 

- - -

$\left\lvert 0_ {\rho} \right\rangle$ is constructed from $\left\lvert 0 \right\rangle$ via *displacement* operation. To see that, first we need to define the `smeared ladder operator` $a(f)$ where $f\in L^{2}(\mathcal{D})$ on some measurable domain $\mathcal{D}$. As usual, the Fourier expansion of $f(\vec{x})$ reads

$$
f(\vec{x}) = \int \frac{d^{d}p}{(2\pi)^{d}}\, \tilde{f}(\vec{p})e^{ i\vec{p}\cdot \vec{x} },
$$

note that in the plane wave expansion of fields there is a factor of $\frac{1}{\sqrt{2\omega _ {p} }}$, however it doesn't make any sense to include that factor in the expansion of $f(\vec{x})$, since $f$ is just a function, why should we introduce a mas parameter $m$ in the first place? Without mass you can't define $\omega _ {p}$. 

Define the smeared ladder operators as (in agreement with `Franco Strocchi`)

$$
\boxed{ 
\begin{align*}
a^{\dagger}(f) :=& \int \frac{d^{d}p}{(2\pi)^{d}} \, \tilde{f}(\vec{p}) a^{\dagger}_ {p}, \\
a(f) :=& \int \frac{d^{d}p}{(2\pi)^{d}} \, \tilde{f}(\vec{p})  a_ {p}.
\end{align*}
}
$$

This smear happens in the momentum space. Caution, $a^{\dagger}(f)$ is **not** the Hermitian conjugate of $a(f)$, $a^{\dagger}(f) \neq (a(f))^{\dagger}$. 

The commutation relation:

$$
\begin{align*}
[a(f),a^{\dagger}(g)] =& \int \frac{d^{d}p}{(2\pi)^{d}} \,  \tilde{f}(\vec{p}) \tilde{g}(\vec{p})=\int d^{d}x \,  f(\vec{x})g(\vec{x}), \\
[a(f),(a(g))^{\dagger}] =& \int \frac{d^{d}p}{(2\pi)^{d}} \,  \tilde{f}(\vec{p}) \tilde{g}(\vec{p})^\ast =\int d^{d}x \,  f(\vec{x})g(\vec{x})^\ast ,
\end{align*}
$$

particularly we have 

$$
\boxed{
[a(f),(a(f))^{\dagger}] = \int \frac{d^{d}p}{(2\pi)^{d}} \, \left\lvert \tilde{f}(\vec{p})  \right\rvert ^{2}. 
} 
$$

Define the canonical momentum smeared against $f$ as

$$
\pi(f) := \int d^{d}x \,  \pi(\vec{x}) f(\vec{x}),
$$

- - -

By the Baker-Campbell-Hausdorff formula, we have 

$$
e^{ -a^{\dagger}(f) } a_ {p} e^{ a^{\dagger}(f) } = a_ {p} +\tilde{f}(\vec{p}),
$$

thus the state $\exp (a^{\dagger}(f)) \left\lvert 0 \right\rangle$ has a peculiar property:

$$
a_ {p} e^{ a^{\dagger}(f) }\left\lvert 0 \right\rangle = \tilde{f}(\vec{p})  e^{ a^{\dagger}(f) }\left\lvert 0 \right\rangle.
$$

However, $e^{ a^{\dagger}(f) }$ is not a unitary operator, which means that when acting on a state it can change the norm of it. To make it a unitary operator while preserving the desired properties, we can define a new operator:

$$
\mathcal{D}_ {f}:= e^{ -i\pi(f) },\quad \pi(f) = \int \frac{d^{3}p}{(2\pi)^{3}} \,  \sqrt{\frac{\omega _ {p} }{2}} (-ia_ {p} \tilde{f}(\vec{p})^\ast +\text{h.c.}).
$$

$\mathcal{D}_ {f}$ is a unitary operator that satisfies 

$$
\mathcal{D}_ {f}^{\dagger} a_ {p}  \mathcal{D}_ {f} = a_ {p} -\sqrt{\frac{\omega _ {p} }{2}}\tilde{f}(\vec{p}).
$$

Then maybe $\mathcal{D}_ {f}$ can be used to create $\left\lvert 0_ {\rho} \right\rangle$ from $\left\lvert 0 \right\rangle$: 

$$
 \left\lvert 0_ {\rho} \right\rangle = \mathcal{D}_ {k(\vec{x})} \left\lvert 0 \right\rangle, 
$$

where 

$$
\tilde{k}(\vec{p})= - \frac{g}{\omega _ {p} ^{2}}\tilde{\rho}(\vec{p}).
$$

Looks like we can't just insert the source function with coupling $g\rho$ into the displacement and hope it gives the correct ground state.

- - -

The Euclidean symmetry $E(\vec{a},R)$ is implemented by a unitary operator $U(\vec{a},R)$, where $\vec{a}$ is the translation vector and $R$ the rotation. Euclidean group is a semidirect product of translation $T(\vec{a})$ and rotation $R$, $E=T\rtimes R$. Let's focus on the translation for now. 

Under translation the field operator transforms as $T(\vec{a})\phi(\vec{x})T^{-1}(\vec{a})=\phi(\vec{x}+\vec{a})$, hence the original ladder operator transforms as $T(\vec{a})a_ {p}T^{-1}(\vec{a})=a_ {p} e^{ i\vec{p}\cdot \vec{a} }$, i.e. $a_ {p}$ acquires a phase under translation. Similarly for $\tilde{\rho}(\vec{p})$.

Since the source term explicitly breaks the Euclidean symmetry, a natural question is how does $T(\vec{a})$ affect $\left\lvert 0_ {\rho} \right\rangle$? Does $\left\lvert 0_ {\rho} \right\rangle$ just acquires a phase as well? Direct calculation shows that 

$$
T(\vec{a}) \left\lvert 0_ {\rho} \right\rangle = e^{ i\vec{p}\cdot \vec{a} }\left\lvert 0_ {\rho} \right\rangle.
$$

- - -

An important question is, can the polarized (or displaced) vacuum $\left\lvert 0_ {\rho} \right\rangle$ be expanded in original Fock states? According to the calculation did by Coleman, the answer should be yes, let's try to verify that. Starting from the simplest case, let's try to calculate the superposition between vacuum states with and without source:

$$
\begin{align*}
\left\langle 0 \middle\vert 0_ {\rho} \right\rangle  
=& \left\langle 0 \right\rvert\exp \left\lbrace -i\pi(k) \right\rbrace \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert \exp \left\lbrace K - K^{\dagger}\right\rbrace \left\lvert 0 \right\rangle
\end{align*}
$$

where

$$
K := g\int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{1}{\omega _ {p} \sqrt{2\omega _ {p} }} a_ {p} \tilde{p}(\vec{p})^\ast.
$$

Using the BCH formula (provided $[X,Y]$ commutes with both $X$ and $Y$)

$$
e^{ X+Y } = e^{ X }e^{ Y }e^{ -1/2 [X,Y]}
$$

and 

$$
[K,K^{\dagger}] =g^{2} \int \frac{d^{3}p}{(2\pi)^{3}}\, \frac{1}{2\omega _ {p} ^{3}}   \left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2} =: \beta,
$$

we have 

$$
\begin{align*}
\left\langle 0 \middle\vert 0_ {\rho} \right\rangle  
=& \left\langle 0 \right\rvert\exp \left\lbrace -i\pi(k) \right\rbrace \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert \exp \left\lbrace K - K^{\dagger}\right\rbrace \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert \exp \left\lbrace -K^{\dagger}+K\right\rbrace \left\lvert 0 \right\rangle \\
=& e^{ -\frac{1}{2} \beta }\left\langle 0 \right\rvert e^{ A^{-} } e^{ A^{+} }   \left\lvert 0 \right\rangle \\
=& e^{ -\frac{1}{2}\beta}.
\end{align*}
$$

It means that if $\tilde{\beta}(\vec{p})$ decreases fast enough, then $\beta$ is finite and so is the superposition between the two ground states! Otherwise, the superposition vanishes. **The $g\to 0$ limit is well defined.**

The above result can also be obtained via Wick's theorem,

$$
\text{string of }a,a^{\dagger} = \mathcal{N}_ {a}\left\lbrace \text{all possible contractions} \right\rbrace.
$$

The vev is nonzero only for even $n$, with formula similar to

$$
\left\langle 0 \right\rvert(a^{\dagger}(f)-a(f))^{n} \left\lvert 0 \right\rangle= [a(f),a(f)^{\dagger}] (n-1)!! = (n-1)!! S_ {f} ^{n}
$$

where 

$$
S_ {f} :=- \int \frac{d^{d}p}{(2\pi)^{d}} \, \left\lvert \tilde{f}(\vec{p})  \right\rvert ^{2} .
$$

- - -

Next we move on to calculate the wave function $\left\lvert 0_ {\rho} \right\rangle$, starting with $\left\langle \vec{p} \middle\vert0_ {\rho} \right\rangle$. We have

$$
\begin{align*}
\left\langle \vec{p} \middle\vert 0_ {\rho} \right\rangle  =& \left\langle 0 \right\rvert a_ {p} e^{ -i\pi(f) } \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert a_ {p}e^{-K^{\dagger}}e^{K} e^{-\beta/2} \left\lvert 0 \right\rangle \\
=& \left\langle 0 \right\rvert ([a_ {p} ,e^{-K^{\dagger}}]+e^{K^{\dagger}}a_ {p}) e^{K} e^{-\beta/2}\left\lvert 0 \right\rangle\\
=& \left\langle 0 \right\rvert [a_ {p} ,e^{-K^{\dagger}}] e^{K} e^{-\beta/2}\left\lvert 0 \right\rangle
\end{align*}
$$

We have 

$$
[a_ {p} ,e^{-K^{\dagger}}] = -g \frac{\tilde{\rho}(\vec{p})}{\omega _ {p} \sqrt{2\omega _ {p} }}e^{-K^{\dagger}},
$$

Hence 

$$
\left\langle \vec{p} \middle\vert 0_ {\rho} \right\rangle  = -ge^{-\beta/2}  \frac{\tilde{\rho}(\vec{p})}{\omega _ {p} \sqrt{2\omega _ {p} }}
$$

where

$$
\beta = g^{2} \int \frac{d^{3}p}{(2\pi)^{3}}\, \frac{1}{2\omega _ {p} ^{3}}   \left\lvert \tilde{\rho}(\vec{p}) \right\rvert ^{2}.
$$

Which is in pretty good agreement of Coleman's result up to a phase.


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
