---
layout: post
title: Constructing a Finite Tension Domain Wall in 4D Part III
date: 2024-12-25
author: Baiyang Zhang
catalog: true
tags:
  - kink
---

# Divergence cancellation in kink sector

We want to calculate the continuum contribution to the tension, which is Eq. (4.42) in the long version of the note:


$$
\begin{align*}
\rho_ {1}^{A} =& -\int \frac{dk_ {1}}{2\pi} \frac{dp_ {1}}{2\pi} \,  \frac{9\pi^{2}p_ {1}^{2}}{(m^{2}+k_ {1}^{2})(m^{2}+4k_ {1}^{2})}\text{csch}^{2}\left( \frac{\pi(p_ {1}-k_ {1})}{m} \right) \\
&\times \int \frac{dk_ {2}dk_ {3}}{(2\pi)^{2}} \,  \frac{(\omega _ {k} -\omega_ {p_ {1}k_ {2}k_ {3}})^{2}}{\omega_ {p_ {1}k_ {2}k_ {3}}},
\end{align*}
$$

where in the last line $\omega _ {k} = \omega_ {k_ {1}k_ {2}k_ {3}}=\sqrt{k_ {1}^{2}+k_ {2}^{2}+k_ {3}^{2}+m^{2}}$, and $\omega_ {p_ {1}k_ {2}k_ {3}}=\sqrt{p_ {1}^{2}+k_ {2}^{2}+k_ {3}^{2}+m^{2}}$. 

We want to integrate the second line first, call it $I$:

$$
I = \int \frac{dk_ {2}dk_ {3}}{(2\pi)^{2}} \,  \frac{(\omega _ {k} -\omega_ {p_ {1}k_ {2}k_ {3}})^{2}}{\omega_ {p_ {1}k_ {2}k_ {3}}},
$$

Using the formula 

$$
\int_ {-\infty}^{\infty} dk \,  \frac{(\sqrt{a+k^{2}}-\sqrt{b+k^{2}})^{2}}{\sqrt{b+k^{2}}} = -a+b+a\ln\left( \frac{a}{b} \right),
$$

we can integrate $k_ {3}$ out first,

$$
I = \int_ {-\infty}^{\infty} \frac{dk_ {2}}{(2\pi)^{2}} \, [(-a+a\ln a)-(-b+a\ln b)]. 
$$

where 

$$
a = k_ {1}^{2}+k_ {2}^{2}+m^{2}, \quad  b = p_ {1}^{2}+k_ {2}^{2}+m^{2}.
$$

Define 

$$
a := \alpha+k_ {2}^{2}, \quad  b = \beta+k_ {2}^{2},
$$

and in order to study the behavior at infinite momenta we insert a cutoff $\Lambda$, define:

$$
\begin{align*}
f_ {\Lambda}(k_ {1}):=& \frac{1}{2\pi^{2}}\int_ {0}^{\infty} dk_ {2} \, [-\alpha-k_ {2}^{2}+(\alpha+k_ {2}^{2}\ln(\alpha+k_ {2}^{2}))], \\
f_ {\Lambda}(p_ {1}):=& \frac{1}{2\pi^{2}}\int_ {0}^{\infty} dk_ {2} \, [-\beta-k_ {2}^{2}+(\alpha+k_ {2}^{2}\ln(\beta+k_ {2}^{2}))].
\end{align*}
$$

so that 

$$
I = f_ {\Lambda}(k_ {1}) - f_ {\Lambda}(p_ {1}).
$$

We can do the integrals analytically now. Note that when simplifying the integrated result, we need to expand $\ln(\alpha+\Lambda^{2})$ to $\ln \Lambda^{2}+\alpha / \Lambda^{2}-\alpha^{2} / 2\Lambda^{4}$. In the end we have

