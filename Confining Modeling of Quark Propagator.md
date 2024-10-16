---
layout: post
title: Confining Modeling of Quark Propagator
catalog: true
tags:
---
### Confining Modeling of Quark Propagator

**A.E. Radzhabov$^1$ and X.L. Shang$^2$**

$^1$Matrosov Institute for System Dynamics and Control Theory SB RAS, 664033, Irkutsk, Russia$^*$  
$^2$Institute of Modern Physics, Chinese Academy of Sciences, Lanzhou 730000, China$^†$

---

### Abstract

We propose a confining extension of the quark model with nonlocal currents. The quark propagator is modified by introducing a cut in α-space, which in momentum space corresponds to the subtraction of pole singularities. A two-phase structure is suggested to model the confinement-deconfinement phase transition. In the confined phase, the quark propagator lacks pole singularities, whereas, in the deconfined phase, a single quark pole exists.

---

### Introduction

Understanding strong interactions is a complex task. The fundamental theory of strong interactions, quantum chromodynamics (QCD), is formulated in terms of quarks and gluons. However, experimentally observed hadrons are interpreted as their bound states due to the non-perturbative nature of QCD, where the strong coupling constant, $\alpha_s$, is small only at large scales. Under normal conditions, quarks and gluons are confined inside hadrons. However, under certain physical conditions, such as heavy-ion collisions or within neutron stars, a different state of matter can form where fundamental constituents become deconfined and propagate freely.

The only ab initio non-perturbative method for investigating strong interactions is lattice QCD simulations, which have made significant progress in recent years. Despite this, the theoretical understanding of the underlying degrees of freedom still requires modeling since numerical simulations only provide numerical results without deeper insight. Symmetries of strong interactions can serve as a guiding principle, like chiral perturbation theory [1], which deals with Goldstone bosons, or the quark version of the Nambu–Jona-Lasinio (NJL) model [2], where spontaneous chiral symmetry breaking results in the formation of a quark condensate and massive constituent quarks instead of current quarks.

More sophisticated approaches are based on coupled systems of Dyson–Schwinger equations for quark and gluon propagators and their vertices, along with Bethe–Salpeter equations for hadronic bound states [3]. These approaches describe quarks with a momentum-dependent mass $m(p^2)$ and wave-function renormalization $Z(p^2)$. At large momentum transfer, the mass function tends to the current mass. Nonlocal versions of NJL models [4, 5] combine aspects of these approaches: the interaction structure resembles the NJL model, while the nonlocal quark current leads to a quark propagator with momentum-dependent mass.

However, the absence of confinement can make calculations problematic. If the denominator of the quark propagator has real-valued zeros:

$$k^2 + m^2(k^2) = 0,$$

this results in imaginary parts in the meson polarization loop. One solution is to have a mass function $m(k^2)$ that only results in complex-valued solutions of this equation. This situation is similar to the Lee-Wick model [6] and can be interpreted as a model of confinement [7]. Apart from technical issues in calculating Feynman diagrams, the physical meaning of these singularities remains unclear. Moreover, in mediums with varying finite temperature or baryon density, the positions of singularities change, raising questions about the model's reliability.

In this paper, we show that a simple modification can remove these unwanted singularities and restore confidence in quark models. The idea is that confinement should alter the model, which is based on chiral symmetry. Unphysical observables associated with quark degrees of freedom should be absent. Additionally, a method to realize the confinement-deconfinement phase transition is needed. The Polyakov loop extension of the quark model, which uses an effective potential based on gauge degrees of freedom, aims to achieve one aspect of confinement: the suppression of free quark pressure in the confining phase [8].

We suggest an additional modification to the quark model: cutting the inverse Laplace image of part of the quark propagator in the confined phase. The resulting momentum space-transformed function has no pole singularities. The new momentum scale parameter associated with this cut can be interpreted as the confinement scale $\Lambda_c$. From general expectations, $\Lambda_c$ should be less than the scale of spontaneous symmetry breaking $\Lambda$. To correspond with the confined phase, it is suggested to separate the quark pole in the deconfined phase and perform an α cut for the remaining function. For numerical estimation, we use a set of model parameters with $\bar{q}q = -(240\text{MeV})^3$ [9].

---

### Nonlocal Model

The Lagrangian of the simplest nonlocal chiral quark model with pseudoscalar–scalar sectors is:

