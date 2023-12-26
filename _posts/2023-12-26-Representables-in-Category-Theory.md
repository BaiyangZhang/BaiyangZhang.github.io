---
layout: post
title: Representables in Category Theory
subtitle: What do objects see?
date: 2023-12-26
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
H^{A}: B \mapsto \mathcal{A}(A,B) 
$$
where $\mathcal{A}(A,B)$ are the collection of arrows from $A$ to $B$, here $\mathcal{A}(A,B)$ is regarded as a set. Thus
$$
H^{A}:  \mathcal{A}\to \text{Set}
$$
where $\text{Set}$ is the category of sets, of which the objects are all kinds of sets and the arrows are function from one set to another. Let $B\in \mathcal{A}$ be an object in $\mathcal{A}$. Obviously $H^{A}$ is a *set-valued functor* defined on $\mathcal{A}$. For $A' \in \mathcal{A}$, 
$$
H^{A}(A') := \mathcal{A}(A \to A') \text{ regarded as a set}.
$$

An easy way to remember the direction of arrow (at least for me) is to think of $A$ in $H^{A}$ standing up high, since it is a superscript, it is standing "upstairs", as a result $A$ has a pretty good view, allowing it to "see" other objects (say, $B$) in $\mathcal{A}$, and the arrow $A \to B$ represents that $A$ is watching $B$. With this analogy, in novel *1984* by Orwell, the big brother is watching everyone in the nation, making him the *initial object.* Similarly, given $A \in \mathcal{A}$, when we need to talk about arrow coming from other objects *into* $A$ later, we will define the functor $H_  {A}$ where $H_ {A}(B)$ is the set of arrows from $B$ to $A$ this time, for $A$ sits at the bottom and everyone can see $A$. 

