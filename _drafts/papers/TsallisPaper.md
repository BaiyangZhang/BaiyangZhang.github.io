---
layout: post
title: 
date: 
author: Baiyang Zhang
catalog: true
tags:
---



Using $q$-algebra, it is straightforward to verify that the $q$-sigmoid functions of the first and second kinds are related by the relation $\sigma_q(z) = \overline{\sigma}_{1-q}(z)$. Therefore, from now on we will focus on the case where $q < 1$.
# Abstract


We introduce two kinds of Tsallis statistics-enhanced sigmoid functions, denoted $\sigma_q$ and $\bar{\sigma}$, based on $q$-deformed exponents for $q<1$, that are free of empirically chosen cutoffs. These generalizations of the classical sigmoid enables more flexible and robust fitting method in the context of classification problems, particularly when dealing with complex, non-linear dependencies in data. The $q$-deformed classifiers are applied to [data sets], demonstrating its robustness, noise resistance, and stability. In the simulated experiments, the improved algorithm outperforms traditional methods like Logistic Regression, SVM, and Random Forest, with significantly smaller standard deviation. On real cancer datasets, our method achieves substantial improvements in $F1$ and $Youden$ Index scores, particularly outperforming Logistic Regression with traditional sigmoid function by up to 14% in $F1$ and 31% in $YI$ for breast cancer data. These results demonstrates the exceptional robustness, noise resistance and stability of Tsallis statistics-enhanced method, making it a reliable solution for complex and noisy data environments.


# Discussion



In principle, different samples may be associated with distinct values of the non-extensive factor, as nonlinearity may depend on the specific value of the linear combination of input features. However, this approach takes a high risk of overfitting, which would significantly compromise the predictability of the model. Therefore, we restrict our analysis to the case where the value of $q$ is universal across all samples. A useful perspective is to treat the nonlinearity parameter on equal footing with the weight vector $\theta$, together forming the set of universal parameters of the model. Furthermore, the $q$-factor also appears in the $\beta$ function in Eq.~\eqref{eq:derivative}, and the $\beta$ function modulates the behavior of the learning rate. As a result, the nonlinear adjustment to the learning rate is also universal.


There are several potential directions to generalize our work. Beyond its application in non-linear logistic regression, our method can be directly extended to multinomial regression. Specifically, the $q$-exponentials can be incorporated into the generalized softmax function to form a $q$-deformed multi-class classifier. However, we believe that the most significant application of Tsallis statistics in the context of regression methods lies in the generalization of the entropic loss function. Cross-entropy can be seen as a measure of the additional information content gained from observation, which we aim to minimize. It is therefore logical to extend the conventional cross-entropy to Tsallis entropy, and investigate its performance across various datasets, seeking new effects that arise from the introduction of the $q$-deformation degree of freedom. This will be the focus of our future research.


improving classification performance in noisy and complex data environments.


1) to more than two discrete possible outcomes. The generalization to softmax function is straightforward. 2) Generalize the cross entropy. 