$$L = L_{\text{free}} + L_{P,S},$$
$$L_{\text{free}} = \bar{q}(x)(i\partial̂ - M_c)q(x),$$
$$L_{P,S} = \frac{G}{2}\left[(J^a_S(x))^2 + (J^a_P(x))^2\right],$$

where $M_c$ is the current quark mass matrix with diagonal elements $m_c$, and $G$ is the four-quark coupling constant.

The nonlocal quark current can be taken in one-gluon-exchange-like (OGE) [4] or instanton liquid model (ILM) [5, 10] forms. The structure of OGE-type currents is:

$$J^a_{,\mu} M(x) = \int d^4x_1 d^4x_2 \delta \left(x - \frac{x_1 + x_2}{2}\right) g((x_1 - x_2)^2) \bar{q}(x_1) \Gamma^a_{,\mu} M q(x_2),$$

with $M = S, P$ and $\Gamma^a_S = \lambda^a$, $\Gamma^a_P = i\gamma_5\lambda^a$. For the SU(2) model, the flavor matrices are $\lambda^a \equiv \tau^a$, $a = 0, \ldots, 3$ with $\tau_0 = 1$. The function $g(x)$ is the form factor encoding the nonlocality of the QCD vacuum.

The bosonized Lagrangian via Hubbard-Stratonovich transformation is:

$$L_{\text{eff}} = \bar{q}(x)(i\partial̂ - M_c)q(x) + \sigma_0 J^0_S(x) - \frac{1}{2G}\left[(P^a(x))^2 + (S̃^a(x) + \sigma_0 \delta^a_0)^2\right] + P^a(x)J^a_P(x) + S̃^a(x)J^a_S(x).$$

Spontaneous chiral symmetry breaking leads to a non-zero vacuum expectation value of the scalar isoscalar field $\langle S^0 \rangle_0 = \sigma_0 \ne 0$. After shifting the scalar isoscalar field $S^0 = S̃^0 + \sigma_0$, the momentum-dependent quark mass appears:

$$m(p) = m_c + m_d g(p),$$

where the scalar coefficient $m_d = -\sigma_0$ can be found from the self-consistent equation:

$$m_d = \frac{G}{8N_c} \int \frac{d^4k}{(2\pi)^4} \frac{g(k^2) m(k^2)}{k^2 + m^2(k^2)}.$$

The quark propagator is:

$$S(p) = (p̂ - m(p))^{-1}.$$

The pion polarization loop is:

$$\Pi_\pi(p^2) = \frac{4N_c N_f}{(2\pi)^4} \int d^4k f^2(q^2) \text{InvD}(k^2_-) \text{InvD}(k^2_+) \left[(k_- \cdot k_+) + m(k_+) m(k_-)\right],$$

where $\text{InvD}^{-1}(k^2) = k^2 + m^2(k^2)$, and the momenta are $p = k_+ - k_-$ and $q = \frac{k_+ + k_-}{2}$. The splitting of momenta is arbitrary $k_+ = k + np$ and $k_- = k - (1-n)p$, where $0 < n < 1$, and the result should be insensitive to the splitting of momenta, which can be used to check calculations. The pion mass can be found from the equation:

$$-G^{-1} + \Pi_\pi(M^2_\pi) = 0.$$

---

### Singularities of the Quark Propagator

The analytical structure of the quark propagator strongly depends on the form factor. For a Gaussian form factor $g(k^2) = \exp(-k^2/\Lambda^2)$, the denominator of the quark propagator has infinitely many solutions of

 $k^2$ for complex-valued $k^2$. For some parameters, the first two poles could be for real negative-valued $k^2$, and after $p^2 > 4m^2_{\text{pole}}$, the imaginary part appears in the meson polarization loop.

For complex-valued poles, the situation is more complicated. Imaginary parts of different poles cancel each other, but the real part of the polarization loop has a cusp, which is unphysical. This occurs at:

$$M^2_{\text{thr}} = 2\text{Re}(m^2_{\text{pole}}) + 2\sqrt{\text{Re}(m^2_{\text{pole}})^2 + \text{Im}(m^2_{\text{pole}})^2}.$$

To perform calculations in medium, $G$ and $\Lambda$ are considered constant, and $m_d$ is the only parameter in the quark sector that changes. It is instructive to consider the position of poles for different $m_d$ with fixed $G$ and $\Lambda$. At the vacuum value of $m_d$, the first two poles are complex-valued, while decreasing $m_d$ moves the first two poles to the real axis, and at a critical value $m_d^{\text{crit}}$, these complex-conjugated poles become real-valued.

