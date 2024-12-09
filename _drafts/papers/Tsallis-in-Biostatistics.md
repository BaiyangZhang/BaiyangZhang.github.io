---
layout: post
title: 
date: 
author: Baiyang Zhang
catalog: true
tags:
---






# Abstract


# Introduction


## 1. History of Non-Extensive Entropy: Rényi and Tsallis Entropy




Classical entropy measures, such as Shannon entropy and Boltzmann-Gibbs entropy, have achieved immense success in various fields. However, they are constrained by certain inherent properties, most notably the requirement of additivity, which limits their applicability in describing complex systems that exhibit unusual behaviors, including multifractal structures and non-equilibrium dynamics \cite{Feinstein1958-FEIFOI}. This limitation has led to the development of several generalizations of traditional entropy, some of which preserve additivity, such as Rényi entropy \cite{Rnyi1961OnMO}, while others explicitly break it. Among the most widely used non-additive entropy measures is Tsallis entropy \cite{Tsallis1988}, which introduces a nonextensive parameter $q\in\mathbb{R}$ to characterize deviations from extensiveness. Tsallis entropy has found extensive applications in various fields, including high-energy physics \cite{PhysRevD.109.052008, ALICE:2022pbb, Baptista:2023btx}, machine learning \cite{Brochet2022, Hadzibeganovic2009}, and biostatistics \cite{Thilagaraj2019, Pardede2023, Brochet2022}, etc.

The key aspect of Tsallis statistics is the introduction of the so-called $q$-exponential and $q$-logarithmic functions, defined as \cite{Yamano2002}

$$
\begin{align}
\exp⁡_ {q}(x) &=  
\begin{cases}
\left( 1 + (1 - q) x \right)^{\frac{1}{1 - q}}, &  1 + (1 - q) x >0,  \\
0,  &\text{otherwise},
\end{cases} \\
\log_q(x) &= \frac{x^{1 - q} - 1}{1 - q},
\end{align}
$$

and recover the standard exponential and logarithmic functions as $q\to 1$. $q$-exponential captures the non-linear deformation from standard exponential, similarly for $q$-logarithmic, allowing for a more flexible description of systems that deviate from traditional, additive models. These functions have found widespread use in diverse fields, such as statistical mechanics, where they help describe systems far from equilibrium and systems with fractal-like properties \cite{Tsallis1988, Beck2001}. The application of $q$-exponential and $q$-logarithm has been explored to model phenomena such as gene expression variability and survival analysis, where the underlying data often exhibits heavy-tailed distributions or non-equilibrium dynamics \cite{Pardede2023, Thilagaraj2019}. These generalized functions have been incorporated into loss functions and optimization methods, offering a robust framework for modeling classification problems where traditional methods fail to capture complex dependencies in data \cite{Brochet2022, Hadzibeganovic2009}. The flexibility of the $q$-exponential and $q$-logarithm functions thus makes them valuable tools for extending traditional methods in both theoretical and applied research.

## 2. Historical Development of Logistic Regression Method

Logistic regression is a widely used discriminative model in statistical learning, particularly effective for binary classification tasks. Its primary advantage lies in its simplicity and interpretability; the model estimates the probability of a binary outcome by applying the logistic function to a linear combination of input features, allowing for straightforward interpretation of feature coefficients. Additionally, logistic regression is computationally efficient and performs well when the relationship between the independent variables and the log-odds of the dependent variable is linear.

However, logistic regression has notable limitations. It assumes a linear relationship between the input features and the log-odds of the outcome, which may not hold in complex real-world scenarios. This linearity constraint can lead to suboptimal performance when capturing intricate patterns in data. Moreover, logistic regression is sensitive to outliers and may struggle with multicollinearity among predictors, potentially leading to unstable estimates. In cases where classes are not linearly separable, the model's predictive accuracy can diminish. Furthermore, logistic regression is less effective with large feature sets or when interactions between features are present, as it does not inherently model such interactions.

