---
layout: post
title: Quantum Domain Wall in 4D Part II
date: 2024-07-15
author: Baiyang Zhang
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

It has two classical minima are obtained at $\pm \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$. As a result we have two degenerate vacua states $\left\lvert{0^{\pm}}\right\rangle$ satisfying 

$$
\left\langle{0^{-}}\right\rvert \phi \left\lvert{0^{-}}\right\rangle =- \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }},\quad  
\left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle =+ \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}
$$

Now we want to study the quantum physics around one of the vacua, say $\left\langle \phi \right\rangle = \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$, and we want to apply perturbation methods, since it is usually the only way we know how to proceed. The question is, what is the Hamiltonian that can get the job done? In the context of Lagrangian formalism and path integral, the answer is quite straightforward, we can redefine the field operator to be $\phi\to \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}+\phi'$, so that the classical vacuum is obtained at $\phi'$ equals zero. The small fluctuation about $\frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$ gives us the quantum effects, we will essentially calculate

$$
Z[J] = \int D\phi' \, \exp \left\lbrace iS[\phi']+i \int \phi' J   \right\rbrace ,
$$

but only include $\phi'\sim 0$. 

How can we do the same thing but with Hamiltonian formalism? Anything that can be done with one formalism can equally be done in the other, it is just a matter of which formalism is more convenient. 

The problem is that, with Hamiltonian formalism, perturbative methods are just not applicable, because the expectation values $\left\langle \phi \right\rangle := \left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle$ is by no means a small quantity, in fact $\left\langle \phi \right\rangle$ sclaes as $1 / \sqrt{ \lambda_ {0} }$, it actually blows up as $\lambda_ {0}\to 0$. Then, we need to find some new field operator $\phi'$ such that $\left\langle \phi' \right\rangle=0$, then we can study the effects of fluctualtion of $\left\langle \phi' \right\rangle$ perturbative in $\left\lvert{0^{+}}\right\rangle$ state. Turns out, $\phi'$ is connected to $\phi$ by a unitary transformation, and in the case at hand the unitary operator turns out to be the displacement operator $\mathcal{D}_ {v_ {0}}$, where $v_ {0}$ is some parameter to be determined. Note that we have replaced the arbitrary function $f(\vec{x})$ with a constant function $v_ {0}$. We will explain it in the following.

Recall the defining property of displacement operator, $\mathcal{D}_ {f}^{\dagger}\phi \mathcal{D}_ {f}=\phi+f$. Thus if we let 

$$
\boxed{ 
v_ {0} = -\frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}
}
$$

then (at least at leading order)

$$
\left\langle{0^{+}}\right\rvert \mathcal{D}_ {v_ {0}}^{\dagger} \phi \mathcal{D}_ {v_ {0}}\left\lvert{0^{+}}\right\rangle  
= \left\langle{0^{+}}\right\rvert \phi+v_ {0}\left\lvert{0^{+}}\right\rangle  
= \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}-\frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}=0,
$$

hence

$$
\boxed{ 
0=\left\langle{0^{+}}\right\rvert \phi'\left\lvert{0^{+}}\right\rangle, \quad  \phi':= \mathcal{D}_ {v_ {0}}^{\dagger}\phi \mathcal{D}_ {v_ {0}}.
}
$$

It inspires us to define a new Hamiltonian in exatly the same fashion, 

$$
\mathcal{H} := \mathcal{D}_ {v_ {0}}^{\dagger} \hat{\mathcal{H}} \mathcal{D}_ {v_ {0}}.
$$

We are interested in the spectrum of the Hamiltonian. The good news is that, a unitary transformation preserves the spectrum! Now, to study the quantum corrections, instead of working with $\hat{H}, \phi$ and $\left\lvert{0^{+}}\right\rangle$ where perturbative methods fail, we can work with $H, \phi'$ and $\left\lvert{0^{+}}\right\rangle$ where $\phi'$ can be dealt with perturbatively. 

**Remarks.** Generally speaking, let $\mathcal{O}$ be any operator and $\left\lvert{\psi}\right\rangle$ its eigen state. If $\mathcal{O}'=\mathcal{D}^{\dagger}\mathcal{O} \mathcal{D}$ is the unitary transformation of $\mathcal{O}$, then its eigen state is $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$, not $\left\lvert{\psi}\right\rangle$. It maybe seems weird to some people to team up $\mathcal{O}'$ and $\left\lvert{\psi}\right\rangle$, not $\mathcal{O}'$ and $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$. In fact, it is the point! If we pair $\mathcal{O}'$ with $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$ it would be a trivially-transformed version of working with $\mathcal{O}$ and $\left\lvert{\psi}\right\rangle$, we would not get anything new! However, since $\left\lvert{\psi}\right\rangle$ is not the eigen state of $\mathcal{O}'$, it indeed raise some problems, the first and formost is that now $\mathcal{O}'$ is not diagonalized in $\left\lvert{\psi}\right\rangle$, we need to find a way to diagonalized it. That would be the other half the the project. 

A comparison between 


In renormalized parameters the Hamiltonian reads

$$
\begin{align*} 
\hat{H}(\vec{x}) &\supset \int d^{3}x \, : \frac{1}{2}\pi^{2}+\frac{1}{2}(\partial_ {i}\phi)^{2} - \frac{m^{2}}{4}\phi^{2}+\frac{g^{2}}{4}\phi^{4}:_ {m} \\ &\;\;\;\; + \int d^{3}x \, : \frac{\delta m^{2}}{4}\phi^{2}-\frac{1}{2}g \delta g\phi^{4}+\frac{3}{2}g^{2}I\phi^{2}-\frac{3}{4}m^{2}I +A :_ {m}. 
\end{align*}
$$