At finite temperature, $m_d^{\text{crit}}$ corresponds to the chiral phase transition point. If the presence of real-valued poles is considered an indicator of the confinement-deconfinement phase transition, these two phase transitions synchronize. However, there are problems with the analytical continuation of polarization loop integrals beyond $M_{\text{thr}}$. The Lee-Wick prescription for complex-valued poles suppresses the imaginary part of polarization loops, but the real part after this continuation has an unphysical cusp at the pinch point, restricting the model's applicability.

---

### Suggestions for Removing Quark Thresholds

Various methods exist to remove thresholds:

1. Represent the quark propagator as an entire function in the virton model [12]:

$$S(p) = -M \exp(-lp̂ - p^2 L^2 / 4).$$

2. Use an IR-cutoff in the NJL model with proper time regularization [14]:

$$1 / (s + M^2) = \int_0^\infty d\tau e^{-\tau(s + M^2)} \rightarrow \int_{\tau^2_{\text{IR}}}^{\tau^2_{\text{UV}}} d\tau e^{-\tau(s + M^2)} = \frac{e^{-\tau_{\text{UV}}(s + M^2)} - e^{-\tau_{\text{IR}}(s + M^2)}}{s + M^2}.$$

3. Represent the scalar (or vector) part of the quark propagator as an entire function [20]:

$$\text{InvD}(k^2) = \frac{1 - \exp(- (k^2 + m^2_c) / \Lambda^2)}{k^2 + m^2_c}.$$

4. Cut in $\alpha$-space of polarization loops. Each quark propagator is represented with usual prescriptions in $\alpha$-space, and the total expression for $n$, where $\alpha_i = t x_i$, is cut over the total sum $t = \sum_{i=1}^n \alpha_i$:

$$\Pi = \int_0^{1/\lambda^2} dt \, t^{n-1} \int_0^1 dn x_i \, \delta(1 - \sum_{i=1}^n x_i) F(t x_1, \ldots, t x_n).$$

There are two main approaches: modifying each propagator [12, 20] or the whole diagram [13–15, 21]. In the nonlocal model, the problem with momentum-dependent mass $m(p^2)$ necessitates modifying interaction vertices with external currents along with the quark propagator for gauge invariance. Therefore, modifying the whole diagram is unclear.

---

### Confining Prescription for Quark Propagator: α-Representation

To implement a prescription for the quark propagator using $\alpha$-space, when the denominator of the quark propagator has only pole singularities, it can be represented as a sum of its poles:

$$\text{InvD}(k^2) = \sum_{i=1}^N \frac{R_{z_i}}{k^2 + z_i},$$

where $N$ is the number of poles (for the Gaussian form factor $N = \infty$). Poles are sorted by the size of the real part of $z_i$ with $z_1$ having the smallest real part. Another expansion of the denominator is based on its high-energy $k^2$ behavior, i.e., expansion over $m_d$:

$$\text{InvD}(k^2) = \frac{1}{k^2 + m^2_c} - \frac{2 m_c m_d g(k^2)}{(k^2 + m^2_c)^2} + O(m^2_d).$$

The Laplace transform is defined as:

$$\text{InvD}(k^2) = \int_0^\infty d\alpha e^{-\alpha k^2} \text{InvD}(\alpha).$$

Series corresponding to the above equations can be obtained with inverse Laplace transforms for each term:

$$\text{InvD}(\alpha) = \sum_{i=1}^\infty R_{z_i} e^{-\alpha z_i},$$

$$\text{InvD}(\alpha) = e^{-\alpha m^2_c} - 2 e^{-\alpha_1 m^2_c} \alpha_1 m_c m_d \theta(\alpha_1) + \ldots,$$

where $\alpha_i = \alpha - 1/\Lambda^2_i$. The first series is valid for arbitrary form factors, while the second series' first term is model-independent, and the actual analytical form of $g(k^2)$ should be used for others.

The Laplace-transformed function is convergent for positive $k^2$ if the real parts are positive $\text{Re}(z_i) > 0$. For negative $k^2$, the transformation is only valid for $\text{Re}(z_1) \ge -k^2$. Suppose the Laplace-transformed function is cut at some point $1/\Lambda^2_c$ in $\alpha$-space:

$$\text{InvDR}(\alpha) = \text{InvD}(\alpha) \theta(1/\Lambda^2_c - \alpha) = \sum_{i=1}^\infty R_{z_i} e^{-\alpha z_i} \theta(1/\Lambda^2_c - \alpha).$$

