---
layout:     post   				                    # 使用的布局（不需要改）
title:      Basic Algebraic Geometry Class 13		# 标题 
subtitle:   Completeness
date:       2023-2-10 				# 时间
author:     Baiyang Zhang 						# 作者
header-img: img/mathArt7.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - Math
    - Commutative Algebra
    - Notes
---

### Completeness

The goal here is to introduce a useful analogue of compactness for the Zariski topology.

If $k=\mathbb{C}$, then in classical topology $\mathbb{P}^{n}$ is compact, indeed it is the one point compactification, while $\mathbb{A}^{n}$ is not. For example the complex plane can be compactified into a Riemann sphere. However compactness depends on the open sets (recall that a space is compact iff every open cover has a finite sub open cover), but open sets in Zariski topology is problematic, it is too coarse, meaning it has too few open and closed sets. When you define compactness, you need the space to be Hausdorff, while Zariski topology is not. 

One observation is that, with respect to Hausdorff topology, one can show that for a Hausdorff topological space $X$, it is compact if and only if the projection

$$
X\times Y\to Y
$$

is closed where $Y$ is any topological space, and a `closed map` means that the image of closed sets are closed. It is like a dual notion for continuous maps. Now in this situation of course we have the product topology on $X\times Y$, but it needs not be so for varieties. One direction of the statement (the "if" part, compactness implies closed projection) is just the tube lemma, the other direction (the "only if" part, non-compactness implies non-closed projection) is more complicated to prove, interested reader can find a lot of reading material online.

So we take this as the definition of completeness. An algebraic variety is `complete` if the projection $\pi : X\times Y\to Y$ is closed for any algebraic variety $Y$. That is, if $Z \subset X\times Y$ is closed, then $\pi(X)\subset Y$ is closed. 

- - -

The first thing we want to show is that, by this definition, the projective space is complete. This is somehow the main reason we defined this notion.

First one can prove that the map

$$
\pi: \mathbb{P}^{n} \times \mathbb{P}^{m} \to \mathbb{P}^{m}
$$

is closed. If $Z\subset\mathbb{P}^{m}\times\mathbb{P}^{n}$ is closed, then the condition $a\notin Z$ is open. Remember that we want to enter $\mathbb{P}^{m}$ by any algebraic variety, but now we only start with $\mathbb{P}^{m}$. The map simply takes 

$$
(x,y)\mapsto y, \quad  x \in \mathbb{P}^{n},\, x \in  \mathbb{P}^{m}.
$$

Denote the affine coordinates on $\mathbb{P}^{n}$ by $[x_{0},\dots,x_ {n}]$ and on $\mathbb{P}^{m}$ by $[y_{0},\dots,y_ {m}]$. What do we mean by saying that some subvariety on $\mathbb{P}^{n}\times\mathbb{P}^{m}$ is closed? Well, we can use the Segre embedding, saying that $Z$ is closed if $Z=V(f_{1},\dots,f_ {r})$ where each $f_ {p}$ is homogeneous of degree $d$, in both $x_ {i},y_ {j}$. Next define

$$
g_ {p} = f_ {p}(\bullet,a)
$$

where $\bullet$ is a place holder, a blank, where we can put a parameter, and $a$ is a point in $\mathbb{P}^{m}$, thus $g_ {p}$ is a polynomial on $\mathbb{P}^{n}$. Now the requirement $a \notin Z$ means that there exists no $x \in\mathbb{P}^{n}$ such that $(x,a)\in Z$, which means the zero loci $V(g_{1},\dots,g_ {r})=\emptyset$. This in turn amounts to saying that the ideal generated by $g_ {i}$, $(g_{1},\dots,g_ {r})$ is either the whole ring (which would be all in the affine case), or the ring $(x_{1},\dots,x_{n})$. From here on one can show that the condition $a \notin Z$ amounts to the condition that some determinant is non-zero, but the determinant is just some polynomial function, non-zero determinant means non-zero polynomial function, which is an open condition.

If $\mathbb{P}^{m}$ is replaced by some affine variety $Y$, the projection 

