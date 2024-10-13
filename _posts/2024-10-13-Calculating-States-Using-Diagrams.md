---
layout: post
title: Calculating States Using Diagrams
date: 2024-10-13
author: Baiyang Zhang
catalog: true
tags:
  - kink
---

# Rules for Hamiltonians
## Rules for $H_ {3}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H3Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fig.1. Rules for various components of $H_3$. I regard them as vertices. The meaning of graphical elements are explain later.
</div>

## Rules for $H_ {4}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H4Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fig.2. Rules for various components of $H_4$. 
</div>
## Rules for $H_ {5}^{(-)}$

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H5Rules.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fig.3. Rules for various components of $H_5$. The coefficients $C_ {5,3}$ and $C_ {5,1}$ are made of counter terms. In specific we have $C_ {3}= \frac{m\delta g}{\sqrt{2}} +\frac{g \delta m_ {1}^{2}}{2\sqrt{2}m} - \frac{m^{2}\delta m_ {1}^{4}}{2\sqrt{2}g}$ and $C_ {1}= m^{2}\delta v_ {3}-\frac{3gm\mathcal{I}_ {1}}{\sqrt{2}}+\frac{m^{3}\delta g^{2}}{\sqrt{2}g^{3}}-\frac{m \delta g\delta m_ {1}^{2}}{2\sqrt{2}g^{2}} -\frac{\delta m_ {1}^{4}}{8\sqrt{2}gm}$.
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
Fig.4. States at leading order. The first panel gives the leading order correction to the vacuum state, while the second and third panel gives the leading order correction to momentum states.
</div>

## Next Leading Order

The fundamental diagrams for $\left\lvert \vec{p} \right\rangle_ {2}^{(-)}$ are shown in the below.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/p2Fundamental.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fig. 5. Fundamental diagrams of $g^2$ corrections to $\left\lvert \vec{p} \right\rangle_ {2}^{(-)}$ States. By fundamental I mean the diagrams directly built up block-by-block by Hamiltonians and lower order states. Fundamental diagrams are good for study the cancelation between loops and counter terms. After the renormalization procedure is done, based on the number of extarnal legs, the fundamental diagrams can ben summed over to give more concise, summarized diagrams. 
</div>


Let's number the diagrams left to right, top to bottom. The contributions are 

$$
\begin{align*}
(1) :\;&  H_ {4}^{(4)} \left\lvert \vec{p} \right\rangle_ {0}^{(1)} = \frac{g^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \, \left\lvert \vec{p},\vec{p}_ {1,2,3,-1-2-3} \right\rangle_ {0} ,  \\
(2) :\;&  H_ {3}^{(3)} \left\lvert \vec{p} \right\rangle_ {1}^{(2)} = \frac{3g^{2}m^{2}}{4\omega_ {p}}\int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \,  \frac{\left\lvert \vec{p}-\vec{p}_ {3}, \vec{p}_ {1,2,3,-1-2} \right\rangle_ {0}}{\omega _ {p}-\omega_ {3}-\omega_ {p-p_ {3}}} , \\
(3) :\;&  H_ {3}^{(3)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} = -\frac{m^{2}g^{2}}{2} \int \frac{d^{3}p_ {1,2,3,4}}{(2\pi)^{12}} \, \frac{\left\lvert \vec{p},\vec{p}_ {1,2,3,4,-1-2,-3-4} \right\rangle_ {0}}{\omega_ {1}+\omega_ {2}+\omega_ {1+2}}, \\
(4) :\;&  H_ {3}^{(1)} \left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{3g^{2}m^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \,  \frac{3\left\lvert \vec{p},\vec{p}_ {1,2,3,-1-2-3} \right\rangle_ {0}}{\omega_ {2+3}(\omega_ {1}+\omega_ {2+3}+\omega_ {1+2+3})}   ,   \\
(5) :\;& H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} = - \frac{9g^{2}m^{2}}{4\omega_ {p}} \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p}-\vec{p}_ {1}-\vec{p}_ {2},\vec{p}_ {1,2} \right\rangle_ {0}}{\omega_ {1+2}(-\omega _ {p} +\omega_ {p-p_ {1}-p_ {2}}+\omega_ {1+2})} ,   \\
(6) :\;&  H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{3g^{2}m^{2}}{4} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \, \frac{\left\lvert \vec{p}_ {1,2,3,-1-2},\vec{p}-\vec{p}_ {3} \right\rangle_ {0}}{\omega_ {p}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} ,    \\
(7) :\;&  H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} = -\frac{9g^{2}m^{2}}{8\omega _ {p} } \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{\left\lvert \vec{p} \right\rangle_ {0}}{\omega_ {1}\omega_ {p+p_ {1}}(-\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})},  \\
(8) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset  - \frac{9m^{2}g^{2}}{4\omega _ {p} } \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p}-\vec{p}_ {1}-\vec{p}_ {2},\vec{p}_ {1,2}  \right\rangle_ {0}}{\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}  \\
(9) :\;&  H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset - \frac{3}{8}g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}\int d^{3}x \,   \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \,  \frac{1}{\omega_ {1}\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} \\
(10) :\;& - H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset  \frac{9g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}}{8\omega _ {p} }\int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{1}{\omega_ {1}\omega_ {p+p_ {1}}(\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})} \\
(11) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{9m^{2}g^{2}}{4} \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p},\vec{p}_ {1,-1} \right\rangle_ {0}}{\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}   \\
(12) :\;&  H_ {4}^{(0)}\left\lvert p \right\rangle_ {0}^{(1)} \supset \int d^{3}x \,  A_ {4}'  
\end{align*}
$$

