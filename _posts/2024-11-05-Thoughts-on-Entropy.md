---
layout: post
title: Some Thoughts on Entropy
date: 2024-11-05
author: Baiyang Zhang
catalog: true
tags:
---

# Boltzmann-Gibbs (BG) Entropy

There are so many different interpretations of entropy and somehow there are all equivalent to each other. Conceptually there are different definitions for entropy in physics and information theory, but the mathematical expression are the same, it must mean that there is a deep connection underneath.

Chronologically, the first definition for entropy is macroscopic, given by Rudolf Clausius in 1865, when Marx founded the first International. The increase of entropy is defined to be proportional to the heat $Q$ that enters a system at temperature $T$, 

$$
dS := \frac{Q}{T}.
$$

This definition tells us nothing about what entropy actually is. It is sometimes convenient to visualize entropy as some kind of "fluid" that can flow from one object to another. When heat (a form of energy) flows around between objects, it carries certain amount of entropy with it, $Q / T$. Since heat only flows from high temperature to low temperature, and the amount of heat is of course conserved during the flow, consequently entropy can only increase, it is only "half conserved", unlike energy. 

For an isolated system, we have the microscopic definition for entropy given by Boltzmann, 

$$
S = k_ {B} \ln \Omega,
$$

where $\Omega$ is the multiplicity, namely the number of microscopic states corresponding to certain macroscopic states, and $k_ {B}$ is the Boltzmann constant which we will set to be equal to $1$. 

There is a pretty good explanation about what are microstates and what are macrostates given by D. Shroeder in his textbook *The introduction to thermal physics*. For example, consider ten identical but distinguishable coins, the probability space is $(\Omega, \sigma, P)$ where $\Omega$ is the sample space, $\sigma$ is the sigma-algebra and $P$ the probability measure. Let's toss the ten coins and see what is the final result. Each coins has two possible outcomes, head or tail. A macro state is described by some general properties, for example there are total 2 heads out of ten coins; a micro state requires we to fix each coin, for example the ten coins are *htthtttttt* where h stands for head and t for tail. A macro state in general comprises of several micro states, for example a state where "there are two heads" include $10\times 9 / 2 =45$ micro states. Another way to see it is that **microstates are points in the sample space $\Omega$, while macro states are sets in the sigma-algebra.**

The definition for entropy $k \ln \Omega$ only applies to when each microstate has equal probability, it can be generalized to the case where different microstates have different probabilities, which is more suitable to real life and thus often seen in the context of information theory:

$$
S = - \sum_ {i} p_ {i} \ln(p_ {i}),
$$

where $p_ {i}$ is the probability for a microstate $\left\lvert i \right\rangle$. To see how to do it, consider an unfair coin with probability $p$ to give head and $1-p$ to give tail. Let's toss it $M$ times, or equivalently toss $M$ identical coins. We will calculate the total entropy for $M$ coins first. Then let's assume that entropy is additive (or extensive), that is, the total entropy of $M$ coins is given by $M$ times the entropy of a single coin. Here lies another fundamental assumption: entropy of independent systems are additive. 

Since the probability to give a head is $p$, among $M$ total incidents there are $pM$ heads. Let's denote it by $n$, which is assumed to be a big number. Now the question is: how many micro states there are that gives the macro state, namely with $N$ heads in total? The number $\Omega$ of such microstates is given by

$$
\Omega(n\text{ heads}) = \frac{M!}{n!(M-n)!},
$$

the total entropy is 

$$
S(n):=S(n\text{ heads}) = \ln \Omega(n \text{ heads}) = \ln\left( \frac{M!}{n!(M-n)!} \right).
$$

Here we can adopt the Stirling's approximation, 

$$
n! \approx \sqrt{2\pi n}  \left( \frac{n}{e} \right)^{n}  \approx \left( \frac{n}{e} \right)^{n}
$$

This approximation is quite accurate, for $n=3$ the relative error for $\sqrt{2\pi n}(n / e)^{n}$ is $2.7\%$, and $0.3\%$ for $n=10$. Write it as 

$$
\ln n! \approx \frac{1}{2}\ln(n)+n\ln n-n,
$$

where we have thrown away an additive constant $\frac{1}{2} \ln(1\pi)=0.9189\cdots$. Hell, $\ln n$ is also a small quantity compare to $n$ and $\ln n$ so let's throw it away as well. Take it to the entropy expression and simplify, we have

$$
S(n) = M\ln M - n\ln n-(M-n)\ln(M-n) = -(M-n)\ln\left( \frac{M-n}{M} \right)-n\ln\left( \frac{n}{M-n} \right)
$$

