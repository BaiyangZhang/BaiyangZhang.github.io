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

Let $X$ be a Riemann surface and $(U_ {p},\phi_ {p})$ an coordinate patch of $X$ containing a point $p$ in it. A `coordinate system` of $X$ is a map $X\to \mathbb{C}$. Note that a map of inverse direction $\mathbb{C} \to X$ would be called a `parametrization`. A coordinate system can be considered a function on $X$ that varies particularly, reflecting the fact that we use the function defined on the space to study the geometry of the space, a manifestation of the duality between geometry and algebra.

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

- - -

**Why the name divisor?**

Just as a number's divisor evenly divides the number, the divisors in complex analysis are related to the "division" of functions by their zeroes and poles. A zero of a function can be thought of as a point where the function 'divides' by the variable, whereas a pole is where the division becomes singular or undefined. To be more specific, a zero of a function $f(z)$ is a point $a$ in the complex plane where $f(a) = 0$. Metaphorically, this can be seen as the function $f(z)$ being "divisible" by the factor $(z - a)$. For example, if $f(z) = (z - a)g(z)$, where $g(z)$ is another function, then $f(z)$ has a zero at $z = a$. Here, $(z - a)$ is like a 'divisor' for the function $f(z)$, similar to how an integer divides another integer.

On the other hand, a pole of a function $f(z)$ at a point $a$ is a place where $f(z)$ tends toward infinity as $z$ approaches $a$. In this metaphorical context, a pole can be thought of as a point where the division of the function by $(z - a)$ becomes 'singular' or 'undefined'. This is analogous to how division by zero in arithmetic is undefined. For example, consider $f(z) = \frac{1}{(z - a)}$. As $z$ approaches $a$, the function approaches infinity, signifying a pole at $a$. Here, $f(z)$ behaves as if it were the result of a 'division' by $(z - a)$, and this 'division' is undefined or singular at $z = a$.

The divisor is a formal sum of points (in the one-dimensional case, such as on Riemann surfaces) or subvarieties, each associated with an integer. This sum mirrors the way a number can be expressed as a product of its prime divisors raised to certain powers.

In summary, a zero of a function is a point where the function can be "divided" by a certain factor without issues, resulting in the function being zero. A pole, on the other hand, is where this 'division' leads to an undefined or singular situation, akin to division by zero, resulting in the function tending towards infinity. The term "divisor" carries over the essence of division and factorization from basic arithmetic to the more sophisticated settings of complex analysis (and algebraic geometry), capturing the fundamental way in which functions can be 'divided' by their behavior at certain points or subspaces.

- - -

In contrast to principal divisors, a general divisor on a manifold or variety is simply a formal sum of points (in the one-dimensional case) or more generally, of subvarieties of codimension $1$, weighted by integers. These are not necessarily associated with any particular meromorphic function.

We say two divisors are `linearly equivalent` $D \sim D'$ if their difference is a principal divisor 

$$
D - D' = (f) \text{ for some moromorphic function } f.
$$

We use the name `divisor class` to denote the linear equivalence class of a divisor.

Since principal divisors are so important, one of the main questions at this point is, which divisors are principal divisors? Phrased differently, given a divisor, are there functions with prescribed poles and zeros? The theorem of Riemann–Roch will give us the first part of the answer. 

But first, we need to define the `degree` of a divisor $\text{deg}$.

**Degree of a divisor.** Given a divisor $\text{Div}(X)$ of a Riemann surface $X$, the degree of the divisor is an integer 

$$
\text{dig}: \text{Div}(X) \to \mathbb{Z}, \quad  \sum_ {a}n_ {a} a \mapsto \sum_ {a} n_ {a}.
$$

The set of divisors of degree zero, denoted by $\text{Div}^{0}(X)$, is the set of principal divisors, since *every meromorphic function has the same number of zeros as poles* ( as a consequence of the argument principle). 

- - -

The quotient of all divisors by the principal divisors is called `Picard group` $\text{Pic}(X)$. Recall that the quotient by something is to regard the "something" as zero, so for a Picard group, we effectively treat all the principal divisors as zero. The quotient of all the zero-degree divisors $\text{Div}^{0}(X)$ by principal divisors are called the `restricted Picard group` $\text{Pic}^{0}(X)$. 

Now let's define a space of meromorphic functions using the divisor. Let $D$ be an arbitrary divisor, let 

$$
L(D) := \left\lbrace f\in \mathcal{M}(X) \,\middle\vert\, (f)\geq -D \right\rbrace .
$$

Recall how we compare to divisors, we say divisor $D>D'$ if every coefficient of $D$ is bigger than that in $D'$. 

Since $L(D)$ is defined as the set of all meromorphic functions $f$ such that the divisor of $f$ satisfies $(f) \geq -D$, this condition means that the poles of $f$ are no worse than those specified by $D$, and possibly better (fewer or lower order). For example, if $n\cdot a, a\in X$ is a term in $D$, then the $f\in L(D)$ are allowed to have order at $a$ no less than $-n$, in other words, to have poles with multiplicity $\leq n$. If $-n\cdot a$ is a term in $D$ then $f$ can only have a zero at $a$ with multiplicity less or equal than $n$. 

$L(D)$ is indeed a vector space. First, notice that it is closed under addition, if $f$ and $g$ are in $L(D)$, then $f + g$ is also in $L(D)$. The reason is that the poles of $f + g$ cannot be worse than the worst poles of $f$ and $g$ separately. Since both $f$ and $g$ have their poles controlled by $D$, so does their sum. Secondly, it is closed under scalar multiplication of a complex number, if $f$ is in $L(D)$ and $c$ is a complex number, then $cf$ is also in $L(D)$. Multiplying by a scalar doesn’t introduce any new poles, so the pole structure of $cf$ is the same as that of $f$. Thirdly, there exist the zero element, the constant function 0 is in $L(D)$ because it has no poles, thus satisfying the condition trivially. Finally, it satisfies the condition of associativity and commutativity, these follow from the standard properties of function addition and scalar multiplication.

