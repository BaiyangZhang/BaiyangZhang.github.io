---
layout: post
title: Introduction to Transseries
subtitle: 
date: 2023-11-08
author: Baiyang Zhang
header-img: img/background2.jpg
catalog: true
tags:
---

## Introduction

In history, formal power series are used extensively for finding the resolution of differential equations. If the resulting power series is convergent, it gives rise to a germ which can be analytically continued to (multi-valued) functions on a Riemann surface. However, very often, the power series we found from solving a differential equation is divergent, then it is not clear *a prior* how to attach reasonable sums to them.

The modern theory of `resummation` was developed systematically by Stieltjes, Borel and Hardy, who invented some resummation methods which *are stable under the common operators of analysis*. Later, Poincare established the equivalence between computations with formal power series and asymptotic expansions. Newton, Borel and Hardy were all aware of the systematic aspects of their theories and they consciously tried to complete their framework so as to capture as much of analysis as possible. The great unifying theory nevertheless had to wait until the late 20-th century and Ecalle’s work on transseries and Dulac’s conjecture. 

- - -

Transseries have found significant applications in various areas of physics, particularly in high-energy physics. They are employed as algebraic tools to investigate self-consistent Dyson–Schwinger equations, which are integral equations that arise in the field of quantum field theory, specifically in Yukawa theory and quantum electrodynamics [1](https://www.sciencedirect.com/science/article/pii/S0003491616300793). These equations are pivotal in understanding the interactions of particles and fields at a fundamental level.

In the realm of general relativity, transseries are applied to asymptotic analysis. General relativity stands as one of the cornerstones of modern physics, governing the laws of gravitation and the dynamics of large-scale structures in the universe . By applying transseries in this domain, researchers can gain insights into the asymptotic behavior of gravitational fields and the dynamics of spacetime.

Furthermore, transseries are used in the *extraction of non-perturbative physics from perturbation theory through resurgence and alien calculus*. Perturbation theory is a fundamental tool in quantum mechanics and quantum field theory, allowing for the approximation of complex systems. The non-perturbative effects are those that cannot be captured by perturbation theory alone, and transseries help to identify and understand these effects [2](https://www.sciencedirect.com/science/article/pii/S0003491619301691)..

Additionally, in the context of integrable, asymptotically free field theories, transseries have applications in studying the free energy of such systems when coupled to a conserved charge. These studies are significant in high-energy physics, particularly in understanding the thermodynamics and statistical mechanics of particle systems [3](https://link.springer.com/article/10.1007/JHEP08%282022%29279).

These examples showcase the versatility and importance of transseries in advancing the understanding of fundamental physics, from the microscale of particle interactions to the macroscale of cosmic phenomena.

I hope the information provided has sparked your interest in transseries. Now, let's delve into the subject itself.

- - -

Define a ordered group ${\frak G}$ (frak G) of transmonomials. Define a differential field $\mathbb{T}$ of `transseries`. Transmonomials are generalizations of monomials in polynomials, by including exponential and logarithmic. In this note and that follows, we will consider the limit where $x\to \infty$. 

Let's start with exponents first.

**Log-free transmonomials.** They are of form 
$$
x^{b}e^{ L },\quad  b\in \mathbb{R},\; L \in \text{large log-free transseries.} 
$$

For example, the following are all log-free transmonomials,
$$
x^{-1},\; x^{\pi}x^{x^{\sqrt{ 2 }}-3x},\; e^{ \sum_ {i}x^{-1}e^{ x } },etc.
$$

The multiplication is defined in the obvious way. The group identity is just $1$. 

We define a binary relation $\gg$, read "far larger than". Keep in mind that we assumed $x\to \infty$. So how does this "far larger than" work? We compare the exponents $e^{ L }$ first, whichever with the largest exponent $L$ is far larger than others; if they have same exponents, then we compare the power of $x$, namely $x^{b}$, whichever with larger $b$ is far larger then others. To be specific,
$$
x^{b_ {1}}e^{ L_ {1} } \gg  x^{b_ {2}}e^{ L_ {2} }\quad  \text{ if } L_ {1} > L_ {2} \;\lor\; (L_ {1}=L_ {2}\;\land\; b_ {1}>b_ {2} ),
$$
where $\lor$ is logic or. For example, $x^{-5}\gg x^{20}e^{ -x }$ since $x^{-5}=x^{-5}e^{ 0 }$ and $0>-x$. 

**Log-free transseries.** A log-free transseries $T$ is a formal sum of log-free monomials ${\frak g}$,
$$
T = \sum_ {i} c_ {i} {\frak g}_ {i},\quad  c_ {i} \in \mathbb{R} .
$$
We require the order of transmonomials be such that, each ${\frak g_ {i}}$ is far smaller than all previous terms, namely they appear in descending orders. This is similar to the case of regular polynomials where we usually put the highest powers at first. 

The transseries $T$ is said to be `purely large` if all transmonomials ${\frak g}_ {i}$ are far larger than $1$ (not $0$), namely ${\frak g_ {i}}\gg  1 \;\forall i$. $T$ is said to be `small` if all ${\frak g}_ {i}\ll 1$ (why isn't it called purely small?). The largest (in the sense of far larger than) transmonomial is called the `dominant term`, let's call it $c_ {0}{\frak g}_ {0}$. If the dominant term has positive coefficients, $c_ {0}>0$, then $T$ is said to be positive. This enables us to compare the size of two transseries $S,T$, we say $S>T$ if $S-T>0$. So we just need to compare their dominant terms.

- - -

We consider only transmonomials and transseries of “finite exponential height”. For example, we don't want
$$
e^{ x^{x^{x\dots}} }.
$$

The `differentiation` of $T$ with respect to $x$ is defined the usual way. 

- - -

Next let's include logarithmic. $\log$ acting $m$ times is denoted $\log_ {m}x$ or $\log_ {(m)}x$, namely
$$
\log_ {(m)}x = \log \dots \log x,\quad  m\; \log .
$$

A general transseries is obtained by substitution of some $\log_ {m}x$ for $x$ in a log-free transseries. 

*Every nonzero transseries has a multiplicative inverse.* This is similar to formal power series. 

*A lot of functions can now be regarded as a transseries*. For example, e hyperbolic sine is a two-term transseries.

## Formal Constructions

In mathematics, the move towards higher levels of formality entails adopting rigorous and precise language, definitions, and proofs, which brings clarity and precision, ensuring that mathematical concepts are universally understood and applied correctly. It allows for the development of solid, gap-free proofs, having a deeper understanding of mathematical structures and providing a robust foundation for complex theories. This precision in communication is critical in a global context, where scientists from different fields rely on universally recognized formalisms to understand each other effectively. 

However, this precision comes at a cost. It can make the subject less accessible to beginners (like myself), potentially hindering educational and interdisciplinary work. A focus on stringent formalism might even inhibit creative thinking, as the rigidity of formal proofs could constrain the exploratory, intuitive processes that often drive mathematical discovery. Moreover, the lengthy and detailed nature of formal proofs can make mathematical work less efficient, both in terms of personal understanding and communication with others. There's also the risk of diminishing intuition, which is a crucial aspect of mathematical thought, particularly in the preliminary stages of research. It is definitely crucial to have a balance between concrete examples and general formalism, what is I hope to achieve in this note.

- - -

The set of monomials ${\frak G}$ form a field, which is also a group if we focus on multiplication alone. ${\frak G}$ is *not* finitely generated, to see this consider the finitely generated group with generator 
$$
\mu_ {1},\mu_ {2},\dots,\mu_ {n},
$$
the generated group has elements of form
$$
\left\{ \mu_ {1}^{k_ {1}}\times \mu_ {2}^{k_ {2}}\times \dots \times \mu_ {n}^{k_ {n}} \,\middle\vert\, k_ {1},\dots,k_ {n} \in \mathbb{Z} \right\} .
$$
Note that the exponents must be integers. 

Let's use capital letters to denote a set of indices, for example define 
$$
K := (k_ {1},k_ {2},\dots,k_ {n})
$$
then 
$$
\mu_ {1}^{k_ {1}}\dots \mu_ {n}^{k_ {n}} =: \mu^{K}.
$$

This will save some writing. The problem is that $\mu^{K}$ can also be interpreted as $\mu^{k_ {1}k_ {1}\dots k_ {n}}$, but it should be clear from the context. 

