---
layout: post
title: Representables in Category Theory
subtitle: What do objects see?
date: 2023-12-23
author: Baiyang Zhang
header-img: img/background2.jpg
catalog: true
tags:
---

### Representables

A category is a world of objects, all looking at one another. Each sees the world from a different viewpoint. Take the category of topological spaces for example, consider the object with only one point, denoted $\star$, given another topological space $T$, a map 
$$
\star\to T
$$
can be regarded as $\star$ looking at $T$. What does $\star$ see? Since $\star$ itself is a point, the image given by a continuous map (by definitions the morphisms in the category of topological spaces are continuous maps) of $\star$ is another point in $T$, that's to say, a point can only see points! It can't see any other structures, limited by what it is. This is similar to what happens in a society with real people in it. A curve, on the other hand, could see much more. It can see a point if it wants, but it can also see another curve in other objects. In the language of category theory, all the things an object could see translates into *the set of arrow going out from it*.

We can also ask the dual question: *fixing an object of a category, what are maps into it*? Take the category $\text{Set}$ of sets for example. Consider a set with only two elements. Given any set $X$, the maps from $X$ to the two element set is the subset of $X$! 

In the following we will talk about how each object sees and is seen by the category. This naturally leads to the notion of `representable functors`, or just `representables`. 

- - -

Fix an object $A \in \mathcal{A}$. Consider the *totality* of maps *out of* $A$. To each $B\in \mathcal{A}$, there is assigned the set $\mathcal{A}(A,B)$ of maps from $A$ to $B$. This assignation is actually **functorial**, in the sense that to *each* $B\in\mathcal{A}$, there is a set $A(A,B)$, and to each arrow in $A$, there is another arrow in the codomain of this functorial, which we will define shortly.

**Definition 1.** Let $\mathcal{A}$ be a locally small (meaning that the arrows from one object to another actually form a set) category and $A\in \mathcal{A}$. Define a functor
$$
H^{A}: B \mapsto \mathcal{A}(A,B) ,\quad  \mathcal{A}\to \text{Set},
$$
where $B\in \mathcal{A}$ is any object in $\mathcal{A}$. In other words, $H^{A}$ is a set-valued functor defined on $\mathcal{A}$. For objects $A' \in \mathcal{A}$, 
$$
H^{A}(A') := \mathcal{A}(A \to A'),
$$
for maps in $g: A' \to A''$ in $\mathcal{A}$,  
