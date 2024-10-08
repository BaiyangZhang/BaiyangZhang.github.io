---
layout:     post   				    # 使用的布局（不需要改）
title:     Covariant Differentiation and Curvature			# 标题 
subtitle:   
date:       2023-3-16 				# 时间
author:     Baiyang Zhang 						# 作者
header-img: img/mathArt10.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - Geometry
    - Minkowski
    - Frankel
---

*Disclaimer: Nothing in this note is original.*

### Covariant Derivative

Consider a surface $M^{2}$ in $\mathbb{R}^{3}$. We then define a `covariant derivative` as follows. Let $\mathbf{v}$ be a tangent field defined in the neighborhood of a point $p$. Let $\mathbf{X}$ be a tangent vector defined at $p$. The covariant derivative is defined by 

$$
\nabla_ {\mathbf{X}}\mathbf{v} = \mathbf{X}(\mathbf{v})+\Gamma^{\alpha}_ {\beta \gamma} \mathbf{X}^{\beta} \mathbf{v}^{\gamma}\; \partial _ {\alpha}.
$$

We have thus constructed the notion of a derivative of a tangent vector field $\mathbf{v}$ with respect to a vector $\mathbf{X}$ at $p$. The result is again a tangent vector at $p$. It is furthermore clear that if $\mathbf{X}$ is itself a tangent vector field, then $\nabla_ {\mathbf{X}}\mathbf{v}$ is again a vector field. 

A covariant differentiation operation, defined fully in a moment, is also called a `connection`. 

The connection in a Riemannian manifold in which the $\Gamma^{\alpha}_ {\beta \gamma}$ are given by the Christoffel symbols is called the Levi-Civita connection, though Christoffel would be the natural name to associate with this connection.

Later on we shall see that we shall need to differentiate objects that are much more general than tangent vector fields, and then the Christoffel symbols will be replaced by other quantities. For example, when discussing particle physics we shall have to differentiate wave functions, and we shall see that it is natural to define a covariant derivative in which the role of the Christoffel symbols is played by the electromagnetic vector potential $A$!

Let $M^{n}$ be a manifold. An affine `connection` or `covariant differentiation` is an operator $\nabla$ that assigns to each pair consisting of a vector $\mathbf{X}$ at $p$ and a vector field $\mathbf{v}$ defined near $p$, a vector $\nabla_ {\mathbf{X}}\mathbf{v}$ at $p$ that satisfies

$$
\nabla _ {\mathbf{x}}(a\mathbf{v}+b\mathbf{w}) = a \nabla _ {\mathbf{x}} \mathbf{v} +b\nabla _ {\mathbf{x}}\mathbf{w},
$$

and 

$$
\nabla _ {a\mathbf{X}+b\mathbf{Y}}(\mathbf{v})=a \nabla _ {X}\mathbf{v} + b\nabla _ {Y}\mathbf{v},
$$

and the Leibniz rule

$$
\nabla _ {X}(f\mathbf{v}) = X(f)\mathbf{v}+f\nabla _ {X}(\mathbf{v}).
$$

We also demand that if $\mathbf{X}$ is a smooth field then $\nabla_ {\mathbf{X}}\mathbf{v}$ is also a smooth vector field. In our work up until now we have always used local coordinates $x$ to yield a basis $\partial_ {x}$ for the tangent vectors in a patch $U$. For many purposes, however, it is advantageous to use a more general basis. A `frame` of vector fields in a region $U$ consists of $n$ **linear independent** **smooth** vector fields $\mathbf{e} = (\mathbf{e}_ {1},\dots,\mathbf{e}_ {n})$ in $U$. A special case is a `coordinate frame`, where $\mathbf{e}_ {i} = \partial_ {i}$. 

First note that a frame $\mathbf{e}$ usually is not a coordinate frame, since $[\mathbf{e}_ {i},\mathbf{e}_ {j}]$ is usually not zero, while $[\partial_ {i},\partial_ {j}]$ usually is. In fact we have

**Theorem.** A frame $\mathbf{e}$ is locally a coordinate frame iff 

$$
[\mathbf{e}_ {i},\mathbf{e}_ {j}] = 0 \;\forall\; i,j.
$$

