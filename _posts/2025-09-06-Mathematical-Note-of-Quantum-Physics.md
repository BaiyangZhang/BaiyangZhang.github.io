---
layout: post
title: Mathematical Note of Quantum Physics
date: 2025-09-06
author: Baiyang Zhang
catalog: true
tags:
---

Let $T: \mathcal{H}\to\mathcal{H}'$ be a linear operator. $T$ is said to be `bounded` if $\left\lVert T(\xi)\right\rVert\leq C\left\lVert \xi \right\rVert$ for all $\xi \in\mathcal{H}$ where  $C<\infty$. The smallest of such $C$ is called the `operator norm` of $T$, denoted $\left\lVert T \right\rVert$. $T$ is bounded iff $T$ is continuous. 

The space of all the **bounded** linear operator that maps $\mathcal{H}$ to itself is denoted $B(\mathcal{H})$. It is a Banach space with operator norm.

The kernel $\text{ker}(T)$ of a bounded operator $T$ is a closed subspace of $\mathcal{H}$.

*Riesz's representation lemma.* Let $T$ be a bounded (complex) functional of $\mathcal{H}$. Then $T$ can be represented by a state $\eta \in\mathcal{H}$ such that for all $\xi \in\mathcal{H}$, $T(\xi)=\left\langle \eta,\xi \right\rangle$. 

$T\in B(\mathcal{H})$ is an `isometry` if $\left\langle T\xi,T \eta \right\rangle=\left\langle \xi,\eta \right\rangle$ for all $\xi,\eta \in\mathcal{H}$.

$U\in B(\mathcal{H})$ is unitary iff $U$ is surjective and isometry.

In general topology, a set $K$ is **compact** if every open cover of $K$ has a finite subcover. 

`Sequential compactness` means that every sequence has a convergent subsequence whose limit lies in the set itself. 

In **metric spaces** (like $\mathbb{R}^n$, Hilbert spaces, Banach spaces), these two definitions are equivalent. In general topological spaces, they are _not_ equivalent.

set $K \subset H$ is **relatively compact** if its closure $\overline{K}$ is compact. **Compact** means: every sequence in $\overline{K}$ has a convergent subsequence with a limit in $\overline{K}$. So, relatively compact means: all sequences have convergent subsequences, possibly converging to points just outside $K$, but within its closure.

A linear operator $T: \mathcal{H} \to \mathcal{H}$ is **compact** if it maps bounded sets to relatively compact sets. In other words, take any bounded set $B \subset \mathcal{H}$, then $T(B)$ should have the property that every sequence in it has a convergent subsequence (in $\mathcal{H}$). This is stronger than just continuity. Compact operators “shrink” infinite-dimensional complexity down so that images behave almost like finite-dimensional sets.

A Hilbert space $\mathcal{H}$ is `separable` if there exists a **countable dense subset** $D\subset \mathcal{H}$.

The `spectrum` of  $T: \mathcal{H}\to\mathcal{H}$ is like a generalization of the eigenvalues. It is defined as 

$$
\sigma(T) := \left\lbrace \lambda \in \mathcal{C} \,\middle\vert\, \text{ker}(T-\lambda \mathbb{1})\neq 0  \right\rbrace .
$$

If $T:\mathcal{H}\to\mathcal{H}$ is compact and self-adjoint, then $T$ at least has one eigenvalue, $\pm\left\lVert T \right\rVert$.

**Spectral theorem.** Let $T: \mathcal{H}\to\mathcal{H}$ be compact and self-adjoint. We have the following:
1. The spectrum is real.
2. ...

If $T$ is a bounded operator and $[T,T^\ast]=0$ then $T$ is said to be `normal`.

The multiplication operator $M_ {g}$, $M_ {g} \psi := g\psi$, is the only normal operator up to unitary equivalence. If $T: \mathcal{H}\to\mathcal{H}$ is a bounded, normal operator, then there exists a bounded function $g$ such that $T = U^{\dagger} M_ {g} U$, where $U$ maps $\mathcal{H}$ to $L^{2}$ space. 

Let $T: D(T)\to\mathcal{H}$ be an unbounded operator, $D(T)$ is the domain of $T$. We say $T$ is `densely defined` if $D(T)$ is dense in $\mathcal{H}$. That means, for each $x\in\mathcal{H}$, there exists a sequence $x_ {i}$ in $D(T)$ such that $x_ {i}\to x$ in $H$. Equivalently, $\overline{D}(T) = \mathcal{H}$. 

If $T$ is densely defined, then one can define $T^\ast$.

If the graph $\text{Gr}(T):=\left\lbrace (x,Tx) \,\middle\vert\, x\in\mathcal{H} \right\rbrace$ is a closed subspace of $\mathcal{H}\otimes \mathcal{H}$, then $T$ is called closed. 

When we write $E_ n \uparrow X$, it means$E_ 1 \subseteq E_ 2 \subseteq E_ 3 \subseteq \cdots$, an increasing sequence of sets, and the union of all the $E_ n$ is the whole set $X$.

The `image` of $T$ is sometimes written as $\text{ran}(T)$, the range of $T$. 

$T$ is symmetric is $\left\langle T\eta,\xi \right\rangle=\left\langle \eta,T\xi \right\rangle$ on the domain of $T$. $T$ is said to be self-adjoint if it is symmetric on all of $\mathcal{H}$. 

- - -

The space of pure states of quantum mechanics is the projective space $\mathcal{S}:=\mathbb{P}(\mathcal{H})$. The observables are (sometimes unbounded) self-adjoint operators defined on a dense subspace of $\mathcal{H}$. 

The spectral theorem for self-adjoint operators says that, every self-adjoint operator $T$ on a Hilbert space is **unitarily equivalent** to a multiplication operator $M_ {\alpha}$ on some $L^2$-space. Note that, the theorem does not say that TTT is literally multiplication on your original Hilbert space. It only says that after a suitable change of coordinates (via a unitary transform), it becomes multiplication.

A bounded operator $T$ is said to be `trace class` (or of `nuclear class`) if

$$
\left\lvert T \right\rvert := \sum_ {n=1}^\infty s_ n(T) < \infty,
$$

where $s_ n(T)$ are the singular values of $T$, i.e. the eigenvalues of the positive operator

$$
\left\lvert T \right\rvert  := (T^\ast T)^{1/2}
$$

arranged in decreasing order and counted with multiplicity. The number $\left\lvert T \right\rvert$​ is called the `trace norm`.

- - -

