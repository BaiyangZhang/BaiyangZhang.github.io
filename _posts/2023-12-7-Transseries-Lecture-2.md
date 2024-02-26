---
layout: post
title: Introduction to Transseries Lecture 2
subtitle: 
date: 2023-12-06
author: Baiyang Zhang
header-img: img/background2.jpg
catalog: true
tags:
---

## Hahn Series

Hahn series are used in the field of `non-standard analysis`, which is a branch of mathematical logic and analysis that deals with the rigorous treatment of infinitesimals. They are named after the Austrian mathematician Hans Hahn. 

A Hahn series is a generalization of a power series where the exponents are allowed to be elements of an *ordered abelian group* rather than just integers or real numbers. This allows for more flexibility and complexity in the series. The coefficients of a Hahn series are typically taken from a field, commonly the real or complex numbers.

Hahn series introduce more flexibility in exponents, which can come from a broader class (ordered abelian groups), allowing for a more nuanced expression of asymptotic behaviors. We will talk more about this later. Hahn series also provide a framework for analyzing functions at points where traditional power series fail, such as at singularities or when considering behavior at infinity.  These tools are particularly valuable in areas like differential equations, analytic number theory, and dynamical systems, where understanding the precise behavior of functions in extreme conditions is crucial.

First, let us begin with an *ordered abelian group* ${\frak M}$, called the `monomial group` (or `value group`). Let's break it down.

To understand monomial groups, it's crucial to first clarify what a monomial is. A monomial is a product of powers of variables with *non-negative integer* exponents. For example, $x^2y$ and $z^5$ are monomials in the variables $x, y$ and $z$.

The study of monomial groups typically revolves around the operation of multiplication. This focus on multiplication rather than addition sets monomial groups apart from other algebraic structures like vector spaces or additive groups. A monomial group is simply a set of monomials closed under the operation of multiplication. Of course the group must satisfy four fundamental properties, namely closure, associativity, the existence of identity element and the existence of inverses. 

For example, the set of monomials in one variable $x$, where the exponent is a non-negative integer, forms a monomial group under multiplication. For instance, the set $\left\lbrace 1, x, x^2, x^3, \ldots \right\rbrace$ is a monomial group. The multiplication of any two elements in this set results in another element of the set, maintaining closure.

By order we mean either *totally ordered* (which is a binary relation $\leq$ that satisfies comparability, also called totality, meaning the any two elements are comparable, transitivity, reflexivity $a\leq a$ and anti-symmetry, $a\leq b$ and $b\leq a$ imply $a=b$ ) or linearly ordered (the elements can be thought of as lying on a straight line in such a way that every element has a distinct position, and you can move from one end of the line to the other, encountering each element in a definite order). Linearly ordered is the same thing as totally ordered. 

In our case, the order relation is again "far larger then" $\gg$. However, note that this is **not a totally order**, we don't require reflexivity and antisymmetry, since $a \gg a$ can not be correct. We do require comparability and transitivity though. The concept of `large` and `small` are defined with respect to identity $1$, if ${\frak g}\in {\frak M}$ and ${\frak g} \ll 1$ then ${\frak g}$ is said to be `small`, if ${\frak g} \gg 1$ the it is said to be `large`. 

In algebra, a `valuation` is a function on a field that provides a *measure of the size or multiplicity of elements of the field*. A field with a valuation on it is called a valued field. 

As a convention, we will use fraktur font, lower case for elements and upper case for sets. 

The evaluation 

$$
T: {\frak M} \to \mathbb{R}
$$

is denoted as $\mathbb{R}^{ {\frak M} }$. $T$ can be regarded as a function defined on ${\frak M}$ with value in $\mathbb{R}$. For ${\frak g} \in {\frak M}$, we also write $T[{\frak g}]$ for the value of $T$ at ${\frak g}$, we don't use round parenthesis since $T(x)$ is reserved for another use. 

The `support` of a function $T \in \mathbb{R}^{ {\frak M} }$ is the collection of ${\frak g}$ on which $T$ is non-zero, 

$$
\text{supp} (T) := \left\lbrace {\frak g}\in {\frak M} \,\middle\vert\, T[{\frak g}]\neq 0 \right\rbrace .
$$

This definition is in agreement with that in real analysis, where the support of a function is defined as the closure of the set where the function is non-zero. Here we don't talk about closeness... yet. 

Let ${\frak A}$ (Gothic A) be a subset of ${\frak M}$ and $\text{supp}(T) \subseteq {\frak A}$. We say $T$ is supported by ${\frak A}$. ${\frak A}$ is in general bigger a set then the actual support of $T$. 

Since we are interested in series, we will in general write $T$ as a *formal* combination of group elements,

$$
T = \sum_ { {\frak g} \in {\frak A} } a_ { {\frak g} }\cdot {\frak g}.
$$

Here is the peculiar part: the value of $T[{\frak g}]$ is $a_ { {\frak g} }$. If ${\frak g}\notin {\frak A}$ then $T[{\frak g}]=0$. 

Such $T$ is called `Hahn series` or `generalized power sereis`.

As one might guess, a constant $c$ in a Hahn series is a regular constant in $\mathbb{R}$. That is, $T$ is a constant if

