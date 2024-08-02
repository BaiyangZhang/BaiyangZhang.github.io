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

Recall that the original, un-shifted Hamiltonian in terms of bare parameter, without normal ordering reads

$$
\hat{\mathcal{H}}^{0}(\vec{x}) = \frac{1}{2}\pi^{2}(\vec{x})+\frac{1}{2} (\partial_ {i}\phi)^{2} - \frac{m_ {0}^{2}}{4} \phi^{2}(\vec{x}) + \frac{\lambda_ {0}}{4} \phi^{4}(\vec{x}) + A, 
$$

It has two classical minima are obtained at $\pm \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$. As a result we have two degenerate vacua states $\left\lvert{0^{\pm}}\right\rangle$ satisfying 

$$
\left\langle{0^{-}}\right\rvert \phi \left\lvert{0^{-}}\right\rangle =- \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }},\quad  
\left\langle{0^{+}}\right\rvert \phi \left\lvert{0^{+}}\right\rangle =+ \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}
$$

Now we want to study the quantum physics around one of the vacua, say $\left\langle \phi \right\rangle = \frac{m_ {0}}{\sqrt{ 2\lambda_ {0} }}$, and we want to apply perturbation methods, since it is usually the only way we know how to proceed. The question is how to do perturbation theory with Hamiltonian formalism? For the validation of perturbation method, the field fluctuation should be small, meaning $\left\langle \phi \right\rangle$ should be small, but it is clearly not the case here, since $m_ {0} / \sqrt{ 2 } g_ {0}$ is not small by any sense. 

- - -

Another thing we need to keep in mind is the difference between bare and renormalized parameters, eventually we need to write down the observables in terms of not bare, but renormalized parameters. Following the philosophy of *renormalized perturbative method*, we should 1) separate the Hamiltonian into renormalized terms and counter terms, 2) use the counter terms to cancel the divergence from loops, which are now written in terms of renormalized parameters. We wrote the vev of $\phi$ in terms of bare parameters, but that is only for pedagogical reasons, what we should really do it first write the Hamiltonian into the renormalized perturbation theory form, 

$$
\hat{\mathcal{H}} =  \frac{1}{2}\pi^{2}(\vec{x})+\frac{1}{2} (\partial_ {i}\phi)^{2} - \frac{m^{2}}{4} \phi^{2}(\vec{x}) + \frac{\lambda}{4} \phi^{4}(\vec{x}) + A + \text{couter terms,}
$$

then look for the minimum of the double-well potential, now $\left\langle \phi \right\rangle = m / \sqrt{ 2 }g$, with out naught subscript. 

- - -

The last but not the least thing we need to worry about is the normal ordering. So far my assumption is that, the Hamiltonian is defined at some intrinsic parameter $m_ {0}$, so the normal ordering should also be defined at $m_ {0}$; however, to make the calculation easier, we shift the normal ordering to another scale: $m$. We have already talked in length about how to perform this shift. The final result should not depend on the shift though.

- - -

In the context of Lagrangian formalism and path integral, the perturbation method is quite straightforward, we can redefine the field operator according to $\phi\to \frac{m }{\sqrt{ 2\lambda  }}+\phi'$, so that the classical vacuum is obtained at $\phi'$ equals zero. The small fluctuation about $\frac{m }{\sqrt{ 2\lambda  }}$ gives us the quantum effects, we will essentially calculate

$$
Z[J] = \int D\phi' \, \exp \left\lbrace iS[\phi']+i \int \phi' J   \right\rbrace ,
$$

but only include $\phi'\sim 0$. 

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

In summary, now $\mathcal{H}=\mathcal{D}^{\dagger}_ {v}\hat{\mathcal{H}}\mathcal{D}_ {v}$ is a operator-valued function of $\phi' = \mathcal{D}_ {v}^{\dagger} \phi \mathcal{D}_ {v}$, and $\phi'$ can be dealt with perturbatively. For the value of $v$, we could choose it to be the bare parameter or renormalized parameter, the final result should not depend on the convention we choose, in our note, in the spirit of renormalized perturbation theory, we choose $v$ to be renormalized, the associated displacement operator is $\mathcal{D}_ {v}$. Still, $v$ receives quantum corrections order by order, the full expression for $v$ would be an expansion in $g$:

$$
v = -\frac{m}{\sqrt{ 2 }g} +\delta v, \quad  \delta v = \delta v_ {1}+\delta v_ {2}+\cdots, \quad \delta v_ {i} \sim \mathcal{O}(g^{i}).
$$

