---
layout: post
title: Analytic Structure
subtitle: 
date: 2023-12-03
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


