---
layout: post
title: The Poincare Duality
subtitle: 
date: 2023-10-24
author: Baiyang Zhang
header-img: img/mathArt14.jpg
catalog: true
tags:
  - math
  - quantum
  - field
  - theory
  - confinement
---

### Simplicial vs. Singular complex

I put it here not because it is really related to our discussion about Poincare duality, just because I was confused and need to make some note somewhere. If you are only interested in Poincare duality please jump to the second part directly.

A singular complex and a simplicial complex are both concepts from algebraic topology to study a space, however, they are used in different contexts and have some key differences:

Simplicial complex is a collection of simplices (points, line segments, triangles, and their n-dimensional analogues) that are glued together in a certain way. The collection must satisfy two conditions:
1. Every face of a simplex in the collection is also in the collection.
2. The intersection of any two simplices in the collection is either empty or a face of both.

On the other hand, a singular complex is not a collection of simplices, but a collection of singular simplices, which are continuous maps from the standard simplex to a topological space. Singular simplices can be used to study the topology of any space, not just those that can be decomposed into simplices.

Simplicial complexes are used in situations where *a space can be nicely decomposed into simplices*. They are useful in the study of homology and cohomology, as well as in computational topology. Meanwhile, singular complexes are used to define singular homology and cohomology, which *can be applied to any topological space*, including those that can't be nicely decomposed into simplices. Singular homology and cohomology are more general than their simplicial counterparts.

A simplicial complex has a clear geometric representation as a collection of simplices glued together. On the contrary, a singular complex doesn't have as clear a geometric representation since it consists of maps from simplices to a space, rather than the simplices themselves. Simplicial complexes are less flexible than singular complexes since they can only be used to study spaces that can be decomposed into simplices

In summary, a simplicial complex is a collection of simplices glued together in a specific way, while a singular complex is a collection of continuous maps from the standard simplex to a topological space. Simplicial complexes have a clear geometric representation and are useful in studying spaces that can be decomposed into simplices, while singular complexes are more flexible and can be used to study any topological space.

## Poincare's Duality

### Summary

Poincaré duality is a fundamental and profound concept in algebraic topology, bridging homology and cohomology, two primary tools we use to probe the topological structure of a manifold. This relationship can provide a richer understanding of the manifold's geometry and topology. 

In simple terms, Poincaré duality tells us that for a *compact*, *orientable* manifold $M$ of dimension $n$, the $k$-th homology group of $M$ is isomorphic to the $(n-k)$-th cohomology group. Mathematically, this is represented as:
$$
H_ k(M; \mathbb{Z}) \cong H^{n-k}(M; \mathbb{Z}).
$$
To truly appreciate Poincaré duality, we must first have a solid grasp of some core concepts in algebraic topology.

**1. Homology:**
   - Homology provides a way to associate algebraic objects, called homology groups, to topological spaces. These groups capture the essence of "holes" in the space at different dimensions. For example, the $0$-th homology group measures the number of connected components, the $1$-st homology group captures loops, and the $2$-nd homology group represents cavities or voids in the space.

**2. Cohomology:**
   - Cohomology, similar to homology, assigns algebraic objects, cohomology groups, to a topological space. However, instead of measuring "holes," cohomology groups measure the ways in which functions can be integrated over these "holes." Algebraically speaking, cohomology is a linear operation that turns the elements of homology into numbers.

Now, let's delve deeper into Poincaré duality. For a compact, orientable $n$-dimensional manifold $M$, we can consider a $k$-dimensional cycle $Z$ (which represents an element of the $k$-th homology group) and a $(n-k)$-dimensional cohomology class $\omega$. Poincaré duality states that we can pair $\omega$ with $Z$ to produce a number, and this pairing is *non-degenerate*. In simpler terms, for each non-zero $k$-dimensional cycle, there exists a $(n-k)$-dimensional cohomology class that "detects" it, and vice versa.

Poincare duality has profound implications for the study of manifolds. It tells us that *the topology of a manifold at small dimensions reflects its topology at large dimensions*. This symmetry provides an elegant and powerful tool for understanding the manifold's structure.

In our upcoming sections, we will explore the details.

### Review of homology

*Induced homomorphism in homology*

In homology theory, an induced homomorphism is a function between homology groups that is naturally derived from a continuous function between topological spaces. In other words, if you have a **continuous** function $f: X \to Y$ between two topological spaces $X$ and $Y$, then this function will "induce" a homomorphism $f_ *: H_ n(X) \to H_ n(Y)$ between the homology groups of $X$ and $Y$.

The induced homomorphism has the following properties:

1. **Functoriality:**
   - If $f: X \to Y$ and $g: Y \to Z$ are continuous functions, then $(g \circ f)_  * = g_  * \circ f_ *$.
   - If $id_ X: X \to X$ is the identity function, then $(id_ X)_ * = id_ {H_ n(X)}$.

2. **Preservation of Homologous Cycles:**
   - If two cycles are homologous in $X$, then their images under $f_ *$ will be homologous in $Y$.

Mathematically, if $f: X \to Y$ is a continuous map, then for each non-negative integer $n$, there is an induced homomorphism:
$$
f_ *: H_ n(X) \to H_ n(Y)
$$
The induced homomorphism is defined by taking a homology class $[z]$ in $H_ n(X)$ and mapping it to the homology class $[f(z)]$ in $H_ n(Y)$, where $f(z)$ is the image of the cycle $z$ under the map $f$. This can be expressed as:
$$
f_ *([z]) = [f(z)]
$$
The concept of induced homomorphisms allows us to study how the topological properties of spaces are related through continuous functions.

**Relative homology groups**

The notation $H_k(M, N; R)$ denotes the $k$-th relative homology group of a pair of topological spaces $(M, N)$ with coefficients in a ring $R$. Here, $M$ is a topological space, $N$ is a subspace of $M$, and $R$ is a ring (commonly $\mathbb{Z}$ for integer coefficients or $\mathbb{Q}$ for rational coefficients).

Relative homology groups are a generalization of homology groups that allow us to study the topology of a space relative to a subspace. The $k$-th relative homology group $H_k(M, N; R)$ measures the $k$-dimensional holes in $M$ that are not in $N$, with the homology classes represented with coefficients in the ring $R$.

The definition of the $k$-th relative homology group involves the following steps:

1. **Chain Complex:**
   Consider the chain complex of $M$ and the chain complex of $N$ with coefficients in $R$. These are sequences of $R$-modules and boundary homomorphisms that capture the $k$-dimensional simplices in $M$ and $N$, respectively.

2. **Quotient Chain Complex:**
   Form the quotient chain complex $C_k(M, N; R) = C_k(M; R) / C_k(N; R)$.

3. **Boundary Homomorphisms:**
   Define boundary homomorphisms $\partial_k: C_k(M, N; R) \to C_{k-1}(M, N; R)$ on the quotient chain complex.

4. **Homology Group:**
   Finally, the $k$-th relative homology group $H_k(M, N; R)$ is the quotient group of cycles modulo boundaries in the quotient chain complex.

In summary, $H_k(M, N; R)$ represents the $k$-th relative homology group of the pair $(M, N)$ with coefficients in the ring $R$. This group captures the $k$-dimensional holes in $M$ that are not in $N$, providing a powerful tool for analyzing the topology of a space relative to a subspace.
