---
layout: post
title: Homotopy, Extension, and some topology of SU(N)
subtitle: 
date: 2023-11-18
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Frankel
---

*Disclaimer: Nothing in this note is original.*

## Homotopies and Extensions

The problem of extension in homotopy typically deals with the following question: given a continuous map defined on a subspace of a topological space, can it be extended to a continuous map on the entire space? Take the extension of a function on a sphere for example. Let $\mathbb{S}^{1}$ be the equator of a $\mathbb{S}^{2}$, and a continuous map $f$ define on $\mathbb{S}^{1}$:
$$
f: \mathbb{S}^{1} \to \mathbb{R}.
$$
The extension problem would be, can you find a function 
$$
F: \mathbb{S}^{2} \to \mathbb{R}
$$
such that the restriction of $F$ on $\mathbb{S}^{1}$ gives $f$? The ability to extend $f$ depends on its homotopy properties. For instance, if $f$ represents a simple loop around the equator, it may or may not be extendable based on how it "wraps around" the sphere. Certain topological features of the function $f$, such as its winding number or degrees, can serve as **obstructions** to extending it over the entire sphere. In this particular example, $f$ is extendable to the whole sphere if it has zero winding, otherwise the non-zero winding will cause some singularity when extending it to the whole $\mathbb{S}^{2}$. 

- - -

Now, consider a sphere of arbitrary dimension $n$, and consider it as the boundary of some $n+1$ dimensional disk $\mathbb{D}^{n+1}$ (a ball if $n>0$). Let $M$ be a $n$ dimensional manifold. We have the following simple observation.

**Extension Theorem.** The function 
$$
f:\mathbb{S}^{k} \to M^{n}
$$
is homotopic to a constant map iff $f$ can be extended to a map of the ball
$$
F: \mathbb{D}^{k+1} \to M.
$$
The proof is rather intuitive, just think of the homotopy as shrinking $\mathbb{S}^{k}$ all the way to the center of the circle. 

The extension theorem is important when discussing **defects**.

- - -

## Covering homotopy

Let $\pi: E \to M$ be a vector bundle and $f: W \to E$ be a map of a space $W$ into the bundle space $E$. Then the composition 
$$
W \xrightarrow{f}E \xrightarrow{\pi} M
$$
defines a map $\overline{f}$ from $W$ to $M$,
$$
\overline{f} := \pi \,\circ\, f.
$$

Now, let $\overline{F}: \overline{f}\to \overline{f_ {1}}$ be a homotopy (a series of continuous functions parametrized by $t$ from $\overline{f}$ to $\overline{f_ {1}}$), we claim that we can **cover the homotopy** $\overline{F}$ by a homotopy of the original map $F: f\to f_ {1}$. That is, there is a map
$$
F: W\times [0,1] \to E
$$
such that for $w \in W$,
$$
F(w,0)=f(w),\quad  F(w,1)=f_ {1}(w).
$$
The trick to prove the existence of covering of a homotopy is to find a way to lift the homotopy from $M$ to $E$. To be specific, consider a fixed point $w \in W$ and look at the curve 
$$
\overline{C}:t \in [0,1] \to \overline{F}(w,t)
$$
in $M$. We need to find a unique lifting of $\overline{C}$ to a curve $C$ in $E$. The way to achieve that is to endow the bundle a connection $\omega$, then require $C$ to be the **horizontal lift**. 

*Note that if $\overline{f}$ is homotopic to a constant map $p_ {0}$, it need not be that $f$ will be homotopic to a constant map*.

What we have said for a vector bundle can also be shown to hold for a principal fiber bundle.

It turns out that one can cover homotopies in **any** fiber bundle, without any use of a connection. In fact, one generalizes the notion of a fiber bundle to that of a `fiber space`. This is a space $P$ equipped with a map $\pi: P\to M$ such that **homotopies can always be covered**. Such spaces need not be local products.

## Some Topology of $SU(n)$

$SU(n)$ is represented by $N \times N$ complex matrices acting on $\mathbb{C}^{n}$. Since each $g \in SU(N)$ is unitary, $SU(N)$ sends the unit sphere $\mathbb{S}^{2N-1} \subset \mathbb{C}^{n}$ 
$$
\mathbb{S}^{2N-1} = \left\lbrace z \in  \mathbb{C}^{N} \,\middle\vert\, \left\lvert z_ {1} \right\rvert^{2} + \dots + \left\lvert z_ {N} \right\rvert^{2}=1  \right\rbrace 
$$
into itself. The action is also transitive (meaning any two points on $\mathbb{S}^{2N-1}$ can be connected by some group action). The isometry group for the point $(1,0,\dots,0)$ is clearly
$$
\begin{bmatrix} 
1 & 0 \\
0 & SU(N-1)
\end{bmatrix}
$$
which we shall briefly denote simply by $SU(N-1)$. 

We have
$$
\mathbb{S}^{2N-1} \cong  \frac{SU(N)}{SU(2N-1)}.
$$

and in fact $SU(N)$ is a principal $SU(N − 1)$ bundle over $\mathbb{S}^{2N-1}$, with fiber at each point $p\in M$ being the little group of $p$. Thus we write
$$
SU(N-1)\to SU(N) \to \mathbb{S}^{2N-1}
$$
**Theorem.** If $F\to P \to M$ is a fiber bundle with connected $M$ and connected $F$, then $P$ is also connected.

As a corollary, $SU(N)$ is connected. To see that, note $SU(1)$ is a single point, $SU(2)$ is a $3$-sphere and is connected, as are all $k$-spheres for $k\geq 3$. From
$$
SU(2) \to SU(3) \to \mathbb{S}^{5}
$$
we see that $SU(3)$ is connected. The connectness of higher $SU$ groups follow from induction.


Another example of the above theorem is the `Hopf fibration`. The Hopf fibration is a fiber bundle where the total space $P$ is $\mathbb{S}^{3}$, the base space $M$ is $\mathbb{S}^{2}$ and the fiber $F$ is $\mathbb{S}^{1}$. 

- - -

Recall that we say that $M$ is simply connected provided every map of a circle into $M$ is homotopic to a constant map. During the homotopy, the closed curve gets “contracted” or “deformed” to the point. 

**Theorem.** Let $F\to P \to M$ be a fiber bundle whose fiber and base space are both simply connected. Then $P$ is simply connected. 

