---
layout: post
title: Mean, Median and Variance
subtitle: 
date: 2024-02-27
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
  - "#biostatistics"
---

*Disclaimer: Nothing in this note is original.*
# Introduction

In life some questions are too important to be left to opinion, superstition, or conjecture. For example, which drug should a doctor prescribe to treat an illness? What factors increase the risk of an individual developing coronary heart attack? To answer these questions (even remotely), we need *objective, evidence-based* decision making method. 

**Evidence-based practice:**  Using sound research findings based on observed or collected data to make decisions.

In principle, people collect and process information every day of their lives. Since it’s something we do frequently, you might think we would be really good at it…but we’re not. We are not good at picking out patterns from a sea of noisy data. And, on the flip side, we are too good at picking out non-existent patterns from small numbers of observations.

In order to mitigate any of our own personal biases when answering important questions about the way the world works (i.e., to do good science), we must be careful to be rigorous in the way we proceed. The **scientific method** is the process used to answer scientific questions.

1. Ask the question
2. Construct a hypothesis
3. Test it with a study or an experiment
4. Analyze data and draw conclusions (wish its as simple as that)
5. Communicate results

However, collecting and analyzing data can be complicated. Statistics helps us design studies, test hypotheses, and use data to make scientifically valid conclusions about the world. In general, scientists use the scientific method to make generalizations about classes of people on the basis of their studies. The class of people that they are trying to make generalizations about is called the **population**. Most of the time, it is impractical and expensive to study all individuals in a population, Instead of sampling everyone in the population, or taking a **census**, typically we study only a portion of the population called the **sample**. In order to determine how best to obtain a sample to answer the research questions, we must be cautious about the study design. Then, researchers make **generalizations**, or **inference**, about the entire population based on studying the sample.

In this note we consider two broad categories of statistical analysis: `descriptive statistics`, which deals with methods for summarizing and/or presenting data and `inferential statistics`. 

**Descriptive statistics**: Methods for summarizing and/or presenting data.
**Inferential statistics**: Methods for making generalizations about a population using information contained in the sample.

- - -

It is difficult to sort through large streams of data and make any meaningful conclusions. Instead, we can better understand data by condensing it into human readable mediums through the use of data `summaries`, often displayed in the forms of tables and figures. However, in doing so, information is often be lost in the process. A good data summary will seek to strike a balance between clarity and completeness of information.

There are two broad types of data that we may see in the wild, which we will call `categorical data` and `continuous data`. As the name suggests, categorical data (sometimes called `qualitative` or `discrete` data) are *data that fall into distinct categories*. Categorical data can further be classified into two distinct types:

- Nominal data: data that exists without any sort of natural or apparent ordering, e.g., colors (red, green, blue), gender (male, female), and type of motor vehicle (car, truck, SUV). 
- Ordinal data: data that does have a natural ordering, e.g., education (high school, some college, college) and injury severity (low, medium, high).

`Continuous data` (sometimes called quantitative data), on the other hand, are data that can take on any numeric value on some interval or on a continuum. Examples of continuous data include height, weight, and temperature. Categorical and continuous data are summarized differently, and we’ll explore a number of ways to summarize both types of data.

Below are some terminologies.

`Absolute frequency`: The number of observations in a category 
`Rate/Relative frequency`: The number of observations in a category relative to any other quantity
`Percent/Proportion`: The number of observations per 100 
`Bar plot`: Visualization of categorical data which uses bars to represent each category, with counts or percents represented by the height of each bar 
`Stratification`: The process of partitioning data into categories prior to summarizing

- - -

The two most common ways to describe the center are with the `mean` and the `median`. We all know what the mean is. The median is another common *measure of the center of a distribution*. In particular, for a set of observations, *the median is an observed value that is both larger than half of the observations, as well as smaller than half of the observations*. 

Sometimes there lies some data that are extremely different than the rest. Take the salaries of staff of some American university, the highest paid employee is usually the football coach, and much much higher then the rest. This one high salary, which is not representative of most of the salaries collected, is known as an `outlier`. In this  particular case, the mean is highly sensitive to the presence of outliers while the *median is not*. Measures that are less sensitive to outliers are called `robust` measures. The median is a robust estimator of the center of the data.

The shape of a distribution is often characterized by its `modality` and its `skew`. The modality of a distribution *is a statement about its modes, or “peaks.”* Distributions with a single peak are called `unimodal`, whereas distributions with two peaks are call `bimodal`. `Multimodal` distributions are those with three or more peaks. The `skew` on the other hand describes *how our data relates to those peaks*. Distributions in which the data is dispersed evenly on either side of a peak are called `symmetric distributions`; otherwise, the distribution is considered skewed. The direction of the skew is towards the side in which the tail is longest.

- - -

In addition to measuring the center of the distribution, we are also interested in the spread or dispersion of the data. Two distributions could have the same mean or median without necessarily having the same shape. Perhaps the most intuitive methods of describing the dispersion of our data are those associated with `percentile-based` summaries. Formally, the $p$-th percentile is some value $V_ {p}$ such that 

1. $p\%$ of observations are $\leq V_ {p}$;
2. $1-p\%$ of observations are $\gg V_ {p}$. 

The `quartile` is made of 

$$
\begin{align*}
Q_ {1} &= 25\text{th} \text{ percentile} = 1\text{st} \text{ or lower quartile}\\
Q_ {2} &= 50\text{th} \text{ percentile} = 2\text{nd} \text{ quartile or median}\\
Q_ {3} &= 75\text{th} \text{ percentile} = 3\text{rd} \text{ or upper quartile}\\
\end{align*}
$$

A commonly used percentile-based measure of spread combining these measures is the **interquartile range (IQR)**, defined as

$$
\text{IQR} := Q_ {3} - Q_ {1}.
$$
