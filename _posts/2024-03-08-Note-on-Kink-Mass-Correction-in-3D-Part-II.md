---
layout: post
title: Note on the kink mass correction in 3D Part II
subtitle: 
date: 2024-03-08
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
  - kink
---

## Domain wall in phi-fourth model

Recall that we are working in $D = d+1$ dimensional space-time, the space-dimension is $d$. For now let's consider $d=2$. In 2-dimensional space, a kink can extend to form a domain wall, for more info about domain walls see my other [note](https://www.mathlimbo.net/blog/2024/Domain-Wall/). The world line of such a domain wall would be world sheet. Now let's try to calculate the quantum corrections to the tension of such a domain wall.

The energy is given by the space integral of the Hamiltonian density,

$$
H = \int d^{d}x \,  \mathcal{H},\quad  \mathcal{H}  = \frac{1}{\lambda}\left[ \frac{\tilde{\pi}^{2}}{2}+\frac{(\nabla \tilde{\phi})^{2}}{2} + V(\tilde{\phi}) \right]
$$

where 

$$
\tilde{\phi}:= \sqrt{ \lambda } \phi,\quad  \tilde{\pi} := \sqrt{ \lambda } \pi .
$$

Note that we have written $\phi$ as $\tilde{\phi}$ so that the coupling becomes an overall pre-factor. Keep in mind that, in this formalism, the energy is no longer simply $H=\int \, V$ but $H = \int \, V / \lambda$. 

Let the spatial coordinates be $x$ and $y$. Consider the potential (expanded in the negative vacuum)

$$
V(\tilde{\phi}) = \frac{\tilde{\phi}^{2}}{4} (\tilde{\phi}-\sqrt{ 2 }m)^{2}.
$$

Now consider a flat domain wall in $x=0$ plane. The classical kink solution in the $x$-direction is 

$$
\widetilde{f}(x,y) = \frac{m}{\sqrt{ 2 }} \left( 1+\tanh \frac{mx}{2} \right)
$$

where again, $\widetilde{f} = \sqrt{ \lambda }f$ by definition. 

The energy now reads

$$
H = \int dy  \int dx \, \frac{1}{\lambda} \left(  \frac{1}{2}  (\partial_ {x} \widetilde{f})^{2}+  V(\tilde{f})  \right) =: \int dy \, \rho_ {0}(y), 
$$

where $\rho_ {0}$ is now interpreted as the tension of the domain wall. The calculation is exactly the same as for the kink energy, but to refresh the memory I decided to do it again.

Introduce a new variable $t := \frac{mx}{2}$, we have

$$
\widetilde{f}(t) = \frac{m}{\sqrt{ 2 }} (1+\tanh t),\quad  dx = \frac{2}{m} dt,\quad  \partial_ {x} = \frac{m}{2} \partial_ {t}.
$$

The potential contribution to the energy is 

$$
\begin{align*}
\int dx \,  \frac{1}{\lambda} V(\tilde{f}) &= \frac{m^{3}}{8\lambda}\int dt \, (\tanh ^{2}(t)-1) ^{2}\\
&= \frac{m^{3}}{8\lambda} \int dt \, \frac{1}{\cosh^{4}t} \\
&= \frac{m^{3}}{6\lambda},
\tag{1} 
\end{align*}
$$

where we have used 

$$
\int dt \, \frac{1}{\cosh^{4}t} = \frac{4}{3}. 
$$

Similarly, the contribution from the space-derivative term reads

$$
\begin{align*}
\frac{1}{\lambda} \int dx \, \frac{1}{2} (\partial_ {x}\widetilde{f})^{2}  &= \frac{m^{3}}{8\lambda} \int dt \,  (\partial_ {t}\tanh t)^{2} \\
&= \frac{m^{3}}{8\lambda} \int dt \,  \frac{1}{\cosh^{4}t} \\
&= \frac{m^{3}}{6\lambda}.
\end{align*}
\tag{2} 
$$

Putting Eq. (1) and Eq. (2) together, we have 

$$
\rho_ {0} = \frac{m^{3}}{3\lambda}.
$$

- - -

The dimensional analysis gives us

$$
[\lambda] = 4-D = 3-d,
$$

hence in $2+1$ dimension the coupling has dimension of mass. 

## Normal Modes

Since we assumed the domain wall to be flatly lying in the $y$-plane, the normal modes in 2-d space can be *factorized* into $x$ and $y$ components,

$$
{\mathfrak g} _ {k_ {x}k_ {y}} (x,y) =  {\mathfrak g}_ {k_ {x}}(x) \times  e^{ -i y k_ {y}}.
$$

The normal modes are the solution of the equation of motion in the kink background, or Poschl-Teller potential. These modes include a continuum

$$
 {\mathfrak g} _ {k}(x) = \frac{e^{-ikx}}{\omega_ {k} \sqrt{m^2+4k^2}}\left[2k^2-m^2+(3/2)m^2\text{sech}^2(m x/2)-3im k\tanh(m x/2)\right]
$$

with eigenvalue $\omega_ {k} = \sqrt{ k^{2}+m^{2} }$, a zero mode 

$$
{\mathfrak g}_ {B} = -\sqrt{ \frac{3m}{8} } \text{sech}^{2}\left( \frac{mx}{2} \right)
$$

with eigenvalue $0$ and a shape mode

$$
 {\mathfrak g} _ {S} = \frac{\sqrt{ 3m }}{2} \tanh \frac{mx}{2} \text{sech} \frac{mx}{2}
$$

with eigenvalue less then the rest mass of excited particle, $\omega_ {s} = \frac{\sqrt{ 3 }}{2}m$. 

Momentum in the $y$-direction also contributes to the total energy, putting them together with the zero modes, shape modes and continuum in the $x$ direction we have 

$$
\omega_ {Bk_ {}y} = \left\lvert k_ {y} \right\rvert ,\quad  \omega_ {Sk_ {y}} = \sqrt{ \frac{3m^{2}}{4}+k_ {y}^{2} },\quad  \omega_ {k_ {x} k_ {y}} = \sqrt{ m^{2}+k_ {x}^{2}+k_ {y}^{2} }.
$$

Note that 

- there is a zero mode corresponding to $k_ {B},k_ {y}=0$,
- the mass gap disappears, due to the mass-gap-less of $y$-momentum.

The formalism we developed in generic dimension $d$ surely also applies to $d=2$. Let $\vec{p}=(p_ {x},p_ {y})$ and $\vec{k}=(k_ {x},k_ {y})$. The Fourier transform is 

$$
 \tilde{\mathfrak{g} }_ {k_ {x},k_ {y}} (\vec{p})= \int d^{2}x \,   \mathfrak{g} _ {k}(\vec{x}) e^{ -i\vec{k}\cdot \vec{x} } = (2\pi)\delta(k_ {y}-p_ {y}) \times   \tilde{\mathfrak{g}} _ k (p_ {x}).
$$

Again we see the factorization in $x$ and $y$, the $\delta$-function in $y$ direction is due to the plane wave expansion. 

