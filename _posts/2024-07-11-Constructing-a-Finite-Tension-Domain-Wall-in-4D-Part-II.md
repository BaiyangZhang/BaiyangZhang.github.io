---
layout: post
title: Quantum Domain Wall in 4D Part I
subtitle: 
date: 2024-07-11
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - "#domainWall"
  - kink
---

# Spontaneous Symmetry Breaking

Recall that the original Hamiltonian in terms of bare parameter, without normal ordering reads

$$
\hat{H}(\vec{x}) = \frac{1}{2}\pi^{2}(\vec{x})+\frac{1}{2} (\partial_ {i}\phi)^{2} - \frac{m_ {0}^{2}}{4} \phi^{2}(\vec{x}) + \frac{\lambda_ {0}}{4} \phi^{4}(\vec{x}) + A, 
$$

It has two classical minima are obtained at $\pm v_ {0}$, where

$$
v_ {0} := \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}.
$$

As a result we have two degenerate vacua states $\left\lvert{0^{\pm}}\right\rangle$ satisfying 

$$
\left\langle{0^{-}}\right\rvert \phi \left\lvert{0^{-}}\right\rangle =-v_ {0},\quad  
\left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle =+v_ {0}
$$

Now we want to expand the field about one of the vacua, say $-v_ {0}$, in order to apply the standard perturbation method. Thus our question is, what does the Hamiltonian look like when it is expanded about this minimum? In the context of Lagrangian formalism and path integral, the answer is quite straightforward, we can redefine the field operator to be $\phi\to v_ {0}+\phi'$, so that now the vacuum is obtained at $\phi'$ is zero,

$$
\left\langle{0^{-}}\right\rvert  \phi' \left\lvert{0^{-}}\right\rangle  = 0.
$$

How should we achieve the same task but in Hamiltonian formalism? Anything that can be done with one formalism can equally be done in the other, we just need to find the right unitary operator, which in our case turn out to be the displacement operator $\mathcal{D}_ {v_ {0}}$, note that we have replaced the arbitrary function $f(\vec{x})$ with a constant function $v_ {0}$. Let's check it out. We know the defining property that $\mathcal{D}_ {f}^{\dagger}\phi \mathcal{D}_ {f}=\phi+f$, thus

$$
\left\langle{0^{-}}\right\rvert \mathcal{D}_ {v_ {0}}^{\dagger} \phi \mathcal{D}_ {v_ {0}}\left\lvert{0^{-}}\right\rangle  = \left\langle{0^{-}}\right\rvert \phi+v_ {0}\left\lvert{0^{-}}\right\rangle  = -v_ {0}+v_ {0}=0
$$

which we define to be 

$$
\boxed{ 
0=\left\langle{0^{-}}\right\rvert \phi'\left\lvert{0^{-}}\right\rangle, \quad  \phi':= \mathcal{D}_ {v_ {0}}^{\dagger}\phi \mathcal{D}_ {v_ {0}}.
}
$$







In renormalized parameters the Hamiltonian reads

$$
\begin{align*} 
\hat{H}(\vec{x}) &\supset \int d^{3}x \, : \frac{1}{2}\pi^{2}+\frac{1}{2}(\partial_ {i}\phi)^{2} - \frac{m^{2}}{4}\phi^{2}+\frac{g^{2}}{4}\phi^{4}:_ {m} \\ &\;\;\;\; + \int d^{3}x \, : \frac{\delta m^{2}}{4}\phi^{2}-\frac{1}{2}g \delta g\phi^{4}+\frac{3}{2}g^{2}I\phi^{2}-\frac{3}{4}m^{2}I +A :_ {m}. 
\end{align*}
$$