In this case, the Laplace transformation becomes valid for arbitrary $k^2$. The behavior of $\text{InvD}(\alpha)$ is shown in Fig. 1.

---

### Finite Temperature Behavior

The mean field thermodynamic potential is given by:

$$\Omega_{\text{MF}} = \frac{m^2_d}{2G} - 4 \sum_{i=0,\pm} \int_{k,n} \ln\left[k^2_{n,i} + m^2(k^2_{n,i})\right] + U(\Phi, \bar{\Phi}) + \Omega_0,$$

where $k_{n,i} = (\omega^i_n - i\mu)^2 + k^2$ and $\int_{k,n} = T \sum_n \frac{d^3p}{(2\pi)^3}$. Fermionic Matsubara frequencies are partially shifted due to the presence of the Polyakov loop $\omega^\pm_n = \omega_n \pm \phi_3$, $\omega^0_n = \omega_n$, and $\omega_n = (2n+1)\pi T$. The infinite normalization constant $\Omega_0$ ensures that the pressure is zero at vacuum conditions, i.e., at zero temperature and chemical potential for the vacuum value of $m_d$.

In the presence of the Polyakov loop, the equations of motion for the mean fields are:

$$\frac{\partial \Omega_{\text{MF}}}{\partial m_d} = 0, \quad \frac{\partial \Omega_{\text{MF}}}{\partial \phi_3} = 0.$$

For comparison, three models are considered:

1. The usual quark model.
2. The confined quark model (sum in eq. 21 starts from $i=1$).
3. The confinement-deconfinement toy model (sum in eq. 21 starts from $i=1$ in the confined phase and $i=2$ in the deconfined phase. The border between phases is set by the properties of $\text{InvD}(k^2)$, where it has real (deconfined) or only complex poles (confined)).

Since the procedure of subtracting poles is $m_d$-dependent, this behavior must be included when taking derivatives from the thermodynamic potential. Alternatively, the analytical form of the

 gap equation (7) can be retained:

$$\frac{\partial \Omega_R}{\partial m_d} = \text{Gap},$$

and the thermodynamic potential can be numerically calculated from the gap equation:

$$\Omega_R = \int_0^{m_d} d m_d \text{Gap} + C,$$

where the integration constant $C$ is taken at zero dynamical mass for given $T$, $\mu$, and $\phi_3$. It is instructive to consider the thermodynamic potential as a function of $m_d$ in vacuum, as there is no influence from the Polyakov loop, allowing study of the $m_d$ dependence. The thermodynamic potential is shown for three models in Fig. 3: the usual quark model, the confined quark model, and the confinement-deconfinement model.

---

### Finite Temperature/Chemical Potential Behavior

Finite temperature behavior of the quark condensate and Polyakov loop is shown in Fig. 4. Even for the confining model, the dynamical quark mass decreases with increasing temperature due to the gap equation. At finite $T$, the Matsubara frequency is proportional to $T$, suppressing the right-hand side due to the form factor.

The finite $T$ phase transition in model (3) is first order, indicating that the gap equations in the two phases are not completely synchronized. However, the finite $T$ behavior of model (3) is close to the usual quark model. At finite chemical potential, the second minimum at low $m_d$, indicating a deconfined phase, appears, and the system transitions from the confined to deconfined state at some critical $m_d$.

---

### Conclusions

A simple prescription based on a cut in Laplace space for modeling the confining quark propagator is considered. This approach improves the analytical behavior of the quark propagator. At finite $T/\mu$, a two-phase scheme can be considered where the quark propagator lacks pole singularities in the confined phase and has a single physical pole in the deconfined phase. Mean field calculations in this scheme show that critical temperature and chemical potential positions are almost unchanged, but there is a first-order phase transition at finite $T$ instead of a crossover. Spurious poles in the complex plane are absent, indicating that these poles do not have physical consequences. Instead, the mass function has cuts in the complex plane, and instabilities are present but less significant.

The most important conceptual problem is the exponential growth of polarization loops in Minkowski space. This issue arises because if the quark propagator lacks singularities at finite $p^2$, it will have an essential singularity at infinity. How to solve this problem remains unclear, but sub-leading $1/N_c$ corrections, such as pion dressing of the quark propagator, may introduce physically motivated singularities. This possibility was discussed by V. N. Gribov in his confinement theory [26].

---

**Acknowledgements**

