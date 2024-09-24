---
layout: post
title: Diagrammatic Rules for Jarah Diagrams
date: 2024-09-18
author: Baiyang Zhang
catalog: true
tags:
  - kink
---

These rules are currently being used by myself and no one else, it is by no means standard or widely accepted. I find it extremely fun to play with those rules and diagrams.

The rules are shown in the figures below. The numbers label the momentum, for example $1$ stands for $\vec{p}_ {1}$. We only need to label the independent momenta for two reasons: 1) each vertex conserves the momenta hence we can fix the not-labeled momentum without problem and 2) it is important to balance the momenta and delta functions, as we will explain later. One of the various kinds of divergences, namely a factor of $(2\pi)^{3}\delta^{3}(0)$ or equivalently (not mathematically rigorously though) $\int d^3x$ comes from the fact that the Dirac delta functions over-determine the momenta, it is also included in the diagrammatic method.

In the following rules, some factors (such as a factor of 3) is perhaps better treated as symmetry factors, but for practical purpose I treat them as part of the definition of the the vertices.

I note that the diagrams I have are used to calculate quantities such as $H_ {3}\left\lvert \vec{p} \right\rangle_ {1},H_ {4}\left\lvert \Omega \right\rangle_ {2}$ only, in order to obtain the final **state** we need to further invert some operators. The inversion is quite straightforward though.

# Rules for Hamiltonians
## Rules for $H_ {3}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H3Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for various components of $H_3$. I regard them as vertices. The meaning of graphical elements are explain later.
</div>

## Rules for $H_ {4}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H4Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for various components of $H_4$. 
</div>
## Rules for $H_ {5}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H5Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    ules for various components of $H_5$. The coefficients $C_ {5,3}$ and $C_ {5,1}$ are made of counter terms. In specific we have $C_ {3}= \frac{m\delta g}{\sqrt{2}} +\frac{g \delta m_ {1}^{2}}{2\sqrt{2}m} - \frac{m^{2}\delta m_ {1}^{4}}{2\sqrt{2}g}$ and $C_ {1}= m^{2}\delta v_ {3}-\frac{3gm\mathcal{I}_ {1}}{\sqrt{2}}+\frac{m^{3}\delta g^{2}}{\sqrt{2}g^{3}}-\frac{m \delta g\delta m_ {1}^{2}}{2\sqrt{2}g^{2}} -\frac{\delta m_ {1}^{4}}{8\sqrt{2}gm}$.
</div>

# Diagrams for States

## Leading Order

At leading order there is one vacuum state correction and two momentum eigenstate corrections, their diagrammatic expressions are given in the figure below. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/LOStates.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
States at leading order. The first panel gives the leading order correction to the vacuum state, while the second and third panel gives the leading order correction to momentum states.
</div>

## Next Leading Order

The fundamental diagrams for $\left\lvert \vec{p} \right\rangle_ {2}^{(-)}$ are shown in the below.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/p2Fundamental.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fundamental diagrams of $g^2$ corrections to $\left\lvert \vec{p} \right\rangle_ {2}^{(-)}$ States. By fundamental I mean the diagrams directly built up block-by-block by Hamiltonians and lower order states. Fundamental diagrams are good for study the cancelation between loops and counter terms. After the renormalization procedure is done, based on the number of extarnal legs, the fundamental diagrams can ben summed over to give more concise, summarized diagrams. 
</div>

# Feynman-like Rules

With above ingredients we may introduce the rules to connect them now.

Roughly speaking we find all the possible way to concatenate a Hamiltonian to a state. Each red circle indicates that it must be concatenated to some other line to form a propagator, if not the diagram vanishes. After the concatenation we still need to *balance the momenta against the delta functions* (I am not sure if balance is the right verb here), as we will explain shortly.

For example, say we want to calculate $H_ {4}^{(2)}\left\lvert \Omega\right\rangle_ {0}$, we need to do the following:

1. Find the diagrams corresponding to $H_ {4}^{(2)}$, there are two of them. Find the diagram corresponding to $\left\lvert \Omega \right\rangle_ {0}$, there is only one.
2. Put the diagrams from $H_ {4}^{(2)}$ on the left and that from $\left\lvert \Omega \right\rangle_ {0}$ on the right, with all the independent momenta labeled in the fashion that is given in the figures below. Find all the possible ways to concatenate them. 
3. For each concatenation, write down the symmetry factor first. There is usually more than one way to connect a circle to a leg (in the diagram of $\left\lvert \Omega \right\rangle_ {0}$), the number of doing that is the symmetry factor. 
4. If a circle is connected to two independent labeled momenta, we'll call it "fully labeled." If it's connected to only one labeled momentum, we'll call it "half-labeled." Arrange the labels so that **as many circles as possible are fully labeled**. Each circle will cancel out a connected momentum, and you can cross them off simultaneously. If a circle isn’t connected to any labeled momentum, chance is they will survive the balancing process and give us a divergent factor. It's easier than it sounds. Once you've crossed them off, replace the circle with an arrow pointing in the direction of increasing coupling. A line with an arrow represents a regular propagator.
5. If there is a circle that no matter how to label and re-label the independent momenta still can't be eliminated, keep it, a circle connected with two legs is an irregular propagator, it will contribute a factor of $\int d^{3}x$, or $(2\pi)^{3}\delta^{3}(0)$.
6. Use the momentum conservation at each vertex to write down the momentum for each leg, external and internal. They should all be expressed in terms of independent momenta.
7. Read from left to right, don't forget to write down the symmetry factor. The left-most external legs give us the final state, each of them gives us an momentum eigenstate. **If there is not a single leg then the state is $\left\lvert \Omega \right\rangle_ {0}$**. Whenever you see an independent momentum, write the integral measure $\int d^3p / (2\pi)^{3}$. Whenever you see a propagator, write down the corresponding factor, which is listed in the figure below. Write down the expression for the vertex and the state. 
8. Simplify and check.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/jarahRules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Rules for two kinds of propagators, regular and circled ones. Each regular propagator contributes a factor of $\frac{1}{2\omega}$, in the mean while a circled propagator contributes an extra divergent factor of $\int d^3 x$, or $(2\pi)^3\delta^3(0)$ as I sometimes like to write.
</div>