$$
\begin{align*}
2\pi^{2}f_ {\Lambda}(k_ {1}) =& \frac{2}{3} \pi  \alpha ^{3/2}+\alpha  \Lambda  \log \left(\Lambda ^2\right)-2 \alpha  \Lambda -\frac{5 \Lambda ^3}{9}+\frac{1}{3} \Lambda ^3 \log \left(\Lambda ^2\right), \\
2\pi^{2}f_ {\Lambda}(p_ {1}) =& \pi  \alpha  \sqrt{\beta }+\alpha  \Lambda  \log \left(\Lambda ^2\right)-2 \alpha  \Lambda -\frac{5 \Lambda ^3}{9} -\frac{1}{3} \pi  \beta ^{3/2}+\frac{1}{3} \Lambda ^3 \log \left(\Lambda ^2\right).
\end{align*}
$$

miraculously the divergence, namely the terms containing $\Lambda$, all cancels out. Thus

$$
I = f_ {\Lambda}(k_ {1}) - f_ {\Lambda}(p_ {1}) = \frac{\alpha ^{3/2}}{3 \pi }-\frac{\alpha  \sqrt{\beta }}{2 \pi }+\frac{\beta ^{3/2}}{6 \pi }.
$$

The original integral now reads

$$
\begin{align*}
\rho_ {1}^{A} =& -\int \frac{dk_ {1}}{2\pi} \frac{dp_ {1}}{2\pi} \,  \frac{9\pi^{2}p_ {1}^{2}}{(m^{2}+k_ {1}^{2})(m^{2}+4k_ {1}^{2})}\text{csch}^{2}\left( \frac{\pi(p_ {1}-k_ {1})}{m} \right) \\
&\times \left( \frac{(k_ {1}^{2}+m^{2})^{3/2}}{3\pi}- \frac{(k_ {1}^{2}+m^{2})\sqrt{p_ {1}^{2}+m^{2}}}{2\pi}+ \frac{(p_ {1}^{2}+m^{2})^{3/2}}{6\pi} \right) \\
=& - \frac{3\pi}{2} \int \frac{dk_ {1}}{(2\pi)} \frac{dp_ {1}}{(2\pi)} \,  \frac{p_ {1}^{2}\sqrt{k_ {1}^{2}+m^{2}}}{(m^{2}+4k_ {1}^{2})}\text{csch}^{2}\left( \frac{\pi}{m}(p_ {1}-k_ {1}) \right)\\
&\times \left( 2-3\sqrt{\frac{p_ {1}^{2}+m^{2}}{k_ {1}+m^{2}}}+\left( \frac{p_ {1}^{2}+m^{2}}{k_ {1}^{2}+m^{2}} \right)^{3/2} \right)
\end{align*}
$$


# Renormalization with Quantum Action

The three point function is given by 

$$
\begin{align*}
\left\langle \Omega \right\rvert \mathcal{T} \phi(\vec{x}_ {1},E_ {1})\phi(\vec{x}_ {2},E_ {2})\phi(0) \left\lvert \Omega \right\rangle =& -i \int \frac{dE_ {1}dE_ {2}}{(2\pi)^{2}}  \frac{d^{d}p_ {1}d^{d}p_ {2}}{(2\pi)^{2d}}\,  \frac{e^{ -i(E_ {1}t_ {1}+E_ {2}t_ {2}+\vec{x}_ {1}\cdot \vec{p}_ {1}+\vec{x}_ {2}\cdot \vec{p}_ {2}) }}{(E_ {1}^{2}-\omega_ {1}^{2}+i\epsilon)(E_ {2}^{2}-\omega_ {2}^{2}+i\epsilon)} \\
&\times \frac{\Gamma(\vec{p}_ {1},E_ {1},\vec{p}_ {2},E_ {2})}{(E_ {1}+E_ {2})^{2}-\omega_ {1+2}^{2}+i\epsilon}
\end{align*}
$$

