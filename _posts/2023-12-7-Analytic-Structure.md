---
layout: post
title: Analytic Structure
subtitle: 
date: 2023-12-07
author: Baiyang Zhang
header-img: img/background13.jpg
catalog: true
tags:
---

### Holomorphic and Meromorphic Functions

Let $X$ be a Riemann surface and $(U_ {p},\phi_ {p})$ an coordinate patch of $X$ containing a point $p$ in it. A coordinate system of $X$ is a map $X\to \mathbb{C}$, a map $\mathbb{C} \to X$ would be called a parametrization. A coordinate system is a function on $X$. 

Let $Y\subset X$ be a open subset of $X$. Denote the set of all holomorphic function on $Y$ by $\mathcal{O}(Y)$ or $\mathcal{O}_ {Y}$. This notation reminds us of the sheaf theory.  

Let $Y\subset X$ be an open subset, a function $f$ on $Y$ is called a meromorphic function if $f$ is holomorphic on $Y$ except on a set $A$ of isolated points, $A$ is called the set of poles. Let $p\in A$ be a pole, then
$$
\lim_{ x \to p } \left\lvert f(x) \right\rvert =\infty.
$$

*Note that the poles must be isolated points*. 

We denote the set of meromorphic functions by $\mathcal{M}(Y)$. A meromorphic function is of form 
$$
\text{meromorphic}= \frac{\text{holomorphic function }f}{\text{holomorphic function }g}
$$
thus the poles are zeros of $g$. This is true because every holomorphic function, which is not identically zero, has only *isolated* points as zeros. 

Since the meromorphic functions are quotients of holomorphic functions, we can construct the inverse of it, thus all the meromorphic functions on $Y$, or $X$ for that matter, form a `field`.

Given two Riemann surfaces $X$ and $X'$, a holomorphic function $f: X \to X'$ is a functions that is holomorphic on all the coordinate patches. If $f$ is a bijection with an inverse $f^{-1}$ which is also holomorphic, then we call $f$  an `analytic holomorphic` function. **Analytic is to holomorphism what continuous is to open sets**.

One of the most important topic is the classification of Riemann surfaces up to analytic holomorphism. 

Let $X$ be a compact Riemann surface and $f$ a global holomorphic function, then $f$ can only be a constant function. In other words, 
$$
\mathcal{O}(X) = \mathbb{C}.
$$

- - -

The Riemann sphere is a geometric model that extends the complex plane to include a point at infinity. Imagine the complex plane as a horizontal sheet. The Riemann sphere is then a sphere sitting on this plane, touching it at the origin. Every point on the complex plane is projected onto the sphere (except the point at infinity, which is represented by the top point of the sphere, or the "north pole"). This projection is typically done using stereographic projection, where each point on the complex plane is connected by a line to the north pole of the sphere, and the point of intersection on the sphere is the corresponding point. 

The one-dimensional complex projective space $\mathbb{C}\mathbb{P}^1$, or just $\mathbb{P}^{1}$ in this note, is formed by considering lines through the origin in a two-dimensional complex vector space $\mathbb{C}^2$. Essentially, you take all possible complex lines (one-dimensional subspaces) in $\mathbb{C}^2$, and each line is considered a point in $\mathbb{P}^1$. This space includes all the points of the complex plane, along with an additional "point at infinity" to account for limits along each possible direction in the complex plane.

The equivalence between these two comes from how they treat points at infinity. In the Riemann sphere, there is a single point at infinity (the north pole of the sphere), which is the limit point for all directions in the complex plane. In $\mathbb{P}^1$, each line through the origin in $\mathbb{C}^2$ corresponds to a point in projective space. Lines parallel to the complex plane (but not within it) converge to a single "point at infinity," similar to the north pole of the Riemann sphere.

Both the Riemann sphere and $\mathbb{P}^1$ provide a way to compactify the complex plane by adding a point at infinity, thus allowing for a seamless handling of limits and behaviors that would otherwise be "infinite" or "undefined" in the regular complex plane. They are different representations of the same conceptual space, with the Riemann sphere providing a more geometric and intuitive picture, while $\mathbb{P}^1$ offers a more algebraic and abstract framework.

- - -

The principal part of a meromorphic function $f(z)$ at a pole $a$ refers to the portion of the function's Laurent series that contains the terms with negative powers of $(z - a)$. Recall that a function is meromorphic on a domain if it is holomorphic throughout the domain **except for isolated poles**. For a meromorphic function near a pole $a$, you can express the function as a Laurent series. This is a series expansion that, unlike the Taylor series, includes terms with negative powers. The Laurent series for $f(z)$ around the pole $a$ can be written as:
$$
   f(z) = \sum_{n=-\infty}^{\infty} c_n (z - a)^n
