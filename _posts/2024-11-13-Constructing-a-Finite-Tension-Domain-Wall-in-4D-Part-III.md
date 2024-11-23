---
layout: post
title: Constructing a Finite Tension Domain Wall in 4D Part III
date: 2024-11-13
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