where $\omega_ {1}:=\omega_ {\vec{p}_ {1}}$, $\mathcal{T}$ stands for the time-ordered product. Does integrating over $E_ {1}$ gives us the time ordered product, similar to how we obtained the Feynman propagator? Or is it just the basis of Fourier transform? To see how it works, let's assume that $t_ {1}>t_ {2}>0$. We can perform the integral over $E_ {1}$ using the contour method, and get 

$$
\left\langle \Omega \right\rvert \mathcal{T} \phi(\vec{x}_ {1},E_ {1})\phi(\vec{x}_ {2},E_ {2})\phi(0) \left\lvert \Omega \right\rangle = \text{I}+\text{II},
$$

where 

$$
\begin{align*}
\text{I} =& - \int \frac{d^{d}p_ {1} d^{d}p_ {2}}{(2\pi)^{2d}} \,  e^{ -i(\vec{p}_ {1}\cdot \vec{x}_ {1}+\vec{p}_ {2}\cdot \vec{x}_ {2}+\omega_ {1}t_ {1}) } \int \frac{dE_ {2}}{(2\pi)}  \frac{e^{ -iE_ {2}t_ {2} }}{2\omega_ {1}} \\
&\times  \frac{\Gamma(E_ {1}=\omega_ {1})}{(E_ {2}+\omega_ {2}-i\epsilon)(E_ {2}-\omega_ {2}+i\epsilon)(E_ {2}+\omega_ {1}+\omega_ {1+2}-i\epsilon)(E_ {2}+\omega_ {1}-\omega_ {1+2})+i\epsilon}, \\
\text{II} =& - \int \frac{d^{d}p_ {1} d^{d}p_ {2}}{(2\pi)^{2d}} \,  e^{ -i(\vec{p}_ {1}\cdot \vec{x}_ {1}+\vec{p}_ {2}\cdot \vec{x}_ {2}+\omega_ {1+2}t_ {1}) } \int \frac{dE_ {2}}{2\pi} \frac{e^{ -i E_ {2}(t_ {2}-t_ {1}) }}{(E_ {2}+\omega_ {2})(E_ {2}-\omega_ {2})} \\
&\times  \frac{\Gamma(E_ {1}=\omega_ {1+2}-E_ {2})}{2(\omega_ {1+2}+E_ {2}-i\epsilon)(E_ {2}-\omega_ {1+2}+\omega_ {1}-i\epsilon)(E_ {2}-\omega_ {1+2}-\omega_ {1}+i\epsilon)}, 
\end{align*}
$$

whenever needed, we can replace $\omega_ {1,2}$ with $\omega_ {1,2}-i\epsilon$. This is consistent with Mark Sredinickie's convention that $m^{2}$ are to be replaced by $m^{2}-i\epsilon$ when necessary. 

Integrate $\text{I}$ with respect to $E_ {2}$ follow the lower semi-circle, we have 

$$
\begin{align*}
\text{I} =& i \int \frac{d^{d}p_ {1}d^{d}p_ {2}}{(2\pi)^{2d}} \,  \frac{e^{ -i(\vec{p}_ {1}\cdot \vec{x}_ {1}+\vec{p}_ {2}\cdot \vec{x}_ {2}+\omega_ {1}t_ {1}) }}{2\omega_ {1}} \\
& \times \left\lbrace  \frac{e^{ -it_ {2}\omega_ {2} }\Gamma(E_ {1}=\omega_ {1},E_ {2}=\omega_ {2})}{2\omega_ {2}(\omega_ {1}+\omega_ {2}+\omega_ {1+2})(\omega_ {1}+\omega_ {2}-\omega_ {1+2})}  \right. \\
&+\left. \frac{e^{ -it_ {2}(\omega_ {1+2}-\omega_ {1})}\Gamma(E_ {1}=\omega_ {1},E_ {2}=\omega_ {1+2}-\omega_ {1})}{2\omega_ {1+2}(\omega_ {1+2}-\omega_ {1}+\omega_ {2})(\omega_ {1+2}-\omega_ {1}-\omega_ {2})} \right\rbrace 
\end{align*}
$$