$$
   where $c_n$ are the coefficients of the series.

The principal part of $f(z)$ at the pole $a$ specifically refers to the sum of the terms of the Laurent series with negative powers of $(z - a)$. This part of the Laurent series looks like:
$$
   \sum_{n=1}^{\infty} c_{-n} (z - a)^{-n}
$$

So, when we talk about the principal part of a meromorphic function $f(z)$ at a pole $a$, we're focusing on the terms in the function's Laurent series that capture the behavior of $f(z)$ as $z$ approaches $a$ and the function goes towards infinity. 

- - -

Every meromorphic function on the Riemann sphere is a rational function (i.e. the quotient of two polynomials), we write
$$
\mathcal{M}(\mathbb{P}^{1}) = \text{Quot}(\mathbb{C}[z]).
$$
To see that, take $f\in\mathcal{M}(\mathbb{P}^{1})$. $f$ has only finite many poles. Around each pole, we can separate the function into the principal part (namely the divergent part) and the holomorphic part. We can subtract the principal parts from $f$ hence obtaining a holomorphic function. But then this new function must be a constant. Then $f$ must be the quotient of two polynomials. 

## Divisor

A divisor is a formal sum that provides a way to keep track of the zeros and poles of meromorphic functions on a complex manifold (like a Riemann surface). It is especially useful in the study of complex functions, algebraic curves, and algebraic geometry. 

A divisor on a complex manifold is a formal sum of points on the manifold, with each point $p$ associated with an integer $n_p$. It is typically written as   
$$
   \text{Div} = \sum n_p p
$$
where $n_p > 0$ for a zero of order $n_p$, $n_p < 0$ for a pole of order $|n_p|$, and $n_p = 0$ means that $p$ is neither a zero nor a pole of the function in question.

Divisors are used to study the properties of meromorphic functions and to formulate concepts like the degree of a divisor, the principal divisor (associated with a meromorphic function), and to define line bundles. In the context of Riemann surfaces, divisors play a crucial role in the formulation of the Riemann-Roch theorem, which is fundamental in the intersection of algebraic geometry and complex analysis.

In short, given a Riemann surface $X$, the group of divisors $\text{Div}(X)$ is a group freely generated by points of $X$. We will denote the elements of $\text{Div}(X)$ as $D,D'$, etc. Let 
$$
D,D' \in  \text{Div}(X), \quad  D = \sum_ {a}n_ {a} a,\quad  D' = \sum_ {a} m_ {a} a,
$$
we define 
$$
D + D' = \sum_ {a}(n_ {a}+m_ {a})a.
$$
We say $D<D'$ iff $n_ {a}<m_ {a}$ for all $a$. 

For $f\in\mathcal{M}(X)$ a meromorphic function defined on $X$, and a point $a \in X$, recall that the `order` (or multiplicity) of $a$ is defined as 
$$
\text{ord}_ {a}(f) := 
\begin{cases}
0, & \text{holomorphic at } a \text{ and } f(a)\neq 0 \\
k, & \text{has a zero of multiplicity k at } a \\
-k,& \text{has a pole of multiplicity k at } a \\
\infty, & \text{identically zero.}
\end{cases}
$$

To every meromorphic function $f$ we may assign a divisor
$$
(f) := \sum_ {a} \text{ord}_ {a}(f) \cdot a.
$$
We call such divisors `principal divisors`. 

Principal divisors turn multiplication between functions into addition, similar to the exponent function. To be exact, given two meromorphic functions $f$ and $g$ we have
$$
(f\cdot g) = (f)+(g),\quad  (f^{-1} ) = - (f).
$$

Principal divisors are important because they relate the geometry of the manifold (or variety) to the algebra of its function field. A notable property is that *the sum of the orders of zeros and poles of any meromorphic function on a compact manifold is zero*, leading to the principal divisor being of degree zero (which we will talk about later).

In contrast to principal divisors, a general divisor on a manifold or variety is simply a formal sum of points (in the one-dimensional case) or more generally, of subvarieties of codimension $1$, weighted by integers. These are not necessarily associated with any particular meromorphic function.

We say two divisors are `linearly equivalent` $D \sim D'$ if their difference is a principal divisor 
$$
D - D' = (f) \text{ for some moromorphic function } f.
$$
We use the name `divisor class` to denote the linear equivalence class of a divisor.