In summary, while logistic regression offers clarity and efficiency for binary classification under linear assumptions, its performance can degrade in the presence of non-linear relationships, outliers, multicollinearity, and complex feature interactions. These limitations necessitate careful consideration and, in some cases, the adoption of more flexible modeling approaches to adequately capture the underlying data structures.
## 3. Study of Sigmoid Function in Logistic Regression

The sigmoid function is a cornerstone in logistic regression, used to map the linear output of the model into a probability. It transforms any real-valued input to a range between 0 and 1, enabling its interpretation as a probability. The study of the sigmoid function's properties and its adaptations has been an area of interest, particularly when extending logistic regression to complex applications, including gene expression data in biostatistics.

## 4. Gradient Method in Logistic Regression and Recent Developments

The gradient method, especially gradient descent, is a popular optimization technique used to minimize the cost function in logistic regression models. The choice of step length (learning rate) is critical for ensuring convergence, especially when dealing with high-dimensional datasets. Recent developments have focused on adaptive learning rate methods and optimization techniques that enhance the efficiency and accuracy of logistic regression.

# The Method


## Generalized sigmoid functions


In this paper we focus on binary classification, specifically on the generalization of sigmoid function with Tsallis $q$-exponentials and $q$-logarithm. Recall that $q$-exponential is a non-linear generalization of standard exponential function, \cite{Yamano2002}
$$
\exp_ {q}(x) := \begin{cases}
(1+(1-q)x)^{1/(1-q)},   &  1+(1-q)x>0 \\
0, & \text{otherwise}
\end{cases}
$$
which recovers to the regular exponential function at $q\to 1$ limit. Let $z$ be the linear combination of the input features. The standard sigmoid function $\sigma(z)$ bridges the weighted linear combination of features of the model, usually represent the microscopic information, with the conditional probability $\hat{p}(1\mid z)$ for a positive outcome,

$$
\hat{p}(1\mid z) \equiv \sigma(z) = \frac{1}{1+e^{ -z }}.
$$

As a concise and systematic way to introduce the nonextensive deviation, the sigmoid function can be directly generalized using Tsallis $q$-function to \cite{Pardede2023}

$$
\sigma_ {q}(z) := \frac{1}{1+\exp_ {q}(-z)}.
$$




 However, this definition suffer from a major drawback, that is it adopts step-function like behavior at $z=1 / (1-q)$, due to discontinuity of $\exp _ {q}(z)$. In order to remedy this situation we have two options: 1) modify the definition of $\sigma_ {q}(z)$ by introducing upper and lower cutoffs which are chosen empirically, one example can be found in \cite{Pardede2023}; 2) modify the definition of $q$-exponential in Eq.~\ref{eq:qexp} in such a way that the resulting $\sigma_ {q}(z)$ adopts appropriate behavior. In theory both are acceptable, however in order to gain the maximal controllability of the classifier and minimize degrees of freedom, we choose to modify Eq.~\ref{eq:qexp} as the following,
$$
\exp_ {q}(z) := 
\begin{cases}
\infty,  &  q>1 \text{ and } z> 1/(q-1) ,  \\
0,  &   q<1\text{ and }z<1/(q-1), \\
(1+(1-q)x)^{1/(1-q)},  &  \text{otherwise}.
\end{cases}
$$
  

- - -


 It can be easily verified that 

$$
\frac{ \partial \sigma_ {q}(z) }{ \partial z }  = \beta(q,z)\sigma_ {q}(z)(1-\sigma_ {q}(z))
$$

where 

$$
\beta(q,z) = \frac{1}{1-z(1-q)}.
$$

As for surrogate loss function we choose the cross entropy loss function without penalty, 

$$
L= - \sum_ {i=1}^{n}[y_ {i}\log(\sigma _ {q_ {i} }(z_ {i} ))+(1-y_ {i})\log(1-\sigma_ {q_ {i} }(z_ {i} ))],
$$

