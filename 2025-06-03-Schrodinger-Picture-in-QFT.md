---
layout: post
title: Schrodinger picture in QFT
date: 2025-06-03
author: Baiyang Zhang
catalog: true
tags:
---

# 


We define the tree level vacuum |Omega> to be the state annihilated by all annihilation operators

$$
a_p \left\lvert \Omega \right\rangle=0
$$

and a squeezed state to be any state of the form

$$
e^{ \sum_ {mn}c_ {mn}a^{\dagger}_ {m} a^{\dagger}_ {n}  } \left\lvert \Omega \right\rangle
$$

for some matrix $c_{mn}$.  Bogoliubov introduced the Bogoliubov transformation in 1958 based on the observation that a squeezed state can always be written as a Bogoliubov transformation on a vacuum state.  Now consider the decompositions of $\phi(x)$ and $\pi(x)$ at an arbitrary mass $\mu$

$$
\begin{align*}
\phi(x) =& \int \frac{dp}{\sqrt{2\omega_ {\mu,p}}} \, e^{ -ipx }(a^{\mu\dagger}_ {p}+a^{\mu}_ {-p}) , \\
\pi(x) =& i \int \frac{dp}{\sqrt{2\omega_ {\mu,p}}} \,  e^{ -ipx } (a^{\mu\dagger}_ {p}-a^{\mu}_ {-p}),
\end{align*}
$$

Consider this decomposition at two values of $\mu$, let us call them $\mu_ {1}$ and $\mu_ {2}$.  Then this is a linear set of 4 equations for 6 unknowns that lets us solve for $a^{\mu_ {2}}$ in terms of $a^{\mu_ {1}}$ and $a^{\mu_ {1}\dagger}$.  In other words, the pairs $a^{\mu_ {1}}, a^{\mu_ {1}\dagger}$ and $a^{\mu_ {2}}, a^{\mu_ {2}\dagger}$ are related by a Bogoliubov transformation.

Coleman’s (4.43) defines $\left\lvert 0,\mu \right\rangle$ as the state annihilated by $a^{\mu}_ {p}$.  The above argument shows that this state is related by a Bogoliubov transformation to the vacuum states $\left\lvert 0,m \right\rangle$ or $\left\lvert 0,M \right\rangle$.  In other words, changing the second argument ($\mu$) in the ket is equivalent to a Bogoliubov transformation.  However, a Bogoliubov transformation implements a squeeze (which is the reason that Bogoliubov introduced them, because the BCS superconducting ground state in a squeezed state).  Therefore we conclude that:  Coleman’s $\left\lvert 0,\mu \right\rangle$ is a squeezed state.  

Coleman’s squeezed state is annihilated by $a^{\mu}_ {p}$.  Our squeezed state $\left\lvert 0 \right\rangle$ is annihilated by  $b_ {k},b_s$ and $\pi_ {0}$.  The Bogoliubov transformation that maps $(a_ {p},a_ {p}^{\dagger})$ to $(a^{\mu}_ {p},a^{\mu\dagger}_ {p})$ is not the same Bogoliubov transformation that maps $(a_ {p},a_ {p}^{\dagger})$ to $b_ {k},b_ {k}^{\dagger},b_ {S},b_ {S}^{\dagger},\phi_ {0},\pi_ {0}$.  Therefore Coleman’s squeezed state $\left\lvert 0,\mu \right\rangle$ is not the same squeezed state as our squeezed state $\left\lvert 0 \right\rangle$.