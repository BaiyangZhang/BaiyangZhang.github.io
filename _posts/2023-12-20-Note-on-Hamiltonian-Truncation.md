---
layout: post
title: Note on Hamiltonian Truncation
subtitle: 
date: 2023-12-20
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
- kink
---
### Background

### The symplectic manifold

The finite-dimensional covariant Hamiltonian approach to field theory is vigorously developed from the seventies in its multisymplectic and polysymplectic variants. The final purpose is to covariant Hamiltonian quantization of field theory. For classical field theory, the Hamiltonian formalism provides an alternative to the Lagrangian formalism for deriving the equations of motion. Furthermore, the Hamiltonian approach offers a geometrical interpretation of the field theory, in a sense combines geometry and algebra together. To fully appreciate it, we need to know what is a symplectic manifold first. 

A symplectic manifold is a type of smooth manifold equipped with a special kind of geometric structure known as a `symplectic form`. As we all know, a manifold is a *topological space* that **locally resembles Euclidean space**. In the case of a smooth manifold, this means that around every point, the manifold can be approximated by a patch of Euclidean space in such a way that the transition maps between these patches are smooth (infinitely differentiable). A symplectic form on a manifold is a specific kind of differential form that is **closed** and **non-degenerate**. In more concrete terms, a symplectic form is a $2$-form, and non-degeneracy means that the form pairs vectors in a way that is **invertible** – no non-zero vector is mapped to zero – ensuring that the form provides a kind of generalized volume element on the manifold.

To be more mathematically rigorous, let $M$ be a topological space that is Hausdorff (any two distinct points have disjoint neighborhoods) and second-countable (has a countable basis for its topology).  Additionally, $M$ is locally homeomorphic to $\mathbb{R}^n$, meaning every point in $M$ has a neighborhood that is topologically the same as an open subset of Euclidean space (this practically says that $M$ is a manifold). A smooth manifold is a manifold equipped with an atlas of charts such that the transition maps between overlapping charts are smooth. On $M$, a symplectic form $\omega$ is a closed, non-degenerate differential $2$-form. Mathematically, this means 
- **Closed**: The exterior derivative $d\omega$ is zero, $d\omega = 0$. This implies that $\omega$ is **locally exact**.
- **Non-degenerate**: For any vector $v\in T_ {p}M$ where $p \in M$, if $\omega(v, w) = 0$ for all vectors $w$ at that point, then $v$ must be the zero vector. This ensures that the form $\omega$ pairs vectors in a fully invertible way.

Note that a symplectic manifold is necessarily even-dimensional. If $M$ is a symplectic manifold with symplectic form $\omega$, and the dimension of $M$ is $2n$, then $\omega^n$ (the $n$-th wedge power of $\omega$) is a volume form on $M$, providing a natural orientation.

**Darboux's theorem.** Locally, all symplectic manifolds of the same dimension are isomorphic. This means that around any point in a symplectic manifold, one can find local coordinates (often called "canonical coordinates" or "Darboux coordinates") $(q_1, \ldots, q_n, p_1, \ldots, p_n)$) in which the symplectic form has the standard expression $\omega = \sum_{i=1}^{n} dq_i \wedge dp_i$.

In classical mechanics, symplectic manifolds serve as the stage for Hamiltonian dynamics. The *phase space of a classical mechanical system*, which includes both its positions and momenta, *can be treated as a symplectic manifold*. The symplectic form encodes the fundamental *Poisson brackets* of the system, which are central to Hamiltonian mechanics. It provides the geometric framework within which the evolution of the system can be elegantly expressed using Hamilton's equations. The structure of symplectic manifolds imposes several interesting properties. For instance, in **even-dimensional** spaces, they allow for the formulation of Hamiltonian vector fields and symplectic transformations. These concepts have far-reaching applications not only in physics but also in areas like symplectic topology, geometric quantization, and more.

### Hamiltonian equations

Most readers are much more comfortable with the Lagrangian formalism of field theory than the Hamiltonian formalism, so let's start with the former. The transition from Lagrangian to Hamiltonian is achieved by **Legendre transformation**. We first define the canonical momenta $\pi_i$ conjugate to each field $\phi_i$ by

$$ \pi_i = \frac{\partial \mathcal{L}}{\partial (\partial_t \phi_i)}, $$

where $\mathcal{L}$ is the Lagrangian density and $\partial_t \phi_i$ is the time derivative of the field.

The Hamiltonian density $\mathcal{H}$ is then given by

$$ \mathcal{H} = \sum_i \pi_i \partial_t \phi_i - \mathcal{L}, $$

where the sum runs over all fields in the theory.

The equations of motion in the Hamiltonian formalism for field theory are then given by Hamilton's equations, analogous to the Hamiltonian formalism in classical mechanics. These equations are

$$ \frac{\delta \mathcal{H}}{\delta \phi_i}=-\dot{\pi}(x), $$
$$ \frac{\delta \mathcal{H}}{\delta \pi_i} = \dot{\phi}_i, $$

