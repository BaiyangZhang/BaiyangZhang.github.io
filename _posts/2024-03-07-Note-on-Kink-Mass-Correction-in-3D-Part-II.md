---
layout: post
title: Note on the kink mass correction in 3D Part II
subtitle: 
date: 2024-03-07
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
  - kink
---

# Domain wall in phi-fourth model

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
\end{align*}
$$

where we have used 

$$
\int dt \, \frac{1}{\cosh^{4}t} = \frac{4}{3}. 
$$

Similarly, the contribution from the space-derivative term reads

$$
\begin{align*}
\frac{1}{\lambda} \int dx \, \frac{1}{2} (\partial_ {x}\widetilde{f})^{2}  &=  \\
\end{align*}
$$