A.E.R. is supported by the CAS President's International Fellowship Initiative (Grant No. 2023VMA0015) and the project of the Ministry of Education and Science of the Russian Federation ("Analytical and numerical methods of mathematical physics in problems of tomography, quantum field theory, fluid and gas mechanics" no. 121041300058-1).

The authors thank I.V. Anikin, Yu.M. Bystritskiy, and V.P. Lomov for fruitful comments. We are also grateful to B. Zhang for careful reading of our manuscript and useful remarks.

**Contact Information:**
- A.E. Radzhabov: aradzh@icc.ru
- X.L. Shang: shangxinle@impcas.ac.cn

---

**References**

1. J. Gasser and H. Leutwyler, Annals Phys. 158, 142 (1984).
2. Y. Nambu and G. Jona-Lasinio, Phys. Rev. 124, 246 (1961).
3. C. D. Roberts and S. M. Schmidt, Prog. Part. Nucl. Phys. 45, S1 (2000), arXiv:nucl-th/0005064.
4. D. Gomez Dumm and N. N. Scoccola, Phys. Rev. D65, 074021 (2002), hep-ph/0107251.
5. A. E. Dorokhov and L. Tomio, Phys. Rev. D62, 014016 (2000).
6. T. D. Lee and G. C. Wick, Nucl. Phys. B 9, 209 (1969).
7. M. Bhagwat, M. A. Pichowsky, and P. C. Tandy, Phys. Rev. D67, 054019 (2003).
8. C. Ratti, M. A. Thaler, and W. Weise, Phys. Rev. D73, 014019 (2006).
9. D. Gomez Dumm, A. Grunfeld, and N. Scoccola, Phys. Rev. D74, 054026 (2006).
10. R. S. Plant and M. C. Birse, Nucl.Phys. A628, 607 (1998).
11. A. Windisch, Phys. Rev. C 95, 045204 (2017), arXiv:1612.06002 [hep-ph].
12. A. Z. Dubnickova, G. V. Efimov, and M. A. Ivanov, Fortsch. Phys. 27, 403 (1979).
13. G. V. Efimov and M. A. Ivanov, The Quark Confinement Model of Hadrons (IOP, Bristol, UK, 1993) p. 177.
14. D. Ebert, T. Feldmann, and H. Reinhardt, Phys. Lett. B 388, 154 (1996), arXiv:hep-ph/9608223.
15. D. Blaschke, G. Burau, M. K. Volkov, and V. L. Yudichev, Eur. Phys. J. A11, 319 (2001).
16. L. X. Gutierrez-Guerrero, A. Bashir, I. C. Cloet, and C. D. Roberts, Phys. Rev. C 81, 065202 (2010), arXiv:1002.1968 [nucl-th].
17. H. L. L. Roberts, C. D. Roberts, A. Bashir, L. X. Gutierrez-Guerrero, and P. C. Tandy, Phys. Rev. C 82, 065202 (2010), arXiv:1009.0067 [nucl-th].
18. K.-l. Wang, Y.-x. Liu, L. Chang, C. D. Roberts, and S. M. Schmidt, Phys. Rev. D 87, 074038 (2013), arXiv:1301.6762 [nucl-th].
19. F. Marquez, A. Ahmad, M. Buballa, and A. Raya, Phys. Lett. B747, 529 (2015), arXiv:1504.06730 [nucl-th].
20. A. E. Radzhabov and M. K. Volkov, Eur. Phys. J. A19, 139 (2004).
21. T. Branz, A. Faessler, T. Gutsche, M. A. Ivanov, J. G. Korner, and V. E. Lyubovitskij, Phys. Rev. D81, 034010 (2010), arXiv:0912.3710 [hep-ph].
22. A. A. Osipov, A. E. Radzhabov, and M. K. Volkov, (2006), arXiv:hep-ph/0603130 [hep-ph].
23. A. Radzhabov, D. Blaschke, M. Buballa, and M. Volkov, Phys. Rev. D83, 116004 (2011), arXiv:1012.0664 [hep-ph].
24. J. P. Carlomagno and M. F. I. Villafane, Phys. Rev. D 100, 076011 (2019), arXiv:1906.04257 [hep-ph].
25. S. Benic, D. Blaschke, and M. Buballa, Phys. Rev. D 86, 074002 (2012), arXiv:1206.6582 [hep-ph].
26. V. N. Gribov, Eur. Phys. J. C 10, 91 (1999), arXiv:hep-ph/9902279.