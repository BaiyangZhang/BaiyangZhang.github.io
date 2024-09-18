---
layout: post
title: My Version of Rules for Jarah Diagrams
date: 2024-09-18
author: Baiyang Zhang
catalog: true
tags:
  - kink
---

These rules are currently being used by myself and no one else, it is by no means standard or widely accepted. I find it extremely fun to play with those rules and diagrams.

# Rules for $H_ {3}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H3Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for various components of $H_3$. I regard them as vertices. The meaning of graphical elements are explain later.
</div>


# Rules for $H_ {4}^{(-)}$

The rules are shown in the figure below. The numbers label the momentum, for example $1$ stands for $\vec{p}_ {1}$. We only need to label the independent momenta for two reasons: 1) each vertex conserves the momenta hence we can fix the not-labeled momentum without problem and 2) it is important to balance the momenta and delta functions, as we will explain later.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H4Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for various components of $H_4$. 
</div>

# Diagrams for States So Far



# Feynman-like Rules

Roughly speaking we find all the possible way to concatenate a Hamiltonian to a state. Each red circle indicates that it must be concatenated to some other line to form a propagator, if not the diagram vanishes. After the concatenation we still need to *balance the momenta against the delta functions* (I am not sure if balance is the right verb here), as we will explain shortly.

For example, say we want to calculate $H_ {4}^{(2)}\left\lvert \Omega\right\rangle_ {0}$, we need to do the following:

1. Find the diagrams corresponding to $H_ {4}^{(2)}$, there are two of them. Find the diagram corresponding to $\left\lvert \Omega \right\rangle_ {0}$, there is only one.
2. Put the diagrams of $H_ {4}^{(2)}$ on the left and that for $\left\lvert \Omega \right\rangle_ {0}$ on the right, with all the independent momenta labeled. Find all the possible ways to concatenate them. 
3. For each concatenation, write down the symmetry factor first. There is usually more than one way to connect a circle to a leg (in the diagram of $\left\lvert \Omega \right\rangle_ {0}$), the number of doing that is the symmetry factor.
4. Each circle will cancel a connected momenta, cross them off at the same time. If a circle is connected to no labeled momentum, see if you can rearrange the independent labels so that one of them appears connected with a circle. It is easier done than said. After we cross them over, replace the circle with an arrow, which points to the direction of the increasing coupling. A line with an arrow is a regular propagator.
5. If there is a circle that no matter how to label and re-label the independent momenta still can't be eliminated, keep it, a circle connected with two legs is an irregular propagator, it will contribute a factor of $\int d^{3}x$, or $(2\pi)^{3}\delta^{3}(0)$.
6. Use the momentum conservation at each vertex to write down the momentum for each leg, external and internal. They should all be expressed in terms of independent momenta.
7. Read from left to write, don't forget to write the symmetry factor. The left-most external legs give us the final state, each of them gives us an momentum eigenstate. Whenever you see an independent momentum, write the integral measure $\int d^3p / (2\pi)^{3}$. Whenever you see a propagator, write down the corresponding factor, which is listed in the figure below. Write down the expression for the vertex and the state. 
8. Simplify and check.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/jarahRules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for two kinds of propagators, regular and circled ones. Each regular propagator contributes a factor of $\frac{1}{2\omega}$, in the mean while a circled propagator contributes an extra divergent factor of $\int d^3 x$, or $(2\pi)^3\delta^3(0)$ as I sometimes like to write.
</div>

```

# Two examples


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/example.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Here is an example of how to calculate $H_3^{(-3)}\lvert\Omega\rangle_1^{(3)}$.
</div>