---
layout: post
title: Discussion Notes
subtitle: 
date: 2024-04-01
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
---


Hi,

  

I think I don't understand divergences that aren't logarithmic.  Here are some things that confuse me:

  

1) If a divergence goes like $\ln(\Lambda)$, then the derivative with respect to $\Lambda$ is $1/\Lambda$. This is great because if in the denominator of the integrand you have some $p+p_i$ where you integrate over $p$ and there are a few values of $p_i$, then the value of $p_i$ only affects the integral through a $p_i/\Lambda$, which vanishes in the large $\Lambda$ limit.  Here $p_i$ is the momentum in an external leg, so by renormalizing with one value of $p_i$, you renormalize with all values ... so you really kill all of the divergences.  On the other hand, if the divergence is, for example, quadratic, then the integral with have terms like $\Lambda p_i$.  So here the dependence on $p_i$ is big, so you can't kill the divergence at multiple $p_i$ simultaneously. 

  

This may be consistent.  I guess it means that since the regularization (the cutoff) isn't Lorentz invariant, then you expect that the relation between the bare and the renormalized Hamiltonian isn't invariant.  So at most one of the two will be invariant.  In this case, if you want Lorentz invariance in the renormalized theory, then the counterterms (the bare theory) should have some non-Lorentz invariance terms like $\Lambda$ p.  But once you allow for these ... things are bad because you don't know which bare theories you can use any more.

  

2) My basic intuition is that the cutoff shouldn't matter once it is big.  In the case of a ln($\Lambda$) cutoff, it's true that changing the cutoff a bit (by p_i) changes things by p_i/$\Lambda$ whose limit goes to 0.  But, as described above, this doesn't work once the divergence is worse than logarithmic.

  

Now there's some good news:

  

1) In 3+1d at 1 loop there are only ln divergences except for the vacuum energy, which is quadratic.  However the vacuum energy doesn't have any external legs, so A_4 can't depend on any values of momentum scale p_i and you are saved from the above problem.  Now, if we wanted to calculate the 2 loop kink mass, we'd have to subtract the 2 loop soliton sector disconnected diagram from the divergent diagram that gives A_4.  So here we are subtracting two quadratic-diverging integrals and we could run into ambiguities depending on how we cut off the soliton sector integrals.  I think we should cut them off like in the paper with Andy, by turning all of the k's into p's and cutting off the p's.  Hopefully that is well defined?  But anyway, at 2 loops in 3+1d we're out of luck because there is a quadratic divergence in the sunset diagram which confuses me for the reasons above.

  

2) In gauge theories, maybe quadratic divergences always go away?  For example, Peskin and Schroeder in chapter 10 figure 10.1 mentions that the naively quadratic divergence from a fermion loop in the photon propagator is actually logarithmic.  Maybe you are always saved in gauge theories?  I also read that the triangle anomaly diagram has a linear divergence ... maybe the problems above are connected to the anomaly?

  

So it means that eventually we'll have to make a choice:

  

A) Ignore all divergences which are worse than logarithmic because they don't show in Nature (or hopefully in superQCD) ... except for maybe the triangle anomaly which maybe is special because it has an anomaly

  

B) Eventually try to do 3+1d at 2 loops and so confront the quadratic divergences.  We could of course use dimensional regularization here, but I don't know how D_f acts on it (although there are papers that say you can see dimensional regularization as some extra terms in the Hamiltonian, so maybe you can use that formulation).  Maybe we could use Pauli-Viillars? That is a bit more straightforward so far as D_f is concerned ...

  

Anyway we don't have to choose now ... we should finish 1 loop in 3+1d and 2 loops in 2+1d.

  

Jarah

- - -

I've read your emails three times already and need to go through them a fourth time to give a meaningful reply. However, I do have a related question about the polynomial divergence of the vacuum energy. Can you show me in [this paper](http://users.physik.fu-berlin.de/%7Ekamecke/ps/coleman.pdf) how is equation (2.20) obtained? I just can't get the clean expression 

$$\frac{1}{8\pi}(\mu^{2}-m^{2}),$$

I keep getting extra multiplicative factors involving $\ln\Lambda$. This equation is the same as Eq. (4.35) in Coleman's Erice lecture on classical and quantum lumps, where he claims that "an easy integration reveals" it. 

Do you have some time tomorrow for a online discussion maybe?