To prove it, we need only show that this bracket condition implies the existence of functions $(x^{i})$ such that $\mathbf{e}=\partial / \partial x^{i}$. Let $\sigma^{i}$ be the dual (to $\mathbf{e}_ {i}$) form basis, we have 

$$
d\sigma^{i}(\mathbf{e}_ {j},\mathbf{e}_ {k}) = \sigma^{i}([\mathbf{e}_ {j},\mathbf{e}_ {k}])
$$

and so $d\sigma^{i}=0$ for all $i$. Namely, $\sigma^{i}$ is closed, then locally $\sigma^{i}$ is exact. It means that there exists $x^{i}$ such that $\sigma^{i} = dx^{i}$, for some functions $x^{i}$. Then it follows that $\mathbf{e}=\partial / \partial x$. 

Let now $\mathbf{e} = (\mathbf{e}_ {1},\dots,\mathbf{e}_ {n})$ be a frame of vector fields in a region $U$. We then have 

$$
\mathbf{X} = X^{i} \mathbf{e}_ {i}
$$

Once defined the frame, we can evaluate the covariant derivative in terms of these frames. For many purposes it will be important to employ frames that are not coordinate. For the present, however, it is an unnecessary complication.

*For the remainder of this Section we shall restrict ourselves to the use of coordinate frames.*

In the surface case, we see that curvature is at least related to the commutation of second covariant derivatives of vector fields. We will not copy the exact expression for curvature here, interested readers can refer to any textbook on differential geometry. 

#### The Riemannian Connection

In any manifold Mn with an affine connection, that is, with a covariant differentiation operator $V$, we can consider parallel displacement of a vector $\mathbf{Y}$ along a parameterized curve $x = x (t)$, defined again by

$$
\nabla_ {t} \mathbf{Y} = 0.
$$

There are an infinite number of distinct affine connections on any manifold. (In $\mathbb{R}^{3}$, e.g., one may choose the connection arbitrarily in the single coordinate patch.) If the manifold is Riemannian, however, there is one connection that is of special significance in that it relates `parallel displacement` with the `Riemannian metric` in an important way. In the case of a surface mkM%2 in $\mathbb{R}^{3}$ , the Levi-Civita connection, first of all, was symmetric, and second, had the property that parallel displacement preserved scalar products of vectors. 

**Theorem.**  On a Riemannian manifold there is a unique symmetric connection that satisfies

$$
\frac{d}{dt} \left\langle \mathbf{X},\mathbf{Y} \right\rangle  = \left\langle \nabla_ {t}\mathbf{X},\mathbf{Y} \right\rangle + \left\langle \mathbf{X},\nabla_ {t}\mathbf{Y} \right\rangle 
$$

for any pair of vector fields defined along a parameterized curve, and this connection is the Riemannian connection.

### Cartan's Exterior Covariant Differential

The question we want to answer here is that, *how can we express connections and curvatures in terms of forms*?

#### Vector-Valued Forms

Cartan extended the notion of the exterior derivative of a $p$-form to that of the exterior **covariant** derivative of a `vector-valued p-form`. This remarkable machinery is ideally suited for computations involving the Riemann curvature tensor, and also seems to be the natural language for dealing with the gauge fields of present-day physics and the stress tensors of elasticity.

Let $A$ be a mixed tensor that is once contravariant and $p$ times covariant and that is skew symmetric in its covariant indices. Locally

$$
A = \mathbf{e}_ {i} \otimes \sum_ {J>}A^{i}_ {j_{1}\dots j_ {p}}\sigma^{j_{1}}\wedge \dots \wedge \sigma^{j_ {p}}.
$$

Thus $A$ is of the form 

$$
A = \mathbf{e}_ {i} \otimes \alpha,\quad  \alpha \in \Omega^{p}.
$$

To $A$ we may then associate a vector-valued $p$-form, that is, a $p$-form (written $A$ or $\alpha$), whose values are vectors rather than scalars,

$$
\alpha(\mathbf{v}_{1},\dots,\mathbf{v}_ {p}):=\mathbf{e}_ {i} \alpha^{i}(\mathbf{v}_{1},\dots,\mathbf{v}_ {p}).
$$

Vector-valued forms occur frequently in classical vector analysis. In terms of cartesian coordinates,

$$
d\mathbf{r} = (dx^{1},dx^{2},dx^{3})
$$

