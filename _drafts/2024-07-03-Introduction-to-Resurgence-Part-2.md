---
layout: post
title: Introduction to Resurgence Part 2
date: 2024-06-26
author: Baiyang Zhang
catalog: true
tags: resurgence
---

# An Example: Euler's Equation


As an mathematical example of the application of resurgence method, let's consider the Euler's equation,

$$
x^{2}f'-x+f=0
$$

and look for the solution of $f(x)$ on $\mathbb{R}$. This equation can be solved using the method of **integrating factors**, but we try to solve it using the method of power series. Assume the solution is of form

$$
f = \sum_ {k=0} a_ {k} x^{k},
$$

substitute this to the equation and compare terms order-by-order, we get the following relation:

$$
\begin{align*}
a_ {0}&= 0, \\
a_ {1} &= 1, \\
(k-1) a_ {k-} &= -a_ {k} \text{ for } k\geq 2.
\end{align*}
$$

Solving it we get 

$$
a_ {k} = (-1)^{k-1}(k-1)!,
$$

nice and simple. The only problem is that, the power series defined by it diverges for any $x$:

$$
f(x) = \sum_ {k=0}^{\infty} (-1)^{k} k!x^{k+1},
$$

Also, we know that the solution of first order differential solution should have a constant of integral, which is a free parameter. But here we found no trace of it. 

It turns out that, the method of power series can only find solutions that has a sensible Taylor expansion. Note that this method is aimed at finding the recursive relation between the coefficients of the power expansion of the possible solution, what if the solution has no sensible power expansion in the first place? It is not impossible, for some function are themselves well-defined, but indeed has trivial Taylor expansion about certain points. The most famous example of such functions, sometimes called non-perturbative, is $e^{ \bullet/x }$ at $x=0$, where $\bullet$ is any constant. We will see that the (family of) solutions that we are missing is indeed of such form. 

The homogenous form of the Euler equation read 

$$
x^{2}g' +g=0,
$$

its solution has form 

$$
g(x) = a e^{ 1/x }, \quad  a = \text{const}.
$$

Hence the general solution to the Euler equation is 

$$
f = \sum(\cdots) + g(x) = \sum(\cdots) + a e^{ 1/x },
$$

now $a$ is the missing constant of integral we are looking for.

Now the crisis of divergence still remains. This prolem can not be solved by shifting the point about which we expand the power series. In the previous case we are expanding about $x_ {0}=0$, have we changed it to $x_ {0}=c$ for some number $c$ would not render the power expansion to be convergent. To tackle the problem we must do something more radical. It is called the Borel resummation. 

 - - -

There are many approaches to resumming divergent series, such as Abel summation, Cesaro summation, $\zeta$-function regularization, etc. The method that is appropriate for our setting was introduced by Emile Borel in 1899, and is therefore called `Borel summation`.