rewrite in terms of probabilities for head and tail, $p_ {h}= n / M$ and $p_ {t}=1-p_ {h}$, we have

$$
\frac{S}{M} = -p_ {h}\ln(p_ {h})-p_ {t}\ln p_ {t}=-\sum p\ln p.
$$

Here $\frac{S}{M}$ is simply the entropy of a single coin. This result can be readily generalized to the most general case, for a single system with $n$ possible outcomes whose probabilities are $p_ {n}$, the entropy is 

$$
S = - \sum_ {i=1}^{n} p_ {i}\ln p_ {i}.
$$

Note that we have dealt with two kinds of entropies:

1. Entropy associated with a single random variable, like the final state of a coin;
2. Entropy associated with a distribution on multiple identical random variables, such as the final states of many coins.

They are connected by the assumption that entropy is **extensive**. As we will see that this assumption will be violated by Tsallis entropy.

# Information Entropy

- - -

In information theory, the expression for entropy adopts an entirely different interpretation, however the mathematical expression is exactly the same, which is amazing! In information theory, people write the entropy as 

$$
S = \sum p_ {i} \ln\left( \frac{1}{p_ {i}} \right)
$$

and make sense of $\ln(1 / p)$ directly. As far as I know, there are commonly two interpretations: 

- $\ln(1 / p_ {i})$ measures the "surprise" of a outcome;
- Shannon's interpretation [Shannon:1948], $\ln(1 / p_ {i})$ measures the "information content" of a outcome;

The entropy is then the average value of so-called "surprise", or information content. It is a matter of taste of which you adopt.

In his work, Shannon was interested in finding a measure that could quantitatively capture the information content of a message source. He proposed several properties that this measure (which we now call entropy) should satisfy to be a useful and consistent measure of information. These properties included:

1. **Additivity**: The entropy of two independent sources should be the sum of their individual entropies.
2. **Continuity**: The measure should change continuously as the message probabilities change.
3. **Symmetry**: The measure should not depend on the order of the messages.
4. **Maximum**: The measure should be maximal for a uniform distribution, where all messages are equally likely.

Shannon's Uniqueness Theorem essentially states that, given these properties (along with a few others), the entropy of a discrete random variable is unique and is given by the now-familiar formula:

$$
S = -\sum_{i} p(x_i) \ln p(x_i)
$$

The theorem's significance lies in its establishment of entropy as a **unique measure** that satisfies these intuitive and necessary properties for quantifying information. It solidified the concept of entropy as the foundational metric in information theory, leading to profound implications for communication, coding theory, and even other disciplines like statistics and thermodynamics.

Different sets of postulates have been given, which characterize the Shannon entropy. The simplest such set of postulates is given by D. K. Fadeev and A. Feinstein in the late 1950s. Fadeev's postulates are as follows: Let $(p_ {1},\cdots,p_ {n})$ be a discrete probability distribution,

1. $S(p_ {1},\cdots,p_ {n})$ is invariant under a permutation of its variables;
2. $S(p,1-p)$ is a continuous function of $p$ for $0\leq p \leq 1$;
3. $S\left( \frac{1}{2},\frac{1}{2} \right)=1$;
4. $S(t p_ {1},(1-t)p_ {1},p_ {2},\cdots,p_ {n})=S(p_ {1},p_ {2},\cdots,p_ {n})+p_ {1}H(t,1-t)$ for $0\leq t \leq {1}$.

The proof can be found in Rényi's original paper on Renyi entropy. Condition (4) is stronger than the additivity, which states that for two probability distributions $\mathcal{P}$ and $\mathcal{Q}$, we have 

$$
S(\mathcal{P}\times \mathcal{Q}) = S(\mathcal{P}) + S(\mathcal{Q}).
$$

As a matter of fact, if we relax condition (4) to the above expression, there will be a family of quantities satisfying them, for instance, all the quantities characterized by $\alpha>0$ and $\alpha \neq1$:

$$
H_ {\alpha}(p_ {1},\cdots,p_ {n} ) := \frac{1}{1-\alpha}\ln\left( \sum_ {k=1}^{\infty} p_ {k} ^{\alpha} \right),
$$

which reduces to Shannon's entropy at $\alpha=1$. 






- - -

Kullback and Leibler (1951) developed the principle of minimum cross entropy (POMCE) and in the late 1950s Jaynes (1957a,b) developed the principle of maximum entropy (POME). 

The connection between likelihood function and cross entropy. 

Note that the cross entropy is not a metric since it is not symmetric under the exchange between $p$ and $\hat{p}$. 


