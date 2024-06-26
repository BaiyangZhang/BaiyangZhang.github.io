---
layout:     post   				    # 使用的布局（不需要改）
title:      Basic Measure Theory Part II 				# 标题 
subtitle:    #副标题
date:       2022-10-13 				# 时间
author:     Baiyang Zhang 						# 作者
header-img: img/mathArt2.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - math
    - functionalAnalysis
    - distribution
    - measureTheory
---

# Table of Contents

- [1. Integral of Measurable Functions](#1-integral-of-measurable-functions)
- [2. Lebesgue's Dominated Convergence Theorem](#2-lebesgues-dominated-convergence-theorem)
- [3. Fubini's Theorem](#3-fubinis-theorem)
		- [3.1. Notes](#31-notes)

# 1. Integral of Measurable Functions

In what follows, we suppose that all function are measurable and defined on the measure space $(X,\mathcal{A},\mu)$. 

First we define the integral with respect to some measure $\mu$,
**Definition** Let $\phi=\sum_{i=1}^n \alpha_{i} 1_ {A_{i}}$ be a simple function; then 

$$
\int \phi \, d\mu=\sum_{i-1}^n \alpha_{i} \mu(A_{i})
$$

is called the integral of $\phi$ with respect to the measure $\mu$. 

Recall that function is simple if it is measurable and takes finite number of values, such as the step function defined on $[-1,1]$.

The integral of $\mu$ with respect to $\mu$ is finite if and only if the measure of the set where $\phi(x) \neq 0$ is finite. In other words, the measure of the support of $\phi$ must be zero. 

This definition is quite intuitive, for example, if we want to know how expensive a bag of fruit is, we just count the number of certain kind of fruit (the measure of the set), multiply it by the price (value of the function on this set), and sum over all kinds of the fruits. 

Whatever properties for integrals certainly hold for integral with respect to measure $\mu$ as well, for example 

$$
\int (\phi_{1}+\phi_{2}) \, d\mu =  \int (\phi_{1}) \, d\mu + \int (\phi_{2}) \, d\mu,
$$

I am too lazy to list all of them here.

Now we need to generalize this concept to continuous functions, say $f(x)$. Starting from the simplest case, for now we will assume $f(x)\geq 0$.

**Definition** Let $f$ be a position measurable function, then the integral of $f$ with respect to the measure of $f$ is 

$$
\int f \, d\mu = \text{sup} \int \psi \, d\mu, 
$$

where the supremum is taken over all positive simple functions $\phi$ such that $\phi<f$ everywhere. This means we are limiting function $f$ from below. $f$ is said to be $\mu$ integrable if its integral is *finite*.

$f$ is only integrable if the the set 

$$
\{ x \mid f(x) = \infty \} 
$$

is $\mu$-negligible. Note that this condition is necessary but not sufficient. 

Next we give the monotone convergence theorem without proof.

**Theorem** Monotone convergence theorem. Let $(f_{n})$ be a sequence of positive measurable functions such that 

$$
f_{n}(x) < f_{n+1}(x) \quad \forall n\in \mathbb{N} \quad \forall x\in X
$$

and 

$$
\forall x\in X \quad \lim_{ n \to \infty } f_{n}(x) = f(x).
$$

Then 

$$
\lim_{ n \to \infty } \int f_{n} \, d\mu = \int f \, d\mu.  
$$

This theorem is also called the Beppo Levi theorem. 

The integral of a positive function is only zero if the function is zero almost everywhere.

What about functions that are not positive? The solution is rather intuitive: We separate positive and negative parts and treat them both as positive functions. Given a real-valued function $f$, define 

$$
f^+ = \begin{cases}
f(x)  &  f(x) >0  \\
0  &  f(x) < 0
\end{cases}
$$

and 

$$
f^- = \begin{cases}
-f(x)  &  f(x) < 0  \\
0  &  f(x) > 0
\end{cases}
$$

where both $f^{\pm}$ are positive functions. $f$ is said to be $\mu$-integrable if both $f^+$ and $f^-$ are integrable, and the integral of $f$ is 

$$
\int f \, d\mu = \int f^+ \, d\mu - \int f^- \, d\mu.   
$$

Quite intuitive, isn't it? For complex-valued functions, we just need to treat its real and imaginary part as real functions, everything follows from that of a real-valued function. 

The interesting thing is that, as far as integral is concerned, we can neglect the sets with zero measure. Traditionally, any function has an operation called evaluation which is defined pointwise, e.g. given a real-valued function $f(x)$, we can evaluate it at point $x = x_{0}$, which gives us a real number. However, a point has measure zero, so, again, as far as integral is concerned, evaluation is not needed. You could perfectly come up with a function which can't be evaluated at some point, for instance a function at $x=x_{0}$ might not be defined, but still the function could be integrable. To say a function is $\mu$-integrable just means that $f^{+,-}$ are $\mu$-integrable respectively. 

Two functions $f,g$ has the same integral if they equal to each other almost everywhere, and this is a equivalence relation. 

The sum of a convergent series is nothing but an integral on the counting measure. Recall that give an finite set $S$ and $A \subseteq S$ then the *cardinality* of $A$ is the number of elements in $A$, sometimes denoted by $\text{Num}(A)$. Then $\text{Num}$ as a measure is called the counting measure. 

**Theorem** The set of all $\mu$-integral functions form a vector space, it is denoted by $\mathcal{L}_{\mu}^1$.

The superscript $1$ denotes the power of the function. $\mathcal{L}^2_ {\mu}$ would mean the square of the functions are integrable. This theorem is easy to verify since addition, subtraction and number-production of an element in $\mathcal{L}_ {\mu}^1$ is still in $\mathcal{L}_{\mu}^1$. 

**Theorem** If $f$ is $\mu$-integrable, so is $\lvert f \rvert$, and we have

$$
\left\lvert \int f \, d\mu  \right\rvert \leq \int \left\lvert f \right\rvert  \, d\mu.  
$$

Recall that for $f$ to be $\mu$-integrable, by definition both $f^+$ and $f^-$ are required to be finite.

A measurable function is $\mu$-integrable if and only if $\left\lvert f \right\rvert$ is $\mu$-integrable. 

If a function is Riemann integrable on $[a,b]$ then it is also Lebesgue integrable on $[a,b]$, and the two results agree. Indeed, if $f$ is Riemann integrable then we can always find two limiting step functions sandwiching $f$ from above and below, 

$$
g_{\epsilon} \leq f \leq h_{\epsilon}
$$

where $g,h _{\epsilon}$ are step functions and 

$$
\int (g_{\epsilon} - h_{\epsilon}) \, d\mu < \epsilon. 
$$

Step function are always Lebesgue integrable, plus the function is bounded, thus $f$ is also Lebesgue integrable. To summarize we have 

$$
 \text{Riemann integrable} \implies \text{Lebesgue integrable}.
$$

The inverse, however, is not necessarily true. A famous example is the Dirichlet function, defined on $[0,1]$ and 

$$
f(x) = \begin{cases}
0  &  \text{if x is rational}, \\
1  &  \text{if x is irrational}.
\end{cases}
$$

$f=1$ almost everywhere, since the Lebesgue measure of the rational numbers in $[0,1]$ is $0$. Recall that $f=1$ almost everywhere means that the set on which $f=0$ has measure zero, and this is true since $f(ratioanl)=0$ and rational numbers are countable, plus each point has zero measure, and countable many zeros are still zero. However, it is impossible to find two step function to sandwich Dirichlet function, thus it is not Riemann integrable. 

The class of Riemann integrable functions is quite restricted. Of course a continuous, bounded function on a finite interval $[a,b]$ is Riemann integrable, but being Riemann integrable actually requires less – any bounded function on $[a,b]$ which is continuous *almost everywhere* is Riemann integral. For example, the $\theta(x)$ function defined on $[-2,2]$ is continuous except at $x=0$, so it is continuous almost everywhere, thus Riemann integrable. 

E.g. The function 

$$
f: x \mapsto \frac{\sin x}{x}
$$

is not integrable with respect to the Lebesgue measure on $\mathbb{R}^+$ since $\left\lvert f \right\rvert$ is not integrable on $\mathbb{R}^+$.

We know that $\frac{\sin x}{x}$ is conditionally convergent, such notion does not exist in Lebesgue theory of integral. 

# 2. Lebesgue's Dominated Convergence Theorem

According to my mathematical friends, the dominated convergence theorem is one of the most important results of Lebesgue's integration theorem. It tells us how to deal with the limit of a sequence of functions under the integral sign, and it might be trickier than some physicist might have thought.

To understand Lebesgue's theorem we need the following lemma.

**Fatou's lemma.** Let $(f_{n})$ be a sequence of functions which are nonnegative and measurable on $(X,\mathcal{A},\mu)$. Then

$$
\boxed{
\int \lim_{ n \to \infty } \text{inf } f_{n} \, d\mu \leq \lim_{ n \to \infty } \text{inf } \int f_{n} \, d\mu . 
}
$$

The equal sign is not surprising at all, what usually surprises people is the less than sign, for Fatou's lemma tells us that if you first take pointwise limit of a sequence of functions, then integrate the limit, what you get might be less than integrate each function in the sequence and take the limit later.

To have an intuitive feeling about the lemma, consider an example where the less-than-relation holds. Consider a sequence of functions $(f_{n}),\,n\in \mathbb{N}$ defined on $\mathbb{R}$ with Borel $\sigma$-set,

$$
f_{n}(x) = 
\begin{cases}
\frac{1}{n}  &  x\in (0,n), \\
0   &  \text{otherwise}.
\end{cases}
$$

This sequence uniformly converges to zero function on $\mathbb{R}$, Thus 

$$
\int  \lim_{ n \to \infty } \text{ inf } f_{n} \, d\mu = \int_{0}^n \lim_{ n \to \infty } \text{ inf }\frac{1}{n} \, d\mu = \int 0 \, d\mu = 0,  
$$

On the other hand, the integral of $f_{n}$ on $\mathbb{R}$ is always $1$, thus

$$
\lim_{ n \to \infty } \text{ inf } \int   f_{n} \, dx = \lim_{ n \to \infty } \text{ inf } \int_{0}^{n} \frac{1}{n} \, d\mu  = \lim_{ n \to \infty } \text{ inf } 1 = 1,
$$

and $0<1$. 

The integral of a function not only depends on its pointwise value, but also the support. In this context, taking the pointwise limit of a function might give you different results because the limit procedure might give you some function value which is qualitative different, for example $\frac{1}{n}$ is qualitatively different from $0$ because there is a number that multiplies $\frac{1}{n}$ could give you $1$ but there is no such number for $0$. By taking the limit under the integral sign, we might miss the information about the support of the function, while taking the limit of the integral will not. That's why these two results could be different. 

The condition that $(f_{n})$ being non-negative is also important, it is necessary for the $\leq$ sign to hold.

To prove the lemma, define

$$
g_{n} := \underset{k\geq n}{\text{ inf }} f_{k},
$$

then $g_{n}$ is 1)measurable since $f_{n}$'s are measurable, 2) non-decreasing and 3) $g_{n} \leq f_{n}$ by construction. Properties 2) and 3) are pointwise. We have 

$$
\lim_{ n \to \infty } \int g_{n} \, d\mu = \int \lim_{ n \to \infty } \text{ inf } f_{n} \, d\mu,  
$$

Where we have interchanged the order of $\lim_{ n \to \infty }$ and $\int  \, d\mu$. This is allowed since both sides are $<\infty$. Since $g_{n} \leq f_{n}$, we have 

$$
\int g_{n} \, d\mu \leq \int f_{n} \, d\mu \implies \lim_{ n \to \infty } \int g_{n} \, d\mu \leq \lim_{ n \to \infty } \int f_{n} \, d\mu = \lim_{ n \to \infty } \text{ inf } \int f_{n} \, d\mu.   
$$

The lemma follows.

**Theorem** Lebesgue's dominated convergence theorem. Let $(X,\mathcal{A},\mu)$ be a measure space, let $(f_{n})$ be a sequence of measurable functions from $X$ to $\mathbb{R}$ or $\mathbb{C}$ that converge to $f$ almost everywhere. If there exists $\mu$-integral function $g$ such that, for all positive integers $n$, $\left\lvert f_{n} \right\rvert \leq g$, then

$$
\lim_{ n \to \infty }  \int f_{n} \, d\mu = \int f \, d\mu. 
$$

Note the position of the limit, it is in front of the integral not under it, so information about the support of the function is already included in the integral. 

$f$ is measurable since $g$ is and

$$\left\lvert f_{n} \right\rvert \leq g \implies \left\lvert f \right\rvert \leq g.
$$

For the same reason $f$ is integrable. Since $\left\lvert f_{n} - f \right\rvert \leq 2g$, the sequence of functions 

$$
2g - \left\lvert f_{n}-f \right\rvert
$$

are non-negative. Then Fatou's lemma applies and yields 

$$
\int \lim_{ n \to \infty } \text{ inf } (2g-\left\lvert f_{n}-f \right\rvert ) \, d\mu \leq \lim_{ n \to \infty } \text{ inf } \int (2g-\left\lvert f_{n}-f \right\rvert ) \, d\mu.
$$

Since $\lim \text{ inf } f_{n} = f$, we have 

$$
2\int g \, d\mu \leq 2 \int g \, d\mu - \lim_{ n \to \infty } \text{ inf }\int  \left\lvert f_{n}-f \right\rvert  \, d\mu. 
$$

Since $\int g \, d\mu < \infty$, we can subtract it on both sides,

$$
\lim_{ n \to \infty } \text{ inf }\int  \left\lvert f_{n}-f \right\rvert  \, d\mu \leq 0,
$$

however the integral of a non-negative must be non-negative, thus 

$$
\lim_{ n \to \infty } \text{ inf }\int  \left\lvert f_{n}-f \right\rvert  \, d\mu = 0 \implies 
\boxed{
\lim_{ n \to \infty } \int f_{n} \, d\mu = \int f \, d\mu  
}.
$$

The $n$-independent function $g$ is said to *dominate* the sequence $(f_{n})$. Roughly speaking it provides some kind of an upper limit so the sequence of functions behave nicely under limiting procedure. 

There indeed exists functions that can not be dominated by other functions, such as our old friend $f_{n}: x \mapsto \frac{1}{n} 1_ {[0,n]}$. To see that $f: x \mapsto \frac{1}{n} 1_ {[0,n]}$ has no dominating function $g(x)$ we notice that the support of the function goes to $\infty$ as $n \to \infty$. Of course you can find a function so that $\left\lvert f_{n} \right\rvert \leq g$ for all $n$, such as $g = 1$ on $\mathbb{R}$, but then $g$ wouldn't be measurable. Thus dominated convergence theorem doesn't apply here. The theorem applies to function $f: x\mapsto x^n$ defined on $[0,1]$, since it is dominated by $1_ {[0,1]}$. The takeaway is that, the support of a function matters!

In Riemann's integral theory there is something called the improper integral, such as infinite integral, or when the integrand is discontinuous. They generalize Riemann's integral theory. There is no such thing in Lebesgue's integral theory. 

**Example** Consider the sequence of functions defined on $[0,1]$,

$$
f_{n}: x \mapsto \frac{n^{3/2}x}{1+n^2 x^2}
$$

which tends to zero at large $n$. However, the convergence is not uniform since no matter how large $n$ is, there always exists a very small $x \sim \frac{1}{n}$ where $f_{n} \sim \frac{\sqrt{ n }}{2}$. Thus it is not clear that its Riemann integral is zero or not, 

$$
\lim_{ n \to \infty } \int_{0}^1 f_{n} \, dx  \overset{?}{=} 0.
$$

Here is where the dominated convergence theorem come to aid. We can find a measurable function $\frac{~1}{\sqrt{ x }}$ that dominates $f_{n}$, thus

$$
\lim_{ n \to \infty } \int_{0}^1  \, f_{n}dx = \int_{0}^{1} \lim_{ n \to \infty } f_{n} \, dx =0.
$$

The following results are important to study a function defined by an integral. Since summation is just a discrete form of integral, the results apply equally to functions defined by a series. 

**Theorem**  Let $(X,\mathcal{A},\mu)$ be a measure space and $(Y,d)$ be a metric space; if $f$ is a function defined on $X \times Y$ such that 
1. for all $y \in Y$, $x \mapsto f(x,y)$ as a function of $x$ is measurable,
2. for all $x\in X$, $y \mapsto f(x,y)$ as a function of $y$ is continuous at $y_{0}$,
3. there exists an integrable function $g$ on $X \times Y$ such that for all $x\in X$ and $y \in Y$, $\left\lvert f(x,y) \right\rvert\leq g$.

Then, for all $y\in Y$, $x \mapsto f(x,y)$ is integrable, and the function defined by integral

$$
F: y \to \int f(x,y) \, d\mu
$$

is continuous at $y=y_{0}$.

The proof can be found in textbooks. The proof of course uses the Lebesgue's dominance convergence theorem. 

There is a similar theorem, 
**Theorem** let $(X,\mathcal{A},\mu)$ be a measure space and $\mathbb{I}$ an open interval of $\mathbb{R}$, if $f$ is a function defined on $X \times \mathbb{I}$ and satisfies 
1. $x \mapsto f(x,y)$ is integrable for all $x\in X$,
2. $y\mapsto f(x,y)$ is differentiable for $x$ almost everywhere, 
3. there exists a function defined on $X \times \mathbb{I}$ that dominates $f(x,y)$,

then for all $y \in \mathbb{I}$, the function 

$$
x \mapsto \frac{d}{dy} f(x,y)
$$

is integrable, and the function 

$$
F: y \mapsto \int f(x,y) \, dy
$$

is differentiable. 

As an example, let's look at the Bessel function of the first kind, defined by

$$
J_{n}(x) = \frac{1}{\pi} \int_{0}^{\pi} \cos(n\theta-x\sin \theta) \, d\theta 
$$

Since $x \mapsto \cos(n\theta-x\sin \theta)$ is continuous with absolute value $\leq 1$ (being dominated by a measurable function),  $J_{n}$ is continuous. It is also differentiable, hence $J_{n}$ is also differentiable. It is actually infinitely differentiable, it is the solution of equation 

$$
y'' + \frac{1}{x} y' +\left( 1-\frac{n^2}{x^2} \right)y = 0.
$$

Within the framework of Lebesgue's integral theory, differentiation under the integral sign is not permitted. 
Consider the function $F$ defined by 

$$
F(x) = \int_{-\infty}^{\infty} \frac{e^{ixy}}{1+y^2} \, dy,
$$

the integrand is bounded by $\frac{1}{1+y^2}$, which is integrable on $\mathbb{R}$. Follow the same arguing we see that $F(x)$ is continuous. If we differentiate under the integral sign, we obtain

$$
F(x) = \int_{-\infty}^{\infty} \frac{iy e^{ixy}}{1+y^2} \, dy,
$$

which is bounded by 

$$
\frac{y}{1+y^2}
$$

which is not measurable, thus the theorem we introduced before doesn't apply, and $F'(x)$ can not be expressed by the above integral. In fact the original integral can be calculated using the residue theorem yielding 

$$
F(x) = \pi e^{-\left\lvert x \right\rvert }
$$

and the absolute value is where the problem arises. This function is not differentiable at $x=0$ but infinitely differentiable at the complement of the origin.

# 3. Fubini's Theorem

We often meet double integrals, that is integrals of measurable functions defined on some product space $X \times Y$ where both $X$ and $Y$ are measurable spaces, $(X,\mathcal{A},\mu)$ and $(Y, \mathcal{B},\nu)$. The product $\sigma$-algebra is denoted $\mathcal{A} \otimes \mathcal{B}$ and product measure $\mu \otimes \nu$. 

Let $E$ be a subset of $X \times Y$, the sets

$$
E_{x} := \{ y \mid (x,y) \in E \} \quad \text{ and }\quad E^y := \{ x \mid (x,y)\in E \}
$$

are called the $x$-section and $y$-section of $E$. It is called a section since, given a map $\pi_{x}: (x,y)\mapsto x$, and regard $E\xrightarrow{  \pi_{x}  } x$  as a fiber bundle then $E_{x}$ is just the section of $\pi_{x}$. Similar for $E_{y}$.

Without proof, we claim that measurable sets have measurable sections. This should be intuitive since the section is a subset of the product space, and the $\sigma$-algebra of the product space still applies to the subset. I am not sure why in $E_{x}$, $x$ appears in the subscript while in $E^y$, $y$ appears in the superscript. 

To put the above claim in mathematical language, we have 

**Theorem** Let $(X \times Y, \mathcal{A} \otimes \mathcal{B})$ be the product measurable space, if $E$ belong to $X \times Y$ then

$$
\text{for all } x \in X, \quad y \in Y, \quad \text{ we have }  E^{y} \in \mathcal{A} \text{  and  } E_{x} \in \mathcal{B}.
$$

As a corollary, given a function $f$ on $X \times Y$, for all $x \in X$, the function $f_{x}(y):= y \mapsto f(x,y)$ is measurable, as it is nothing but the $x$-section.

We distinguish two closely related concepts, namely *finite measure* and *$\sigma$-finite measure, the extra $\sigma$- makes all the difference.

given a measure space $(X,\mathcal{A},\mu)$, 
- the measure is called finite measure, if the measure of the entire $X$ is finite, and a subset $A \subset X$ is of finite measure if $\mu(A) < \infty$. This is quite self-explanatory. On the other hand, 
- The measure is called $\sigma$-finite if $X$ is a union of countable (could be infinite) subsets, each subset has a finite measure. A subset of $X$ is said to have finite $\sigma$-measure if it is countable union of measurable sets with finite measure. 

$\sigma$-finite is a weaker condition than finite measure. For example, $\mathbb{R}$ under the Lebesgue is NOT a finite measure since $\mu(\mathbb{R}) = \infty$, however it is $\sigma$-finite, since we can separate $\mathbb{R}$ into countable intervals, each with finite $\sigma$-measure. 

The next theorem deals with the order of double integrals, and it makes use of the concept of $\sigma$-finiteness. 

**Theorem** Let $(X,\mathcal{A},\mu)$ and $(Y,\mathcal{B},\nu)$ be two measure spaces, the measure $\mu$ and $\nu$ being $\sigma$-finite. If $E$ belong to the $\sigma$-algebra $\mathcal{A} \otimes \mathcal{B}$, then, for all $x \in X$ and $y \in Y$, 

$$
\int \nu(E_{x}) \, d\mu(x) = \int \mu(E^y) \, d\nu(y).
$$

This theorem is important but the proof is not (for physicists at least) so we will skip it, interested readers can refer to textbooks on measure theory. 

**Fubini's theorem.** Let $(X,\mathcal{A},\mu)$ and $(Y,\mathcal{B},\nu)$ be two measure spaces, measure $\mu,\nu$ being $\sigma$-finite. Let $f$ be a $\mu \otimes \nu$-integrable function defined on $X \times Y$. The function

$$
x \mapsto \int f(x,y) \, d\nu(y)
$$

as a function of $x$ is $\mu$-integrable. Namely, we can first perform the integral over $y$, the remaining function of $x$ is $\mu$-integrable.  Similarly, we can perform the integral over $x$ first and the remaining function of $y$ is still integrable, namely the function

$$
y \mapsto \int f(x,y) \, d\mu(x)
$$

is $\nu$-integrable. The order of integral is exchangeable,

$$
\begin{align}
\int f \, d\mu(x)\otimes \nu  & = \int \left[ \int f(x,y) \, d\nu(y)  \right] \,  \, d\mu(x)   \\
 & = \int \left[ \int f(x,y) \, d\mu(x)  \right] \, d\nu(y) .
\end{align}
$$

The proof is also skipped here, we only mentioned that the definition of Lebesgue integral, namely liming the real integral of a function by the infimum of simple functions, is used, as well as the monotone convergence theorem.

Since the two measures $\mu,\nu$ play a symmetric role, we can also write 

$$
\int f \, d\mu \otimes \nu = \int f \, d\mu(x) d\nu(y)
$$

If the function is $\mu \otimes \nu$-integrable, Fubini's theorem is often used to justify interchanging the order of the integrals. 

To apply Fubini's theorem, it is essential to verify that the function $f$ is $\mu \otimes \nu$ integrable, that is, $f$ has to be measurable, and $\left\lvert f \right\rvert$ is also measurable, which means one of the three following things,
- $\int \left\lvert f \right\rvert \, d\mu \otimes \nu < \infty,$
- $\int d\mu(x) \, \int d\nu(y) \,  \left\lvert f(x,y) \right\rvert < \infty,$
- $\int d\nu(y)\, \int d\mu(x)  \,  \left\lvert f(x,y) \right\rvert < \infty.$

Fubini's theorem for positive functions is also known as the **Fubini-Tonelli** theorem.

Since summation is just integral with counting measure, we could replace one or both of the integral signs as summation. Then Fubini's theorem states that we can interchange the order of summation (or of summation and integral) in the case of absolutely convergent double series (or summation of integrals, etc.). An counter example is 

$$
\int_{-\infty}^{\infty} e^{ -x^2-\lambda x^4 } \, d = \int_{-\infty}^{\infty} e^{ -x^2 } e^{ -\lambda x^4 } \, dx = \int_{-\infty}^{\infty} e^{ -x^2 }\sum_{n=0}^\infty \frac{(-\lambda)^n}{n!}x^{-4n} \, dx,
$$

the radius of convergence of the summation is $\infty$. However if we interchange the order of integral and summation, namely move the summation in from of the integral sign, we have

$$
\sum_{n=0}^\infty \frac{(-\lambda)^n}{n!}\int_{-\infty}^{\infty} e^{ -x^2 }x^{-4n}  \, dx 
$$

where the integral can be performed with the help of Gamma function, then  after some calculation we have a divergent power series, thus not measurable. Then Fubini's theorem does not apply to this situation. 

When applicable, Fubini's theorem can be used to integral a function defined by another integral. However, it is possible that interchanging the order of integrals gives two different results. For example, consider function 

$$
f: x \mapsto \frac{x^2-y^2}{(x^2+y^2)^2}
$$

defined on $[0,1]\times[0,1]\backslash (0,0)$ where $(0,0)$ is the origin where the function blows up, and $A\backslash B$ means $A$ minus $B$. Since $(0,0)$ is a point and points have measure zero, it is not necessary to define $f$ for $(x,y) = (0,0)$. Since 

$$
\frac{d}{dx} \frac{-x}{x^2 + y^2} = \frac{x^2-y^2}{(x^2+y^2)^2},
$$

we have 

$$
\int_{0}^{1} dy \, \int_{0}^{1} dx\, f(x,y) = - \frac{\pi}{4},
$$

however if we interchange the order of integral, we have 

$$
\int_{0}^{1} dx \, \int_{0}^{1} dy\, f(x,y) =  \frac{\pi}{4},
$$

note the extra minus sign. Hence $f$ is not integrable. As a matter of fact we have

$$
\int_{0}^{1} dy \int_{0}^{1} dx \, \left\lvert \frac{x^2-y^2}{(x^2+y^2)^2} \right\rvert = \infty.
$$

If interchanging the order of the repeated integrals gives identical results, that doesn't prove that Fubini's theorem applies, for the integral of the absolute value of the function might not be convergent. Consider, for example, function $f$ defined on $R_{+}^2$, $f:(x,y)\mapsto \sin(x^2+y^2)$. Expanding $\sin(x^2+y^2)$ and taking into consideration the Fresnel's integral

$$
\int_{0}^{\infty} e^{ ix^2 } \, dx =\sqrt{ 2\pi }(1+i) / 4
$$

we have 

$$
\int_{0}^{\infty}  dy\, \int_{0}^{\infty} dx \, \sin(x^2+y^2) = \int_{0}^{\infty}  dx\, \int_{0}^{\infty} dy \, \sin(x^2+y^2) = \frac{\pi}{4}.
$$

However, $\sin(x^2+y^2)$ is not measurable on $R_{+}^2$ since the integral of its absolute value is divergent, 

$$
\int_{0}^{\infty} dy \, \int_{0}^{\infty} dx \,\left\lvert \sin(x^2+y^2) \right\rvert =\infty,
$$

this result if readily obtained using the change of variables: $x = \rho \cos \theta, y = \rho \sin \theta$.

Note that the for Fubini's theorem to be valid, the measure $\mu,\nu$ have to be $\sigma$-finite.  The most popular example for a non-sigma-finite measure maybe the counting measure on $\mathbb{R}$. The counting measure gives the cardinal (number of elements) of a set, and the set of all the real numbers is uncountable. On the contrary, the set of rational numbers $\mathbb{Q}$ in countable.

Consider a function $f$ defined on $[0,1]\times[o,1]$ by 

$$
f(x,y) = 
\begin{cases}
1, & x=y, \\
0, & \text{otherwise.}
\end{cases}
$$

Here comes the interesting part: on the $y$-axis we adopt the counting measure $\nu(y)$ instead of the familiar Lebesgue measure, while on the $x$-axis we still use the Lebesgue measure $\mu(x)$. Recall that $\nu(\text{point}) = 1$, we have 

$$
\int_{0}^{1} f(x,y) \, d\nu(y) = 1, 
$$

if we integrate with respect to $y$ first then to $x$, we have 

$$
\int_{0}^{1} d\mu(x) \, \int_{0}^{1} d\nu(y) \,   f(x,y) = \int_{0}^{1} d\mu(x) \,1 = 1.
$$

But if we integrate with respect to $x$ first, we get

$$
\int_{0}^{1} d\nu(y) \,\int_{0}^{1} d\mu(x) \,    f(x,y) = \int_{0}^{1} d\mu(x) \, 0 = 0,
$$

Apparently the Fubini's theorem doesn't apply here. 

The convolution of two real-valued integrable (with respect to Lebesgue measure) functions $f,g$ is defined as 

$$
f\ast g (x) = \int_{-\infty}^{\infty} f(x-y)g(y) \, dy ,
$$

which is also integrable, since 

$$
\int \left\lvert f\ast g \right\rvert  \, dm \leq \int \left\lvert f \right\rvert  \, dm \int \left\lvert g \right\rvert  \, dm,
$$

where $dm$ is whatever measure used for the integral. 

Next we give an example where the interchange of integral and summation makes sense. Consider the integral 

$$
\int_{0}^{\infty} \frac{\sin x}{e^{ x }-1} \, dx 
$$

which is convergent. We may write

$$
\begin{align}
\int_{0}^{\infty} \frac{\sin x}{e^{ x }-1} \, dx  & = \int_{0}^{\infty} \frac{\sin x}{e^{ x }(1-e^{-x})} \, dx  \\
&= \int_{0}^{\infty} dx \, \sum_{k=1}^\infty e^{ -kx }\sin x \\
&= \sum_{k=1}^\infty \int_{0}^{\infty} dx \, e^{ -kx }\sin x,
\end{align}
$$

where we have used 

$$
(1-e^{ -x })^{-1} = \sum_{n=0}^\infty e^{ -(n+1)x }.
$$

The interchange of the sign $\sum$ and $\int$ is justified, since the Fubini theorem applies to the function $(x,k)\mapsto e^{ -kx }\sin x$, which is due to the fact that 

$$
\int e^{ -kx } \sin x \, dx <\infty
$$

the exponential suppression makes the integrand Lebesgue integrable. By the end of the day we get

$$
\int_{0}^{\infty} \frac{\sin x}{e^{ x }-1} \, dx = \sum_{k=1}^\infty \frac{1}{1+k^2}.
$$

The right hand side of the above expression can be calculated by the residual theorem. Finally, we have 

$$
\int_{0}^{\infty} \frac{\sin x}{e^{ x }-1} \, dx = \frac{1}{2} (\pi \coth \pi-1).
$$

As we can see, Lebesgue's theory is kind of a generalization of Riemann's theory in term of the concept of measure. Lebesgue's theorem can be stated as follows,

**Theorem** A function defined on a *bounded* interval $[a,b]$ is Riemann integrable if and only if it is bounded and continuous *almost everywhere*.

### 3.1. Notes

Given a map $f$ from a set $X$ into a set $Y$, the preimage of a $\sigma$-algebra in $Y$ is a $\sigma$-algebra in $X$ but the inverse is not necessary true. However, if $\mathcal{A}$ is a $\sigma$-algebra in $X$, the set of all the subsets of $Y$ such that their preimage is in $\mathcal{A}$ forms as $\sigma$-algebra and is called the induced $\sigma$-algebra.

Let $(a_{n})$ be a sequence of $\mathbb{R}$ and for any $k \in \mathbb{N}$, define 

$$
b_{k} = \text{inf }(a_{k},a_{k+1},\dots) = \text{inf }\{ a_{n} \mid n\geq k \}
$$

and 

$$
B_{k} = \text{sup }(a_{k},a_{k+1},\dots) = \text{sup }\{ a_{n} \mid n\geq k \}
$$

then 

$$
\lim_{ n \to \infty } \text{inf }a_{n} = \text{sup } (b_{1},b_{2},\dots)
$$

and 

$$
\lim_{ n \to \infty } \text{sup }a_{n} = \text{inf }(B_{1},B_{2},\dots).
$$

lim inf is called the lower limit of the sequence $a_{n}$, respectively lim sup is called the upper limit. 

As the last part of the note, let's briefly summarize the integration theory for function defined on a finite interval $[a,b]$.

By a partition $\pi$ of a closed interval $[a,b]$ we mean the *finite* set 

$$
\pi = \{ a=x_{0},x_{1},\dots,x_{m-1}, x_{m}=b\}
$$

where $x_{0}<x_{1}<\dots <x_{m}$. In other words, a partition is a way to divide an interval into finite disjoint subsets without neglecting anything.

The norm of the partition is 

$$
\delta(\pi) = \text{sup }(x_{k} - x_{k-1}).
$$

Given a continuous function on $[a,b]$, the Cauchy sum associated to $f$ and $\pi$ is defined as 

$$
S_{\pi}(f) := \sum_{k=1}^m f(x_{k-1})(x_{k}-x_{k-1}).
$$

$f$ being continuous, it can be shown that as long as the norm of the partition is sufficiently small, the difference between Riemann integral and Cauchy sum is arbitrarily small. To be more specific, if $(\pi_{n})$ is a sequence of partitions of $[a,b]$ such that $\lim_{ n \to \infty }\delta(\pi_{n})=0$, then $(S_{\pi_{n}}(f))$ is a Cauchy sequence. Cauchy sequence is a sequence whose elements become arbitrarily close to each other as the  sequence progresses. This limit is called the Cauchy integral of $f$ on $[a,b]$, denoted by 

$$
\int_{a}^{b} f(x) \, dx .
$$

The class of Cauchy integrable functions is much larger than the class of continuous functions. 

Any finite linear combination of characteristic functions of open bounded intervals of $\mathbb{R}$ is called a step function, and the step functions on $\mathbb{R}$ form a vector space. Given a step function $s(x)$, the mapping 

$$
s \mapsto \left\lVert s \right\rVert =\text{sup }s(x) \text{ for all } x\in\mathbb{R}
$$

is called the norm of the uniform convergence. If a sequence of step functions converges uniformly to a function $f$, this function is said to be *regulated*. Obviously regulated function has Cauchy integrals. 

A regulated function can be discontinuous at countable number of points.

A function is Cauchy integrable if and only if it is regulated. Riemann integrability applies to a slightly larger class of functions. Recall that a function $f$ defined on $[a,b]$ is said to be Riemann integrable if, for all positive $\epsilon$, there exists two step function $g_{\epsilon},h_{\epsilon}$ such that 

$$
g_{\epsilon} \leq f \leq h_{\epsilon}
$$

and 

$$
\left\lvert \int h_{\epsilon} \, dx - \int g_{\epsilon} \, dx  \right\rvert <\epsilon.
$$

If a function is bounded and Cauchy integrable, then it is also Riemann integrable. 