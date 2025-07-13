---
layout: post
title: "Excerpt: Confinement on Narrow Cylinder Manifolds"
date: 2024-11-22
author: Baiyang Zhang
catalog: true
tags:
---

*Warning: This note is gonna be a list of concepts and conclusions. None or few explanations will be presented.*

# Representation of SU(3)

Irreducible finite-dimensional representations of SU(3) can be classified in terms of its highest weight. Since the SU(3) is simply connected, its finite-dimensional irreducible representations are in one-to-one correspondence with the finite-dimensional irreducible representations of its Lie algebra $\mathfrak{su}(3)$. 

Since SU(3) is compact, and any finite-dimensional representation of a compact Lie group is *complete reducible* (it has to do with the existence of an invariant inner product on the vector space of the representations), then all of the finite-dimensional representation of SU(3) are direct sums of irreducible representations of SU(3). 

Regard the Lie group as a manifold and the Lie algebra as the vector space at the origin of the manifold. The Lie algebra is has the following basis: 1) $H_ {1}, H_ {2}$ which form the Cartan subalgebra, 2) 

$$
\begin{align*}
X_ {1}=& \begin{pmatrix}
0 & 1 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \; 
X_ {2}= \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix}, \; 
X_ {3}= \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \\
Y_ {1}=& \begin{pmatrix}
0 & 0 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \; 
Y_ {2}= \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix}, \; 
Y_ {3}= \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
1 & 0 & 0
\end{pmatrix}.
\end{align*}
$$

The basic strategy in classifying the representations of $\mathfrak{sl}(3)$ is to simultaneously diagonalized $\pi(H_ {1})$ and $\pi(H_ {2})$, where $\pi(-)$ denotes the representation of $-$. Then their eigenvalues are the weights of a state, and their common eigenvectors are called weight vectors. 

Next we define the root system in 2-dimension. An ordered pair $\alpha=(a_ {1},a_ {2})$ is called a root if both $a_ {1},a_ {2}$ are nonzero and there exists a nonzero vector $z \in\mathfrak{su}(2)$ such that $[H_ {1},z]=a_ {1}$ and $[H_ {2},z]=a_ {2}$. The element $z$ is called a root vector. 

It means that $z$ is a simultaneous eigenvector of $\text{ad}_ {H_ {1}}$ and $\text{ad}_ {H_ {2}}$. In other words, roots are non-zero weights in the adjoint representation. For SU(3) there are six roots. All the roots form a root system, conventionally called $A_ {2}$. 

It is convenient to single out two roots corresponding to $X_ {1}$ and $X_ {2}$, they are given special names: positive simple roots. They generate all the six roots by reflection, addition and subtraction. 

- - -

Dynkin diagrams are graphical tools that classify and encode the structure of **simple Lie algebras**, **simple Lie groups**, and **root systems**. A **Dynkin diagram** is constructed based on the simple roots:

1. **Vertices**: Each vertex corresponds to a simple root.
2. **Edges**: The edges between vertices encode the angles between the simple roots $\alpha _ {i}$​ and $\alpha _ {j}$​, based on their inner product:
   
   - No edge: they are perpendicular;
   - Single edge: $\pi / 3$,
   - Double edge: 135$^{\circ}$ with a direction indicating the relative length of roots.
   - Triple edge: 150$^{\circ}$ with a direction.

# Center Symmetry and Confinement

The basic notion of confinement is that there is no **asymptotic** colored states. In QCD there is no order parameter for confinement. QCD has no deconfinement phase transition, only a cross over(no distinct order parameter exists). 

For pure Yang-Mills, there exists the deconfinement phase transition and its order parameter, which is the **Polyakov loop**. 

Center symmetry and Polyakov loop only makes sense in a Euclidean space, not Minkowski space. 

Center symmetry is a special kind of gauge transformation by $\Omega$, but $\Omega(t+L)=C\Omega$, where $C$ is an element of the center of the gauge group $G$. In other words, $\Omega$ is periodic in the compactified direction **up to the center of the group**. 

Center symmetry is indeed a symmetry of the action. 

There exists gauge invariant (hence possibly physical) observables that are **not** invariant under the center symmetry. For example the Polyakov loop. 

Physically, the vev of Polyakov loop is connected to the free energy of adding an external static color source in the fundamental representation. 

Generalized (other than fundamental representation of a group) Polyakov loops have different $n$-alities. The n-ality of a representation is how many fundamental representation one needs to combine to make the representation; i.e. the *number of boxes in the Young tableau*, modulo $N_ {c}$. Under a center symmetry transforms as 

$$
\Phi_ {n}(\vec{x}) \to  z_ {i} ^{n} \Phi_ {n}(\vec{x}),
$$

where $n$ is the `n-ality` of the representation. In a center symmetric phase (confining), Polyakov loop associated with representations having n-ality other than $n=0$ must vanish. 

Adjoint representation has $n$-ality zero. Physically, it means that putting a adjoint-color particle will induce the system to pop a gluon out of the vacuum which neutralizes it. 

That's how confinement is explain in pure Yang-Mills theory. However, it does not explain gluon confinement. It does explain quark confinement but in a theory which has no quarks.

In QCD everything breaks down. The fundamental quarks need to satisfy certain boundary conditions on the compactified direction, but center symmetry will violate the boundary condition, hence is not allowed. Center symmetry is not a symmetry for QCD.

- - -

# With Solitons

The interaction between two instantons is approximated by 

$$
S(\tau) = \pm \frac{A}{g} (e^{ -\tau }+e^{ -(\beta-\tau) })
$$

which accounts for the exponential 

For certain quantum models, the Borel-Ecalle resummation introduces ambiguity, and the instanton-instanton interaction also introduces the ambiguity, and they cancel each other. **This probably can be explain by the displacement operator!** Another question is, *if we apply the unitary transformation between vacuum and kink sector realized by displacement operator into the vacuum-instanton ambiguity cancellation, what would we find?*