$$
\pi: \mathbb{P}^{n} \times  Y \to Y
$$

is closed. 

Lastly one can replace $Y$ by any varieties. The detail of the process can be found online. 

### Veronese embedding

The ideal is to find an embedding "of degree $d$ " 

$$
\mathbb{P}^{n} \to \mathbb{P}^{N}
$$

such that a homogenous polynomial of degree $d$ is map to a polynomial of degree one, namely a  linear function. It uses the fact that $\mathbb{P}^{n}$ is complete. 

Let

$$
N+1 = \begin{pmatrix}
n+d \\
d
\end{pmatrix}
$$

be the number of monomials of degree $d$ in $x_{0},\dots,x_ {n}$. A trick is to introduce some place holders when thinking about the combination. Call them $f_{0},\dots,f_ {N}$. 

We claim that the map

$$
F: \mathbb{P}^{n}\to\mathbb{P}^{N}, \quad  x\mapsto [f_{0}(x): \dots :f_ {N}(x)]
$$

defines an isomorphism from $\mathbb{P}^{n}$ onto the projective variety $F(\mathbb{P}^{n})\subset\mathbb{P}^{N}$.

Observe that as a subset of $f_{0},\dots,f_ {N}$ we have $x_ {i}^{d}$, and the variety given by them $V(x_{1}^{d},\dots,x_ {n}^{d})=\emptyset$, thus $V(f_{0},\dots,f_ {N})=\emptyset$. Then from previous lectures we know that $F(\mathbb{P}^{n})$ is closed, since $\mathbb{P}^{n}$ is complete. 

For any ordering of the $f_ {i}$, the map $F$ is called the `degree` $d$ `Veronese embedding`. The coordinates on $\mathbb{P}^{N}$ are called the `Veronese coordinates`  on $\mathbb{P}^{n}$. This can be extended to any projective variety $X\subset\mathbb{P}^{n}$. 

As an interesting application, we claim without proof that, if $X\subset\mathbb{P}^{n}$ is a projective variety and $f\in \mathcal{S}(X)_ {d}$ with $d\geq{1}$, then $X-V(f)$ is an affine variety. As a special case, let $X=\mathbb{P}^{n}$ and $f=V(x_{0})$, then $\mathbb{P}^{n}-V(x_{0})$ is just the affine slice. It's like removing the point at infinity, thus undoing the compactification.

### Rational maps

Rational maps are generalizations of morphisms of algebraic varieties. 

Algebraic geometry is all about understanding varieties via their coordinates functions. For affine varieties it is great. But for complete varieties it raises problems. On complete varieties, there are no non-constant global regular functions. So, what do you do about this? The remedy is that, we want to allow more functions. The condition that a function be defined everywhere is too strict, we want to allow functions that are not defined on some small sets, just like meromorphic functions (functions with poles). 

More generally, we will allow maps defined only on dense open subsets. Recall that a set is called dense if its closure is the whole set. The bonus is that it allows us to study "bad" functions. 

Let $X,Y$ be algebraic varieties. Remember that our idea is to study functions defined on dense, open subsets, up to equality on a dense open subset. We will explain what equality mean in the next paragraph.

Consider pairs $(U,f)$ and $(V,g)$, where $U,V$ are open dense subsets of $X$, which inherits the variety (sheaf) structure, whose elements are $f$ and $g$. These two pairs are said to be `equal` if on some dense open subset of their intersection $W \subset U\cap V$, we have $f \mid_ {W}=g \mid_ {W}$. Roughly speaking ,two equivalent pairs can be regarded as two patches of the same thing.

**Definition.** A `rational map` from $X$ to $Y$ is an equivalence class of pairs $(U,f)$ of a dense, open subset $U\subset X$ and a morphism $f: U\to Y$.

If you don't like the idea equivalence class, just think of the rational map as maps on dense, open subset of $X$ but with a weaker notion of equality, two maps are equal if they agree on some dense open subset. It is denoted by $f: \dashrightarrow Y$.