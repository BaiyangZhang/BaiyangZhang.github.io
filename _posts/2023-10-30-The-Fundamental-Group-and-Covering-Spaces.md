---
layout: post
title: The Fundamental Group and Covering Spaces
subtitle: 
date: 2023-10-30
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - geometry
  - frankel
---

*Disclaimer: Nothing in this note is original.*

Let $\gamma$ be a loop with base point $p_ {0}$, on a connected (not necessarily simply connected) maniofld $M$. This circle is a map

$$
\gamma: [0,1]\to M,\quad  \gamma(0)=\gamma(1)=p_ {0}.
$$

Consider all such loops with the same base point. Recall that if we can deform one loop to another in a continuous fashion while preserving the base point, we say they are homotopic,

$$
\gamma_ {1} \sim \gamma_ {2}.
$$

If some loop $\gamma$ is homotopic to a point, or a constant, then we call it trivial and write 

$$
\gamma \sim 1.
$$

Note the requirement that the base point must be fixed, sometimes it happens that a loop can be shrink to a point if you are allowed to move it around in the manifold, but if you have to fix a base point then it is no longer true. Hence, sometimes a loop is `homologically` trivial but not homotopically trivial.

Given two loops $\gamma_ {1}$ and $\gamma_ {2}$ on M, by reparameterization (so that each loop is traversed with double speed) we may compose them to give a new loop, which is traditionally written from left to right, for example $\gamma_ {1}\gamma_ {1}(\theta)$ means traverse along $\gamma_ {1}$ first then $\gamma_ {2}$. This defines the *"multiplication"* of loops. This multiplication is defined up to homotopy, under which the loops form a group structure. This is the `fundamental group` of $M$, written 

$$
\pi_ {1}(M; p_ {0}).
$$

If we don't care about the base point, then we simply write

$$
\pi_ {1}(M).
$$

Recall that, by definition, a space is `simply connected` if all loops are contractible to a point, that is, if the group $\pi_ {1}(M)$ consists only of the identity. 

Some famous example include that $\pi_ {1}(S_ {1})=\mathbb{Z}$, $\pi_ {1}(SO(3))=\mathbb{Z}_ {2}$, etc.

- - -

**Covering space**

We shall say that a connected space $\overline{M}$ is a covering of the connected $M$, with covering or projection map 

$$
\pi: \overline{M} \to M,
$$

if each $x\in M$ has a neighborhood $U$ such that the preimage $\pi ^{-1}(U)$ consists of *disjoint open* subsets $\left\{ U_ {\alpha} \right\}$ of $\overline{M}$, each *diffeomorphic* under $\pi$.

For example, we can cover $\mathbb{S}^{1}$ with $\mathbb{R}$ infinite times. 

The notion of covering space can also be described in terms of fiber bundles as follows: 

A covering space of a manifold $M$ is a connected space $\overline{M}$ that is a fiber bundle over $M$ with fiber $F$ a discrete set of points.

Let $M$ be a connected manifold. The universal covering manifold $\overline{M}$ of $M$ is a covering space that has trivial fundamental group. 

- - -

Let $\gamma,\gamma_ {1}$ be two paths form $p_ {0}$ to $p$. An orientable covering is such that if when we translate an orientation along the closed curve $\gamma\gamma ^{-1}$ we return with the original orientation. It is important that we are dealing with homotopy classes: if a closed curve $C$ preserves orientation, and if $C'$ is homotopic to $C$, then $C'$ will also preserve orientation.

An orientable covering is in general smaller than the universal covering, but not necessarily.

By the same arguments, it can be shown in general that the orientable cover of $M$ is either $M$ itself, if $M$ is orientable, or a 2-sheeted cover of $M$. As an example, a two-sheeted-orientable cover of the Klein bottle is the torus!

**Lifting paths**

Given a covering $\pi: \overline{M} \to M$, the lift of a path $\gamma$ in $M$ is roughly speaking a continuous path $\overline{\gamma}$ in $\overline{M}$ whose projection $\pi(\overline{M})$ is $\gamma$ itself.

By definition of the universal cover, the points of the fiber $\pi ^{-1}(p_ {0}), p_ {0}\in M$ are in $1:1$ correspondence with the distinct homotopy classes of closed curves in $M$ starting at $p_ {0}$. Summarizing, 

**Theorem.** The universal cover $\overline{M}$ of $M$ is simply connected and the number of sheets in the covering is equal to the number of elements (the `order`) of $\pi ^{-1}(p_ {0})$. 

If a manifold is not orientable, there is some closed curve that reverses orientation. We have the following explanation of the terminology that we have been using:

**Theorem.** The orientable cover of $M$ is always orientable. The number of sheets is $1$ if $M$ is orientable and $2$ if $M$ is not orientable.

- - -

In homotopy group $\pi_ {1}(M)$, there sometimes exists properties that can be used to define subgroups of $\pi_ {1}$. For example, if $M$ is not orientable, then two curves $\gamma,\gamma_ {1}$ in *different* homotopy class may preserve the orientation or not. $\gamma$ and $\gamma_ {1}$ may both preserve the orientation, then they belong to the same subgroup of $\pi_ {1}$ that is defined to be the loops that preserve the orientation. The identity of this subgroup is the equivalence class of all the loops that preserves the orientation, while the other element is the class of loops that flip the orientation, if you are in doubt just think of loops on a Mobius strip. 

There is a relation between the subgroups of $\pi_ {1}$ and the covering space. Given any subgroup $G$ of $\pi_ {1}$, we may associate a covering space $M_ {G}$ of $M$ as follows: We again consider pairs $p\in M,\gamma$, and we identify $(p,\gamma)$ with $p,\gamma_ {1}$ iff the homotopy class of the loop $\gamma \gamma_ {1}^{-1}$ lies in the subgroup $G$.

- - -

What happens if we put universal covering space with Lie group? After all Lie groups are nothing but manifolds themselves. It is more or less intuitive that, for a Lie group $G$, its universal covering space is itself another Lie group $\overline{G}$. For example, $SO(3)\cong \mathbb{R}P^{3}$ is a Lie group, its universal covering space is $SU(2)\cong \mathbb{S}^{3}$, which is another Lie group. 




