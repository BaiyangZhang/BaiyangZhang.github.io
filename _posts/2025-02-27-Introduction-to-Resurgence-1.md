---
layout: post
title: Introduction to Resurgence Note 1
date: 2025-02-27
author: Baiyang Zhang
catalog: true
tags:
  - resurgence
---

# Table of Content


- [1. Motivation](#1-motivation)
- [2. Analytic continuation and monodromy](#2-analytic-continuation-and-monodromy)
- [3. Another example by Poincare](#3-another-example-by-poincare)
- [4. The differential algebra](#4-the-differential-algebra)

# 1. Motivation

The following are some examples of potential applications of resurgence theory.

-   Normal forms for dynamical systems
-   Gauge theory of singular connections
-   Quantization of symplectic and Poisson manifolds
-   `Floer` homology and `Fukaya` categories
-   Knot invariants
-   Wall-crossing and stability conditions in algebraic geometry
-   Spectral networks
-   WKB approximation in quantum mechanics
-   **Perturbative expansions in quantum field theory (QFT)**

One of the most astonishing achievements of resurgence theory in QFT is that one can uncover the non-perturbative results from perturbative expansion alone! Typically, calculating non-perturbative results requires every possible resource you can have, such as the topology of the vacuum manifold, some real special cancellation, but perturbative calculation is much more straightforward, how can it contain the information that was so hardly revealed by all kinds of non-perturbative techniques? Nevertheless, resurgence theory enables us to derive non-perturbative results, such as instanton contribution, through the analytical continuation of perturbative data! On the one hand, it feels like black magic; on the other hand, perhaps I shouldn’t be so surprised, since if we could obtain the full perturbative expansions to all orders, we can essentially reproduce the equation of motion, the Lagrangian, which inherently includes all non-perturbative information. At least in theory then, perturbative expansions should be capable of yielding non-perturbative insights. However, this is only in theory. It's still utterly astonishing to witness it happening in front of your eyes in practice. Rainbow doesn't become less beautiful just because you've learnt the science behind it.

Actually, I would argue that it is impossible to make sense of perturbation theory **without** knowing at least some facets of resurgence theory. We include more and more perturbative terms in any perturbative power expansion, the power series eventually diverges, so what sense does it make to just consider the first few terms? Claiming that the first few terms of a divergent series give the dominant results would be ridiculous. However the miraculous agreement between perturbative QED and experiments clearly suggests that perturbation expansion makes sense, it is by no chance an accident. The answer to this question lies in resurgence theory.

- - -

H. Poincare mentioned "a kind of misunderstanding between geometers and astronomers about the meaning of the word convergence", he proposed a simple example: consider the following series

$$
\sum \frac{1000^{n}}{n!} \text{ and }\sum \frac{n!}{1000^{n}},
$$

Poincare said that for geometers, i.e. mathematicians in his time, the first one converges because at large $n$ the terms gets smaller and smaller. But for astronomers the first one is as good as divergent since the next terms doesn't get smaller until $n$ is larger than $1000$. For astronomers the second series diverges because the first $1000$ terms decreases quickly. 

He then proposes to reconcile both points of view by clarifying the role that divergent series (in the sense of geometers) can play in the approximation of certain functions. This is the origin of the modern theory of asymptotic expansion. 

In physics, the divergence of power series can be shown via different approaches:

1. Dyson Freeman show it in a heuristic way, see his short paper;
2. By combinatorial argument. The number of Feynman diagrams grows factorially as $n!$, while the contribution of each diagram decreases as $g^{n}$, then if there is no cancellation between different diagrams, the perturbative series grows as $g^{n} n!$, which eventually diverges. Lipatov[^1] first show that in scalar QFT the series indeed grows as $n!$. Similar growth are found in quantum mechanics[^2] and matrix models[^3].

[^1]: Divergence of the Perturbation Theory Series and the Quasiclassical Theory, Published in: Sov.Phys.JETP 45 (1977), 216-223, Zh.Eksp.Teor.Fiz. 72 (1977), 411-427.
[^2]: J. Zinn-Justin, “Perturbation Series at Large Orders in Quantum Mechanics and Field Theories: Application to the Problem of Resummation”, Phys. Rept., vol. 70, p. 109, 1981. doi: 10.1016/0370-1573(81)90016-8;C. M. Bender and T. T. Wu, “Anharmonic oscillator. 2: A Study of perturbation theory in large order”, Phys. Rev., vol. D7, pp. 1620–1636, 1973. doi: 10.1103/PhysRevD.7.1620.
[^3]: M. Marino, R. Schiappa, and M. Weiss, “Nonperturbative E↵ects and the Large-Order Behavior of Matrix Models and Topological Strings”, Commun. Num. Theor. Phys., vol. 2, pp. 349–419, 2008. doi: 10.4310/CNTP.2008.v2.n2.a3. arXiv: 0711.1954 [hep-th].

# 2. Analytic continuation and monodromy

In this note we shall focus on `formal power series`, sometimes called the `polynomial forms`. When regarded as formal power series with real coefficients of indeterminant $t$, denoted $\mathbb{R}[t]$, the previous example should be written as (note the appearance of extra variable $t$)

$$
\sum \frac{1000^{n}}{n!}t^{n} \quad  \text{ and } \quad  \sum \frac{n!}{1000^{n}}t^{n}
$$

where the first one has **infinite** **radius of convergence** with respect to $t$, while the second one has **zero radius of convergence**. For us, `divergent series` will usually mean a formal power series with zero radius of convergence.

`Formal power series` is a generalization of normal power series, or polynomial, in the sense that we consider a power series of infinite order as a formal object and don't worry about evaluation, or if it is convergent. Given a ring $R$, consider the set of formal power series in $X$ with coefficients from $R$, denoted by $R[[X]]$, which is itself another ring. To see it, note that multiply one polynomial to another and we have a new polynomial, similarly for other requirements for a ring. It is called the **ring of formal power series in the variable $X$ over $R$**.

First we clarify some definitions and concepts that might be useful in the future.

We say a complex-valued function $f:\Omega \to \mathbb{C}$ is `analytic` if $f$ is represented by a convergent power series expansion on a neighborhood around every point $a\in\Omega$. 

We say a complex-valued function $f:\Omega \to \mathbb{C}$ is `holomorphic` iff it satisfied Cauchy-Riemann relation, which is equivalent to $\partial f/\partial \overline{z}=0$ . If we regard $z$ and $\overline{z}$ as independent variables, a holomorphic function $f$ is only a function of $z$ not $\overline{z}$.

A differential manifold is a topological space (given by closed sets and all that stuff) with differential structure, which is Hausdorff and second-separable. It practically means that you can find a way to do derivatives on the manifold. A $n$-Dimensional real (Complex) manifold is locally homeomorphic to $\mathbb{R}^N (\mathbb{C}^n)$, plus the condition that the transition from one chart (coordinate system) to another is `homeomorphic (holomorphic)`.

An `open disk` of radius $r$ around $z_ 0$ is the set of points $z$ on $\mathbb{C}$ that satisfies

$$
\left\lvert z-z_ 0 \right\rvert  < r.
$$

A **open deleted disk of radius $r$ around $z_ 0$** is the set of points with

$$
0 < \left\lvert z-z_ 0 \right\rvert  < r.
$$

a deleted disk is also called a punctured disk, since the origin $z_  {0}$ has been taken out.

- - -

A complex atlas on a 2-dimensional manifold is a collection of charts that cover the manifold, where each chart maps a portion of the manifold to an open subset of the complex plane $\mathbb{C}$, and the transition functions between overlapping charts are holomorphic (complex differentiable).

- $\mathbb{C} P^n$ Model: The (n+1)-tuple $z = (z^0,\cdots,z^n)$ defines a vector in space $\mathbb{C}^{n+1}$. Define a equivalence relation $\sim$ between two vectors,

  $$
(u^0,\cdots,u^n) \sim (v^0,\cdots,v^n) \text{ if } \exists \lambda\neq 0 \in \mathbb{C} \text{ so that } \mathbf{u} = \lambda \mathbf{v}
$$

then

$$
\mathbb{C} P^{n} \equiv (\mathbb{C}^{n+1}-\left\lbrace0\right\rbrace)/\sim,
$$

and the $n+1$ numbers are call `homogeneous coordinates` and is denoted by $[z^0,\cdots,z^n]$. We can make one of them constantly equal to 1, then only the rest are really coordinates, it is called `inhomogeneous coordinates`.

The Riemann sphere $\mathbb{C}P^1$ is a classic example of real-dimension two (denoted $\text{dim}_ {\mathbb{R}}=2$) complex manifold. It can be visualized as the complex plane plus a point at infinity. To see that all the infinities on a complex plain can be identified as a single point, notice that in $[z_ {0},z_ {1}]$ when $z_ {1}\to \infty e^{ i\theta }$ it is equivalent to $\left[ \frac{z_ {0}}{\infty e^{ i\theta }},1 \right]$, and no matter the angle $\theta$ it always goes to $[0,1]$. To construct a complex atlas for the Riemann sphere, we use two charts:

3. **Chart $U_ 1$**: This chart covers the sphere minus the point at infinity. It maps each point $z$ in the complex plane $\mathbb{C}$ to itself:
   $$
   \phi_ 1: U_ 1 \rightarrow \mathbb{C}, \quad \phi_ 1(z) = z
   $$
   Here, $U_ 1 = \mathbb{C}$.

4. **Chart $U_ 2$**: This chart covers the sphere minus the origin. It maps each point $z$ in the complex plane, excluding the origin, to its reciprocal:
   $$
   \phi_ 2: U_ 2 \rightarrow \mathbb{C}, \quad \phi_ 2(z) = \frac{1}{z}
   $$
   Here, $U_ 2 = \mathbb{C} \setminus \{0\}$.

The two charts overlap on $U_ 1 \cap U_ 2 = \mathbb{C} \setminus \{0\}$. The transition functions between these charts are:
- From $U_ 1$ to $U_ 2$:
  $$
  \phi_ 2 \circ \phi_ 1^{-1}(z) = \frac{1}{z}
  $$
- From $U_ 2$ to $U_ 1$:
  $$
  \phi_ 1 \circ \phi_ 2^{-1}(z) = \frac{1}{z}
  $$

Both transition functions are holomorphic, as the function $f(z) = \frac{1}{z}$ is complex differentiable wherever $z \neq 0$.

To say that two complex atlases on a manifold are `analytically equivalent` means that the combined atlas they form (by taking all the charts from both atlases) is itself a complex atlas. This implies that the transition functions between the charts of one atlas and the charts of the other atlas are holomorphic wherever they overlap.

- - -

By a `complex structure` on a manifold, we mean an equivalent class of analytically equivalent complex atlases on the manifold. If we give a manifold a complex atlas, then we have given it a complex structure.

A Riemann surface is a pair $(X,\Sigma)$ where $X$ is a connected 2-dimensional manifold and $\Sigma$ is a complex structure on $X$. The simplest Riemann surface is the complex plane itself.

- - -

`Meromouphic functions` are functions holomorphic except at a discrete set of isolated poles. 

A `domain` in $\mathbb{C}$ is a connected non-empty open subset of $\mathbb{C}$. Note that it has nothing to do with integral domain in abstract algebra.

- - -

**Riemann Sphere**

There are two ways to think of $\overline{C} \equiv \mathbb{C} \cup \left\lbrace\infty\right\rbrace$, namely the compactified complex plane, by adding a point called infinity $\infty$.

- complex projective plane $\mathbb{C}P^1$.
- a 2D sphere $\mathbb{S}^2$. The coordinates is given by the stereographic projection, except for the north pole $N$, $\pi : \mathbb{S}^2-\left\lbrace N \right\rbrace \to \mathbb{C}$.

The space $\overline{\mathbb{C}}$ has the structure of a Riemann surface and it is called the `Riemann sphere`. We can introduce two charts on the Riemann sphere,

$$
\mathfrak{U}_ 1 = \mathbb{C},\quad \mathfrak{U}_ 2 = \mathbb{C}^\ast \cup \left\lbrace\infty\right\rbrace
$$

where $\mathbb{C}^\ast$ is the punctured complex plane, $\mathbb{C}^\ast \equiv \mathbb{C} - \left\lbrace0\right\rbrace$. 

**Theorem.** A function is meromorphic on $\overline{\mathbb{C}}$ iff its restriction on $\mathbb{C}$ is a rational function.

By the restriction of a function, we mean that to restrict the domain so that the it is well defined, no singularities. For example, the function $f:x\to 1/x$ has a singularity at $x=0$, then if we want something which is just like $f$ but has no singularity, we can just restrict the domain to $\mathbb{R} - \left\lbrace0\right\rbrace$, which is said to be a restriction of $f$.

A `germ` of functions at a point $a\in\mathbb{C}$ is a set of function defined in the neighborhood of $a$ which all have the same Taylor expansion. A more mathematical definition is as following.

Use $\mathcal{O}(a)$ to denote the set of functions which are defined in a neighborhood of $a$ and is holomorphic at $a$. Define an equivalence relation $\sim$ so that if $f\sim g$ for $f,g \in \mathcal{O}(a)$, then $f,g$ are identical on some neighborhood of a. The equivalence class is called a germ of holomorphic functions at $a$.

Intuitively, the germ of a function tells us how a function behaves locally at point $a$.

- - -

The `Fundamental Uniqueness Theorem (FUT)` for holomorphic functions:

**Theorem.** If $f,g$ are holomorphic functions on a domain $D\in\mathbb{C}$ and $f \sim g$ for some point $a\in D$, namely f and g are in the same germ at a, then f is identical to g on $D$.

The germ of $f$ will be denoted by $\overline{f}$, if there is no ambiguity about around which point it is defined.

- - -

**Analytic Continuation, Monodromy**

First we introduce the analytic continuation in a different way, more formal and more mathematical. We begin by defining `pairs`. The idea is that, a function is not only defined by the values but also the domain on which it is defined.

A `pair` $(U,f)$ is a non-zero open disk $U\subset \mathbb{C}$ (why does it has to be open? I don't know.) and a function, holomorphic on $U$, such that the radius of $U$ is the maximum radius of convergence of the series expansion of $f$. The center of the pair is the center of $U$. Usually $U$ will stop at some singular point.

Another concept is adjacency, two pairs $(U,f)$ and $(V,g)$ are said to be `adjacent` if $U\cap V \neq 0$ and $f \equiv g$ on $U\cap V$.

If there is a `finite` sequence of pairs $(U_ i,f_ i),\quad i = 0,1,\cdots, n$ so that for all $i$, $(U_ i,f_ i)$ is adjacent to $(U_ {i\pm 1},f_ {i\pm 1})$, then $(U_ 0,f_ 0)$ is said to be the analytical continuation of $(U_ n,f_ n)$.

We can define a analytical continuation along a curve $\gamma: [0,1] \to \mathbb{C}$. The definition is kind of intuitive so I will skip it here. Now the question is, is the analytical continued function $(U_ n,f_ n)$ dependent on the path? The answer is the monodromy theorem:

**Theorem.** If the two path are homotopic, then the analytical continuation results to the same functions.

If in any doubt, just think of the $\ln{z}$ function.

- - -

**Linear Differential System**

A `linear system` is short for a complex linear ordinary differential system. A linear system of order p is a system with p first order ordinary differential equations.

$$
\frac{dy(x)}{dx} = A(x) y(x),\quad y(x) =
  \begin{pmatrix}
    y_ 1(x)\\
    \vdots \\
    y_ p(x)
  \end{pmatrix}
$$

where $y(x)$ is a column vector of functions, and $A$ is the $p\times p$ coefficient matrix. The system is referred to as $(S)$. 

We used $\mathbb{C}(x)$ to denote the field of complex rational functions, and $\mathscr{M}(D)$ the field of meromorphic functions on domain $D$, and $\mathscr{O}(D)$ the ring of holomorphic functions on domain $D$.

A `fundamental solution` of $(S)$ is a $p\times p$ matrix whose columns are $\mathbb{C}$-linear independent solutions to $(S)$.

The `Wronskian` for $n$ functions are defined to be

$$
W(f_ 1,\cdots, f_ n)(x) \equiv
  \begin{vmatrix}
    f_ 1(x) & \cdots & f_ n(x)\\
    f'_ 1(x)& \cdots & f'_ n(x)\\
    \cdots \\
    f^{(n-1)}(x) & \cdots & f^{(n-1)}(x)
  \end{vmatrix}.
$$

Let $\Sigma= \left\lbrace a_ 1,\cdots,a_ n \right\rbrace\subset \overline{\mathbb{C}}$ be the set of singular points of $(S)$. Let $U_ \Sigma \equiv \overline{\mathbb{C}}\backslash \Sigma$.

Recall a nice property of Wronskian:
Let $\mathscr{D}$ a domain in $U_ \Sigma$, $W$ a $p\times p$ solution of $(S)$, the following are equivalent:

- W is a fundamental solution of $(S)$
- $\det{W(x)}\neq 0$ for some $x \in \mathscr{D}$
- $\det{W(x)}\neq 0$ for all $x \in \mathscr{D}$

In other words, the Wronskian is either nonzero on the entire domain, or identically zero.

- - -

**Differential Galois Theory**

A `differential field` $(k,\partial)$ is a field $k$ with derivation.
A `differential homomorphism` $\phi:(k_ 1,\partial)\to(k_ 2,\partial)$ from $k_ 1$ to $k_ 2$ is a field homomorphism that commutes with $\partial$. A triple $(k_ 1, \phi, k_ 2)$ is called a differential extension. $k_ 2$ is also called a differential extension of $k_ 1$.

A differential system

$$
  \partial  y = A y
$$

where $A$ is a $p \times p$ matrix.

# 3. Another example by Poincare

To get some feeling about resurgence, let's start with an example first given by Poincare. This example shows **how an divergent series emerges from a function.** 

Fix $w\in \mathbb{C}$ and $\left\lvert w \right\rvert<1$. Consider the series of functions of the complex variable $t$,

$$
\phi_ {k}(t) := \frac{w^{k}}{1+kt},\quad  \phi(t):= \sum_ {k\geq 0} \phi_ {k}(t).
$$

This series is uniformly convergent on

$$
U:=C^{\ast } - \left\lbrace -1,-\frac{1}{2},-\frac{1}{3},\dots \right\rbrace .
$$

Hence the sum $\phi$ is `holomorphic` in $U$. Actually $\phi$ is meromorphic on $\mathbb{C}^{\ast}$ (not on $\mathbb{C}$ since the origin would be a limiting point of the poles) with simple poles at $1 / \mathbb{N}$.

We now show how this function $\phi$ gives rise to a divergent formal series when $t$ approaches $0$. The idea is to expand each $\phi_ {k}$ first in terms of $t$. For each $k \in \mathbb{N}$, we have a *convergent* Taylor expansion at $t=0$,

$$
\phi_ {k}(t) = w^{k}\sum_ {n\geq 0}(-1)^{n}(kt)^{n}, \quad  \left\lvert t \right\rvert< \frac{1}{k} .
$$

One might be tempted to recombine the (convergent) Taylor expansion of $\phi_ {k}$ to give $\phi(t)$. It amounts to considering the well-defined **formal series**

$$
\tilde{\phi}(t) := \sum_ {n\geq 0}(-1)^{n} b_ {n} t^{n}, \quad b_ {n}:= \sum_ {k\geq 0}k^{n} w^{k}.
$$

We see that $b_ {n}$ is convergent since

$$
\lim_ { k \to \infty } \frac{(k+1)^{n}w^{k+1}}{k^{n}w^{k}} = w <1 \text{ by construction}.
$$

However, it turns out that **this formal series is divergent!**

To see this, make the substitution $w = e^{ s }$. Then, since $\text{Re }w <1$, we have 

$$
b_ {0}=(1-w)^{-1} = (1-e^{ s })^{-1}
$$

and

$$
b_ {n} = \left( w \frac{d}{dw}  \right)^{n}b_ {0} = \left( \frac{d}{ds} \right)^{n} b_ {0}.
$$

There is an easy way to tell if a series has non-zero radius of convergence, by some kind of a "dominance criterion". If the series of study $a_ {n}$ is dominated by $AB^{n}$ where $A,B$ are real and $A,B>0$, namely for all but finite $n$ we have $\left\lvert a_ {n} \right\rvert \leq AB^{n}$. Then the formal series 

$$
F(\xi) := \sum(-1)^{n} a_ {n} \frac{\xi^{n}}{n!}
$$

would have infinite radius of convergence. **$F$ can be seen as a map of the formal series to a function of $\xi$, note that we have inserted a factor of $1 / n!$ into the sum to make is more convergent**. In our case of $b_ {n}$, we see that 

$$
F(\xi) = \sum(-1)^{n} b_ {n} \frac{\xi^{n}}{n!} = \sum(-1)^{n} \frac{\xi^{n}}{n!}\left( \frac{d}{d s}  \right)^{n} b_ {0}(s) = b_ {0}(s-\xi) = \frac{1}{1-e^{ s-\xi }} .
$$

This functions has finite radius of convergence, since the last expression in the equation above diverges at $\xi=s+2\pi i \mathbb{Z}$. The radius of convergence is not infinite! Thus $\tilde{\phi}$ must have zero radius of convergence.

- - -

Now the question is to understand the relation between $\tilde{\phi}$ and $\phi$. We shall see in this note that the `Borel-Laplace` summation is a way of going from the divergent formal series $\tilde{\phi}$ to the finite function $\phi$. $\tilde{\phi}$ is actually the `asymptotic expansion` of $\phi(t)$  at $t=0$. We shall explain what it means next. 

We can already observe that the moduli of the coefficients $b_ {n}$ satisfy

$$
\left\lvert b_ {n} \right\rvert <AB^{n}  n! ,\quad  n \in \mathbb{N}
$$

for some $A,B>0$. Such inequalities are called `1-Gevrey estimates` for the formal series $\tilde{\phi}(t)=\sum b_ {n}t^{n}$. 

We remark that, since the original function $\phi(t)$ is not holomorphic (nor meromorphic) in any neighborhood of 0, because of the accumulation at the origin of the sequence of simple poles $- \frac{1}{k}$. Thus it would be very surprising to find a positive radius of convergence for $\tilde{\phi}$.

- - -

Resurgence theory can also be used to study power series of the form 

$$
\sum_ {i} \left( \sum_ {j} a_ {ij}t^{j} \right) e^{ -c_ {i} / t }
$$

note that the variable $t$ appears at two places, once in the series and once in the exponent. The exponent term is the small correction that is invisible to Taylor expansion at $t=0$, and the formal series in the parenthesis diverges. 

In the next note we will dive into the details of resurgence theory, beginning with the differential algebra $(\mathbb{C}[[1 / z]],\partial)$. 

# 4. The differential algebra


It will be convenient for us to set $z = 1/t$ in order to “work at $\infty$” rather than at the origin, since we will often talk about compactified spaces. This means that we shall deal with expansions involving *non-positive* integer powers of the indeterminate. We denote the set of all the `formal power series`, i.e., polynomials in $1 / z$ by 

$$
\mathbb{C}[\![z^{-1}]\!] = \left\{ \phi=\sum_ {n\geq 0}a_ {n}z^{-n} \,\middle\vert\, a_ {i} \in \mathbb{C} \right\}.
$$

This is a vector space with basis $1, z^{-1},z^{-2}$, etc. It is also an algebra when we take into account the Cauchy product

$$
\left( \sum a_ {n}z^{-n} \right) \left( \sum b_ {n} z^{-n} \right) = \sum c_ {n} z^{-n}, \quad  c_ {n} = \sum_ {p+q=n} a_ {p} b_ {q}.
$$

The derivation

$$
\partial  = \frac{d}{d z}
$$

further makes it a *differential algebra*, which simply means $\partial$ is a linear map which satisfied the Leibniz rules. 

This is the derivative in terms of $z$, it is natural to ask what is the derivative in terms of $t$. The answer is straightforward,

$$
\partial  = \frac{d}{d z} = \frac{d}{d t^{-1}}  = \frac{d}{-t^{-2}dt} =-t^{2} \frac{d}{d t} .
$$

Then, in mathematical terminology, there is an isomorphism of differential algebra between $(\mathbb{C}[[z^{-1}]],\partial)$ and $(\mathbb{C}[[t]],\partial)$. 

- - -

The `standard valuation`, or sometimes called the `order`, on $\mathbb{C}[[z^{-1}]]$ is the map

$$
\text{val}: \mathbb{C}[\![z^{-1}]\!] \to \mathbb{N} \cup \infty
$$

defined by $\text{val }(0)=\infty$ and 

$$
\boxed{
\text{val }(\phi) := \text{min } \left\{ n\in \mathbb{N} \,\middle\vert\, a_ {n}\neq 0 \right\} ,\quad  \phi =\sum a_ {n} z^{-n} \neq 0.
}
$$

For $\nu \in\mathbb{N}$, we will use the notation 

$$
z^{-\nu}\mathbb{C}[\![z^{-1}]\!] = \left\{ \sum_ {n\geq \nu} a_ {n}z^{-n} \,\middle\vert\, a_ {\nu},a_ {n+1},\dots \in  \mathbb{C} \right\}.
$$

This is the set of all the complex polynomials in $z^{-1}$ such that the standard valuation is no less than $\nu$. 

From the viewpoint of the ring structure, ${\frak I} = z^{-1}\mathbb{C}[[z^{-1}]]$ is the maximal ideal of the ring $\mathbb{C}[[z^{-1}]]$. It is often referred to as the *formal series without constant term*. 

It is obvious that 

$$
\text{val }(\partial \phi) \geq  \text{val }(\phi)+1
$$

with equality iff there is no constant term.

- - -

With the help of the standard valuation, we can introduce the concept of `distance` into the ring of the formal series. Define

$$
d(\phi,\psi) := 2^{-\text{val }(\phi-\psi)},\quad  \phi,\psi \in \mathbb{C}[\![z^{-1}]\!]
$$

as the distance between $\phi$ and $\psi$. It can only take discrete values, such as $1, 1 / 2, 1 / 4,$ etc. 

With the definition of distance, $\mathbb{C}[[z^{-1}]]$ becomes a `complete metric space`. The topology induced by this distance is called the `Krull topology` or the `topology of the formal convergence` (or the ${\frak I}$-adic topology). It provides a simple way of using the language of topology to describe certain algebraic properties.

We mention that a sequence $\phi_ {n}$ of formal series is a Cauchy sequence iff for each $i\in\mathbb{N}$, the $i$-the coefficient is stationary, namely the $i$-th coefficient of $\phi_ {n}$ becomes a constant when $n$ is larger than certain natural number. 