where $\delta / \delta \phi_i$ and $\delta / \delta \pi_i$ represent functional derivatives with respect to the field $\phi_i$ and its conjugate momentum $\pi_i$, respectively. 

From now on let's assume there are only one type of field and canonical momentum, so we can neglect the subscript $i$. Note here the functional derivative $\delta / \delta \phi$ is not equivalent to the partial derivative $\partial / \partial \phi$. To see this, recall how $\delta \mathcal{H}$ and $\delta \mathcal{H} / \delta \phi$ is defined,

$$
\delta H =:  \int d^{d-1}x \, \delta \mathcal{H} = \int d^{d-1}x \, \delta \phi \frac{\delta \mathcal{H}}{\delta \phi},
$$

thus all we need to do is to perform a variation of the field $\phi$ and leaving the canonical momentum $\pi$ untouched, then massage the variation of the Hamiltonian in the form given above. For a generic Hamiltonian $\mathcal{H}(\pi,\phi,\partial_ {x}\phi)$ where $x$ denotes all the spatial coordinates, under the field variation $\phi\to\phi+\delta \phi$ we have

$$
\begin{align*}
H\to H' &=  \int d^{d-1}x \, \mathcal{H}(\phi+\delta \phi,\partial_ {x}\phi+\partial_ {x}\delta\phi, \cdots) \\
&=  \int d^{d-1}x \, \left[ \frac{\partial\mathcal{H}}{\partial \phi }\delta \phi + \frac{\partial \mathcal{H}}{\partial(\partial_ {x}\phi)}\delta(\partial_ {x}\phi) \right] \\
&= \int d^{d-1}x \, \left[ \frac{\partial\mathcal{H}}{\partial \phi }\delta \phi + \frac{\partial \mathcal{H}}{\partial(\partial_ {x}\phi)}(\partial_ {x}\delta\phi) \right] \\ \\
&= \int d^{d-1}x \, \left[ \frac{\partial\mathcal{H}}{\partial \phi }\delta \phi - \left( \partial_ x\frac{\partial \mathcal{H}}{\partial(\partial_ {x}\phi)} \right) \delta\phi \right] \\ \\
&= \int d^{d-1}x \, \delta\phi  \left[ \frac{\partial\mathcal{H}}{\partial \phi } - \left( \partial_ x\frac{\partial \mathcal{H}}{\partial(\partial_ {x}\phi)} \right) \right]  \\
&= : \int d^{d-1}x \, \delta \phi \frac{\delta \mathcal{H}}{\delta \phi}
\end{align*}
$$

thus, 

$$
\frac{\delta \mathcal{H}}{\delta \phi} = \frac{\partial\mathcal{H}}{\partial \phi } - \left( \partial_ x\frac{\partial \mathcal{H}}{\partial(\partial_ {x}\phi)} \right).
$$

Taking this back to the Hamiltonian equations we recover the familiar Euler-Lagrange equation.

These equations describe how the fields and their conjugate momenta evolve over time, analogous to how the position and momentum of a particle evolve in classical mechanics. They provide a complete description of the dynamics of the field system within the Hamiltonian framework.

### Basics of QFT

The starting point of defining a quantum field theory is the choice of a manifold $M$ of dimension $d$. We mostly (but not always) regard the manifold as a Riemannian manifold with a **smooth** metric on it. The manifold may or may not have boundaries, if it does then some additional information is needed at the boundaries to define the theory.

Having defined the manifold $M$, the next ingredient is the choice of objects to consider over $M$, the so-called "degree of freedoms", or `fields`. Now it is helpful to adopt a statistical viewpoint toward QFT,  in order to extract the information about physical observables we need "just" to know the partition function, which is obtain via a so-called path-integral. That is, we integrate all the possible field configurations with a weight, which is essentially given by the exponent of the action. For example, we may consider a principal bundle with a connection over $M$. In physics terminology the choice of the connection is the same as picking a gauge field. We may also be considering the section of a vector bundle over $M$, these fields are sometimes called the `matter field`. 

As another example of QFT we may consider the space of maps

$$
X: M\to N
$$

where $N$ is the `target` manifold. The field theories associated with integrating over the space of such maps are called `sigma models`. 

In quantum field theories we are typically interested in integrating over infinite-dimensional spaces. It turns out that the greater the dimension $d$ of $M$, the more complicated the integrations over these spaces. In fact (ignoring gravitational theories), the only non-trivial quantum field theories that are believed to exist (i.e., for which some kind of integration over the infinite-dimensional space exists) have $d \leq 6$ and most of the standard ones have $d \leq 4$. 

Quantum field theories in different dimensions can be related to each other by an operation known as `Kaluza–Klein reduction`. Roughly speaking this means considering the situation where

$$
M = N \times  K,\quad  K \ll  N
$$

The action may be very large for field configurations that are **not** constant over $K$, so the path-integral, which is weighted by $e^{ -S_ {E} }$, localizes to field configurations that are constant along $K$. This gives rise to an **effective** path integral over field configurations that have only constant modes along $K$. 

