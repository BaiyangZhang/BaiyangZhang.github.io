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

Logistic regression (LR) is a fundamental analytical tool in both the social and natural sciences. As a discriminative classification model, LR focuses on directly classifying the response variable. Compared to generative models like naive Bayes, LR has advantages in simplicity, interpretability, and roughly linear complexity \cite{Vapnik2000, Ng2001}. However, it has limitations, including the problem of unobserved heterogeneity \cite{Mood2010}, weak robustness to outliers such as corrupted data \cite{Feng2014, Carroll1993}, and bias based on maximum-likelihood estimation \cite{Sur2019}. These shortcomings motivated the potential for improvement, which can proceed in three possible directions: 1) generalizing the linear combination of input features, 2) generalizing the binary classifier, and 3) generalizing the entropy loss function. This paper focuses on the second approach, extending the binary classifier using Tsallis q-functions.


However, logistic regression has notable limitations. It assumes a linear relationship between the input features and the log-odds of the outcome, which may not hold in complex real-world scenarios. This linearity constraint can lead to suboptimal performance when capturing intricate patterns in data. Moreover, logistic regression is sensitive to outliers and may struggle with multicollinearity among predictors, potentially leading to unstable estimates. In cases where classes are not linearly separable, the model's predictive accuracy can diminish. Furthermore, logistic regression is less effective with large feature sets or when interactions between features are present, as it does not inherently model such interactions.


## 3. Study of binary classification


In this paper we focus on discriminative probabilistic classifiers. The training corpus comprises of $n$ independent pairs of input/output denoted by $(X^{(i)},y^{i})$, where each $X$ is the $p$-vector feature representation. In the training phase, in general the total loss takes the form \cite{Evgeniou2002}

$$
L(X) = \sum_ {i=1}^{n} \mathcal{L}(\hat{y}^{i},y^{i}) + \mathcal{P},\quad  \hat{y}^{i}=\hat{y}(z(X^{(i)}))
$$

where $\hat{y}$ is the predicted label, $\mathcal{P}$ is the penalty, $\sum\mathcal{L}$ is the loss function or empirical error that we want to minimize, and $z$ is the feature representation. In this paper we only consider the linear case where $z^{i}:=z(X^{(i)})=\beta^{T}X^{(i)}+\beta_ {0}$, where $\beta$ is the weight vector. 

It is of key importance to choose the suitable classification function $\hat{y}(X^{(i)})$ that could faithfully represent the nature of the process understudy, or at least meets the requirement of Fisher consistency \cite{Fisher1922}. For binary classification $y\in\left\lbrace 0,1 \right\rbrace$. The most straightforward choice of loss function would be the 0-1 loss function $\mathcal{L}(\hat{y},y) = \theta(-\hat{y} y)$ where $\theta$ is the Heaviside step function. However, despite its conceptual clarity, 0-1 loss function is discontinuous and non-convex, making it computationally expensive. This raises the need for various types of surrogate loss functions (SLF). Among them the convex ones are particularly favored, such as hinge loss and square loss \cite{Lin2002}. Nevertheless, the computational virtues of convexity comes at the cost of, for example, compromised robustness \cite{Bartlett2003}. Therefore different non-convex loss functions, such as ramp loss or sigmoid loss, are proposed \cite{Zhao2010}. Various loss functions are compared in Ref.~\cite{Hastie2001}. In this paper, we combine the $q$-deformed sigmoid with cross entropy loss and propose a new form of q-deformed cross entropy loss, as will be shown below. We emphasize that this is not yet a Tsallis-entropic generalization of the standard cross entropy, for we have merely replaced the sigmoid while keeping the formalism of standard cross entropy. The performance of $q$-sigmoid enhanced cross entropy loss is compared with [other method]. 

- - -

Here is a more native and academic revision of the text:

---

In this paper, we focus on discriminative probabilistic classifiers. The training corpus consists of nn independent input-output pairs, denoted as $(X^{(i)}, y^{(i)}), where each $X$ represents a $p$-dimensional feature vector. During the training phase, the total loss typically takes the following form \cite{Evgeniou2002}:

L(X)=∑i=1nL(y^(i),y(i))+P,y^(i)=y^(z(X(i))),L(X) = \sum_{i=1}^{n} \mathcal{L}(\hat{y}^{(i)}, y^{(i)}) + \mathcal{P}, \quad \hat{y}^{(i)} = \hat{y}(z(X^{(i)})),

where y^\hat{y} denotes the predicted label, P\mathcal{P} is the penalty term, ∑L\sum \mathcal{L} represents the loss function or empirical error to be minimized, and zz denotes the feature representation. In this work, we focus on the linear case, where z(i):=z(X(i))=βTX(i)+β0z^{(i)} := z(X^{(i)}) = \beta^T X^{(i)} + \beta_0, with β\beta being the weight vector.

A critical aspect of the learning process is the selection of an appropriate classification function y^(X(i))\hat{y}(X^{(i)}) that accurately represents the underlying process or, at the very least, satisfies the requirement of Fisher consistency \cite{Fisher1922}. For binary classification, we have y∈{0,1}y \in \{0, 1\}. The most straightforward choice of a loss function is the 0-1 loss function L(y^,y)=θ(−y^y)\mathcal{L}(\hat{y}, y) = \theta(-\hat{y} y), where θ\theta is the Heaviside step function. However, despite its conceptual simplicity, the 0-1 loss function is discontinuous and non-convex, making it computationally expensive to optimize. This motivates the use of surrogate loss functions (SLFs), particularly convex ones, such as hinge loss and squared loss \cite{Lin2002}.

While convex loss functions are computationally advantageous, they come with trade-offs, such as reduced robustness \cite{Bartlett2003}. Consequently, various non-convex loss functions, such as ramp loss or sigmoid loss, have been proposed \cite{Zhao2010}. A comparison of different loss functions can be found in Ref.~\cite{Hastie2001}. In this paper, we introduce a novel formulation by combining the qq-deformed sigmoid function with cross-entropy loss, resulting in a new form of qq-deformed cross-entropy loss, as described below. It is important to note that this does not represent a Tsallis entropy-based generalization of the standard cross-entropy; instead, we have replaced the sigmoid function while preserving the formalism of the standard cross-entropy. We also provide a comparison of the performance of the qq-sigmoid-enhanced cross-entropy loss with [other method].

---

This version refines the sentence structure, enhances clarity, and improves flow, making it more suitable for an academic audience.


- - -

The remaining parts of this paper is organized as follows: Section \ref{sec2}reviews some important convex and nonconvex loss functions. In Section III we propose a new nonconvex loss function: smoothed 0-1 loss function. In Section IV, an optimization algorithm (QSM) that suitable for both smooth and non-smooth optimization problems are adopted, which makes it possible to compare different loss functions under the same framework. In Section V we develop two binary classification algorithms for both convex and nonconvex loss functions. Section VI describes the experimental settings and res




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