is a vector-valued 1-form, $x^{1,2,3}$ are three different functions defined on $M$. When acting on a vector we have

$$
d\mathbf{r}(v) = (dx^{1}(v),dx^{2}(v),dx^{3}(v)) = (v^{1},v^{2},v^{3}).
$$

that is, $d\mathbf{r}$ is the form that assigns to each vector the same vector. 

Finally, if we define the local matrix $\omega$ of `connection 1-forms` by

$$
\omega^{k}_ {\;\;j}=\omega^{k}_ {ij}\sigma^{i}.
$$

#### Cartan's Structural Equations

Let $\sigma$ be the basis of 1-forms dual to a given frame $\mathbf{e}$. Then $d\sigma$ can of course be written down with no mention of a connection, but if there is a connection we can write $d\sigma$ in terms of connection and torsion,

$$
d\sigma^{i} = -\omega^{i}_ {jk}\sigma^{j}\wedge \sigma^{k} + \tau^{i}
$$

which is called **Cartan's structural equations*.

We shall abbreviate the notations as follows. Denote the list of frame basis $(\mathbf{e}_ {1},\dots,\mathbf{e}_ {n})$ by the matrix $e$ and the column $(\sigma^{1},\dots,\sigma^{n})^{T}$ by $\sigma$. The $n\times n$ matrix of connection 1-form will be denoted by

$$
\omega = \omega^{i}_ {j} := \omega^{i}_ {ij}\sigma^{i}.
$$

and the column vector of torsion 2-forms by $\tau$

$$
\tau = (\tau_ {1},\dots,\tau_ {n})^{T}.
$$

Then we may write 

$$
\nabla_ {\mathbf{e}} = \mathbf{e}\otimes \omega
$$

and the Cartan's structural equation becomes

$$
d\sigma=-\omega \wedge \sigma+\tau.
$$

In our new notation, if $\mathbf{v}$ is a vector we may write $\mathbf{v} = \mathbf{e} v$ where $v$ is the column of components of $v$.

#### The Exterior Covariant Differential of a Vector-Valued Form

Let $\alpha$ be a vector-valued $p$-form. Fix a frame $\mathbf{e}$, then locally we have 

$$
\alpha = \mathbf{e}_ {i} \otimes \alpha^{i}
$$

where $\mathbf{e}_ {i}$ are frame basis and $\alpha^{i}$ are $p$-forms. It can be regarded as a vector of p-forms. We define its exterior covariant differential, the vector-valued $(p + 1)$-form $\nabla \alpha$, by demanding a Leibniz rule

$$
\nabla \alpha= \nabla \mathbf{e}_ {i} \otimes_ {\wedge } \alpha^{i} + \mathbf{e}_ {i} \otimes  d\alpha^{i}
$$

where the notation $\otimes_ {\wedge}$ is defined as follows:

$$
\nabla \mathbf{e}_ {i} \otimes _ {\wedge } \alpha^{i} = (\mathbf{e}_ {k}\otimes \omega^{k}_ {\;\; i}) \wedge \alpha^{i} = \mathbf{e}_ {k} \otimes  \omega^{k}_ {\;\; i}\wedge \alpha^{i}.
$$

In abbreviated notation with the column of $p$-forms we have 

$$
\nabla \alpha = \mathbf{e} \otimes (d\alpha+\omega \wedge \alpha).
$$

When dealing with vector-valued forms, we shall usually use Cartan's device of simply omitting the tensor product sign in equations. Thus the above equation will be written

$$
\nabla \alpha = \mathbf{e}(d\alpha+\omega \wedge \alpha).
$$


#### The Curvature 2-Forms

$\nabla\mathbf{e}$ is a row matrix of local vector-valued $1$-forms. We can then take the exterior covariant differential again

$$
\nabla \nabla \mathbf{e} = \mathbf{e}(\omega \wedge \omega+d\omega).
$$

Thus if we define the local matrix e of `curvature 2-forms` by

$$
\theta:= d\omega+\omega \wedge \omega
$$

we have 

$$
\nabla \nabla\mathbf{e}=\mathbf{e}\theta.
$$

It is just the Riemann curvature in disguise, 

$$
\theta^{i}_ {\;\; j} = \frac{1}{2} R^{i}_ {\; jrs}\sigma^{r}\wedge \sigma^{s}.
$$