## Hamiltonian Truncation

In our case, we consider the phi-fourth theory defined on 

$$
M = \mathbb{T}^{2} \times  \mathbb{R},
$$

where $\mathbb{T}^{2}$ is the flat torus space of size $L \times L$, and the time direction $\mathbb{R}$ is left uncompactified. Since the space manifold is compact, the spectrum of the free theory is discrete and free of IR divergence. Following the procedure of canonical quantization, we first expand the scalar field in terms of ladder operators (in discrete form) as

$$
\phi(\vec{x}) = \sum_ {k_ {1},k_ {2}} c_ {k} a_ {k}e^{ +i \vec{k}\cdot \vec{x} }  + \text{h.c.}
$$

where $\vec{k}$ is the two-dimensional momentum vector $\vec{k}=(k_ {1},k_ {2})$. Since the space is a torus of size $L \times L$, the momentum can only take values 

$$
k_ {i} = \frac{2\pi n_ {i} }{L},\quad  n_ {i} \in \mathbb{Z}.
$$

The coefficient $c_ {k}$ is defined to be 

$$
c_ {k}  = \frac{1}{L\sqrt{ 2\omega_ {k} }},\quad  \omega _ {k}  = \sqrt{ k^{2}+m^{2} }.
$$

The canonical quantization in terms of the ladder operator is rather simple,

$$
[a_ {k} , a_ {k'}^{^{\dagger}}] = \delta_ {k,k'},\quad  \text{zero otherwise.}
$$

The free Hamiltonian is 

$$
\mathcal{H}_ {0} = \frac{1}{2} \pi^{2} + \frac{1}{2 } (\nabla \phi)^{2} + \frac{m^{2}}{2} \phi^{2},
$$

where $\pi$ is the canonical momentum. So far we have assumed that the field configuration is static so there is no contribution from the canonical momentum. Taking Eq. (1) to $\\mathcal{H}_ {0}$ we have

$$
H_ {0} = \int _ {L^{2}} d^{2}x \,  \mathcal{H}_ {0} = \sum_ {k} \omega_ {k} a_ {k} ^{\dagger} a_ {k}  + \text{Const},
$$

where the constant term is the zero point energy. 

The free vacuum is defined by $H_ {0} \left\lvert{0}\right\rangle=0$. 

The interacting Hamiltonian is defined as 

$$
\mathcal{H} (E_ {T}) = \mathcal{H}_ {0} + \mathcal{V}, \quad  \mathcal{V}=g_ {2} \mathcal{V}_ {2} + g_ {4} \mathcal{V} _ {4}+ C(E_ {T}),
$$

where 

$$
\mathcal{V}_ {n} = \frac{1}{n!} :\phi^{n}:
$$

and $:\bullet:$ denotes the normal ordering. $E_ {T}$ is the truncation energy and $C(E_ {T})$ is a counter terms which will be needed later. 

-  - -

The Hilbert space is spanned by the eigenstates of the **free** Hamiltonian, $\left\lvert{E_ {i}}\right\rangle$. In the Hamiltonian truncation approach, we only consider the the states with $E_ {i} < E_ {T}=: \Lambda$. In this case, the **full** Hamiltonian can be considered as a finite-dimensional matrix

$$
H_ {ij} := \left\langle{E_ {i}}\right\rvert H \left\lvert{E_ {j} }\right\rangle .
$$

At weak coupling, the spectrum of the truncated Hamiltonian can be computed using Hamiltonian Perturbation Theory (HPT). 

### Hamiltonian Perturbation Theory

In quantum field theory, Lagrangian perturbation theory has been dominant, especially in the study of scattering processes and elementary particle physics. This approach's explicit covariance has been crucial in implementing the renormalization program. 

The total Hamiltonian $H$ of a system is divided into two parts, 1) the unperturbed Hamiltonian $H_0$, which is solvable and represents the system in the absence of the interaction or perturbation, and 2) the perturbation Hamiltonian $H'$, which represents the interaction or perturbation that is considered small compared to $H_0$.

The idea is to treat the perturbation $H'$ as a small correction to $H_0$ and expand the observables of interest (like the energy levels or scattering amplitudes) in a power series of $H'$.

In the absence of the perturbation, the eigenstates and eigenvalues of $H_0$ are assumed to be known. *These serve as the basis for exploring the effects of the perturbation.* The corrections to the eigenvalues and eigenstates of the system due to $H'$ can be calculated iteratively. In practical calculations, Feynman diagrams (or similar diagrams) are used to visually and systematically represent the terms in the perturbation series. Each diagram corresponds to a mathematical term in the expansion and simplifies the computation of complex interactions.



### Hamiltonian truncation with UV divergence

In the paper "Exploring Hamiltonian Truncation in $d = 2 + 1$", the $\phi^{2}$ theory is analysed using different methods, including analytical, perturbative, and HT solutions, to establish the reliability of the HT method. 