But in order to turn them into diagrammatic rules, we need to inverse $(\omega _ {p}-H_ {2})$ to get components of $\left\lvert \vec{p} \right\rangle_ {2}$, eliminate the integral measures and deal with the creation operators. Hence, **as diagrammatic rules we get**:

$$
\begin{align*}
(1) :\;&  H_ {4}^{(4)} \left\lvert \vec{p} \right\rangle_ {0}^{(1)} : -\frac{g^{2}}{4(\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2+3})}  ,  \\
(2) :\;& H_ {3}^{(3)} \left\lvert \vec{p} \right\rangle_ {1}^{(2)} :\frac{3g^{2}m^{2}}{4\omega_ {p}} \frac{1}{(-\omega _ {p}+\omega_ {3}+\omega_ {p-p_ {3}})(-\omega _ {p} +\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2}+\omega_ {p-p_ {3}})} , \\
(3) :\;&  H_ {3}^{(3)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)}:\frac{m^{2}g^{2}}{2(\omega_ {1}+\omega_ {2}+\omega_ {1+2})(\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {4}+\omega_ {1+2}+\omega_ {3+4})}, \\
(4) :\;&  H_ {3}^{(1)} \left\lvert \vec{p} \right\rangle_ {1}^{(4)} :  \frac{9g^{2}m^{2}}{4\omega_ {2+3}(\omega_ {1}+\omega_ {2+3}+\omega_ {1+2+3})(\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2+3})}   ,   \\
(5) : \;& H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} : \frac{9g^{2}m^{2}}{4\omega_ {p}}\frac{1}{\omega_ {1+2}(-\omega _ {p} +\omega_ {p-p_ {1}-p_ {2}}+\omega_ {1+2})(-\omega _ {p} +\omega_ {1}+\omega_ {2}+\omega_ {p-p_ {1}-p_ {2}})} ,   \\
(6) :\;&  H_ {3}^{(1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} :  \frac{3g^{2}m^{2}}{4\omega_ {p}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})(-\omega _ {p} +\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2}+\omega_ {p-p_ {3}})}  ,    \\
(7) :\;&  H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(2)} = -\frac{9g^{2}m^{2}}{8\omega _ {p} } \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{\left\lvert \vec{p} \right\rangle_ {0}}{\omega_ {1}\omega_ {p+p_ {1}}(-\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})},  \\
(8) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset  - \frac{9m^{2}g^{2}}{4\omega _ {p} } \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p}-\vec{p}_ {1}-\vec{p}_ {2},\vec{p}_ {1,2}  \right\rangle_ {0}}{\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}  \\
(9) :\;&  H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset - \frac{3}{8}g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}\int d^{3}x \,   \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \,  \frac{1}{\omega_ {1}\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} \\
(10) :\;& - H_ {3}^{(-3)}\left\lvert p \right\rangle_ {1}^{(4)} \supset  \frac{9g^{2}m^{2}\left\lvert \vec{p} \right\rangle_ {0}}{8\omega _ {p} }\int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{1}{\omega_ {1}\omega_ {p+p_ {1}}(\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})} \\
(11) :\;& H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(4)} \supset - \frac{9m^{2}g^{2}}{4} \int \frac{d^{3}p_ {1,2}}{(2\pi)^{6}} \, \frac{\left\lvert \vec{p},\vec{p}_ {1,-1} \right\rangle_ {0}}{\omega_ {2}\omega_ {1+2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}   \\
(12) :\;&  H_ {4}^{(0)}\left\lvert p \right\rangle_ {0}^{(1)} \supset \int d^{3}x \,  A_ {4}'  
\end{align*}
$$


## 3rd Order States

Let's start with momentum states. 

### $\left\lvert \vec{p} \right\rangle_ {3}^{(2)}$

$H_ {3}^{(-3)}\left\lvert \vec{p} \right\rangle_ {2}^{(5)}$:

It include two contributions: $H_ {3}^{(-3)}$ acting on panel (4) and panel (6) from figure (5). Let's denote them by $H_ {3}^{(-3)}\cdot(4)$ and $H_ {3}^{(-3)}\cdot(6)$ respectively. Regarding the former we have 

$$
\begin{align*}
(a) =& - \frac{81m^{3}g^{3}}{8\sqrt{2}} \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \, \left\lvert \vec{p}_ {1},\vec{p}-\vec{p}_ {1} \right\rangle \int \frac{d^{3} p_ {2}}{(2\pi)^{3}} \,  \frac{1}{\omega_ {1}\omega_ {2}\omega^{2}_ {1+2}} \\
&\times \frac{1}{(\omega_ {1}+\omega_ {1+2}+\omega_ {2p_ {1}+2})(\omega_ {1}+\omega_ {1+2}+\omega_ {3}+\omega_ {2p_ {1}+2})},\\
(b) =& - \frac{81m^{3} g^{3}}{16\sqrt{2}} \int  \frac{d^{3}p_ {1}}{(2\pi)^{3}} \, \left\lvert \vec{p},\vec{p}-\vec{p}_ {1} \right\rangle \int \frac{d^{3}p_ {2}}{(2\pi)^{3}} \, \frac{1}{\omega_ {2}\omega _ {p} \omega^{2}_ {p-2}}  \\
&\times  \frac{1}{(\omega_ {1}+\omega_ {2-p}+\omega_ {1+2-p})(\omega_ {1}+\omega_ {2}+\omega _ {p} +\omega_ {1+2-p})}, \\
(c) &= - \frac{27m^{3}g^{3}}{16\sqrt{2}} \int d^{3}x \,  \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \, \left\lvert \vec{p},\vec{p}-\vec{p}_ {1} \right\rangle  \int \frac{d^{3}p_ {2}}{(2\pi)^{3}} \, \frac{1}{\omega_ {2}\omega_ {3}\omega_ {2+3}} \\
&\times  \frac{1}{\omega_ {1+2}(\omega_ {3}+\omega_ {1+2}+\omega_ {1+2+3})(\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2+3})}.
\end{align*}
$$

