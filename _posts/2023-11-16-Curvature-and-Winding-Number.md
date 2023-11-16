---
layout: post
title: Curvature and Winding Number
subtitle: 
date: 2023-11-16
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Minkowski
  - Frankel
---

*Disclaimer: Nothing in this note is original.*

We will assume that the Yang-Mills potential $\omega_ {U}$ in patch $U$ has no singularity. 

Let $\theta$ be the two-form curvature, we have the following observation for any vector bundle over all base manifolds,
$$
\theta \wedge \theta = (d\omega+\omega \wedge \omega)\wedge (d\omega+\omega \wedge \omega) ,
$$
using 
$$
\mathrm{Tr}\,(\omega \wedge \omega \wedge d\omega) = \mathrm{Tr}\,(d\omega \wedge \omega \wedge \omega)
$$
and 
$$
\mathrm{Tr}\,(\omega \wedge \omega \wedge \omega \wedge \omega)=0
$$
we have eventually
$$
\mathrm{Tr}\,(\theta \wedge \theta) = d\, \mathrm{Tr}\,\left( \omega \wedge d\omega+\frac{2}{3}\omega \wedge \omega \wedge \omega \right)
$$
thus $\mathrm{Tr}\,(\theta \wedge\theta)$ is *locally exact*, it is locally the differential of a $3$-form, called the `Chern-Simons` $3$-form. $\omega$ is not usually globally defined. 

Coming back to the case of instanton, outside the instanton the curvature vanishes but the connection does not, hence we have
$$
\int_ {U} \,  \mathrm{Tr}\,(\theta \wedge \theta) = \int_ {\partial U = \mathbb{S}^{3}} \,  \left( -\frac{1}{3} \right)\mathrm{Tr}\,(\omega \wedge \omega \wedge \omega).
$$
This allows us to write the winding number in terms of curvature, by applying some kind of Stokes theorem
$$
\frac{1}{24\pi^{2}}\int_ {\mathbb{S}^{3}} \,  \mathrm{Tr}\,(\omega_ {U}\wedge \omega_ {U}\wedge \omega_ {U})
= - \frac{1}{8\pi^{2}} \int_ {\mathbb{R}^{4}} \, \mathrm{Tr}\,(\theta \wedge \theta).
$$

Note that $\theta \wedge\theta$ is *not* the Lagrangian, which is $\mathrm{Tr}\,(\theta \wedge\star \theta)$.  We have
$$
\theta \wedge \theta = (\theta \wedge \theta)_ {0123}\,dt\wedge dx\wedge dy\wedge dz\propto \epsilon^{ijkl}F_ {ij}F_ {kl}
$$
while
$$
\theta \wedge \star \theta \propto F_ {ij}F^{ij}.
$$

### The Chern form for a $U(n)$ bundle

The topological significance of $\mathrm{Tr}\,(\theta \wedge\theta)$, generalizing Poincare’s theorem for closed surfaces (which says the sum of indices times multiplicity equal to the Euler characteristic), is developed by Chern. $\mathrm{Tr}\,(\theta \wedge\theta)$ is but one of a whole family of significant integrands, called the Chern forms. But before going into details, let's review what is `exterior power space` shortly.

Given a vector space $V$ over a field $F$ (like the real numbers $\mathbb{R}$), the exterior algebra is an algebraic structure that extends the concept of scalars and vectors to higher-dimensional analogs. It is denoted as $\bigwedge V$. The $k$-th `exterior power` of $V$, denoted as $\Lambda^k(V)$ or $\bigwedge^{k} V$, is a vector space that consists of all alternating $k$-linear forms on $V$. For example, in $\Lambda^1(V)$, elements are just vectors. An exterior differential form of degree $k$ (or a $k$-form) on a differentiable manifold $M$ is a smooth section of the $k$-th exterior power of the cotangent bundle of $M$. In simpler terms, a $k$-form is a mathematical object that can be integrated over $k$-dimensional submanifolds of $M$. These forms are crucial in defining integrals over manifolds and in the formulation of Stokes' theorem. 