The definition of $L(D)$ captures an essential aspect of the theory of divisors and Riemann surfaces or algebraic curves.  It relates the geometric concept of a divisor to the space of meromorphic functions. $L(D)$ can be used to study the properties of divisors and the surfaces or curves they reside on. 


- - -

Since $L(D)$ is a vector space, we can talk about the dimension of it. In some textbooks people define

$$
l(D)  := \text{dim }L(D)
$$

but we will simply write $\text{dim } L(D)$. In certain cases we are able to determine the dimension of $L(D)$ directly. 

**Example 1.** The Zero Divisor

Let's start with the simplest divisor, the zero divisor $D = 0$. The space $L(0)$ includes all meromorphic functions $f$ whose divisors $(f)$ satisfy $(f) \geq 0$. This means $f$ can only have zeros, no poles. Essentially, $L(0)$ is the space of all holomorphic functions. 

On a compact Riemann surface, the only globally defined holomorphic functions are constants (by Liouville's theorem). Thus, the dimension of $L(0)$ is 1, spanned by the constant function 1.

**Example 2.** A Divisor with a Single Simple Pole

Consider a divisor $D = p$, where $p$ is a point on the Riemann surface, indicating a simple pole at $p$. $L(p)$ consists of meromorphic functions that may have at most a simple pole at $p$ and no other poles. This includes constant functions and functions with a simple pole at $p$. Determining the exact dimension can depend on the specific Riemann surface and the point $p$. However, for a compact Riemann surface of genus $g$, a rough estimate can be given by the Riemann-Roch theorem, which we will talk about later. For a single point, the dimension often exceeds 1, but the exact number depends on the surface's complex structure.


- - -

Next, let's shortly talk about `canonical divisors`. On a Riemann surface, a canonical divisor $K$ is a divisor associated with the (holomorphic) differential forms on that surface or curve. Specifically, it is the divisor of a non-zero meromorphic differential form. Recall that, on a Riemann surface, a differential form is a complex-analytic object that generalizes the concept of functions. Holomorphic differential forms are those that are locally of the form $f(z) dz$, where $f(z)$ is a holomorphic function. The divisor of a differential form $\omega$ is defined similarly to the divisor of a function. It is a formal sum of points, where each point is weighted by the order of zero or pole of $\omega$ at that point.

The canonical divisor $K$ represents the common "pole-zero" structure of all meromorphic differential forms on the surface. If $\omega$ is a meromorphic differential form, then $K = (\omega)$, the divisor of $\omega$.

A simple example is the Riemann sphere (the complex projective line $\mathbb{P}^1$). On the Riemann sphere, consider the differential form $dz$. This form is holomorphic everywhere on the complex plane, which is part of the Riemann sphere. In this case, the canonical divisor $K$ is actually associated with a negative order (a pole) at infinity. This might seem a bit counterintuitive, but it reflects the fact that there are no non-trivial holomorphic differential forms on the Riemann sphere. In simpler terms, $K$ is the divisor corresponding to the differential form $dz$ with a pole of order $2$ at infinity, often denoted as $-2 \cdot [\infty]$.

The fact that the differential form $dz$ has a pole at infinity can be better understood by considering the behavior of $dz$ under a change of coordinates that maps the neighborhood of infinity to a neighborhood of zero, namely the stereographic projection. Recall that under this projection, the north pole of the sphere maps to the point at infinity in the complex plane. To analyze the behavior at infinity, we introduce a new coordinate $w$ such that $w = 1/z$. In this new coordinate, the point $z = \infty$ corresponds to $w = 0$. In the $w$-coordinate, the differential $dz$ transforms as

$$
dz = -\frac{1}{w^2} dw
$$

This comes from the derivative of $z$ with respect to $w$, noting that $z = 1/w$, so $dz/dw = -1/w^2$. Now it is obvious that $-dw/w^2$ has a pole of order $2$ at $w = 0$. 


- - -

The Riemann-Roch theorem is a fundamental result in the field of algebraic geometry and complex analysis, particularly regarding the study of Riemann surfaces. This theorem provides deep insights into the relationship between the **geometry** of a curve and the **algebraic** properties of divisors, and line bundles associated with it. 

For a compact Riemann surface, the Riemann-Roch theorem gives a formula to compute the **dimension of the space of meromorphic functions** associated with a given divisor. The theorem is stated as follows:

**Riemann-Roch Theorem.** If $D$ is a divisor on a compact Riemann surface, then

$$ \text{dim } L(D) - \text{dim } L(K - D) = \text{deg}(D) - g + 1 $$

where $K$ is the canonical divisor, associated with the differential forms on the surface, $\text{deg}(D)$ is the degree of the divisor $D$ and $g$ is the genus of the Riemann surface.

The Riemann-Roch theorem links the geometric properties of Riemann surfaces (like genus) with the algebraic properties of divisors and function spaces. Also, it provides a powerful tool for understanding the behavior of divisors and line bundles on Riemann surfaces. This includes determining the number of independent meromorphic functions or sections of line bundles with certain properties. The theorem laid the groundwork for further developments in algebraic geometry, including sheaf cohomology and modern intersection theory.

As an example, consider the zero divisor $D$ with $\text{deg}(D)=0$. Then the theorem says

$$
1-\text{dim } L(K) = -g+1 \implies \text{dim }L(K) = g.
$$