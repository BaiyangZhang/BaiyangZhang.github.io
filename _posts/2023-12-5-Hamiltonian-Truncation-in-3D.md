---
layout: post
title: " Hamiltonian Truncation in 3D"
subtitle: 
date: 2023-12-05
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
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
$$ \frac{\partial \phi_i}{\partial t} = \frac{\delta \mathcal{H}}{\delta \pi_i}, $$
$$ \frac{\partial \pi_i}{\partial t} = -\frac{\delta \mathcal{H}}{\delta \phi_i}, $$
where $\frac{\delta}{\delta \phi_i}$ and $\frac{\delta}{\delta \pi_i}$ represent functional derivatives with respect to the field $\phi_i$ and its conjugate momentum $\pi_i$, respectively. 

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

## Hamiltonian Truncation

### Definitions

The starting point of defining a quantum field theory is the choice of a manifold $M$ of dimension $d$. We mostly (but not always) regard the manifold as a Riemannian manifold with a **smooth** metric on it. The manifold may or may not have boundaries, if it does then some additional information is needed at the boundaries to define the theory.

Having defined the manifold $M$, the next ingredient is the choice of objects to consider over $M$, the so-called "degree of freedoms", or `fields`. Now it is helpful to adopt a statistical viewpoint toward QFT,  in order to extract the information about physical observables we need "just" to know the partition function, which is obtain via a so-called path-integral. That is, we integrate all the possible field configurations with a weight, which is essentially given by the exponent of the action. For example, we may consider a principal bundle with a connection over $M$. In physics terminology the choice of the connection is the same as picking a gauge field. We may also be considering the section of a vector bundle over $M$, these fields are sometimes called the `matter field`. 

As another example of QFT we may consider the space of maps
$$
X: M\to N
$$
where $N$ is some `target` manifold. 