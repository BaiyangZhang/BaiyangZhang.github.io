---
layout: post
title: The Poincare Duality
subtitle: 
date: 2023-10-26
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

### Introduction

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

#### Review of homology

*Induced homomorphism in homology*

In homology theory, an induced homomorphism is a function between homology groups that is naturally derived from a continuous function between topological spaces. In other words, if you have a **continuous** function $f: X \to Y$ between two topological spaces $X$ and $Y$, then this function will "induce" a homomorphism $f_ *: H_ n(X) \to H_ n(Y)$ between the homology groups of $X$ and $Y$.

The induced homomorphism has the following properties:

1. **Functoriality:**
   - If $f: X \to Y$ and $g: Y \to Z$ are continuous functions, then $(g \circ f)_  \ast = g_  \ast \circ f_ \ast$.
   - If $id_ X: X \to X$ is the identity function, then $(id_ X)_ \ast = id_ {H_ n(X)}$.

2. **Preservation of Homologous Cycles:**
   - If two cycles are homologous in $X$, then their images under $f_ *$ will be homologous in $Y$.

Mathematically, if $f: X \to Y$ is a continuous map, then for each non-negative integer $n$, there is an induced homomorphism:
$$
f_ \ast: H_ n(X) \to H_ n(Y)
$$
The induced homomorphism is defined by taking a homology class $[z]$ in $H_ n(X)$ and mapping it to the homology class $[f(z)]$ in $H_ n(Y)$, where $f(z)$ is the image of the cycle $z$ under the map $f$. This can be expressed as:
$$
f_ \ast([z]) = [f(z)]
$$
The concept of induced homomorphisms allows us to study how the topological properties of spaces are related through continuous functions.

**Relative homology groups**

The notation $H_ k(M, N; R)$ denotes the $k$-th relative homology group of a pair of topological spaces $(M, N)$ with coefficients in a ring $R$. Here, $M$ is a topological space, $N$ is a subspace of $M$, and $R$ is a ring (commonly $\mathbb{Z}$ for integer coefficients or $\mathbb{Q}$ for rational coefficients).

Relative homology groups are a generalization of homology groups that allow us to study the topology of a space relative to a subspace. The $k$-th relative homology group $H_ k(M, N; R)$ measures the $k$-dimensional holes in $M$ that are not in $N$, with the homology classes represented with coefficients in the ring $R$.

The definition of the $k$-th relative homology group involves the following steps:

1. **Chain Complex:**
   Consider the chain complex of $M$ and the chain complex of $N$ with coefficients in $R$. These are sequences of $R$-modules and boundary homomorphisms that capture the $k$-dimensional simplices in $M$ and $N$, respectively.

2. **Quotient Chain Complex:**
   Form the quotient chain complex $C_ k(M, N; R) = C_ k(M; R) / C_ k(N; R)$.

3. **Boundary Homomorphisms:**
   Define boundary homomorphisms $\partial_ k: C_ k(M, N; R) \to C_ {k-1}(M, N; R)$ on the quotient chain complex.

4. **Homology Group:**
   Finally, the $k$-th relative homology group $H_ k(M, N; R)$ is the quotient group of cycles modulo boundaries in the quotient chain complex.

### Mikio Nakahara's approach

In Nakahara's textbook, he approached Poincare duality (Chapter 6, *DE RHAM COHOMOLOGY GROUPS*) as the following. 

First he defined the "standard" version of everything, a standard space is just an Euclidean space $\mathbb{R}^{n}$, a standard n-simplex is a generalization of a triangle to n-dimensional space. To define it more formally, a standard $n$-simplex is a set of points $\{v_ 0, v_ 1, \ldots, v_ n\}$ in $\mathbb{R}^{n+1}$ such that:
1. Each $v_ i$ is a standard basis vector. This means that it has a 1 in the $i$-th coordinate, and 0 in every other coordinate. For example, in $\mathbb{R}^3$, the second standard basis vector is $(0, 1, 0)$.
2. The convex hull of these points is the standard $n$-simplex. Mathematically, this is defined as:
$$
\overline{\sigma}_ {r} := \left\{\sum_ {i=0}^n t_ i v_ i \,\mid \, \sum_ {i=0}^n t_ i = 1 \text{ and } 0 \leq t_ i \leq 1 \text{ for all } i\right\}.
$$

