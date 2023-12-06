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

## Introduction

In history, formal power series are used extensively for finding the resolution of differential equations. If the resulting power series is convergent, it gives rise to a germ which can be analytically continued to (multi-valued) functions on a Riemann surface. However, very often, the power series we found from solving a differential equation is divergent, then it is not clear *a prior* how to attach reasonable sums to them.

The modern theory of `resummation` was developed systematically by Stieltjes, Borel and Hardy, who invented some resummation methods which *are stable under the common operators of analysis*. Later, Poincare established the equivalence between computations with formal power series and asymptotic expansions. Newton, Borel and Hardy were all aware of the systematic aspects of their theories and they consciously tried to complete their framework so as to capture as much of analysis as possible. The great unifying theory nevertheless had to wait until the late 20-th century and Ecalle’s work on transseries and Dulac’s conjecture. 

- - -

Transseries have found significant applications in various areas of physics, particularly in high-energy physics. They are employed as algebraic tools to investigate self-consistent Dyson–Schwinger equations, which are integral equations that arise in the field of quantum field theory, specifically in Yukawa theory and quantum electrodynamics [1](https://www.sciencedirect.com/science/article/pii/S0003491616300793). These equations are pivotal in understanding the interactions of particles and fields at a fundamental level.

In the realm of general relativity, transseries are applied to asymptotic analysis. General relativity stands as one of the cornerstones of modern physics, governing the laws of gravitation and the dynamics of large-scale structures in the universe . By applying transseries in this domain, researchers can gain insights into the asymptotic behavior of gravitational fields and the dynamics of spacetime.

Furthermore, transseries are used in the *extraction of non-perturbative physics from perturbation theory through resurgence and alien calculus*. Perturbation theory is a fundamental tool in quantum mechanics and quantum field theory, allowing for the approximation of complex systems. The non-perturbative effects are those that cannot be captured by perturbation theory alone, and transseries help to identify and understand these effects [2](https://www.sciencedirect.com/science/article/pii/S0003491619301691).

Additionally, in the context of integrable, asymptotically free field theories, transseries have applications in studying the free energy of such systems when coupled to a conserved charge. These studies are significant in high-energy physics, particularly in understanding the thermodynamics and statistical mechanics of particle systems [3](https://link.springer.com/article/10.1007/JHEP08%282022%29279).

These examples showcase the versatility and importance of transseries in advancing the understanding of fundamental physics, from the microscale of particle interactions to the macroscale of cosmic phenomena.

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

We will assume that all the generator $\mu \ll 1$. We will think of these as “ratios” between one term of a series and the next. A `ratio set` is a finite set of small monomials.

Let $k \in \mathbb{Z}^{n}$ be an $n$-tuple of integers, it form a group under addition. Let $p$ be another such $n$-tuple, one say 
$$
k \leq  p \quad  \text{ iff } k_ {i} \leq p _ {i}  \;\forall\; i,
$$
where $k_ {i}$ is the $i$-th component of $k$. 

$J_ {m}$ is a partially ordered set. To be specific, a partially ordered set (or poset) is a set equipped with a binary relation that captures a certain level of order or precedence among its elements. This binary relation is denoted by $\leq$ and must satisfy the following properties for any elements $a, b$, and $c$ in the set:

1. *Reflexivity*: For all elements a in the set, $a\leq a$. In other words, every element is related to itself;
2. *Antisymmetry*: If $a \leq b$ and $b \leq a$, then $a = b$. This property ensures that *no two distinct elements are related in both directions*;
3. *Transitivity*: If $a \leq b$ and $b \leq c$, then $a \leq c$. This property means that if there's an order relationship between $a$ and $b$, and another between $b$ and $c$, there's also an order relationship between $a$ and $c$.

A partially ordered set **does not** require every pair of elements to be comparable; that is, it's possible for $a$ and $b$ to be in the set without $a\leq b$ or $b \leq a$ being true. This distinguishes partially ordered sets from `totally ordered sets`, where **every pair of elements is comparable**.

For $m\in \mathbb{Z}^{n}$, define 
$$
J_ {m} := \left\lbrace k \in  \mathbb{Z}^{n} \,\middle\vert\, k\geq m \right\rbrace .
$$
Apparently $m \in J_ {m}$. The sets $J_ {m}$ will be used to define `grids` of monomials. For example, if 
$$
\mu_ {1} = \frac{1}{x},\quad  \mu_ {2}=e^{ -x }
$$
comprise the ratio group (recall that each element of a ratio group is required to be small), then we can define a `grid` (about which we will say more later)
$$
\left\lbrace \mu^{k} \,\middle\vert\, k\in J_ {(-1,2)} \right\rbrace 
$$
which is the same as
$$
\left\lbrace \mu^{k}=\mu_ {1}^{k_ {1}} \cdot \mu_ {2}^{k_ {2}} \,\middle\vert\, (k_ {1},k_ {2})\geq (-1,2) \right\rbrace .
$$

In our convention, the set of natural numbers $\mathbb{N}$ include zero. 

- - -

### Dickson's lemma

It turns out that the set $J_ {m}$ is `well-partially-ordered`, sometimes called `Noetherian`. A partially ordered set (poset) is said to be well-partially-ordered if it satisfies two conditions:
   - It contains no *infinite strictly descending sequences*. This means there cannot be an infinite sequence of elements $a_1, a_2, a_3, \ldots$ in the set such that $a_1 > a_2 > a_3 > \ldots$.
   - It contains no *infinite antichains*. An `antichain` is a subset of the poset in which no two distinct elements are comparable. In a well-partially-ordered set, there cannot be an infinite set of elements where none are comparable to each other.

On the other hand, a poset is called Noetherian if it satisfies the **descending chain condition** (**DCC**), which states that every descending sequence of elements eventually stabilizes. In other words, there cannot be an infinite strictly descending sequence of elements in the set.

The primary difference between the two concepts is that being well-partially-ordered is a stronger condition than being Noetherian. While both require the absence of infinite strictly descending sequences (the Noetherian property), being well-partially-ordered also requires the absence of infinite antichains. Therefore, every well-partially-ordered set is Noetherian, but not every Noetherian set is well-partially-ordered.

**Proposition.** If $E \subseteq J_ {m}$ and $E \neq \emptyset$, then there is a minimal element $k_ {0} \in E$. 

**Proposition.** Let $E$ from the previous proposition be infinite, then there is an infinite sequence $k_ {i}\subset E$ such that $k_ {0}<k_ {1}<\dots$. 

**Proposition.** For the same $E$, the set of all the minimal elements $\text{min}(E)$ is finite. For every element $k\in E$ there is a $k_ {0} \in \text{min}(E)$ such that $k_ {0} \le k$. 


### Convergence of sets

First let's introduce the symmetric difference of two sets, which is a mathematical operation that results in a new set containing elements that are in **either** of the two sets, but **not in their intersection**. In other words, it combines the elements of each set that are not shared by both. The symmetric difference is denoted by the symbol $\Delta$.

Formally, if you have two sets $A$ and $B$, their symmetric difference $A \Delta B$ is defined as:
$$ A \Delta B = (A - B) \cup (B - A). $$
Here, $A - B$ represents the set of elements in $A$ but not in $B$, and $B - A$ represents the set of elements in $B$ but not in $A$. The union of these two sets ($\cup$) forms the symmetric difference.

Another way to express this is using the union and intersection of sets:
$$ A \Delta B = (A \cup B) - (A \cap B). $$
By subtracting the intersection from the union, you're left with only those elements that are exclusively in either $A$ or $B$, but not in both.

The symmetric difference has several interesting properties:

- It is commutative: $A \Delta B = B \Delta A$.
- It is associative: $(A \Delta B) \Delta C = A \Delta (B \Delta C)$.
- The symmetric difference of a set with itself is the empty set: $A \Delta A = \emptyset$.
- The symmetric difference of a set with the empty set is the set itself: $A \Delta \emptyset = A$.

Now let's define the convergence of a sequence of sets $E_ {i}, i\in I$, where $I$ is an infinite index set. For each $i\in I$, let $E_ {i} \in \mathbb{Z}^{n}$. We say the family $E_ {i,\,i\in I}$ is `point-finite` if each $p\in \mathbb{Z}^{n}$ belong to $E_ {i}$ for only finite many $i$ (could be zero). 

Let $m\in\mathbb{Z}^{n}$ and define $J_ {m}$ as before. If the "limit" of $E_ {i}$ is empty, we write
$$
E_ {i} \xrightarrow{m}\emptyset,\quad  \text{iff } E_ {i} \subset J_ {m} \text{ and } (E_ {i}) \text{ is point-finite.}
$$
More generally, we write 
$$
E_ {i} \to \emptyset
$$
if there exist $m\in\mathbb{Z}^{n}$ such that $E_ {i}\xrightarrow{m}\emptyset$. 

Now we can generalize the situation to other than the empty set. To do that we need the concept of symmetric difference. Intuitively, if the limit of $E_ {i}$ is another set $E$, then there should be infinite sets $E_ {i, \, i>j}$ for some $j$ such that they all "tend to" contain $E$. It implies that $E_ {i}-E$ should tend to be empty, for if there is some element $e$ in the limit of $E_ {i}-E$ then $e$ should be in the limit, too. On the other hand, the limit $E$ shouldn't contain any more element that is not in $E_ {i}$'s. For example, if for all $i>j$, some element $e'$ is not in $E_ {i,i>j}$ then it should not be contained in the limit $E$ as well. These very hand-waving arguments inspires us to define the limit of $E_ {i}$ as follows. 

We write 
$$
E_ {i}\xrightarrow{m} E,\quad  \text{iff }E_ {i} \subset J_ {m} \text{ and } E_ {i}\Delta E\xrightarrow{m}\emptyset .
$$
All the properties we want for a limit of $E_ {i}$ are concisely contained in the condition that $E_ {i}\Delta E$ tend to the empty set. Also, we simply write 
$$
E_ {i}\to E
$$
if there exists some $m$ such that $E_ {i}\xrightarrow{m}E$ and we don't care about the details of $m$. 

Equivalently, we could say that $(E_ {i}\Delta E)$ is point finite.

**Example.** Consider $\mathbb{Z}^{n}=\mathbb{Z}^{1}=\mathbb{Z}$. Let $E_ {i} =\left\lbrace i,i+1,\dots \right\rbrace$ for $i\in \mathbb{N}$. Then the sequence $E_ {i}$ is point-finite. We have 
$$
E_ {i}\to \emptyset .
$$
But if we let $F_ {i}=\left\lbrace -i \right\rbrace$, then even though $F_ {i}$ is point-finite but $F$ can not be contained in some $J_ {m}$ so it does not converge. 

**Notation.** Let $k = (k_ {1},k_ {2},\dots,k_ {n})$ then define $\left\lvert k \right\rvert:=k_ {1}+k_ {2}+\dots+k_ {n}$.

For two pints $p,q$ in $J_ {m}$, we can introduce the concept of distance by defining
$$
d(p,q):= 2^{-\left\lvert p-q \right\rvert }
$$
This reminds me of Krull topology. 

For two sets $E,F\subset J_ {m}$, define
$$
d(E,F):= \sum_ {k\in E\Delta F} 2^{-\left\lvert k \right\rvert },
$$
then for any $E_ {i}\subset J_ {m}$, we have $E_ {i}\to E$ iff $d(E_ {i},E)\to 0$. And $d$ is a metric on the grid $J_ {m}$. 