The exterior power space $\Lambda^k(V)$ provides the algebraic structure that underlies the concept of $k$-forms. When you consider a manifold $M$ with a tangent space at each point that is a vector space $V$, the exterior power $\Lambda^k(T^\ast M)$ (where $T^\star M$ is the cotangent bundle of $M$) is the space in which exterior differential forms live. This means that each $k$-form is an element of $\Lambda^k(T^\star M)$ at each point of $M$.

**Example. 1** 

Considering the exterior powers of a three-dimensional complex vector space $V = \mathbb{C}^3$, with basis $\left\{ v_ {1},v_ {2},v_ {3} \right\}$. We explore the spaces formed by taking the exterior powers of $V$. These spaces are constructed using the wedge product as follows:

*Zeroth Exterior Power*, $\Lambda^0(V)$: This is the space of scalars. It is isomorphic to the field over which the vector space is defined, in this case, the complex numbers $\mathbb{C}$. The dimension of this space is one.

*First Exterior Power, $\Lambda^1(V)$*:  This is just the vector space $V$ itself, with dimension three (since $V = \mathbb{C}^3$). The basis are simply $\left\{ v_ {1},v_ {2},v_ {3} \right\}$.

*Second Exterior Power, $\Lambda^2(V)$*: This space consists of all skew-symmetric bilinear forms on $V$. It can be visualized as the space of oriented planes in $V$. It has dimension  $$
 \binom{3}{2} = 3, \text{ since there are 3 ways to choose pairs from 3 elements.}
 $$
The basis are $\left\{ v_ {1}\wedge v_ {2},v_ {1}\wedge v_ {3},v_ {2}\wedge v_ {3} \right\}$.

*Third Exterior Power, $\Lambda^3(V)$*: This is the space of 3-vectors in $V$. It represents the oriented volume elements in $V$. The dimension is $\binom{3}{3} = 1$ (there is only one way to choose triples from 3 elements). The basis is $v_ {1}\wedge v_ {2}\wedge v_ {3}$.

*Higher Exterior Powers, $\Lambda^k(V)$ for $k > 3$*: For any $k$ greater than the dimension of $V$ (which is 3 in this case), the exterior power $\Lambda^k(V)$ is the trivial vector space {0}, as there are no non-zero $k$-vectors in a 3-dimensional space for $k > 3$.

- - -

Let $V=\mathbb{C}^{N}$ be $N$-dimensional complex vector space. Let $A$ be a $N\times N$ complex matrix that acts on $V$ in the usual way. Consider the` characteristic (eigenvalue) polynomial` of $A$, 
$$
\det(\lambda I-A) = (\lambda-\lambda_ {1})(\lambda-\lambda_ {2})\dots(\lambda-\lambda_ {N})
$$
where $\lambda_ {1},\dots,\lambda_ {N}$ are the eigenvalues of $A$. Putting $\lambda=-1$ we have
$$
\begin{align}
\det(I+A) &= (1+\lambda_ {1})(1+\lambda_ {2})\dots(1+\lambda_ {N}) \\
&= 1 + \sum_ {i}\lambda_ {i} + \sum_ {i<j} \lambda _ {i} \lambda _ {j} +\dots+\prod_ {i=1}^{N}\lambda_ {i} \\
&= 1 + \mathrm{Tr}\,A + \mathrm{Tr}\, \bigwedge^{2}A +\dots+\mathrm{Tr}\,\bigwedge^{N}A
\end{align}
\tag{1}
$$
where the big wedges are called the `elementary symmetric functions` of he eigenvalues of $A$. The reason for this notation is as follows. Since
$$
A: V \to V
$$
is a linear transformation on $V$, we may let $A$ act on each of the *exterior power spaces* $\Lambda^{p} (A)$ by the so-called *exterior power operation* 
$$
\bigwedge^{p}A: \; v_ {1}\wedge \dots \wedge v_ {p} \mapsto (Av_ {1})\wedge (Av_ {2})\wedge \dots \wedge (Av_ {p} ).
$$
Let's take $p=N$ for example. $\Lambda^{N}(V)$ is one dimensional and 
$$
\left( \bigwedge^{N}A \right)(v_ {1}\wedge \dots \wedge v_ {n} ) = \det A\, (v_ {1}\wedge \dots \wedge v_ {n} ).
$$
Thus justifies the definition shown in the last term in Eq. (1). Let's take a look at other terms, for example, at $\Lambda^{2}A$. We treat $A$ as diagonal matrix $\text{diag}(\lambda_ {1},\dots,\lambda_ {N})$ to simplify the calculation, and we can consider 
$$
\bigwedge^{2}(v_ {i}\wedge v_ {j})
$$
as the component of the exterior power operator on basis $v_ {i}\wedge v_ {j}$. Then the trace of $\Lambda^{2}(A)$ is simply the sum total of all its components. We have
$$
\bigwedge^{2}(v_ {i}\wedge v_ {j}) = A_ {im} A_ {jn}(v_ {m} \wedge v_ {n} ) = (\lambda _ {i} \lambda _ {j})\, v_ {i} \wedge v_ {j} 
$$
where $i<j$ implicitly. Then the total sum is 
$$
\mathrm{Tr}\,\bigwedge^{2} A = \sum_ {i<j}\lambda _ {i} \lambda _ {j} .
$$

