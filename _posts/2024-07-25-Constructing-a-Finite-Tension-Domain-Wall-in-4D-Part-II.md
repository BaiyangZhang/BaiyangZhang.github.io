---
layout: post
title: Quantum Domain Wall in 4D Part II
date: 2024-07-25
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

The problem is that, with Hamiltonian formalism, perturbative methods are just not applicable, because the expectation values $\left\langle \phi \right\rangle := \left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle$ is by no means a small quantity, in fact $\left\langle \phi \right\rangle$ scales as $1 / \sqrt{ \lambda_ {0} }$, it actually blows up as $\lambda_ {0}\to 0$. Then, we need to find some new field operator $\phi'$ such that $\left\langle \phi' \right\rangle=0$, then we can study the effects of fluctuation of $\left\langle \phi' \right\rangle$ perturbative in $\left\lvert{0^{+}}\right\rangle$ state. Turns out, $\phi'$ is connected to $\phi$ by a unitary transformation, and in the case at hand the unitary operator turns out to be the displacement operator $\mathcal{D}_ {v_ {0}}$, where $v_ {0}$ is some parameter to be determined. Note that we have replaced the arbitrary function $f(\vec{x})$ with a constant function $v_ {0}$. We will explain it in the following.

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

It inspires us to define a new Hamiltonian in exactly the same fashion, 

$$
\mathcal{H} := \mathcal{D}_ {v_ {0}}^{\dagger} \hat{\mathcal{H}} \mathcal{D}_ {v_ {0}}.
$$

We are interested in the spectrum of the Hamiltonian. The good news is that, a unitary transformation preserves the spectrum! Now, to study the quantum corrections, instead of working with $\hat{H}, \phi$ and $\left\lvert{0^{+}}\right\rangle$ where perturbative methods fail, we can work with $H, \phi'$ and $\left\lvert{0^{+}}\right\rangle$ where $\phi'$ can be dealt with perturbatively. 

**Remarks.** Generally speaking, let $\mathcal{O}$ be any operator and $\left\lvert{\psi}\right\rangle$ its eigen state. If $\mathcal{O}'=\mathcal{D}^{\dagger}\mathcal{O} \mathcal{D}$ is the unitary transformation of $\mathcal{O}$, then its eigen state is $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$, not $\left\lvert{\psi}\right\rangle$. It maybe seems weird to some people to team up $\mathcal{O}'$ and $\left\lvert{\psi}\right\rangle$, not $\mathcal{O}'$ and $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$. In fact, it is the point! If we pair $\mathcal{O}'$ with $\mathcal{D}^{\dagger}\left\lvert{\psi}\right\rangle$ it would be a trivially-transformed version of working with $\mathcal{O}$ and $\left\lvert{\psi}\right\rangle$, we would not get anything new! However, since $\left\lvert{\psi}\right\rangle$ is not the eigen state of $\mathcal{O}'$, it indeed raise some problems, the first and foremost is that now $\mathcal{O}'$ is not diagonalized in $\left\lvert{\psi}\right\rangle$, we need to find a way to diagonalized it. That would be the other half the the project. 

A comparison between what we have said to the case of regular functions might be helpful. 