Regarding the latter we have 

$$
\begin{align*}
(d) =&  - \frac{3m^{3}g^{3}\left\lvert \vec{p},0 \right\rangle}{4\sqrt{2}} \int \frac{d^{3}p_ {1,2,3}}{(2\pi)^{9}} \,  \frac{1}{\omega_ {1}\omega_ {2}\omega_ {1+2}\omega_ {p}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})}     \\
&\times  \frac{1}{(-\omega _ {p} +\omega_ {1}+\omega_ {2}+2\omega_ {1+2}+\omega_ {p-p_ {1}-p_ {2}})},\\
(e) =&  - \frac{9m^{3}g^{3}}{4\sqrt{2}}  \int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \left\lvert \vec{p},\vec{p}-\vec{p}_ {1} \right\rangle  \int \frac{d^{3}p_ {2,3}}{(2\pi)^{6}} \, \frac{1}{\omega_ {2}\omega_ {3}\omega^{2} _ {p} } \\
&\times  \frac{1}{ (\omega_ {2}+\omega_ {3}+\omega_ {2+3})(-\omega _ {p} +\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {2+3}+\omega_ {p-p_ {1}})} ,\\
(f) =&   - \frac{9m^{3}g^{3}}{4\sqrt{2}} \int \frac{d ^{3}p_ {1}}{(2\pi)^{3}} \, \left\lvert \vec{p},\vec{p}-\vec{p}_ {1} \right\rangle  \int \frac{d^{3}p_ {2,3}}{(2\pi)^{6}} \, \frac{1}{\omega_ {2}\omega_ {3}\omega _ {p} ^{2}} \\
& \times  \frac{1}{(\omega_ {1}+\omega_ {2}+\omega_ {1+2})(-\omega _ {p} +\omega_ {1}+\omega_ {2}+\omega_ {3}+\omega_ {1+2}+\omega _ {p-p_ {3}} )} .\\
\end{align*}
$$\

