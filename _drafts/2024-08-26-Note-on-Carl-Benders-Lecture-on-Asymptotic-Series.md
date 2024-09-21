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

so that when $\epsilon=1$ we rocover the original problem. The solution at $\epsilon=0$ is $x=1$, well at least one of the solution. We next expand $x$ in a powe series of $\epsilon$, writine $x=1+\sum_   {i\geq1}c_   {i}\epsilon_   {i}$, substitute it into the equation and work out the coefficients. This works pretty neatly.

However there is another way to introduce the $\epsilon$-parameter, that is to put it in the $x^{5}$ term:

$$
\epsilon x^{5} + x=1,
$$

at $\epsilon=0$ the solution is also $x=1$, but if you next expand $x$ in a power series of $\epsilon$, you'll find that this perturbaton theory does not work at all at $\epsilon=1$. Why?

It is because if you put $\epsilon$ with the $x$, the original problem and $\epsilon=0$ problem has similar behavior: they both have five roots! In a sense the perturbation theory is "continuous" at the origin, $\epsilon=0$. But if you put $\epsilon$ with $x^{5}$, then when $\epsilon=0$ there are only one root, but for nonzero $\epsilon$ there will be five, there is a disrupt jump in the number of solutions, this hints the poor behavior of the perturbation theory.

- - -

Carl Bender said "nothing is ever asymptotic to zero", but isn't a lot of things asymptotic to zero, like $e^{ -1/x }$? 

$x\ll y$ in our context means $x$ is negligible compare to $y$. 

As $x\to x_   {0}$, if $\frac{f(x)}{g(x)}$ goes to $1$, we say $f(x)$ is asymptotic to $g(x)$ at $x_   {0}$; if $\frac{f(x)}{g(x)}$ goes to zero, we say $f(x)$ is negligible compare to $g(x)$. 

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
I(\epsilon) = \int_  0^\infty e^{-\frac{x^2}{\epsilon}} \, dx.
$$

For small $\epsilon$, we expect the main contribution to the integral to come from the region near $x = 0$.

The exponential term $-\frac{x^2}{\epsilon}$ suggests that for large $x$, the integrand decays rapidly. We balance the term inside the exponential by scaling $x$ as $x = \sqrt{\epsilon} u$, which leads to:

$$
I(\epsilon) = \sqrt{\epsilon} \int_  0^\infty e^{-u^2} \, du.
$$

This change of variables is consistent as it simplifies the integral to a Gaussian integral that does not depend on $\epsilon$ (aside from the overall factor).

The integral $\int_  0^\infty e^{-u^2} \, du$ is known and equals $\frac{\sqrt{\pi}}{2}$. Thus,

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

Perturbation method fails when you try to use it to solve the Schrodinger equation for anharmonic osscilator. The reason is that, in perturbation theory we put $\epsilon$ to $\phi^{4}$, the potential reads

$$
V(x)=\frac{m\omega^{2}}{2}x^{2}+\epsilon x^{4},
$$

but something abrupt happens at $\epsilon$, when $\epsilon>0$ the potential is bounded from below, but when $\epsilon\leq$ it is not. 

> Quantum mechanics is not just about a bunch of isolated eigenvalues, there is really just one energy eigenvalue, with different sheets of Riemann surface! 

# Talk 3

The different eigenvalues of a Hamiltonian can be seen as coming from different sheets of the same function! Take 

$$
H=\begin{pmatrix}
E & \epsilon \\
\epsilon  &  E
\end{pmatrix}, \quad  \epsilon \in \mathbb{C}
$$

for example. When we smoothly move $\epsilon$ in the complex plane, we can move from one eigenvalue to another!

The `Shanks transform` is a sequence transformation technique used to accelerate the convergence of a series or to sum divergent series. It’s particularly useful when dealing with slowly converging sequences.

Consider a sequence $S_ n$ that converges to a limit $S$. If the convergence is slow, applying the Shanks transform can often yield a new sequence that converges faster to $S$. The transform is defined as:

$$
S'_ n = \frac{S_ {n+1} S_ {n-1} - S_ n^2}{S_ {n+1} + S_ {n-1} - 2S_ n}
$$

Where $S'_  n$ is the transformed sequence.

The series you mentioned is the alternating harmonic series:

$$
S = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \frac{1}{5} - \frac{1}{6} + \cdots
$$

This series converges to $\ln(2)$. We can apply the Shanks transform to accelerate its convergence.

First, we calculate the partial sums of the series:

   - $S_ 1 = 1$
   - $S_ 2 = 1 - \frac{1}{2} = \frac{1}{2}$
   - $S_ 3 = 1 - \frac{1}{2} + \frac{1}{3} = \frac{5}{6}$
   - $S_ 4 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} = \frac{7}{12}$
   - $S_ 5 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \frac{1}{5} = \frac{47}{60}$

Use the Shanks formula, let's apply it to our problem and we get:

$$
S'_ 3 = \frac{-29}{72} \times \frac{12}{-7} = \frac{348}{504} = \frac{29}{42}
$$

Finally,

$$
S'_ 3 = \frac{29}{42} \approx 0.69048
$$

The actual value of $\ln(2) \approx 0.69315$.

After applying the Shanks transform, the new sequence $S'_ 3 \approx 0.69048$ is closer to the actual value $\ln(2)$ compared to the original partial sum $S_ 3 = 0.83333$. The Shanks transform effectively accelerates the convergence of the alternating harmonic series to its limit.

# Talk 4

First Bender introduced the Richardson extrapolation to accelarate the speed of convergence when summing a convergent series. 

