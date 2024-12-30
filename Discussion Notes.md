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



$$
\Gamma[\phi], 
$$

$$
l = \sum_ {i} \left[ y_ {i}\ln _ {q} \left( \frac{1}{\hat{y}_ {i}} \right) + (1-y_ {i})\ln _ {q} \left( \frac{1}{1-\hat{y}_ {i} } \right) \right]
$$


Certainly! If you'd like to change qq to p^\hat{p} in the expression for the Kullback-Leibler divergence (relative entropy), the modified expression becomes:

DKL(P∥Q)=∑i=1npilog⁡(pip^i)D_{\text{KL}}(P \| \hat{P}) = \sum_{i=1}^{n} p_i \log \left( \frac{p_i}{\hat{p}_i} \right)

Where:

- PP represents the true probability distribution (often corresponding to the actual class labels).
- P^\hat{P} is the predicted probability distribution (the logistic regression model's predicted probabilities).
- pip_i is the true probability for the ii-th data point (which is typically 0 or 1 in binary classification).
- p^i\hat{p}_i is the predicted probability for the ii-th data point belonging to the positive class, given by the logistic function:

p^i=11+exp⁡(−y^i)\hat{p}_i = \frac{1}{1 + \exp(-\hat{y}_i)}

Where y^i\hat{y}_i is the linear prediction for the ii-th data point, i.e., y^i=xi⊤θ\hat{y}_i = \mathbf{x}_i^\top \mathbf{\theta}.

Thus, DKL(P∥P^)D_{\text{KL}}(P \| \hat{P}) measures the divergence between the true label distribution and the predicted probability distribution, which is commonly used in logistic regression via the cross-entropy loss.




In the context of logistic regression, relative entropy (also known as Kullback-Leibler divergence) is used to measure the difference between two probability distributions. Specifically, when comparing the predicted probabilities p^\hat{p} and the true labels pp, the relative entropy is given by:
$$
DKL(P∥Q) = \sum_{i=1}^{n} p_i \log \left( \frac{p_i}{q_i} \right)
$$

Where:

- PP is the true distribution of the labels (often represented by the actual class labels).
- QQ is the predicted distribution (the model's predicted probabilities).
- pip_i is the true probability of the ii-th data point (1 for the positive class, 0 for the negative class in binary classification).
- qiq_i is the predicted probability of the ii-th data point belonging to the positive class.

In logistic regression, the predicted probability qiq_i for a data point xix_i is given by the logistic function:

qi=11+exp⁡(−y^i)q_i = \frac{1}{1 + \exp(-\hat{y}_i)}

Where y^i\hat{y}_i is the linear combination of the features for the ii-th data point, i.e., y^i=xi⊤θ\hat{y}_i = \mathbf{x}_i^\top \mathbf{\theta}.

The relative entropy can be used in the form of the **cross-entropy loss** in logistic regression, which is a common objective function. The cross-entropy between the true labels yiy_i and the predicted probabilities y^i\hat{y}_i is given by:

L(θ)=−1n∑i=1n[yilog⁡(qi)+(1−yi)log⁡(1−qi)]L(\theta) = - \frac{1}{n} \sum_{i=1}^{n} \left[ y_i \log(q_i) + (1 - y_i) \log(1 - q_i) \right]

Where:

- yiy_i is the actual label (0 or 1) for the ii-th data point.
- qi=11+exp⁡(−y^i)q_i = \frac{1}{1 + \exp(-\hat{y}_i)} is the predicted probability for the positive class.

In this form, the cross-entropy loss can be viewed as the negative of the expected relative entropy (or Kullback-Leibler divergence) between the true label distribution and the predicted probability distribution.