and 

$$
\begin{align*}
\text{II} =& -i \int \frac{d^{d}p_ {1}d^{d}p_ {2}}{(2\pi)^{2d}} \,  e^{ -i(\vec{p}_ {1}\cdot \vec{x}1+\vec{p}_ {2}\cdot \vec{x}_ {2}+\omega_ {1+2}t_ {1}) } \\
& \times  \left\lbrace \frac{e^{ -i(t_ {1}-t_ {2})\omega_ {2} } \Gamma(E_ {1}=\omega_ {1+2}-\omega_ {2},E_ {2}=-\omega_ {2})}{4\omega_ {2}(\omega_ {1+2}-\omega_ {2})(-\omega_ {1+2}-\omega_ {2}+\omega_ {1})(\omega_ {1}+\omega_ {2}+\omega_ {1+2})} \right.  \\
&+ \frac{e^{ -i(t_ {1}-t_ {2})\omega_ {1+2} } \Gamma(E_ {1}=2\omega_ {1+2},E_ {2}=-\omega_ {1+2})}{2(\omega_ {1+2}-\omega_ {2})(\omega_ {1+2}+\omega_ {2})(2\omega_ {1+2}-\omega_ {1})(2\omega_ {1+2}+\omega_ {1})}\\
&- \left. \frac{e^{ -i(t_ {1}-t_ {2})(\omega_ {1}-\omega_ {1+2}) }\Gamma(E_ {1}=\omega_ {1},E_ {2}=\omega_ {1+2}-\omega_ {1})}{4\omega_ {1}(\omega_ {1+2}-\omega_ {1}+\omega_ {2})(\omega_ {1+2}-\omega_ {1}-\omega_ {2})(2\omega_ {1+2}-\omega_ {1})} \right\rbrace .
\end{align*}
$$



the difference is that between $E'^{2}-\omega'^{2}-m^{2}+i\epsilon$ and $\omega_ {\vec{p}}^{2}$, I think

$$
\int d^{d}x \,  \frac{\Delta+g}{(2\pi)^{d}}:\phi^{3}(\vec{x}):
$$
- - -


Hi Jarah! In your note,

$$
\text{(2.4)} = -6g \int \frac{d^{d}p_ {1}d^{d}p_ {2}}{(2\pi)^{2d}} \, e^{ i(\vec{x}_ {1}\cdot \vec{p}_ {1}+ \vec{x}_ {2}\cdot \vec{p}_ {2}) } J,
$$

where

$$
J = \int \frac{dE_ {1}dE_ {2}}{(2\pi)^{2}} \, e^{ -i(E_ {1}t_ {1}+E_ {2}t_ {2}) }[(E_ {1}^{2}-\omega_ {1}^{2}+i\epsilon)(E_ {2}^{2}-\omega_ {2}^{2}+i\epsilon)((E_ {1}+E_ {2})^{2}-\omega_ {1+2}^{2}+i\epsilon)] .
$$

I use $\omega_ {1}$ as a short hand notation for $\omega_ {\vec{p}_ {1}}$.

`Question 1:` the factor of $g$ in $(-6g)$ was not in the paper? 

$$
J = \frac{1}{8\omega_ {1}\omega_ {2}\omega_ {1+2}}K,
$$

$$
K = \int \frac{dE_ {1}dE_ {2}}{(2\pi)^{2}} \, e^{ -i(E_ {1}t_ {1}+E_ {2}t_ {2}) }[\cdots] 
$$

For integrate contour, assume $t_ {1}>0$ and $t_ {2}>0$, we can close the lower half plane. At last we get

$$
J = 
$$