- - -

In renormalized parameters the Hamiltonian reads (up to $\mathcal{O}(g^{3})$)

$$
\begin{align*} 
\hat{H}(\vec{x}) &\supset \int d^{3}x \, : \frac{1}{2}\pi^{2}+\frac{1}{2}(\partial_ {i}\phi)^{2} - \frac{m^{2}}{4}\phi^{2}+\frac{g^{2}}{4}\phi^{4}:_ {m} \\ 
&\;\;\;\; + \int d^{3}x \, : \frac{\delta m^{2}}{4}\phi^{2}-\frac{1}{2}g \delta g\phi^{4} + \frac{(\delta g)^{2}}{4}\phi^{4} + \frac{3}{2}(g-\delta g)^{2}I\phi^{2}-\frac{3}{4}m^{2}I +A :_ {m}. 
\end{align*}
$$

We need to sandwich it by $\mathcal{D}_ {v}$ to get the shifted Hamiltonian density $\mathcal{H}$. We will expand $\mathcal{H}$ in powers of $g=\sqrt{ \lambda }$. With some help from Mathematica, we find the following results.

$$
\begin{align*}
\mathcal{H}_ {0} &= A_ 0-\frac{m^4}{16 g^2}, \\
\mathcal{H}_ {1} &= A_ {1} \equiv 0, \\
\mathcal{H}_ {2} &= \frac{\pi^{2}}{2} + \frac{(\partial \phi)^{2}}{2} + \frac{m^{2}\phi^{2}}{2} + \frac{m^{4}}{8g^{2}}\left( -\frac{\delta g_ {1}}{g} + \frac{\delta m^{2}_ {1}}{m^{2}} + \frac{\delta m^{4}_ {1}}{8g^{2}} \right) + A_ {2}, \\ 
\mathcal{H}_ {3} &= - \frac{mg}{\sqrt{ 2 }} \phi^{3} + \phi\left( m^{2}\delta v_ {1}+\frac{m^{3}}{\sqrt{ 2 }g} \left( \frac{\delta g_ {1}}{g} - \frac{\delta m^{2}_ {1}}{2m^{2}} - \frac{\delta m^{4}_ {1}}{2g^{2}} \right) \right) + A_ {3}, \\
\mathcal{H}_ {4} &= \frac{g^{2}}{4}\phi^{4} + \phi^{2}\left( - \frac{3gm\delta v_ {1}}{\sqrt{ 2 }} - \frac{3m^{2}\delta g_ {1}}{2g} + \frac{\delta m^{2}_ {1}}{4} + \frac{3m^{2}\delta m_ {1}^{4}}{4g^{2}} \right) \\
&\;\;\;\; + \phi(m^{2}\delta v_ {2}) + \frac{m^{3}\delta v_ {1}}{\sqrt{ 2 }g}\left( \frac{g}{\sqrt{ 2 }m} \delta v_ {1} + \frac{\delta g_ {1}}{g} - \frac{\delta m_ {1}^{2}}{2m^{2}} - \frac{\delta m_ {1}^{4}}{2g^{2}} \right) + A_ 4, \\
\mathcal{H}_  {5} &=  \phi^{3}\left( g^{2}\delta v_ {1}+\sqrt{2}m\delta g_ {1}- \frac{m\delta m_ {1}^{4}}{\sqrt{2}g}  \right) - \phi^{2}\left( \frac{3mg \delta v_ {2}}{\sqrt{2}} \right) \\
&\;\;\;\; + \phi\left( m^{2}\delta v_ {3} - \frac{3gm\delta v_ {1}^{2}}{\sqrt{2}} - \frac{3m^{2}\delta g_ {1}\delta v_ {1}}{g}+ \frac{1}{2}\delta m_ {1}^{2}\delta v_ {1} - \frac{3mg I_ {1}}{\sqrt{2}} + \frac{3m^{2}\delta m_ {1}^{4}\delta v_ {1}}{2g^{2}} \right) \\
&\;\;\;\; + \frac{m^{3}\delta v_ {2}}{\sqrt{2}g}\left( \frac{\delta g_ {1}}{g} - \frac{\delta m_ {1}^{2}}{2m^{2}} - \frac{\delta m_ {1}^{4}}{2g^{2}} + \frac{\sqrt{2}g\delta v_ {1}}{m} \right) + A_ {5}. 
\end{align*}
$$