Let's number the diagrams left to right, top to bottom. The contributions are 

$$
\begin{align*}
(1) :\;&  H_ {4}^{(4)} \left\lvert \vec{p} \right\rangle_ {0}^{(1)} = \frac{g^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \, \left\lvert \vec{p},\vec{p}_ {1,2,3,-1-2-3} \right\rangle_ {0} ,  \\
(2) :\;&  H_ {3}^{(3)} \left\lvert \vec{p} \right\rangle_ {1}^{(2)} = \frac{3g^{2}m^{2}}{4\omega_ {p}}\int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \,  \frac{\left\lvert \vec{p}-\vec{p}_ {1}, \vec{p}_ {1,2,3,-2-3} \right\rangle_ {0}}{\omega _ {p}-\omega_ {1}-\omega_ {p-p_ {1}}} , \\
(3) :\;&  H_ {3}^{(3)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} = -\frac{m^{2}g^{2}}{2} \int \frac{d^{3}p_ {1,2,3,4}}{(2\pi)^{12}} \, \frac{\left\lvert \vec{p},\vec{p}_ {1,2,3,4,-1-2,-3-4} \right\rangle_ {0}}{\omega_ {1}+\omega_ {2}+\omega_ {1+2}}, \\
(4) :\;& H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} = - \frac{9g^{2}m^{2}}{4\omega_ {p}} \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p}-\vec{p}_ {1}-\vec{p}_ {2},\vec{p}_ {1,2} \right\rangle_ {0}}{\omega_ {1+2}(-\omega _ {p} +\omega_ {p-p_ {1}-p_ {2}}+\omega_ {1+2})} ,   \\
(5) :\;&  H_ {3}^{(1)} \left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{3g^{2}m^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \,  \frac{3\left\lvert \vec{p},\vec{p}_ {1,2,3,-1-2-3} \right\rangle_ {0}}{\omega_ {2+3}(\omega_ {1}+\omega_ {2+3}+\omega_ {1+2+3})}   ,   \\
(6) :\;&  H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{3g^{2}m^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \, \frac{\left\lvert \vec{p}_ {1,2,3,-1-2},\vec{p}-\vec{p}_ {3} \right\rangle_ {0}}{\omega_ {p}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} ,    \\
(7) :\;&  H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} = -\frac{9g^{2}m^{2}}{8\omega _ {p} } \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{\left\lvert \vec{p} \right\rangle_ {0}}{\omega_ {1}\omega_ {p+p_ {1}}(-\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})},  \\
(8) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset  - \frac{9m^{2}g^{2}}{4\omega _ {p} } \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p}-\vec{p}_ {1}-\vec{p}_ {2},\vec{p}_ {1,2}  \right\rangle_ {0}}{\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}  \\
(9) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{9m^{2}g^{2}}{4} \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p},\vec{p}_ {1,-1} \right\rangle_ {0}}{\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}   \\
(10) :\;&  H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset - \frac{3}{8}g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}\int d^{3}x \,   \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \,  \frac{1}{\omega_ {1}\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} \\
(11) :\;&  H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset  \frac{9g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}}{8\omega _ {p} }\int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{1}{\omega_ {1}\omega_ {p+p_ {1}}(\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})} \\
(12) :\;&  H_ {4}^{(0)}\left\lvert p \right\rangle_ {0}^{(1)} \supset \int d^{3}x \,  A_ {4}'  
\end{align*}
$$


# Two examples


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/example.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Here is an example of how to calculate $H_ 3^{(-3)}\lvert\Omega\rangle_ 1^{(3)}$. Here the first factor $6$ comes from the 6 different ways to connect the circles. The top two circles are fully labeled, the buttom one has no label at all, thus there is no independent momentum to ballance against the circle. It contributes the spatial integral in the final expression. Since all the vertices preserve the momenta, and the top to propogators are labeled with $p_ 1$ and $p_ 2$, the last line is fixed to be $-p_ 1-p_ 2$. It is not common to encounter an irregular propagator. There is no external leg on the left-most of the diagram, hence we assign $\left\lvert \Omega \right\rangle_ {0}$ to it.
</div>

