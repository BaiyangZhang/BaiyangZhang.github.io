---
layout: post
title: Fractal Geometry in Physics
date: 2024-07-11
author: Baiyang Zhang
catalog: true
tags:
  - fractal
---


# Introduction

I am writing a paper with Zhi-PengShen on the [Diophatine approximation](## [Diophantine](https://en.wikipedia.org/wiki/Diophantine_approximation)),here is a short introduction on fractal that is prerequisited.

A fractal, such as the [middle third Cantor set](https://brilliant.org/wiki/cantor-set/), usually have the following properties: 

1. Self-similarity; sometimes the self similarity is not strict, it is quasi-self-similar in that arbitrarily small portions of the set can be magnified and then distorted smoothly to coincide with a large part of the set, take the [Julia set](https://en.wikipedia.org/wiki/Julia_set) for example. Or it could be ever weaker, as the statistical self-similarity for random von Koch curve.
2. Has a "fine structure". It contains details at arbitrarily small scales. 
3. Its fractal dimension being different from its `topological dimension` (The topological dimension of a set is always an integer and is 0 if it is totally disconnected, 1 if each point has arbitrarily small neighbourhoods with boundary of dimension 0, and so on). 
4. The geometry of the fractal can not be described simply by the zero locus of some defining condition. 
5. The size of a fractal is usually not quntified by the usual measure, such as length, area. 

In the theory of phase transition we have two notions quite similar to it:

1. the system is scale-invariant at the critical point;
2. there exists non-integer critical exponents at the critical point.

It seems fractal does not have a mathematcially rigor definition. Kenneth Falconer mentioned in his textbook that,

>My personal feeling is that the definition of a ‘fractal’ should be regarded in the same way as a biologist regards the definition of ‘life’. There is no hard and fast definition, but just a list of properties characteristic of a living thing, such as the ability to reproduce or to move or to exist to some extent independently of the environment. Most living things have most of the characteristics on the list, though there are living objects that are exceptions to each of them.

So it's best to learn fractal by studying some examples. Two examples of fractals are:

`Koch's curve`, obtained from a segment of a straight line, by repeating a pattern that gives the line an angle, see the figure below. It is self-similar by construction, the length goes to infinity by a power law as $n\to \infty$.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/KochCcurve.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    The von Koch curve.
</div>

Another example is the coastal line of England, whose length $L(\epsilon)$ depends on the length $\epsilon$ of the yardstick. The coastal length is assumed to have the power law form,

$$
L(\epsilon)\sim ~L_ {0}\epsilon^{-\alpha}.
$$

The power-law behavior reminds us with the critical exponents near the critical point in statistical field theory, for example the magnetization of a ferromagnet near the critical temperature. 

We will talk more about dimension of a fractal, how to define and calculate it, in the future of the note. Now I only mention that the fractal dimension $d_ {\text{frac}}$ of the coastal line is defined to be 

$$
\alpha=d_ {\text{frac}}-d_ {\text{top}}
$$

where $d_ {\text{top}}$ is the topological dimension of the coastal line which is $1$. If the measured length does not dependent on the length of the yardstick $\epsilon$, then $\alpha=0$ and $d_ {\text{frac}}=d_ {\text{top}}$. In our case we have roughly (by actual measurement)

$$
d_ {\text{frac}}\sim 1.25.
$$

- - -

How should we think of the dimension of a fractal? Consider some regular geometric object, such as a familiar two dimensional square $\square$. If we double the side length of it, its area is multiplied by $2^{d}$ where $d$ is the dimension. In general, if the size of an object is multiplied by a factor $\lambda$, its area, or length, or whatever quantity that measures the "content" of the object, should be multiplied by a factor $\lambda^{d}$, where $d$ can be regarded as (one of the many) definitions of dimension. The number obtained in this way is usually referred to as the `similarity dimension` of the set.

Let's try to apply this definition to Koch's curve. It is self-similar, if we shrink it by a factor of $3$, then it reduces to one of its four "components". This component should have length that is one quarter of the original one. In other words, if we multiply Koch's curve by factor $\lambda=\frac{1}{3}$, then the length should be multiplied by $\frac{1}{4}$, the before-mentioned definition of dimension should give

$$
\text{new length}=\text{new size}^{d}\implies \frac{1}{4}=\left( \frac{1}{3} \right)^{d}\implies d\sim 1.26.
$$

However, similarity dimension can not be applied to fractals which lack strict self similarity. There are other definitions of dimension that are much more widely applicable, such the famous Hausdorff dimension (which will be the centeral idea of the note), or box-counting dimension. Very roughly, a dimension provides a description of how much space a set fills. It is a measure of the prominence of the irregularities of a set when viewed at very small scales. 

- - -

There exists various different definitions of dimension of a fractal, and applied on the same set they give different results. However, when applied on a perfectly self-similar fractal, such as the Koch's curve, they should all give the same result.

The fractal dimension is used to quantify this roughness and complexity. The higher the dimension, the higher the roughness, the higher the complexity. The fractional dimension *not only suggests that the fractal is curved*, it tells something drastically different, take the coastal line for example, it tells us the behavior of the total coastal length as the yardstick we use to measure it goes to zero.

The earliest known measure of roughness of an object is the Hausdorff dimension (also known as Hausdorff-Besicovitch dimension) introduced by Felix Hausdorff in 1918, even before fractal geometry was a thing. 

## Case study: Brownian motion

It seems that, in Brownian motion, the momentum change of a molecule at a collision depends only upon the last collision. It is a Gaussian stochastic process. 

Consider a lattice in $D$ dimension, with space and time discretization $\Delta x$ and $\Delta t$. Supposed the molecule of study can only hop from one site to the neighbor site, with direction chosen at random. One can then ask for the probability

$$
P(x_ {1},t_ {1};x_ {0},t_ {0}) = \text{molecure move from }(x_ {0},t_ {0}) \text{ to } (x_ {1},t_ {1}).
$$

The probability should satisfy three conditions,

1. If $t_ {0}=t_ {1}$ then the particle does not move, $P=\delta(x_ {0},x_ {1})$.
2. The total probability is normalized to one.
3. At successive times, it can arrive only from neighbor sites.

The last conditions gives us the dynamics of the particle, it tells how the particle must move. Using the discretized Laplace operator, we can turn the last condition into an equation. Then we can go to the continuum limit by setting $\Delta t\to 0$ and $\Delta x\to 0$. This limit is well defined under the condition that $\Delta t \propto (\Delta x)^{2}$. 

It shouldn't surprise us that at the continuum limit, the probability distribution adopt a Gaussian form.

The probability naturally satisfies the so-called `Kolmogorov equation`, 

$$
\int d^{d}x_ {1} \,  P(x_ {2},t_ {2};x_ {1},t_ {1})P(x_ {1},t_ {1};x_ {0},t_ {0})=P(x_ {2},t_ {2};x_ {0},t_ {0}).
$$

**This will give us a path-integral interpretation of the probability.**