A manifold that (like $\mathbb{R}^{n}$) can be covered by a single distinguished frame field $\mathbf{e}$ is called `parallelizable`. 

### Change of Basis and Gauge Transformations

Given a frame $\mathbf{e}$, we can define the connection $\omega^{i}_ {\; jk}$, then we can define the covariant derivative $\nabla$. Here we don't use $\Gamma^{i}_ {\; jk}$ because we save that symbol to Christoffel symbols only, which is a special kink of connection. However, if we demand that $\nabla$ have a basis-free significance, we shall have to require the $\omega$'s to have a special transformation property under a change of basis.

Let $\mathbf{e}' = \mathbf{e} P$ be a change of frame, where $P$ is a $n\times n$ matrix. Then $\nabla \mathbf{e}$ must be compatible to $\nabla\mathbf{e}'$, which yields 

$$
\omega' = P^{-1}\omega P+P^{-1}dP.
$$

This is the **transformation rule for the matrix of connection $1$-forms**. Look, on the other hand, at the matrix of curvature 2-forms $\theta$. Based on the defining expression for $\theta$, namely $\theta = d\omega+\omega \wedge\omega$, we find that 

$$
\theta'=P^{-1}\theta P.
$$

This has the following consequence; if $\theta = 0$ in some frame then $\theta'=0$ in every frame! 

We can also patch two charts together, the glue being the `transition matrix function`. Let $e_U$ and $e_ {V}$ be frames in open sets $U$ and $V$, respectively. We then have

$$
e_ {V} = e_ {U} C_ {UV}
$$

where $C_ {UV}$ is the transition matrix function mentioned above. Then the transition property of $\sigma$ and $v^{i}$ can also be obtained accordingly. The components $\omega$ transform as

$$
\omega_ {V} = C_ {VU}\omega_ {U} C_ {UV}+C_ {VU}dC_ {UV} ,
$$

just like the gauge transformation, which it is. 

Note that in a Riemannian manifold, one can take any frame and convert it to an orthonormal frame by applying the Gram-Schmidt process. Many computations become much simpler if a n orthonormal frame is employed. In particular, if the frame is orthonormal, $g_ {ij} = \delta_ {ij}$, then the matrix of the connection 1-forms with both indices down is anti-symmetric. 

### Parallel Displacement and Curvature on a Surface

In general, parallel displacement of a vector between two points of a surface is path-dependent. This phenomenon is referred to as holonomy, and, as we shall see, is indeed related to the concept of holonomic and nonholonomic constraints. 

**Theorem.** Let $U\subset M^{2}$ be a compact region in a `Riemannian` surface with piecewise smooth boundary $\partial U$. Assume that $U$ can be covered by a single orthonormal frame field $\mathbf{e}$ (e.g. , $U$ may be contained in a coordinate patch). Let a unit vector $\mathbf{v}$ be parallel translated around $\partial U$, starting with an initial $\mathbf{v}_ {0}$ and ending with $\mathbf{v}_ {f}$. $\mathbf{e}$ defines an orientation in $U$. Then the angle $\alpha$ between $\mathbf{v}_ {0}$ and $\mathbf{v}_ {f}$ is given by

$$
\Delta \alpha = \int \int_{U}\,  K dS = \int \int_{U}\,  K \sigma^{1}\wedge \sigma^{2}.
$$

The proof can be found elsewhere. We just mention an interesting corollary, 
If $M^{2}\subset\mathbb{R}^{3}$, then $\Delta \alpha$ is equal to the signed area of the spherical image of $U$ under the Gauss normal map.

A connection is said to be flat if the curvature is zero, then the parallel displacement on a Riemannian surface is locally independent of path iff $M^{2}$ is flat. 

By "locally" we mean that we must restrict our closed path to be the boundary of a compact region that is covered by an orthonormal frame. Consider, for example, the Mobius band obtained by bending and sewing a flat strip of paper. Although the usual picture of the band in $\mathbb{R}^{3}$ appears curved, this $2$-manifold with boundary has $K = 0$ since $K$ is a bending invariant. However, if one parallel translates the vector $\mathbf{e}_ {2}$ along the mid circle of the band one ends up with $\mathbf{e}_ {2}(1)=-\mathbf{e}_ {2}(0)$. But that is because the mid-circle does not bound any surface. 
