---
layout: post
title: Homotopy-and-Chern-Forms
subtitle: Why is the alternating sum of Betti numbers equal to the Euler characteristic?
date: 2023-12-03
author: Baiyang Zhang
header-img: img/background11.jpg
catalog: true
tags:
  - Geometry
  - Frankel
---
## Lifting spheres from the base to the bundle

Let $E\to M$ be a bundle.

**Sphere lifting theorem.** Any map of a $k$-sphere into $M^{n}$ (with base point $x_ {0}$) can be covered by a map of a $k$-disk into the bundle space $E$, in which the boundary $(k-1)$-sphere is mapped into the fiber $F=\pi^{-1}(x_ {0})$. 

Recall that a `covering space` is simply a bundle over $M$ with a *discrete* fiber. The above theorem implies the below theorem. 

**Theorem.** If $\pi: \overline{M} \to M$is a covering space, then the homomorphism induced by projection 
$$
\pi_ {\ast }: \pi_ {k}(\overline{M}, \overline{\ast }) \to \pi_ {k}(M,\ast )
$$
is an isomorphism for $k\geq 2$. Furthermore, if $k=1$
$$
\pi_ {\star}: \pi_ {1}(\overline{M}, \overline{\ast }) \to \pi_ {1}(M,\ast )
$$
is an isomorphism.

We will neglect the proof here, we just mention that this is a result of the fiber $\pi_ {-1}(x_ {0})$ being discrete. And the reason why $k\geq 2$ is special is that the boundary of $k$-sphere, if $k\geq 2$, is `continuous`, hence the image of it also has to be discrete, however the fiber is discrete, so the image must be a single point. 

As simple corollaries we have
$$
\pi_ {k}(\mathbb{R}P^{n}) = \pi_ {k}(\mathbb{S}^{n}),
$$
$$
\pi_ {k}(T^{n}) = \pi_ {k}(\mathbb{R}^{n}),
$$
all for $k\geq 2$. 

- - -

We know that $SU(N)$ are all simply connected, $\pi_ {1}(SU(N))=0$. Now we show that $\pi_ {2}(SU(N))$ also vanish.

Recall the $SU(N)$ fibering 
$$SU(N-1) \rightarrow SU(N) \rightarrow \mathbb{S}^{2N-1},
$$
where $SU(N-1) \rightarrow SU(N)$ represents the inclusion of $SU(N-1)$ into $SU(N)$. Essentially, $SU(N-1)$ can be thought of as a subgroup of $SU(N)$, where the matrices in $SU(N-1)$ are extended to $N \times N$ matrices by adding 1 as an additional diagonal entry. $SU(N) \rightarrow \mathbb{S}^{2N-1}$ is a bit more complex. $\mathbb{S}^{2N-1}$ represents the $(2N-1)$-dimensional sphere, which can be thought of as a set of points in a complex $N$-dimensional space $\mathbb{C}^N$. The map from $SU(N)$ to $S^{2N-1}$ can be understood as taking a matrix in $SU(N)$ and mapping it to a point on the sphere, typically using the action of $SU(N)$ on a fixed point in $\mathbb{C}^N$. In other words, the $\mathbb{S}^{N-1}$ can be considered as the first column of $SU(N)$ and $SU(N-1)$ can be considered as the subgroup of $SU(N)$. 

From here we have the exact homotopy sequence
$$
	\cdots \to \pi_ {3}(\mathbb{S}^{2N-1})\to\pi_ {2}(SU(N-1))\to\pi_ {2}(SU(N))\to\pi_ {2}(\mathbb{S}^{2N-1})\cdots
$$
for $N\geq 3$ this gives 
$$
0 \to \pi_ {2}(SU(N-1))\to\pi_ {2}(SU(N))\to 0.
$$
To see this, recall that we may assume that $f(\mathbb{S}^{k})$ does not cover all of $\mathbb{S}^{n}$ when $k<n$. Suppose then that the south pole of $\mathbb{S}^{n}$ is not covered. By pushing away from the south pole we may push the entire image to the north pole; we have deformed the map into a constant map. Thus $\pi_ {k}(\mathbb{S}^{n})=0$ if $k<n$. 