Richardson extrapolation can be combined with the trapezoid rule when doing numerical integral. Maybe it can be applied to our project?

The rules in arithmetics that we are so familiar with, the law of associativity, commutivity, are only true **finitely**. They are not true infinitely. For exampole, Bender explained that if they were true, then the following series:

$$
1- \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots
$$

can add up to **any** numbe, such as $\pi$, $52$, etc. The law of distribution is more robust then the law of associativety and commutivity; the latter two have to do with grouping, re-arranging, while the former has to do with multiplication.

# Talk 5

`Euler summation` is a technique used to accelerate the convergence of a series, particularly when dealing with slowly converging or divergent series. The method works by transforming the original series into a new series that converges more quickly, making it useful in both theoretical and applied contexts. It works as

$$
\sum_ {i\in \mathbb{N}} a_ {n} \to \sum_ {i\in \mathbb{N}} a_ {n}  x^{n}\to f(x)
$$

then assigning the original summation (supposed divergent) to be $f(1)$. It can be used to sum, for example, $1-1+1-1+1\cdots$. 

Then Bender introduced Borel summation method, which we will not repeat here for it is already cover in author's other notes. 

- - -

Given any summation machine $\mathcal{S}$, there should be two properties that all of them should satisfy:

1. They should behave like a sum. For example, $\mathcal{S}(a_ {0}+a_ {1}+a_ {2}+\cdots)$ should be equal to $a_ {0}+\mathcal{S}(a_ {1}+a_ {2}+\cdots)$.
2. Linearity. $\mathcal{S}\left( \sum \lambda a_ {i} + \mu b_ {i} \right)$ should be equal to $\lambda \mathcal{S}\left( \sum a_ {i} \right)+\mu \mathcal{S}\left( \sum b_ {i} \right)$. 

These two properties, combined together, prove that both Euler's method and Borel's method, when applied to $1-1+1-1\cdots$, give the same result.

- - -

Why is it that when we sum infinite positive numbers, throught some summation machine it is possible to obtain a negative number? One way to think of it is to compactify the real number line into a circle using sterographic projection. When we add infinite positive numbers, the sum goes to positive infinite on the real axis, but on the compactified circle it runs to the north pole. The thing is, on a circle it is possible that as the summation continues, the sum could pass the north pole and goes through to reach the negative part of the real number circle. 

Another thing is that, the summation machine really works on a Riemann surface, with complex coordinates. Between complex numbers there is no greater or smaller than relation. 

On the complex plane, the infinity really should be regarded as a single number, unlike on the real line. one way to see that is to recall the inverse is a bijection, $z_ {1}^{-1} = z_ {2}^{-1}$ implies taht $z_ {1}=z_ {2}$, vise versa. The complex infinite is the inverse of zero, we can suggestively write 

$$
\lim_ { \epsilon \to 0 }(  \epsilon e^{ i\theta })^{-1} = \infty.
$$

For different $\theta$ we get infinity at different direction. But since different $\theta$ all goes to the same zero, and inverse map is bijective, hence infinity in different direction should all be identified as one point. So the compolex sterotype projection is not just a convenient tool but reflects the essential topology of complex plane. 

`Continued functions` are like continuted fractals. Turns out, continued exponentials $\exp(x\exp(x\exp(x\cdots)))$ has very interesting convergence behaviour, with fractal structure.

# Talk 6

An example of the connection between continued functin (exponential functions in this case) and Taylor series:

$$
e^{ ze^{ ze^{ \cdots } } } = \sum_ {n=0}^{\infty}  \frac{(n+1)^{n-1}}{n!}z^{n}.
$$

The infinite series has a radius of convergence $\frac{1}{e}$, while the continued exponential function has a much bigger area of convergence in the complex plane. 

- - -

divergent series can sometimes be turned into continued fractions which is convergent. Given a divergent asymptotic series which we can't directly sum up, we can sometimes turn it into a sequence, which makes up certain continued functions, it may be continued fraction.

An example of it is the `Pade sequence`. Pade summation seems to be quite magical. Pade doesn't have to converge on a circle too, it is smarter than power series. Pade summation can converge on a area except for a line. 

# Talk 9

The Airy's equation

$$
y'' = xy
$$

has two solutions, the airy function $Ai(x)$ and $Bi(x)$. Using the method of dominance balance, we can get a really good asymptotic behavior of them. 

Introduce the Stokes phenomenon, the Stokes wedge.Take the example of a simple function: $\sinh z$. 





# Talk 11

There is a class of functions called Stieltjes functions, 

$$
f(x) = \int_ {0}^{\infty} dt \,  \frac{\rho(t)}{1+xt}, \quad  \rho(t) \geq 0.
$$
Furthermore, the $n$-th moment of $\rho(t)$ must exist. It has the following properties:

1. $f(x)$ is analytic on the cut plane without negative real axis;
2. $f(x)\to 0$ as $x\to \infty$. 
3. At $x\to 0$, the Stieltjes functions has asymptotic series $\sum_ {i}(-1)^{n}a_ {n}x^{n}$, called Stieltjes series,
4. the negative $-f(x)$ is Herglotz, meaning that in the upper half plane the imaginary part of $f$ is positive, in the lower half plane the imaginary part of $f(x)$ is negative. The sign of the imaginary part of the function is the same as the sign of the imaginary part of the argument $x$.

Herglotz property is a very powerful property. If a function is both entire (analytic everywhere) and Herglotz, it is trivially $c x$, where $c$ is a real constant. 

- - -

The point is, if $f(x)$ have the above four properties, then $f$ is Stieltjes. 