The diagrams are shown below. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/H3Minus3OnP25.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    Fig. 6. The diagrams of $H_3^{(-3)}\left\lvert \vec{p} \right\rangle_ {2}^{(5)}$.
</div>


- - -

### Reducible Diagrams

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/kink/3rdOrderReducible.png" class="img-fluid rounded z-depth-1" style="width: 80%;" %}
    </div>
</div>
<div class="caption">
    The blob stands for all divergent diagrams. These three are the divergent contributions to $\left\lvert \vec{p} \right\rangle_ {3}^{(2)}$,  in the sense that they can be amputated by cutting an external leg.
</div>

Now we can sum up the previous results and organize diagrams according to their topology. 

For the reducible diagrams we have 

$$
\begin{align*}
H_ {4}^{(0)} \left\lvert \vec{p} \right\rangle_ {1}^{(2)} =& - \frac{3m\delta m^{2}g}{2\sqrt{2}\omega _ {p} }\int \frac{d^{3}p_ {1}}{(2\pi)^{3}} \,  \frac{\left\lvert \vec{p}_ {1}, \vec{p}-\vec{p}_ {1} \right\rangle_ {0}}{\omega_ {1}(-\omega _ {p} +\omega_ {1}+\omega_ {p+p_ {1}})},\\
H_ {3}^{(-1)}\left\lvert \vec{p} \right\rangle_ {1}^{(3)} =& - \frac{27m^{3}g^{3}}{8\sqrt{2}\omega _ {p}  }\int \frac{d^{3}p_ {1}}{(2\pi^{3})} \,  \frac{\left\lvert \vec{p}_ {1},\vec{p}-\vec{p}_ {1} \right\rangle_ {0}}{\omega_ {1}(-\omega _ {p} +\omega_ {1}+\omega_ { p-p_ {1}})} \\
&\times  \int \frac{d^{3}p_ {2}}{(2\pi)^{3}} \, \frac{1}{\omega_ {1+2}\omega_ {2}(-\omega _ {p} +\omega_ {1+2}+\omega_ {2}+\omega_ {p-p_ {1}})}, \\
H_ {3}^{(-3)}\left\lvert \vec{p} \right\rangle_ {2}^{(5)} &= - \frac{27m^{3}g^{3}}{8\sqrt{2}\omega _ {p} }\int \frac{d^{3}p_ {1}}{(2\pi)^{3}}  \frac{\left\lvert \vec{p}_ {1}, \vec{p}-\vec{p}_ {1} \right\rangle}{\omega_ {1}(-\omega _ {p} +\omega_ {1}+\omega_ {p-p_ {1}})} \\
&\times  \int \frac{d^{3}p_ {2}}{(2\pi)^{3}} \,  \frac{1}{\omega_ {2}\omega_ {1+2}(-\omega _ {p} +2\omega_ {1}+\omega_ {2}+\omega_ {1+2}+\omega_ {p-p_ {1}})}
\end{align*}
$$
