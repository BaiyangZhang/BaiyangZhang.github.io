---
layout: Note on Carl Bender's Lecture on Asymptotic Series
title: 
date: 2024-08-26
author: Baiyang Zhang
catalog: true
tags:
---

# Talk 1

Say, we want to solve the following equation perturbatively:

$$
x^{5}+x=1.
$$

Perturbation theory is usually done in three steps:

1. Introduce a small variable $\epsilon$, it could be taht when $\epsilon=1$ we recover the original problem;
2. At small $\epsilon$ the original problem is simplified enough to be solvable, the answer is a power expansion of $\epsilon$;
3. Setting $\epsilon=1$ and recover the approximate answer to the original problem. 

In our example, we can make $x$ to be the perturbation, introducing an $\epsilon$ to make the equation look like

$$
x^{5} +\epsilon x=1
$$

so that when $\epsilon=1$ we rocover the original problem. The solution at $\epsilon=0$ is $x=1$, well at least one of the solution. We next expand $x$ in a powe series of $\epsilon$, writine $x=1+\sum_  {i\geq1}c_  {i}\epsilon_  {i}$, substitute it into the equation and work out the coefficients. This works pretty neatly.

However there is another way to introduce the $\epsilon$-parameter, that is to put it in the $x^{5}$ term:

$$
\epsilon x^{5} + x=1,
$$

at $\epsilon=0$ the solution is also $x=1$, but if you next expand $x$ in a power series of $\epsilon$, you'll find that this perturbaton theory does not work at all at $\epsilon=1$. Why?

It is because if you put $\epsilon$ with the $x$, the original problem and $\epsilon=0$ problem has similar behavior: they both have five roots! In a sense the perturbation theory is "continuous" at the origin, $\epsilon=0$. But if you put $\epsilon$ with $x^{5}$, then when $\epsilon=0$ there are only one root, but for nonzero $\epsilon$ there will be five, there is a disrupt jump in the number of solutions, this hints the poor behavior of the perturbation theory.

- - -

Carl Bender said "nothing is ever asymptotic to zero", but isn't a lot of things asymptotic to zero, like $e^{ -1/x }$? 

$x\ll y$ in our context means $x$ is negligible compare to $y$. 

As $x\to x_  {0}$, if $\frac{f(x)}{g(x)}$ goes to $1$, we say $f(x)$ is asymptotic to $g(x)$ at $x_  {0}$; if $\frac{f(x)}{g(x)}$ goes to zero, we say $f(x)$ is negligible compare to $g(x)$. 

- - -

**Method of dominance balance:**

The method of dominance balance is a useful technique in the analysis of asymptotic series, particularly when dealing with differential equations or perturbation problems. This method helps identify the dominant balance between different terms in an equation, which leads to understanding the behavior of the solution in certain limits (e.g., as a parameter tends to zero or infinity).

The method of dominance balance involves the following steps:

1. Identify Relevant Terms: Start by identifying the leading terms in the equation, which usually involve different powers of $\epsilon$.

2. Balance Dominant Terms: Assume that a subset of terms will dominate in a certain limit of $\epsilon$ (e.g., $\epsilon \rightarrow 0$). Equate these terms to determine how the variables scale with $\epsilon$.

3. Check Consistency: Substitute the scaling obtained from the dominant balance back into the original equation to verify that the terms you've neglected are indeed smaller compared to the dominant ones.

4. Determine the Solution: Use the balance to simplify the equation, making it easier to solve, and obtain an asymptotic expression for the solution.

Consider a simple differential equation that arises in boundary layer theory:

$$
\epsilon y'' + y' - y = 0,
$$
where $y = y(x)$ and $\epsilon$ is a small positive parameter.

The equation has three terms: $\epsilon y''$, $y'$, and $-y$. For small $\epsilon$, let's assume $y(x)$ behaves as $y \sim e^{\lambda x}$. Substituting this into the equation:

$$
\epsilon \lambda^2 e^{\lambda x} + \lambda e^{\lambda x} - e^{\lambda x} = 0.
$$

Canceling out the exponential term (since it's non-zero), we get:

$$
\epsilon \lambda^2 + \lambda - 1 = 0.
$$

Now, let's balance the terms based on the assumption that one term might dominate. There are two possible balances:

- Case 1: Balance between $\epsilon \lambda^2$ and $\lambda$.

  Assume $\epsilon \lambda^2 \sim \lambda$, giving $\lambda \sim \frac{1}{\epsilon}$. Substituting back, we find that the neglected $-1$ term is not consistent with this balance as $\lambda$ becomes very large when $\epsilon$ is small.

- Case 2: Balance between $\lambda$ and $-1$.

  Assume $\lambda \sim 1$. Then the equation becomes $\lambda - 1 = 0$, so $\lambda = 1$, which implies that $\epsilon \lambda^2 \sim \epsilon$ is small compared to the dominant balance.

The second balance ($\lambda = 1$) is consistent since the neglected term $\epsilon \lambda^2$ is small when $\epsilon$ is small.

Thus, the leading order solution is $y(x) \sim e^x$. To refine this, we could look at higher-order corrections by considering the small terms we neglected.

As another example, consider the integral:

$$
I(\epsilon) = \int_ 0^\infty e^{-\frac{x^2}{\epsilon}} \, dx.
$$

For small $\epsilon$, we expect the main contribution to the integral to come from the region near $x = 0$.

The exponential term $-\frac{x^2}{\epsilon}$ suggests that for large $x$, the integrand decays rapidly. We balance the term inside the exponential by scaling $x$ as $x = \sqrt{\epsilon} u$, which leads to:

$$
I(\epsilon) = \sqrt{\epsilon} \int_ 0^\infty e^{-u^2} \, du.
$$

This change of variables is consistent as it simplifies the integral to a Gaussian integral that does not depend on $\epsilon$ (aside from the overall factor).

The integral $\int_ 0^\infty e^{-u^2} \, du$ is known and equals $\frac{\sqrt{\pi}}{2}$. Thus,

$$
I(\epsilon) \sim \sqrt{\epsilon} \cdot \frac{\sqrt{\pi}}{2}.
$$

This gives us the asymptotic expansion $I(\epsilon) \sim \frac{\sqrt{\pi \epsilon}}{2}$ as $\epsilon \rightarrow 0$.

# Talk 2

The below ODE

$$
y'' + a(x)y' + b(x) y =0
$$
is a linear equation, but it is fantastically difficult to solve. It can always be reduced to 

$$
\xi''+d\xi=0.
$$

This facilitates the use of method of power series.

Actually there is anothe way to work it out. Let $D$ be the differential operator, the original ODE can be written as 

$$
(D^{2}+aD+b)y(x)=0.
$$

A quadratic form can be factorized, so we in principal can write 

$$
(D^{2}+aD+b)y(x) = (D+\alpha)(D+\beta)y,
$$

where $\alpha,\beta$ are functions of $x$. Expand it we get some equations, one of which is the so-called Riccati equation, and there already exists a procedure of how to solve it. 

The problem is that this method works only for finite $x$, not the entire plane. 