Thus,
$$
\pi_ {2}(SU(N)) = \pi_ {2}(SU(N-1))\dots=\pi_ {2}(\mathbb{S}^{3}) =0.
$$

In fact, E. Cartan has shown that every map of a $2$-sphere into any Lie group is contractible to a point,
$$
\pi_ {2}G=0,\quad  G\text{ a Lie group.}
$$
Also, 
$$
\pi_ {3}(SU(N)) = \pi_ {3}SU(2) = \mathbb{Z} \text{ for } n\geq 2
$$
thus every element of the shape $\mathbb{S}^{3}$ in $SU(N\geq 3)$ can be deformed to lie in an $SU(2)$ subgroup. 

- - -

Heinz Hopf discovered an `essential map` of $\mathbb{S}^{3}$ onto $\mathbb{S}^{2}$, that is, a map $\pi: \mathbb{S}^{3}\to\mathbb{S}^{2}$ which is not homotopic to a constant map. This cannot happen in the case of a 2-sphere mapped into a 1-sphere. With our machinery we can easily exhibit this map. We know that $SU(2)$ acts on its Lie algebra (with three basis, namely the Pauli matrices) as a double cover of $SO(3)$ rotation, and the stability subgroup of the hermitian matrix $\sigma_ {3}$ is the subgroup
$$
\begin{pmatrix}
e^{ i\theta }  & 0 \\
0  &  e^{ -i\theta } 
\end{pmatrix}
\sim \text{ a circle.}
$$
Thus we have the fibration 
$$
\mathbb{S}^{1}\to SU(2) \to \mathbb{S}^{2}.
$$
From the homotopy sequence
$$
0=\pi_ {3}\mathbb{S}^{1}\to\pi_ {3}SU(2)\to\pi_ {3}\mathbb{S}^{2}\to\pi_ {2}\mathbb{S}^{1}=0
$$
we see that 
$$
\pi_ {3}SU(2) = \pi_ {3}\mathbb{S}^{2} = \mathbb{Z}.
$$

We have shown that $\mathbb{S}^{3}=SU(2)$ is a fiber bundle over $\mathbb{S}^{2}$ with (nonintersecting) circles as fibers. This is the `Hopf fibration`.

## Chern Forms as Obstructions

Consider a $U(1)$ bundle. 

**Theorem.** Let $E\to M$ be a hermitian line bundle (that is, a bundle with hermitian metric, $\left\langle u,v \right\rangle=\overline{\left\langle v,u \right\rangle}$), with pure imaginary connection $\omega$ and curvature $\theta$. Let $V$ be any closed, oriented surface embedded in $M$, then
$$
\frac{i}{2\pi} \int _ {V} \, \theta = \int _ {V} \, c_ {1}
$$
is an integer and represents the sum of the indices of any sections $s: V\to E$ of the part of the line bundle over $V$. It is assumed that $s$ has but a finite number of zeros on $V$. 

It is only when this integer vanishes that one can possibly find a nonvanishing section (that is, a frame over all of $V$).\

Next, instantons are associated to $SU(2)$ bundles. The winding number of an instanton is given by 
$$
\frac{1}{24\pi} \int _ {\mathbb{S}^{3}} \, \mathrm{Tr}\,\omega \wedge \omega \wedge \omega  = - \int _ {\mathbb{R}^{4}} \, c_ {2}. 
$$
It is only when the winding number is zero then we can construct a global frame on $\mathbb{R}^{4}$. 

- - -

We have defined the Chern forms for a complex $U(N)$ bundle $E$,
$$
\det\left( I+\frac{i\theta}{2\pi} \right) = 1+c_ {1}(E) + c_ {2}(E)+\dots
$$
and we showed that each $c_ r$ is a closed form, and thus defines a de Rham cohomology class. The factor $i$ is to make each $c's$ real. This cohomology class, with real coefficients, is independent of the connection used, a change of connection (a gauge transformation) will add to the coefficients an exact form hence does not change the de Rham class. The factor $\frac{1}{2\pi}$ ensures the periods are integers. 

**Obstruction cocycle**

The existing of nonzero $c_ {2}$ is an obstruction of having a nonzero frame over the manifold. It can be shown by fist triangularize the base $M$, then try to extend the section from the $0$-skeleton to $1$-skeleton and so on. 