$$
\frac{e^{ -i\omega_ {p_ {1}}t_ {1} }}{\omega_ {p_ {1}}-\frac{i\epsilon}{2\omega_ {p_ {1}}}+E_ {2}-\omega_ {p_ {1}+p_ {2}}+\frac{i\epsilon}{2\omega_ {p_ {1}+p_ {2}}}}
$$

My extra terms to Eq.(2.6):

$$
\begin{align*}
& - \frac{3g}{4} \int \frac{d^{d}p_ {1}}{(2\pi)^{d}}\frac{d^{d}p_ {2}}{(2\pi)^{d}} \,  \frac{e^{ i(\vec{p}_ {1}\cdot \vec{x}_ {1}+\vec{p}_ {2}\cdot \vec{x}_ {2}) }}{\omega_ {1}\omega_ {2}\omega_ {1+2}}\\
&\times \left\lbrace \frac{e^{ -i(\omega_ {1}t_ {1}-\omega_ {1}t_ {2}+\omega_ {1+2}t_ {2}) }}{\omega_ {1}+\omega_ {2}-\omega_ {1+2}} + \frac{e^{ -i(\omega_ {1}t_ {1}-\omega_ {1}t_ {2}+\omega_ {1+2}t_ {2}) }}{\omega_ {1+2}+\omega_ {2}-\omega_ {1}} \right\rbrace ,
\end{align*}
$$

it can be simplified to 

$$
\frac{3g}{2}\int \frac{d^{d}p_ {1}}{(2\pi)^{d}}\frac{d^{d}p_ {2}}{(2\pi)^{d}} \,  \frac{e^{ i(\vec{p}_ {1}\cdot \vec{x}_ {1}+\vec{p}_ {2}\cdot \vec{x}_ {2}) } e^{ -i(\omega_ {1}(t_ {1}-t_ {2})+\omega_ {1+2}t_ {2}) }}{\omega_ {1}\omega_ {1+2}[(\omega_ {1+2}-\omega_ {1})^{2}-\omega_ {2}^{2}]},
$$

Earlier today, by mistake I canceled them.
# Jarah's note

Derivation of Eq.(2.6) from the LHS of Eq. (2.4).

The cubic Hamiltonian in terms of ladder operators:

$$
\begin{align*}
H_ {3}^{(3)} =& g\int \frac{d^{3}p}{(2\pi)^{3}} \, A^{\ddagger}_ {p_ {1}}A^{\ddagger}_ {p_ {2}}A^{\ddagger}_ {-p_ {1}-p_ {2}}, \\
H_ {3}^{(1)} =& \frac{3g}{2} \int \frac{d^{3}p}{(2\pi)^{3}} \, A^{\ddagger}_ {p_ {1}}A^{\ddagger}_ {p_ {2}} \frac{A_ {p_ {1}+p_ {2}}}{\omega_ {p_ {1}+p_ {2}}}, \\
H_ {3}^{(-1)} =& \frac{3g}{4} \int \frac{d^{3}p}{(2\pi)^{3}} \,  A^{\ddagger}_ {p_ {1}+p_ {2}} \frac{A_ {p_ {1}}}{\omega_ {p_ {1}}} \frac{A_ {p_ {2}}}{\omega_ {p_ {2}}}, \\
H_ {3}^{(-3)} =& \frac{g}{8} \int \frac{d^{3}p}{(2\pi)^{3}} \, \frac{A_ {p_ {1}}}{\omega_ {p_ {1}}} \frac{A_ {p_ {2}}}{\omega_ {p_ {2}}} \frac{A_ {-p_ {1}-p_ {2}}}{\omega_ {p_ {1}+p_ {2}}}
\end{align*}
$$

At $\mathcal{O}(g)$, we have 

$$
H_ {3}\left\lvert \Omega \right\rangle = g\int \frac{d^{3}p}{(2\pi)^{3}} \left\lvert \vec{p}_ {1},\vec{p}_ {2},-\vec{p}_ {1}-\vec{p}_ {2} \right\rangle
$$