|                                                                           Functions                                                                            |                                                                                                                                                                      QFT                                                                                                                                                                      |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                      A functions $f(x)$, a special position $x_ {0}$ where the interesting things happen.                                      |                                                                                                             A Hilbert state represented by a functional $\left\lvert{\Psi}\right\rangle$, and some operator $\mathcal{O}(\phi)$.                                                                                                              |
|                                            We want to study the function $f(x_ {0})$ about $x_ {0}$ perturbatively,                                            |                                                                                                                We want to study the $\left\langle{\Psi}\right\rvert\mathcal{O}\left\lvert{\Psi}\right\rangle$ perturbatively,                                                                                                                 |
|                              but $x_ {0}$ is not a small quantity so Maclaurin expansion (Taylor expansion at the origin) fails.                               |                                                                                                      but $\left\langle{\Psi}\right\rvert\phi \left\lvert{\Psi}\right\rangle=:f(x)$ is too large for $\phi$ to be treated perturbatively.                                                                                                      |
| **In a passive perspective, we shift the origin** to $x_ {0}$, then small deviation from $x_ {0}$ can now be studied using Maclaurin expansion perturbatively. | In a passive perspective, we shift the operators, especially the field operator $\phi$ since it is usually the building block of other operators. The expectation value of the new, shifted operator $\phi'$ should be zero, $\left\langle{\Psi}\right\rvert \phi'\left\lvert{\Psi}\right\rangle =0$. Now we can treat $\phi$ perturbatively. |
|                We are using a new, shifted coordinate system $\left\lbrace \overline{x} \right\rbrace$ to study the same old functions $f(x)$.                 |                                                                                                  We are using shifted operators $\mathcal{D}^{\dagger}\mathcal{O}\mathcal{D}$ to study the same old states $\left\lvert{\Psi}\right\rangle$.                                                                                                  |

- - -

In summary, now $\mathcal{H}=\mathcal{D}^{\dagger}_ {v}\hat{\mathcal{H}}\mathcal{D}_ {v}$ is a operator-valued function of $\phi' = \mathcal{D}_ {v}^{\dagger} \phi \mathcal{D}_ {v}$, and $\phi'$ can be dealt with perturbatively. For the value of $v$, we could choose it to be the bare parameter or renormalized parameter, for example $v_ {0}=-\frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$ is given by a bunch of other bare parameters hence itself is also a bare parameter. The renormalized version would be $v:= -\frac{m}{\sqrt{ 2\lambda} }$. The final result should not depend on the convention we choose, so for now we let it be bare, the associated displacement operator is $\mathcal{D}_ {v_ {0}}$. The expansion is given by 

$$
v_ {0} = v+\delta v, \quad  \delta v = \delta v_ {1}+\delta v_ {2}+\cdots, \quad \delta v_ {i} \sim \mathcal{O}(g^{i}).
$$

This can be seen from expanding $v_ {0}$ in terms of $m_ {0}$ and $g_ {0}$.

In renormalized parameters the Hamiltonian reads (up to $\mathcal{O}(g^{3})$)

$$
\begin{align*} 
\hat{H}(\vec{x}) &\supset \int d^{3}x \, : \frac{1}{2}\pi^{2}+\frac{1}{2}(\partial_ {i}\phi)^{2} - \frac{m^{2}}{4}\phi^{2}+\frac{g^{2}}{4}\phi^{4}:_ {m} \\ 
&\;\;\;\; + \int d^{3}x \, : \frac{\delta m^{2}}{4}\phi^{2}-\frac{1}{2}g \delta g\phi^{4} + \frac{(\delta g)^{2}}{4}\phi^{4} + \frac{3}{2}(g-\delta g)^{2}I\phi^{2}-\frac{3}{4}m^{2}I +A :_ {m}. 
\end{align*}
$$

We need to sandwich it by $\mathcal{D}_ {v_ {0}}$ to get $\mathcal{H}$. Making use of the expansion of $v_ {0}$, we will expand the Hamiltonian density in powers of $\lambda=g^{2}$. With some help from Mathematica, we find the following results.

At leading order 

$$
\begin{align*}
\mathcal{H}_ {0} &:= 
\end{align*}
$$


- - -

In comparison, Jarah's results for the shifted Hamiltonian density reads

$$
\begin{align*}
\mathcal{H} &=\frac{1}{2}\pi^{2}+\frac{1}{2}(\partial \phi)^{2}+ \frac{\lambda}{4}(\phi-v+\delta v)^{4}- \frac{m^{2}}{4} (\phi-v+\delta v)^{2} \\
&\;\;\;\;\; + \frac{1}{4}(-2g\delta g+(\delta g)^{2})(\phi-v+\delta v)^{4}\\
&\;\;\;\;\; + \frac{1}{4} (\delta m^{2}+4(g-\delta g)^{2}I) (\phi-v+\delta v)^{2} + \frac{3I}{4}(-m^{2}+\delta m^{2}) +A.
\end{align*}
$$