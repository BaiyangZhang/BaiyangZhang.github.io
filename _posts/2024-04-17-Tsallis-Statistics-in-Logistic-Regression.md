---
layout: post
title: Tsallis Statistics in Logistic Regression
subtitle: 
date: 2024-04-17
author: Baiyang Zhang
header-img: 
catalog: true
tags:
  - tsallis
---

- [1. Introduction](#1-introduction)
	- [1.1. The Basics of Boltzmann-Gibbs Extensive Entropy](#11-the-basics-of-boltzmann-gibbs-extensive-entropy)
	- [1.2. Generalization to non-Extensive entropy](#12-generalization-to-non-extensive-entropy)
- [2. Boltzmann-Gibbs Statistical Mechanics](#2-boltzmann-gibbs-statistical-mechanics)
	- [2.1. Three different forms of BG entropy](#21-three-different-forms-of-bg-entropy)
	- [2.2. Properties of BG entropy](#22-properties-of-bg-entropy)
	- [2.3. Constraints and Entropy Optimization](#23-constraints-and-entropy-optimization)
- [3. Nonextensive Statistical Mechanics](#3-nonextensive-statistical-mechanics)
	- [3.1. Mean Value in Tsallis Statistics](#31-mean-value-in-tsallis-statistics)
- [4. Useful Mathematical Formulae](#4-useful-mathematical-formulae)


# 1. Introduction

`Tsallis statistics` is a generalization of traditional statistical mechanics, devised by *Constantino Tsallis*, to better characterize complex systems. It involves a collection of mathematical functions and associated probability distributions that can be derived by optimizing the `Tsallis entropic form`, a generalization of familiar Boltzmann entropy. A key aspect of Tsallis statistics is the introduction of a real parameter $q$, which adjusts the distributions to exhibit properties intermediate between Gaussian and Levy distributions, reflecting the degree of non-extensivity of the system.

Tsallis distributions  include various families like the $q$-Gaussian, $q$-exponential, and $q$-Weibull distributions. These distributions are notable for their heavy tails and have been applied across diverse fields such as statistical mechanics, geology, astronomy, economics, and machine learning, among others.

The adaptation of Tsallis statistics to these varied fields underscores its versatility in dealing with systems where traditional Boltzmann-Gibbs statistics might not be adequate, particularly in scenarios involving long-range interactions, memory effects, or multifractal structures. Tsallis statistics is particularly useful in the analysis of non-extensive systems, to `biostatistics` could offer a novel perspective on analyzing complex biological data. Tsallis statistics has been successfully applied in various complex physical systems, such as space plasmas, atmospheric dynamics, and seismogenesis, as well as in the analysis of brain and cardiac activity, showing excellent agreement between theoretical predictions and experimental data. This demonstrates the versatility and potential of Tsallis statistics in capturing the dynamics of complex systems, which could be beneficial in biostatistical applications.

Given the interdisciplinary nature of biostatistics, which often deals with complex, high-dimensional data, the non-extensive framework of Tsallis statistics might offer new methodologies for data analysis. For instance, it could be useful in understanding the dynamics of ecosystems, population genetics, or the spread of diseases, where traditional models might not fully capture the underlying processes due to their complexity and the presence of long-range interactions.

To explore this possibility further, one could start by investigating specific biostatistical problems where the assumptions of traditional statistical mechanics are not met, and then applying Tsallis statistics to see if it offers better predictive power or insights. It would also be beneficial to collaborate with experts in biostatistics to identify the most pressing challenges where Tsallis statistics could be applied.

While the application of Tsallis statistics to biostatistics is an intriguing prospect, it is an emerging area that would require substantial interdisciplinary research to fully understand its potential and limitations. Below is a list of potential applications, take it with a grain of salt.

1. **Epidemiological Modeling**: Tsallis statistics could be used to model the spread of diseases, especially in cases where traditional models fail to capture the long-range correlations between individuals in a population.

2. **Genetic Data Analysis**: Analysis of genetic sequences and variations, where non-extensive entropy might better capture the complexity and long-range dependencies within genetic information.

3. **Protein Folding Dynamics**: Investigating the non-linear dynamics of protein folding, where Tsallis statistics may offer insights into the anomalous diffusion processes involved.

4. **Neural Network Analysis**: Modeling the complex interactions within neural networks, particularly in understanding the non-linear dynamics of brain activities and signal transmissions.

5. **Ecological Systems**: Applying Tsallis statistics to model the complexity of ecological systems, where interactions can span vast spatial and temporal scales.

6. **Cancer Growth Modeling**: Understanding the anomalous growth patterns of tumors, where traditional models might not accurately capture the underlying dynamics.

7. **Drug Response Modeling**: Analyzing the variability in drug responses among populations, which may exhibit non-standard distribution patterns that Tsallis statistics could elucidate.

8. **Heart Rate Variability Analysis**: Investigating the complex, non-linear dynamics of heart rate variability, potentially uncovering new insights into cardiovascular health.

9. **Analysis of Medical Imaging Data**: Enhancing the interpretation of complex patterns in medical imaging, such as MRI or CT scans, through non-extensive statistical models.

10. **Public Health Data Analysis**: Applying Tsallis statistics to public health data, potentially uncovering new patterns or correlations in large-scale health trends.


- - -

## 1.1. The Basics of Boltzmann-Gibbs Extensive Entropy

*The whole theory of Tsallis statistics is based on a single concept: the modified Boltzmann-Gibbs (B-G) entropy* $S_ {q}$. $q$ is some index show how much $S_ {q}$ differs from the $BG$ entropy, if $q=1$ then there is no difference. 

To explain why the Boltzmann-Gibbs entropy is said to be additive, let's first clarify what we mean by entropy in this context. In statistical mechanics, the Boltzmann-Gibbs entropy is a measure of the number of microstates that correspond to a given macrostate, providing a quantification of the system's disorder or randomness.

The formula for Boltzmann-Gibbs entropy, $S$, for a system in a particular **macrostate** is given by:

$$ 
S = -k_B \sum_i p_i \ln p_i 
$$

where $p_i$ is the probability of the system being in the $i$-th microstate, and $k_B$ is the Boltzmann constant.

Entropy is said to be additive when, for two independent systems $A$ and $B$, the total entropy $S_{AB}$ of the combined system is the sum of their individual entropies:

$$ 
S_{AB} = S_A + S_B 
$$

This additivity property stems from the assumption of statistical independence of the two systems, which implies that the probability of the combined system $AB$ being in a particular microstate is the product of the probabilities of $A$ and $B$ being in their respective microstates. If $A$ is in a microstate with probability $p_i$ and $B$ is in a microstate with probability $q_j$, then the probability of the combined system being in the microstate characterized by both $p_i$ and $q_j$ is $p_i \cdot q_j$.

As an example, consider two independent systems $A$ and $B$, each with two possible microstates. For system $A$, let the probabilities of the microstates be $p_1$ and $p_2$, and for system $B$, let them be $q_1$ and $q_2$. The entropies of systems $A$ and $B$ are:

$$ S_A = -k_B (p_1 \ln p_1 + p_2 \ln p_2) $$
$$ S_B = -k_B (q_1 \ln q_1 + q_2 \ln q_2) $$

For the combined system $AB$, there are four possible microstates, with probabilities $p_1q_1, p_1q_2, p_2q_1,$ and $p_2q_2$. The entropy of the combined system is:

$$ S
_{AB} = -k_B [(p_1q_1) \ln (p_1q_1) + (p_1q_2) \ln (p_1q_2) + (p_2q_1) \ln (p_2q_1) + (p_2q_2) \ln (p_2q_2)] 
$$

With some algebra, you can show that:

$$ 
S_{AB} = S_A + S_B .
$$

This demonstrates the additivity of entropy for independent systems. *The crucial point here is the assumption of independence*, which allows the probabilities of the combined system to be expressed as products of the individual systems' probabilities, leading directly to the additivity of entropy.

Tsallis in his book compared his generalization of B-G statistics to $q$-statistics to the generalization of a circle to ellipses in explaining the motion of celestial objects. In both cases a single parameter changes everything. However I would argue that in the case of Kepler and others, more physics was revealed then in Tsallis' case. 

## 1.2. Generalization to non-Extensive entropy

In his book Tsallis listed some reasons for considering non-extensive, non-Boltzmann-Gibbs entropy, which can be roughly translated into:

1. There is no (mathematical or physical) reason not to.
2. A statistical description of a system should be based on the dynamics of the system, the macroscopic theory should come from a microscopic one. This opens the way, especially for complex systems, for other than Boltzmann statistics.
3. The existence of long-range interactions on the microscopic level.

# 2. Boltzmann-Gibbs Statistical Mechanics

## 2.1. Three different forms of BG entropy

No we need to come back to one of the most important concept in physics, statistics and information theory: **entropy**. It appears in various fields, each with its unique perspective but underlying similarities in concept. 

Generally, *entropy represents a measure of disorder, randomness, or uncertainty*. In statistics, entropy is a measure of the **unpredictability** or the **randomness** of a distribution. *The higher the entropy, the more unpredictable the outcome*. For example, in a perfectly uniform distribution where all outcomes are equally likely, entropy is at its maximum, indicating maximum uncertainty or disorder. In contrast, a distribution where one outcome is certain has zero entropy, representing complete order. This concept is used in various statistical methods and models to quantify uncertainty or variability within a dataset. In information theory, entropy is a fundamental concept introduced by `Claude Shannon`. It quantifies the average amount of information produced by a stochastic source of data. The more uncertain or random the source, the higher the entropy. In practical terms, entropy helps in understanding the limits of data compression and the efficiency of communication systems. For instance, a message composed of completely random bits has higher entropy and cannot be compressed beyond a certain limit without losing information. On the other hand, a message with a lot of repetitive or predictable parts has lower entropy and can be compressed more effectively.

In each of these fields, entropy helps us understand systems' behavior in terms of unpredictability, disorder, and efficiency. While the context and applications may vary, the core idea revolves around the concepts of uncertainty and the distribution of states or outcomes.

In the previous section we showed the definition of entropy without much justification, because there is none! Not from the first principal at least. The programme to derive the expression of entropy that we are using today is sometimes called the Boltzmann program, since that was what Boltzmann was trying to do, before he strangled himself to death using a curtain or something. 

However, if the possibilities is a continuous distribution, the BG entropy must be modified accordingly, discrete probability $p_ {i}$ must be replaced by probability density $p(x)$ where $x$ is the variable. As a naively guess, I would say that we can write the entropy as 

$$
-k \sum p _ {i} \ln p _ {i}  \to -k \int dx \, p(x) \ln(p(x)), 
$$

where the probability distribution function (or probability density) is normalized,

$$
\int dx \,  p(x) =1.
$$

However, a difference between discrete and continuous probability lies in its dimension! Normalized discrete probabilities $p_ {i}$ sums to 1, $\sum_ {i} p_ {i}=1$, since $1$ is dimensionless, so is $p_ {i}$. This is not true for continuous probability density $p(x)$, since now the normalization condition tells us that $\int dx \, p(x)$ should be dimensionless, and $dx$ has the dimension of length, so $p(x)$ must have dimension of length inversed! Thus, wo need to introduce another parameter, call it $\sigma$, with dimension of length. Then we can define the BG entropy in the continuous scenario:

$$
S_ {BG} = -k\int dx \, p(x) \ln(\sigma\, p(x)). 
$$

For the case of equal probabilities, that is, $p= 1 / \Omega$ where $\Omega$ is the total number of allowed microscopic states, we have 

$$
S_ {BG} = k \ln\left( \frac{\Omega}{\sigma} \right).
$$

We just mention on the fly that, in quantum mechanics, the probabilistic distribution of a mixed state in terms of pure states is described using the density matrix $\rho$, and the BG entropy is generalized to 

$$
S_ {BF} = -k\,\mathrm{Tr}\, (\rho \ln \rho).
$$

## 2.2. Properties of BG entropy

We will list without proof some of the key properties of BG entropy.

- **Non-negativity**. $S\geq 0$ always. $S = k\ln \Omega$ might help to convince you of it.
- **BG entropy is maximized at equal probability**. Anything that drives the system away from it will decrease the entropy.
- **Expansibility**. Adding to a system new possible states with zero probability should not modify the entropy.
- **Additivity**. Let $A,B$ be two systems with entropy $S(A)$ and $S(B)$, putting them together will result in a new system $A+B$ with entropy $S(A+B)=S(A)+S(B)$.
- **Concavity**. Given two different probability distributions $\left\lbrace p_ {i} \right\rbrace$ and $\left\lbrace p'_ {i} \right\rbrace$, we can define an intermediate probability distribution 

$$
\widetilde{p}:= \lambda p + (1-\lambda)p',\quad  \lambda \in (0,1).
$$

Then we have 

$$
S(\widetilde{p})\equiv S(\lambda)> \lambda S(p)+(1-\lambda)S(p').
$$

**Shannon Uniqueness Theorem**. 

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

## 2.3. Constraints and Entropy Optimization

**Imposing the Mean Value**

We might know a priori the mean value of a variable $x$, i.e.

$$
\left\langle x \right\rangle  := \int dx \, x \, p(x)  = \overline{x}  \quad  \text{ is known.}
$$

We can apply the Lagrange multiplier method to find the optimizing distribution with the constraint, together with the normalization condition $\int dx \, p(x)=1$. The Lagrangian functional that we want to extremize reads now 

$$
\Phi[p(x)] = S_ {BG} - \alpha \int dx \, p(x) - \beta \int dx \, x \, p(x)
$$

where we have neglected some constant terms since they don't appear in the Euler-Lagrange equation, that is to say, they don't affect the final result; and

$$
S_ {BG} = -\int dx \, p(x)\ln p(x). 
$$

Using the method of variation, we get 

$$
p(x) = \frac{1}{\overline{x}} e^{ -x / \overline{x} }.
$$

**Imposing the Mean value and the Mean Squared Value**

Supposed that we not only know the mean value $\overline{x}=\left\langle x \right\rangle$, but also the mean square value $\left\langle x^{2} \right\rangle$:

$$
\left\langle x^{2} \right\rangle \equiv \int dx \, (x-\left\langle x \right\rangle )^{2} p(x) 
$$

This time the Lagrangian reads

$$
\Phi[p(x)] = S_ {BG} - \alpha \int dx \, p(x) - \beta_ {1}\int dx \, xp(x) - \beta_ {2} \int dx \, (x-\left\langle x \right\rangle )^{2}p(x).  
$$

Exactly as before, the variational method gives us 

$$
p(x) = \sqrt{ \frac{\beta_ {2}}{\pi} } \exp \left\lbrace -\beta_ {2}(x-\left\langle x \right\rangle )^{2} \right\rbrace 
$$

which is just the Gaussian distribution! This tells us that the Gaussian distribution maximizes the entropy with fixed mean and variance. 

# 3. Nonextensive Statistical Mechanics

Tsallis is convinced that there exists no logical-deductive procedure for generalizing any physical theory. As a possible motivation to generalize the exponential function $e^{ x }$, he started from the equation that $e^{ x }$ satisfies, which is fairly simple:

$$
\frac{dy}{dx} = y.
$$

A possible generalization of the equation is to writhe the RHS as $a+by$, we have 

$$
\frac{dy}{dx} = a+by \implies \frac{dy}{a+by}=dx\implies y=\frac{1}{b}(e^{ b(x+c) }-a),
$$

which does look very promising. Then Tsallis considered a non-linear generalization:

$$
\frac{dy}{dx} = y^{q}, \quad  q\in \mathbb{R},\quad y(0)=1.
$$

The boundary condition $y(0)=1$ is such that is agrees with the usual exponential function $e^{ 0 }=1$. Solving it we get

$$
(1-q) (x+c) = y^{1-q} ,
$$
the boundary condition translates to 

$$
c = \frac{1}{1-q},
$$

thus 

$$
\boxed{ 
y = (1+(1-q)x)^{1/(1-q)} =: e_ {q}^{x}.
}
$$

When $1+(1-q)x<0$, $e_ {q}(x)$ is defined to be zero (**why don't complexify it**?). Also note that $e^{ x }_ {q}$ goes to $e^{ x }$ at $q\to 1$ since, writing $q = 1-\epsilon$, we have 

$$
\lim_ { q \to 1 } e^{ x }_ {q} = \lim_ { \epsilon \to 0 } (1+\epsilon x)^{1/\epsilon} = e^{ x }.
$$

From the same equation that we got the definition of $e^{ x }_ {q}$, we also get the inverse function of $x$ in terms of $y$:

$$
\boxed{ 
x = \frac{y^{1-q}-1}{1-q} =: \log_ {q} y.
}
$$

They are referred to as $q$-exponential functions and $q$-logarithmic functions respectively.

Recall that logarithmic functions turns multiplication into addition, $\log(AB)=\log(A)+\log(B)$, for $q$-logarithmic functions we have something similar,

$$
\log_ {q}(AB) = \log_ {q}(A) + \log_ {q}(B) + (1-q) \log_ {q}(A)\log_ {q}(A).
$$

## 3.1. Mean Value in Tsallis Statistics

There are three types of Tsallis statistics, depending on how they take the mean value. Next we will discuss each of them in chronological order.

Throughout the note we will assume that probabilities are normalized in the usual way,

$$
\sum_ {i} p_ {i} = 1.
$$

Given an observable $\mathcal{O}$, what could be the expected value $\left\langle \mathcal{O} \right\rangle$? The most naive guess, which is also the default definition, is to define 

$$
\left\langle \mathcal{O} \right\rangle  := \sum_ {i}  p _ {i} O_ {i}
$$

where $\mathcal{O}_ {i}$ is the $i$-th possible value of $\mathcal{O}$ with probability $p_ {i}$. However, this definition yields and ill-defined thermodynamic distribution, *some energy states will not be allowed due to mathematical rather than physical reasons, and the distribution is not invariant under an overall shift in energy*. Normally only the energy difference matter, the only situation that I know of where the absolute energy matters is from gravity, which is clearly not the case here. Thus it is not a good definition for taking average. 

- - -

Another way to define the average, known as Tsallis type II, is 

$$
\left\langle \mathcal{O} \right\rangle := \sum_ {i} p_ {i}^{q} \mathcal{O}_ i.
$$
The problem is similar with type I, the sample space is constraint due to some un-natural reason, which I tend to interpret as the evidence of an ill-defined theory. Some divergence that occurs in type I does not occur here, but it introduces new problems, most of all the expected value of unity $\mathbb{1}$ is not $1$. 

However there is a remedy. Arguing from the point of view of information theory on incomplete probability distributions, Q. A. Wang suggested modifying the normalization of probability as 

$$
\sum_ {i} p_ {i}^{q} = 1.
$$

This can be rewritten by defining $P_ {i}:= p_ {i}^{1}$, then 

$$
\left\langle \mathcal{O} \right\rangle := \sum_ {i} P_ {i} \mathcal{O}_ {i} .
$$

- - -

Type III assumes that the average is defined as type II but with an normalization factor:

$$
\left\langle \mathcal{O} \right\rangle  := N \sum_ {i} p_ {i}^{q}\mathcal{O}_ {i},\quad  N = \sum_ {i}p_ {i}.
$$

This solves the problem that the expectation value of identity $1$ is not $1$. The probability derived from is also becomes invariant under an overall shift. 


# 4. Tsallis in Logistic Regression Methods

This part will be presented in a much less pedagogical manner, we will just introduce the functions whenever we encounter them along the way, with little or none explanation. 

Say we are given a matrix $X_ {nm}$ of the expression of  $p$ genes in $n$ samples, from microarray or RNA-seq or some other fancy technologies. Denote the response, or dependent variables as $\vec{y} = (y_ {1},\cdots,y_ {n})$, which is a $n$-tuple. 


# Appendix. Useful Mathematical Formulae

The definition of $q$-logarithm and $q$-exponential, $x>0, q \in\mathbb{R}$:

$$
\begin{align*}
\ln_ {q}x &:= \frac{x^{1-q}-1}{1-q}, \\
e^{ x }_ {q} &:= (1+(1-q)x)^{1/(1-q)}, 
\end{align*}
$$

in the definition of the exponential it is required that $1+(1-q)x>0$, otherwise it is defined to be zero. It is easily checked that they are indeed inverse to each other. 

many formula for $q$-logarithms reminds us of that for the regular $q$-logarithms. 

$$
\begin{align*}
\ln_ {q}(xy) &= \ln_ {q}(x)+ \ln_ {q}(y) + (1-q)\ln_ {q}(x)\ln_ {q}(x) , \\
\ln_ {q}(1+x) &= \sum_ {1}^{\infty} (-1)^{n-1} \frac{(q)_ {n}}{n!} x^{n}, \\
(q)_ {n} &= \frac{\Gamma(q+k)}{\Gamma(q)} = q(q+1)\cdots(q+k-1), \\
\ln_ {q}\prod_ {k=1}^{n}x_ {k} &= \sum_ {k=1}^{n} (1-q)^{k-1}\sum_ {i_ {k} >\cdots>i_ {1}=1}^{n} \ln_ {q}x_ {i_ {1}}\cdots\ln_ {q}x_ {i_ {k}}.
\end{align*}
$$

We also have 

$$
\begin{align*}
\ln_ {q} x &= x^{1-q}\ln_ {2-q}x , \\
q \ln_ {1-q}x^{a} &= a \ln_ {1-a} x^{q} .
\end{align*}
$$

Regarding the $q$-exponentials,

$$
\begin{align*}
\left( e_ {q}^{f(x)} \right) ^{a} &= e^{ af(x) }_ {1-(1-q)/a},\\
\frac{d}{dx} e_ {q}^{f(x)}  &= (e_ {q}^{f(x)})^{q} \times f'(x)
\end{align*}
$$

For more details, refer to the textbook by Tsallis himself and [https://doi.org/10.1016/S0378-4371(01)00567-2](https://doi.org/10.1016/S0378-4371(01)00567-2 "Persistent link using digital object identifier").


