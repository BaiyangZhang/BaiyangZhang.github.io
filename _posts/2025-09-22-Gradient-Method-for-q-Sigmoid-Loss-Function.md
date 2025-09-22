---
layout: post
title: Gradient Method for q-Sigmoid Loss Function
date: 2025-09-22
author: Baiyang Zhang
catalog: true
tags:
  - tsallis
---
## q-log and q-exp

The definition of Tsallis-modified log and exponential functions, so-called $q$-log and $q$-exponentials, for future convenience:

$$
\begin{align*}
\log_ {q} (x) := & \frac{x^{1-q}-1}{1-q}, \\
\exp_ {q}(x) :=& (1+(1-q)x)^{1/(1-q)}_ {+}.
\end{align*}
$$

Note that in the exponential function, if $1+(1-q)x<0$ then $(1+(1-q)x)_ {+}=0$ by definition, in this case if $\frac{1}{1-q}<0$, then we have zero to the power of some negative number, namely $0^{\alpha}$ where $\alpha<0$. This is to be interpreted as $\frac{1}{0^{\left\lvert \alpha \right\rvert}}=\frac{1}{0 }\approx \infty$. The purpose of this particular definition is to make sure that $\exp_ {q}$ has the same asymptotic behavior as the regular exponential function. 

As you can check, at the limit $q\to 1$ they regress to normal log and exp functions. 

For computational convenience, we will stick with the **q-sigmoid of the first kind**, which is the direct deformation of the regular sigmoid function

$$
\sigma(z) = \frac{1}{1+e^{ -z }}.
$$

As a result we have the $q$-sigmoid of the first kind: 

$$
\boxed{ 
\sigma_ {q}(z) := \frac{1}{1+\exp_ {q}(-z)}.
}
$$

$$
\frac{ \partial \sigma_ {q}(z) }{ \partial z }  = \beta(q,z)\sigma_ {q}(z)(1-\sigma_ {q}(z))
$$

where 

$$
\beta(q,z) = \frac{1}{1-z(1-q)}.
$$

This should be compared to the case of regular sigmoid function:

$$
\frac{ \partial \sigma(z) }{ \partial z }  = \sigma(z) (1-\sigma(z)).
$$
The cross entropy loss function now reads

$$
\boxed{ 
L= - \sum_ {i=1}^{n}[y_ {i}\ln(\sigma _ {q_ {i} }(z_ {i} ))+(1-y_ {i})\ln(1-\sigma_ {q_ {i} }(z_ {i} ))].
}
$$

where $z_ {i}=\theta\cdot X^{(i)}$, $X^{(i)}$ the $i$-th observed data and the q-parameters $q_ {i}$ are different for each sample. Someone write it as $z_ {i}=\theta^{T}X^{(i)}$, but I neglect the transpose symbol since now both $\theta$ and $X$ are understood as vectors. For starters we can set all the $q_ {i}$ as the same constant for all samples, do a grid search over certain intervals, such as from 0 to 10 or something. This will greatly reduce the number of free parameters hence prevents over fitting.

We will use the gradient method to find the optimal values of parameters that minimized the loss function. Next we work out the derivative of loss function.

Some straightforward derivation shows that 

$$
\frac{ \partial L(y,\sigma_ {q}(z)) }{ \partial z_ {i}  }  = \beta_ {q}(z_ {i} )(\sigma_ {q}(z_ {i} )-y_ {i} ),
$$

where $\beta_ {q}(z) = \frac{1}{1-z(1-q)}$. The derivative of the loss function with respect to parameters can be readily written as 

$$
\boxed{ 
\frac{ \partial L(y,\theta) }{ \partial \theta ^{a} }  = \sum_ {i} \beta_ {q}(z) (\sigma_ {q}(z_ {i} )-y_ {i})X^{(i)}_ {a}, \quad  z_ {i} =\sum_ {a}\theta^{a} \cdot X^{(i)}_ {a} = \theta \cdot X^{(i)}.
}
$$

Note that I have replace $q_ {i}$ with an universal $q$. In contrast to the classical result, there is an extra $\beta$ factor which is nonlinear in both $q$ and $z$. 

## Deformation (hyper)parameter

the expressions are greatly simplified if we define the `deformation hyperparameter` $\eta:=1-q$,  $\eta \in\mathbb{R}^\ast$ where $\mathbb{R}^\ast:=\mathbb{R}\backslash \left\lbrace 0 \right\rbrace$ is the punctured real line. The deformed exponential functions in terms of $\eta$ reads

$$
\exp_ {\delta}(x) = (1+\eta x)^{1/\eta}_ {+}.
$$

The derivative of $\exp {\eta}(z)$ with respect to $\eta$ is

$$
\frac{ \partial \exp_ {\eta}(z) }{ \partial \eta }  = 
\begin{cases}
\exp_ {\eta}(z) \left( \frac{z}{\eta(1+\eta z)}- \frac{1}{\eta^{2}}\ln(1+\eta z) \right), &  1+\eta x>0, \\
0,  & \text{otherwise}.
\end{cases}
$$

Denote

$$
\gamma(z; \eta):= \frac{z}{\eta(1+\eta z)}-\frac{1}{\eta^{2}}\ln(1+\eta z),
$$

then for $1+\eta x>0$ we have 

$$
\frac{ \partial \exp _ {\eta}(z) }{ \partial \eta } =\exp_ {\eta}(z) \gamma(z;\eta).
$$

The deformed sigmoid function, now addressed to as $\eta$-sigmoid, reads

$$
\sigma_ {\eta}(z) := \frac{1}{1+\exp_ {\eta}(-z)},
$$

whose derivative with respect to $\eta$ is 

$$
\frac{ \partial \sigma_ {\eta}(z) }{ \partial \eta } = \sigma_ {\eta}(z)(1-\sigma_ {\eta}(z))\gamma(-z;\eta).
$$

**The gradient of loss function with respect to the deformation parameter** reads

$$
\boxed{\frac{ \partial L(y,\sigma_ {\eta}(z)) }{ \partial \eta }  =\sum_ {i\in G} \gamma(-z_ {i};\eta)  (y_ {i} -\sigma_ {\eta}(z_ {i} )),}
$$

where $G$ in $i\in G$ means that the regression is done within a certain group of shared clinical covariates, such as age, sex, etc. Note that the deformation parameter $\eta$ depends on the $G$ chose.

# Appendix. Useful Mathematical Formulae

The definition of $q$-logarithm and $q$-exponential, $x>0, q \in\mathbb{R}$:

$$
\begin{align*}
\ln_ {q}x &:= \frac{x^{1-q}-1}{1-q}, \\
e^{ x }_ {q} &:= (1+(1-q)x)^{1/(1-q)},\quad  0 \text{ if } 1+(1-q)x<0.
\end{align*}
$$

Note that in the definition of the exponential it is required that $1+(1-q)x>0$, otherwise it is defined to be zero. This is to make sure the the value of $e_ {q}$ is positive definite. It is easily checked that $\log _q$ and $\exp_ {q}$ are indeed inverse to each other. 

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