Here are a few examples of standard simplices:
- The standard 0-simplex is a single point.
- The standard 1-simplex is a line segment.
- The standard 2-simplex is an equilateral triangle.
- The standard 3-simplex is a regular tetrahedron.

Then Nakahara goes on to define the integral of a n-form on a standard n-simplex. Here you don't need to worry about things such as orientation, volume element (without $\sqrt{ \left\lvert g \right\rvert }$ since is it trivial), nice and simple. He uses *singular* instead of *simplicial* complex to study the topology of a manifold $M$. After defining the *chains, cycles and boundaries* (the basic building blocks of homology), Nakahara defined what a homology group is. It is just the classes of cycles up to boundaries,
$$
B_ {r}(M;\mathbb{R}) :=  Z_ {r}(M;\mathbb{R}) / B(M;\mathbb{R})
$$
where $\mathbb{R}$ denotes the coefficient of the homology group, could be replaced by $\mathbb{Z}_ {2}$ or other groups. 

Recall that Nakahara defined standard simplex $\overline{\sigma}$ and a generic, non-standard simplex $\sigma$ (without the bar) on $\mathbb{R}^{n}$. Mapping continuously a generic simplex $\mathbb{R}^{n}$ to $M$ you have the singular simplex on $M$, singular since the map might be without a inverse. Now we can do integral not only on r-simplexes on $\mathbb{R}^{n}$ but also on r-chains on the manifold $M$, by pulling back the form to be integrated on $M$ to $\mathbb{R}^{n}$, then make use of the linearity of integrals. By the end of the first section, Nakahara introduced the Stokes' theorem. 

In the second section about de Rham cohomology, Nakahara first introduced counterparts of cycles and boundaries of differential forms, namely 
$$
\text{cycles} \longleftrightarrow \text{cocycyles = closed forms}
$$
and 
$$
\text{boundaries} \longleftrightarrow \text{coboundaries = exact forms.}
$$

The boundaries also form vector spaces with $\mathbb{R}$-coefficients. Then the de Rham cohomology group was introduced as the quotient 
$$
H^{r} (M; \mathbb{R}) = \text{Closed forms} / \text{Exact forms}.
$$

All this could be better illustrated using a complex chain maybe, but that's not Nakahara's approach, maybe considering the physics backgrounds of the readers. By the end of the section he introduced the de Rham's theorem, which we already covered in another note under the name "de Rham ...".

In section 6.3, Nakahara introduces a lemma that can help to decide when is a closed form also exact, we have already covered this again in another note talking about Poincare's `potential`. Roughly speaking, on a patch $U\subset M$, if $U$ is contractible to a point, then a closed form defined on it is exact. *Any closed form is exact at least locally.* The de Rham cohomology group is regarded as an obstruction to the global exactness of closed forms.

In section 6.4, Nakahara starts with Poincare duality, which is the topic of our note today. We will take more time to explain it here.

- - -

Let $M$ be a $m$-dimensional *compact* m-dimensional manifold and let $\omega \in H^{r}(M)$ and $\eta \in H^{m-r}$. Noting that $\omega \wedge \eta$ is a volume element, so we can construct an inner product
$$
\left\langle \omega,\eta \right\rangle := \int _ {M} \, \omega \wedge \eta.
$$
The inner product $\left\langle -,- \right\rangle$ is a map that takes an element from $H^{r}$ and $H^{m-r}$ to a number. This map is both linear (obviously) and non-singular, meaning that if $\omega \neq 0$ then $\left\langle \omega,\eta \right\rangle$ can't be zero for all $\eta$. That makes the relation between $H^{r}$ and $H^{m-r}$ a `duality`.

According to Nakahara, this is called the `Poincare duality`. The problem is that, the Poincare duality defined here is between two cohomology groups, in the meanwhile the Poincare duality I read about from somewhere else is between homology and cohomology, between $H_ {r}$ and $H^{m-r}$. Maybe the missing connection between $H_ {r}$ and $H^{r}$ is given by the de Rham theorem? To answer this I'll keep reading Hatcher's textbook.

- - -

After introducing the Poincare duality, Nakahara introduces the cohomology ring where the role of production is played by wedge. Note that this is a ring regarding cohomology, not the differential forms themselves. This is one big difference between homology and cohomology, that we can define a sensible product for cohomology but not for homology. But I am not sure if this statement only applies to de Rham cohomology or to any cohomology.

At the end of this chapter, Nakahara talked about Kunneth formula, which tells 






