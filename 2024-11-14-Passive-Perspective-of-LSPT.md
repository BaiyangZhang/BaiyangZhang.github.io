---
layout: post
title: A Passive Perspective of Linearized Soliton Perturbation Theory
date: 2024-11-14
author: Baiyang Zhang
catalog: true
tags:
  - kink
---


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

The problem is, in Hamiltonian formalism and working with $\hat{\mathcal{H}}$, perturbation methods are just not applicable, because the expectation value $\left\langle \phi \right\rangle := \left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle$ is by no means a small quantity, in fact $\left\langle \phi \right\rangle$ scales as $1 / \sqrt{ \lambda  }$, it actually blows up as $\lambda \to 0$. Then, similar to the Lagrangian case, we need to find some new field operator $\phi'$ such that $\left\langle \phi' \right\rangle=0$, then we can study the effects of fluctuation of $\left\langle \phi' \right\rangle$ perturbative in $\left\lvert{0^{+}}\right\rangle$ state. Turns out, $\phi'$ is connected to $\phi$ by a unitary transformation, and in the case at hand the unitary operator turns out to be the displacement operator $\mathcal{D}_ {v }$, where $v $ is some parameter to be determined. Note that we have replaced the arbitrary function $f(\vec{x})$ with a constant function $v $. We will explain it in the following.

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