- - -

It turns out we can further simplify $\Lambda^{p}A$. Note that
$$
\lambda_ {1}^{p} + \lambda_ {2}^{p} + \dots + \lambda _ {N}^{p} = \mathrm{Tr}\,(A^{p}),\quad  
A = \text{diag}(\lambda_ {1},\dots,\lambda_ {N}).
$$

Take $p=2$ for example, 
$$
\bigwedge^{2} A = \sum _ {i<j} \lambda _ {i} \lambda _ {j}  = \frac{1}{2} \sum_ {ij} \lambda _ {i} \lambda _ {j} - \frac{1}{2} \lambda _ {i} \lambda _ {i}  = \frac{1}{2}(\mathrm{Tr}\,A)^{2} - \frac{1}{2} \mathrm{Tr}\,A^{2}.
$$

Turns out all the exterior power operators can be expressed as a *polynomial* in terms of $\mathrm{Tr}\, A^{n}$ and $(\mathrm{Tr}\,A)^{m}$ for some $m$ and $n$. 

- - -

Now, let $E\to M$ be a complex $\mathbb{C}^{N}$ bundle with structure group $U(N)$. Let the connection be $\omega$. The corresponding $2$-form curvature is still denoted by $\theta$. 

Let's *formally* replace $A$ in Eq. (1) with $i\theta / 2\pi$, replace multiplication with wedge product. To be exact, we work with **polynomial expression** of $\Lambda^{p}A$, and perform these substitutions. Since $\theta$ is a $2$-form there will be no problem with ordering. Regarding $\theta$ as a matrix means that the $(\alpha,\beta)$-th entry of the matrix is $\theta^{\alpha}_ {\;\; \beta}$. Now similar to Eq. (1) we have
$$
\begin{align}
\det \left( I+\frac{i\theta}{2\pi} \right) &= I + \mathrm{Tr}\,\frac{i\theta}{2\pi} + \dots \\
&= I + c_ {1}(E) + c_ {2}(E) + \dots 
\end{align}
$$
where $c_ {1}(E)$ is a 2-form on $U\subset M$, $c_ {r}(E)$ is a $2r$-form on $U$. It's called the $r$-th `Chern form`.

To be specific, the form $c_ {1}$ is 
$$
c_ {1} = \frac{i}{2\pi} \mathrm{Tr}\,\theta = \frac{i}{2\pi} \mathrm{Tr}\,\theta^{\alpha}_ {\;\; \alpha}.
$$
For $c_ {2}$ we have
$$
c_ {2} = -\frac{1}{8\pi^{2}}[\mathrm{Tr}\,\theta \wedge \mathrm{Tr}\,\theta-\mathrm{Tr}\,(\theta \wedge \theta)].
$$

Suppose the bundle has $SU(N)$ structure group rather than $U(N)$. The Lie algebra ${\frak su}(N)$ are traceless, anti-hermitian (mathematical convention) matrices, we have $\mathrm{Tr}\,\theta=0$. 



