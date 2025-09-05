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

where $\pi$ is the canonical momentum ,and the density funciton $\rho(\vec{x})$ is a function of space only, independent of time. This means that the interaction doesn't turn off in the far past and far future. The standard lore is to insert an adiabatic switching function $f(t)$, 

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

## Displacement and Squeeze

Let's use a different



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