where we have included the possibility that different sample has different $q$ value, which is not the case in this paper, for reasons that will be explained later. We use the standard gradient method to find the optimal value of model parameters that minimized the loss function. Let $\theta$ be the vector of parameters and $X^{(i)}$ the vector of features of $i$-th incident, the gradient of loss function reads

$$
\frac{ \partial L(y,\theta) }{ \partial \theta ^{a} }  = \sum_ {i} \beta_ {q}(z) (\sigma_ {q}(z_ {i} )-y_ {i})X^{(i)}_ {a}, \quad  z_ {i} =\sum_ {a}\theta^{a} \cdot X^{(i)}_ {a} = \theta \cdot X^{(i)}.
$$

Note that sample-dependent $q_ {i}$ have been replaced by an universal $q$. In contrast to the classical result, there is an extra $\beta$ factor which is nonlinear in both $q$ and $z$. $\beta$ function automatically appears as learning rate, regulated by input features.

Another equivalent expression for the standard sigmoid function reads

$$
\sigma(z) = \frac{e^{ z }}{e^{ z }+1},
$$

which yields a different generalized sigmoid function after substitution of the $q$-exponent function, what we address to as the second kind of $q$-sigmoid function, denoted as

$$
\overline{\sigma}_ {q}(z) := \frac{\exp_ {q}(z)}{\exp_ {q}+1}. 
$$

This is inequivalent to the $q$-sigmoid of the first kind since the q-exponentials behave different under multiplication compared to standard exponential functions, the former follows so-called  $q$-algebra: \cite{umarov2008}

$$
\begin{align*}
\exp_ {q}(x) \exp_ {q}(y) &= \exp _ {q} (x \oplus _ {q} y),\\
\exp _ {q} (x+y) &= \exp _ {q} (x) \otimes _ {q} \exp _ {q} (y),
\end{align*}
$$

where the binary operations $q$-sum $\oplus _ {q}$ and $q$-product $\otimes _ {q}$ are defined as 

$$
x \oplus_ {q} y := x+y+(1-q)xy, \quad x \otimes _ {q}  y := (x^{1-q}+y^{1-q}-1)_ {+}^{1/(1-q)},
$$

and the symbol $(f)_ {+}$ means $\text{max}(f,0)$. 

Another approach to obtain the $q$-sigmoid function of the second kind is as following. The standard logit function connects the microscopic information represented by $z$ with macroscopic measure result $\hat{p}(1\mid z)$ in a linear fashion,

$$
\text{logit}(\hat{p}) = \log\left( \frac{\hat{p}}{1-\hat{p}} \right)=z.
$$

We generalize it using $q$-logit function by defining

$$
\text{logit}_ {q}(\hat{p}) := \log_ {q}\left( \frac{\hat{p}}{1-\hat{p}} \right)=z.
$$

Invert the relation we have

$$
\hat{p}(1\mid z) := \frac{\exp_ {q}(z)}{\exp_ {q}(z)+1},
$$

which reproduces the $q$-sigmoid function of the second kind. 

We have

$$
\frac{d}{dz} \overline{\sigma}_ {q}(z) = \overline{\sigma}_ {q} (z)(1-\overline{\sigma}_ {q} (z))\beta _ {q} (-z), \quad  \beta _ {q} (-z)=\frac{1}{1+(1-q)z},
$$

the gradient of the associated cross-entropy loss function with respect to the parameters reads

$$
\frac{ \partial \overline{L} }{ \partial \theta_ {a} } =\sum_ {i=1}^{n} [\overline{\sigma}_ {q} (z_ {i} )-y_ {i}] \beta _ {q} (-z_ {i} )X^{(i)}_ {a}, \quad z_ {i} =\sum_ {a}\theta_ {a}X^{(i)}_ {a}= \vec{\theta}\cdot \vec{X}^{(i)}.
$$

## Algorithm






# Numerical simulation results



# Discussion