$$
T[1] = c, \quad  T[{\frak g}] =0 \;\forall\; {\frak g} \neq 1.
$$

since $c$ can be regarded as $c$ multiply $1$ which is an element of ${\frak M}$, $c = c \cdot 1 \in T$. 

if ${\frak m} \in {\frak M}$, then $1 \cdot {\frak m} \in \mathbb{R}^{ {\frak M} }$ is called a `monomial` and identified with ${\frak m}$. That is, $T$ is a monomial if

$$
T[{\frak m}] = 1, \quad  T[{\frak g}] =0 \text{ otherwise.}
$$

In all cases of interest to us, *the support will be well ordered* with respect to $\ll$. That is, for 

$$
{\frak A} \subset \text{supp} (T), \quad  {\frak A} \neq \emptyset ,
$$

there exist a maximal element in ${\frak A}$. To be specific, this should be called "converse well ordered" since well order usually implies that every non-empty subset has a *smallest* element under the given order. But we will continue using "well order" to save some breath. 

Now, consider non-zero terms in $T$. Let's pick out the larges monomial ${\frak g}_ {\text{max} }$, then it is called the `magnitude`of $T$, $\text{mag}(T)={\frak g}_ {\text{max} }$. The corresponding coefficient is called the `leading coefficient`. The coefficient and the monomial put together is called the `dominance` of $T$, $\text{dom}(T)=a_ { {\frak g} } \cdot {\frak g}$ where ${\frak g}$ is ${\frak g}_ {\text{max} }$. We say $T> 0$ if $a_ { {\frak g} }> 0$ and $T<0$ if $a_ { {\frak g} } < 0$. We say $T$ is small if all its monomials ${\frak g} \in \text{supp}(T)$ are small or zero, equivalently $T$ is small if the magnitude of $T$ is small or zero. We say $T$ is large if the magnitude of $T$ is large, other terms in $T$ could be small. However, if all the monomials in $T$ are large then $T$ is said to be purely large. A pure large Hahn series does not have a single small monomial. 

Note that here our usage of terminologies might be different from others. 

Let's take a look at an example. Let 

$$
A = 3 e^{x} + 4x^{2},
$$

then 

$$
\text{mag} (A) = e^{ x }, \text{dom}(A) = 3e^{ x },
$$

$A$ is positive and large, further more $A$ is purely large since $x^{2} \gg 1$ at $x\to \infty$. 

The addition and scalar multiplication are defined in the obvious way. 

- - -

Note the difference between two distinct concepts: *larger than* and *far larger than*. Given two generalized power series $S$ and $T$, we say $S$ is larger than $T$ if $S-T >0$, in the usual sense. However, when we sat $S$ is `far larger than` $T$, written as $S \gg T$, we are comparing the *magnitudes* of them, or equivalently the absolute value of them; i.e. $S \gg T$ iff $\text{mag}(S) \gg \text{mag}(T)$. It does not matter whether the sign of the dominance (the largest term) is positive or negative. 

We say $S$ is `comparable` to $T$, written as $S \approx T$ (other symbols are possible), if $S$ and $T$ have the same magnitude. Further, if they have the same dominance then we say $S$ is `asymptotic` to $T$, written as $S \sim T$. 

**Examples.**

$$
\begin{align*}
-3e^{ x }+4x^{2} &\gg  x^{9}\\
-3e^{ x }+4x^{2} &\approx 7e^{ x }+x^{9} \\
-3e^{ x }+4x^{2} &\sim -3 e^{ x }+x^{9}.
\end{align*}
$$

#### The Two Canonical Decompositions

Next we introduce so-called `canonical decompostion`, which refers to a specific way of breaking a generalized power series into simpler parts. 

Transseries are formal objects that generalize power series to include not only powers of a variable (like $x, x^2, x^3, \ldots$) but also exponentials (like $e^x, e^{-x}$), logarithms (like $\log(x)$), and compositions of these functions. The canonical decomposition of a transseries involves splitting it into distinct parts that reflect its different asymptotic behaviors. 

The purpose of this decomposition is to simplify the analysis of the transseries by studying each of its simpler components separately. This is particularly useful in asymptotic analysis, where the behavior of a function as it approaches a certain limit (like $x \to \infty$, as we assumed throughout this note) is of interest. 

`Canonical Additive Decomposition.` Every Hahn series $A$ can be decomposed *uniquely* into a purely large part $L$, a constant $c$ and a small part $S$, 

$$
A = L + c + S.
$$

Recall that "large" and "small" are in comparison to $1$. 

The multiplication between Hahn series follow the same rules as that between regular power series. As a result it also satisfies the convolution rule, let $A = \sum a_ { {\frak g} }{\frak g}$ and $B=\sum b_ { {\frak g} }{\frak g}$, then

$$
(AB)[{\frak g}] = \sum_ { {\frak mn}={\frak g} }a_ { {\frak m} }b_ { {\frak n} }.
$$

Hans Hahn had shown that (1907) the set of all $T\in \mathbb{R}^{ {\frak M} }$ is an associative, commutative algebra over $\mathbb{R}$ with only one condition: the support is well-ordered. Actually, ever better, it is a field! 