For a map $g: A' \to A''$ in $\mathcal{A}$,  $H^{A}$  maps $g$ to another map from $H^{A}(A')$ to $H^{A}(A'')$ by composition, that is  
$$
H^{A}(A'): A \to A', \quad  H^{A}(A'') : A\to A'', \quad  H^{A}(g): (A\to A') \to (A\to A'')
$$
where $H^{A}(g)$ is realized by
$$
A\to A' \xrightarrow{g} A''
$$
which is a map from $A$ to $A''$, hence an element of $H^{A}(A'')$. 

To explain it in a different way, consider object $X\in H^{A}(A')$, $X$ by construction is a map from $A$ to $A'$. Let $Y \in H^{A}(A'')$, then $Y$ is nothing but a map from $A$ to $A''$. Now, what is an arrow from $X$ to $Y$? It is something that maps $A\to A'$ to $A \to A''$, which can be achieved by the composition $g\,\circ\,X$, where $g: A' \to A''$. 

Sometimes $H^{A}(g)$ is written as $g\,\circ\,-$, where $-$ is a commonly used symbol as a place holder; or written as $g_ {\ast}$, reminding us that it is somehow "induced" by $g$. All are frequently used in publications.

- - -

Again, let $A$ be a locally small (the collection of morphisms between any two objects is a set) category. A functor
$$
X: \mathcal{A} \to \text{Set}
$$
is `representable` if 
$$
X \cong H^{A} \text{ for some } A \in \mathcal{A}.
$$
$A$ is said to be a `representation` of $X$, together with an isomorphism between $H^{A}$ and $X$. In other words, when dealing with a representable functor $X$, identifying a representation for $X$ requires more than just specifying an object $A$; we must also precisely determine how $X$ is isomorphic to $H^A$.

Representable functors are sometimes just called `representables`. Only set-valued functors (functors with codomain $\text{Set}$) can be representable. 

Representable functors are important for a few reason in category theory. The Yoneda Lemma, which is the topic of this note, is a fundamental result in category theory that involves representable functors. We will introduce the Yoneda lemma shortly, but shortly put it, it states that *every functor* is *naturally isomorphic* to a functor represented by some object in the category. This lemma provides a powerful tool for embedding any locally small category into a category of functors (where the arrows are natural transformations). The Yoneda embedding, which arises from this, embeds a category into a category of presheaves, preserving and reflecting properties of objects and morphisms. If you don't know (or not interested in) what a presheave is, just ignore it. 

Representable functors are key in the study of natural transformations. The `naturality condition` in the definition of natural transformations can be better understood and characterized using representables. Representables also play a role in the study of adjoints and limits, which are some key-important concepts in category theory. For instance, adjoint functors can often be characterized using representables, and the existence of certain limits and colimits (limits where all the arrows are reversed) can be analyzed through representable functors. Representable functors are also indispensable to sheaf theory and topos theory, providing a link between geometric intuition and abstract category-theoretic formalism. Unfortunately these fascinating results lie outside the scope of this simple note, or for that matter lie outside of my comprehension.

- - -

Since we are already talking about the category of functors, it is perhaps timely to mention two similar but distinct definitions in category theory, namely the category of functors and the so-called $2$-category.

- **Category of Functors**: This is a construction where the objects are functors and the morphisms between these objects are natural transformations. Specifically, given two categories $\mathcal{C}$ and $\mathcal{D}$, the category of functors, often denoted $\text{Fun}(\mathcal{C}, \mathcal{D})$, has as objects all functors from $\mathcal{C}$ to $\mathcal{D}$ and as morphisms the natural transformations between these functors.

- **$2$-Category**: A $2$-category is a more general and abstract concept. In a $2$-category, there are objects, morphisms between objects (also called `1-morphisms`), and morphisms between morphisms (called `2-morphisms`), or "arrows between arrows". This structure introduces a new level of morphisms.

In a certain sense, the category of functors between two categories can be seen as a specific example of a 2-category, where the objects are the categories, the 1-morphisms are the functors between these categories, and the 2-morphisms are the natural transformations between these functors. However, the concept of a 2-category is broader and can be applied to many other contexts beyond just categories and functors.

- - -

**Ex.1** Consider the category of sets, denoted $\text{Set}$, let $1$ be the set of only one element. Now, what would $H^{1}$ be? It can be written as 
$$
\text{Mor}(1,-) \text{ or } \text{Hom}(1,-) \text{ or } \text{Set}(1,-),
$$
they all mean the same thing: the maps from $1$ to something else. Let $S \in Set$, $H^{1}(S)$ would be the collection of the maps from $1$ to $S$, which is itself another set, hence
$$
H^{1}: \text{Set} \to \text{Set}.
$$
Since a map from $1$ to a set $S$ amounts to an element of $S$, we have
$$
H^{1}(S) \cong S \quad  \;\forall\; S \in  \text{Set}.
$$
It can be shown (which I will not do here) that this isomorphism is *natural* in $S$, so $H^{1}$ is naturally isomorphic to the identity functor $\mathbb{1}_ {\text{Set}}$. Hence $\mathbb{1}_ {\text{Set}}$ is representable, by $1$. 

- - -

Representability is not a property shared by just any set-valued functor. In fact, rather few functors are representable, consider the total amount of functors we could construct. However, forgetful functors *tend to be* representable. We state without proof the following proposition.

**Proposition.** Any set-valued functor with a left adjoint is representable. 

- - -

We have defined, for each object $A$ of category $\mathcal{A}$ , a functor $H^{A}\in[\mathcal{A},\text{Set}]$ (given two categories $\mathcal{A}$ and $\mathcal{B}$, $[\mathcal{A},\mathcal{B}]$ is the functor category from the former to the latter). This describes how $A$ sees the world. As $A$ varies, so does the view. On the other hand, it is always the same world being seen, so the different views from different objects are somehow related. Generally speaking, whenever there is a map between objects $A$ and $A'$, there is also a map between $H^{A}$ and $H^{A'}$. Since $H^{A}$ are $H^{A'}$ are both functors (the "view" of $A,A'$), a map between them are potentially natural transformation, potentially since we need to show that this map satisfies the rule of naturality. 

Precisely, a map
$$
f: A' \to A,\quad  A,A'\in \mathcal{A}
$$
induces a natural transformation
$$
H^{f} : H^{A} \to H^{A'}.
$$

A diagram of this can be found [here](https://q.uiver.app/#q=WzAsMixbMCwwLCJcXG1hdGhjYWx7QX0iXSxbMywwLCJcXHRleHR7U2V0fSJdLFswLDEsIkheQSIsMCx7ImN1cnZlIjotNH1dLFswLDEsIkhee0EnfSIsMix7ImN1cnZlIjo0fV0sWzIsMywiSF5mIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==).

<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsMixbMCwwLCJcXG1hdGhjYWx7QX0iXSxbMywwLCJcXHRleHR7U2V0fSJdLFswLDEsIkheQSIsMCx7ImN1cnZlIjotNH1dLFswLDEsIkhee0EnfSIsMix7ImN1cnZlIjo0fV0sWzIsMywiSF5mIiwwLHsic2hvcnRlbiI6eyJzb3VyY2UiOjIwLCJ0YXJnZXQiOjIwfX1dXQ==&embed" width="560" height="176" style="border-radius: 8px; border: none;"></iframe>



Recall that a natural transformation $\alpha$ between two functors $F$ and $G$, both from category $\mathcal{C}$ to category $\mathcal{D}$, is made up of components. Each component is a morphism in category $\mathcal{D}$.

For each object $X$ in category $\mathcal{C}$, the `component` of the natural transformation $\alpha$ at $X$ is a morphism in category $\mathcal{D}$:
$$ \alpha_ X : F(X) \rightarrow G(X) $$
These components must satisfy a naturality condition, which states that for every morphism $f: X \rightarrow Y$ in category $\mathcal{C}$, the following diagram commutes:
$$
\begin{CD} 
F(X) @>F(f)>> F(Y) \\ @V\alpha_XVV @VV\alpha_YV \\ G(X) @>G(f)>> G(Y) 
\end{CD}
$$
This means that there is essential only one way to go from $F(X)$ to $G(Y)$. This property must hold for all objects and morphisms in category $C$, making the transformation "natural" in the sense that it works consistently across the entire category.

Coming back to $H^{f}$. Let $B\in \mathcal{A}$, what would the component $H^{f}_ {B}$ be? Recall that $f$ maps from $A'$ to $A$, by construction $H^{f}$ maps in the opposite direction, it is the function
$$
H^{A}(B) \equiv \mathcal{A}(A,B) \to H^{A'}(B)\equiv \mathcal{A}(A',B), 
$$
in terms of the elements, let $p \in \mathcal{A}(A,B)$ we have
$$
H^{f}: p \mapsto p\,\circ\,f.
$$

Notice that, each $H^{A}$ is *covariant* (meaning they preserve the direction of the arrows), however they come together to form a *contravariant* thing! What exactly is this thing then? To understand it, the following definition is important:

Let $\mathcal{A}$ be a locally small category, the functor
$$
H^{-}: \mathcal{A}^{\text{op}} \to [\mathcal{A},\text{Set}]
$$
is defined on objects $A$ by $H^{-}(A)=H^{A}$, and on maps $f$ by $H^{-}(f)=H^{f}$.

A lot of explain regarding the notations is in order. Apparently the dash $-$ in $H^{-}$ is a placeholder, to be filled by whatever it acts on, no matter if it is an object or an arrow. $\mathcal{A}^{\text{op}}$ means the 



