---
layout: post
title: Domain Wall
subtitle: 
date: 2024-03-01
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
  - kink
  - domainWall
---

# Introduction

Domain walls in theoretical physics are fascinating phenomena that arise in a variety of contexts, from condensed matter physics to cosmology. They are a type of topological soliton that occurs when a discrete symmetry is spontaneously broken. In simpler terms, domain walls can be thought of as boundaries between different phases or domains where the order parameter (some scalar degree of freedom) differs on either side.


When kink solutions are placed in more than one spatial dimension, they become extended planar structures called “domain walls.” For example, in $3+1$ dimension, a flat $\mathcal{Z}_ {2}$ domain wall in $yz$-plane is 

$$
\phi(t,x,y,z) = \eta\, \tanh\left( \sqrt{ \frac{\lambda}{2} } \, \eta x \right).
$$

The energy density is given by that of $\mathcal{Z}_ {2}$ kink, the our convention it reads

$$
\mathcal{E} = \frac{\lambda \eta^{4}}{2} \cosh^{-4}\left( \sqrt{ \frac{\lambda}{2} } \, \eta x \right)
$$

since the Lagrangian is 

$$
\frac{1}{2} (\partial \phi)^{2}  - \frac{\lambda}{4} (\phi^{2} - \eta^{2})^{2}
$$

and the $\mathcal{Z} _2$ kink solution (with center at $x=0$) reads

$$
\phi_ {k} (x,t) = \eta \tanh\left( \sqrt{ \frac{\lambda}{2} } \eta x \right).
$$

The new aspects of domain walls are that they can be curved and deformations can propagate along them. Another feature of the planar domain wall is that it is invariant under boosts in the plane parallel to the wall. This is simply because the solution is independent of t, y and z and any transformations of these coordinates do not affect the solution.

- - -

The characteristic length of a kink is roughly speaking inverse to some mass, which turns out to be the mass of the fluctuating field in the kink sector $1 / \eta\sqrt{ \lambda }$. For distance scale much larger than that of a kink, we can regard it as a point particle. Recall that in the context of general relativity, the true trajectory of a particle through spacetime is such that it extremizes the proper time. In curved spacetime the trajectory (geodesic) followed by a free particle *maximizes the proper time* compared to nearby paths. Particles are "*lazy*" in the sense that they try to maximize the time spent to get to point B from point A. The action can be written as 

$$
S_ {1+1} = -M \int d\tau ,
\tag{1}
$$

the superscript $1+1$ denotes the dimension. 

The proper time is also the line element of the world line of the particle, let $X^{\mu}$ be the coordinates of the kink center, we can write

$$
d\tau^{2} = g_ {\mu \nu} \left( \frac{dX^{\mu}}{dt} \right) \left( \frac{dX^{\nu}}{dt} \right) dt^{2}.
$$

- - -

The question is, can we derive the action Eq. (1) from the original action for $\phi$ field, of which the kink is a solution? Such a derivation should lead to Eq. (1) plus corrections that depend on the internal structure of the kink. Then Eq. (1) would be the effective action of kink. 

The key assumption to derive the effective action is that, the field profile of a kink is well-approximated by that of the *static kink solution* in the `instantaneous rest frame`. Recall that, if the kink were to be given a velocity $v$, it would be Lorentz boosted to a moving frame. In that case, *the instantaneous rest frame would refer to the original frame before the Lorentz boost*, where the kink solution is static. Lorentz boosting the kink solution involves applying a Lorentz transformation to the coordinates, which would modify the form of kink solution $\phi_ {k}$ to account for the relativistic effects of motion, but in its own rest frame, the kink solution retains the static form given above.Generally speaking, the instantaneous rest frame of a moving object is a reference frame in which the object is at rest at a particular instant in time. This frame is also known as the object's `comoving frame`or `proper frame`. In this frame, the laws of physics take their simplest form, just like they would in a frame where the particle was always at rest.

Let's work in the *kink frame coordinates* which are denoted by $y^{a} = (\tau,\xi)$, $a=0,1$. $\tau$ is also called the kink world-line coordinate. These coordinates are functions of the background coordinates that are denoted by $x^{\mu}=(t,x)$, $\mu=0,1$. The kink world line is the world line of the kink center, denoted by $X^{\mu}=(t,X(t))$. Therefore the tangent vector to the world line is 

$$
T^{\mu} \propto \partial_ {t} X^{\mu} = \left( 1, V  \right), \quad  V:= \frac{ \partial X }{ \partial t }
$$
and $T$ is normalized to $T^{2}=1$.

The unit vector $\hat{N} = N^{\mu}(\tau)$ orthogonal to $\hat{T} = T^{\mu}$ is found by solving 

$$
g_ {\mu \nu} T^{\mu} N^{\nu} = 0, \quad  N^{\mu}N_ {\mu}=N^{2} = -1.
$$

Note the normalization of $N$ is $-1$ since it is time-like. Since we are working in 2D, there is only one $N^{\mu}$. In the special case of a Minkowski background we choose $g_ {\mu \nu} = \eta_ {\mu \nu} = \text{diag}(1,-1)$. (This is gonna piss off some theorists I know) We find 

$$
T^{\mu} = \gamma(1,V),\quad  N^{\mu} = \gamma(V,1),\quad  \gamma = \frac{1}{\sqrt{ 1-V^{2} }}.
$$

The coordinate axis $\tau$ is along $T^{\mu}$ and $\xi$ is along $N^{\mu}$. Therefore, if we arbitrarily choose a time $\tau_ {0}$ when the kink is located at spacetime point $X_ {0}$, then near the kink any other spacetime point coordinate can be written as 

$$
x^{\mu} = X_ {0}^{\mu} + \tau \hat{T}_ {0} + \xi \hat{N}_ {0},
$$

where $\hat{T}_ {0}$ and $\hat{N}_ {0}$ are the tangent and normal unit vector at time $\tau_ {0}$. However, we can always choose a time $\tau$ at which the coordinate in $\hat{T}$ direction is zero, this is always possible at least locally, when $x^{\mu}$ is close to the world line of the kink. It is illustrated in the following figure, which I shamelessly copied from Tanmay's textbook. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/kinkWorldLine.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Thick curve is the kink world line. The kink-frame coordinates $y^a=(\tau,xi)$ are defined in the instantaneous rest frame of the kink and functions of the background coordinates $x^\mu=(t,x)$.
</div>


