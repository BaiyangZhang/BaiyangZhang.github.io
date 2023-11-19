---
layout: post
title: Higher Homotopy Groups
subtitle: Why is the alternating sum of Betti numbers equal to the Euler characteristic?
date: 2023-11-18
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Minkowski
  - Frankel
---
## $\pi_ {k}(M)$

All maps considered in this chapter are supposed to be continuous. 

Consider a map $f$ from $k$-sphere to $n$-dimensional manifold $M$. We shall always ask that some distinguished point on the sphere , the “north pole”, be sent into a distinguished base point, written $\ast$ in $M^{n}$.

For technical reasons we consider the $k$-sphere to be the $k$-cube, denoted $\mathbb{I}^{k}$. In other words
$$
\mathbb{I}^{k} := [0,1] \times \dots \times [0,1],\quad k\text{ of them}.
$$
**The entire boundary $\partial \mathbb{I}^{k}$ identified with a single point**, the north pole. This choice of cubic make it much easier to talk about, for example, the composition of two maps. 

We assume the reader is already familiar with the basic concepts of homotopy group, such as how we compose two elements of a homotopy group, etc. 

The commutivity that two elements of homotopy group is shown in the figure below. 

![commutivity](/img/homotopyCommute.png)

Note that this procedure will not work in the case $n = 1$; there is no room to maneuver. This is why the fundamental group **$\pi_ {i}$ can be nonabelian**.

## Homotopy Groups of Spheres

Now let's talk about $\pi_ {k}(\mathbb{S}^{n})$. First consider the case $k<N$. 

It seems evident that $f(\mathbb{S}^{k})$ cannot cover all of $\mathbb{S}^{n}$ if $k < n$ but this is actually false since we **do not require our maps to be smooth**! Peano constructed a curve, a **continuous** map of the interval $[0, 1]$, whose image filled up an entire square $[0, 1] \times [0, 1]$! 

It is a fact that a continuous map of a sphere into an $M^{n}$ is homotopic (via approximation) to a smooth one. 
To be specific, the **approximation Theorem** states that any *continuous* map between *smooth manifolds* can be approximated arbitrarily closely by a smooth map. In more technical terms, for any continuous map $f$ and any $\epsilon>0$, there exists a smooth map $g$ such that the distance between $f(x)$ and $g(x)$ is less than $\epsilon$ for all $x$. Hence a continuous map $f: \mathbb{S}^{k} \to M$ can be approximated by a smooth map $g$. Moreover, $f$ and $g$ are homotopic, as there exists a continuous deformation (homotopy) from $f$ to $g$. This homotopy essentially 'smoothens' out the irregularities in $f$ to transition it into the smooth map $g$.

Hence we may assume that $f (\mathbb{S}^{k})$ does not cover all of $\mathbb{S}^{n}$ when $k < n$. Suppose then the south pole is not covered, then we can push the image from the south pole, we can push the entire image to the north pole. We have deformed the map into a constant map. Thus 
$$
\pi_ {k}(\mathbb{S}^{n}) =0 \text{ if } k<n.
$$

Consider the case $k=n$. We know that homotopic maps of an $n$-sphere into itself have the same degree. A theorem of Heinz Hopf says in fact that maps of any *connected, closed, orientable* $n$-manifold $M$ into an $n$-sphere $\mathbb{S}^{n}$ are homotopic *if and only if they have the same degree* (the proof is nontrivial). Thus
$$
\pi_ {n}(\mathbb{S}^{n}) = \mathbb{Z}.
$$

## Exact Sequences of Groups

A sequence of groups and homomorphisms 
$$
\dots \to F \xrightarrow{f} G \xrightarrow{g} H \to \dots
$$
are said to be `exact` at $G$ if the kernel of $G$ coincides with the image of $f$,
$$
\text{ker }g = \text{img }f.
$$
In particular, we must have that the composition $g\,\circ\,f$ is the trivial homeomorphism sending all of $F$ into the identity element of $H$. The entire sequence is said to be exact if it is exact at each group. $0$ will denote the group consisting of just the identity (if the groups are *not abelian* we usually use $1$ instead of $0$).

**Some Examples.**

If
$$
0\xrightarrow{f} H \xrightarrow{g} G
$$
is exact at $H$ then the image of $f$ coincides with the kernel of $g$. However the image of $0$ is the identity in $H$ alone, it means that the kernel of $g$ is the identity, nothing else. Then $g$ is injective, namely $1:1$. And since $g$ is $1:1$, we may identify $H$ with its image; in other words, we may consider $H$ to be a *subgroup* of $G$! We would simply write 
$$
0 \to H \xrightarrow{g} G.
$$

If 
$$
H\xrightarrow{h}G\xrightarrow{g} 0
$$
is exact then the image of $h$ is the kernel of $g$, which is the whole $G$. So $h$ is onto. Again we would forget about $g$. 

If 
$$
0 \to G\xrightarrow{h}H \to{}0
$$
is exact, $h$ is both $1:1$ and *onto*, then $G \cong H$. 

Consider an exact sequence of three nontrivial abelian groups, the so-called `short exact sequence`
$$
0 \to F \xrightarrow{f}G \xrightarrow{g}H \to 0
$$
then the kernel of $g$ is the image of $f$, which is considered the subgroup of $G$, 
$$
F \cong f(F) \subset G
$$
and $g$ is onto. Then
$$
H \cong  \frac{G}{F}.
$$
![](/img/shortExactSequence.png)

