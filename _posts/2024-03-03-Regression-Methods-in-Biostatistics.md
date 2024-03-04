---
layout: post
title: "Regression Methods\rin Biostatistics"
subtitle: 
date: 2024-03-03
author: Baiyang Zhang
header-img: img/background1.jpg
catalog: true
tags:
  - biostatistics
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
The IQR is not impacted by the presence of outliers, so it is considered a robust measure of the spread of the data. So, like the median, it enjoys the quality of being a robust measure of the data.

Percentiles are also used to create another common visual representation of continuous data: the `boxplot`, also known as a `box-and-whisker plot`. A boxplot consist of the following elements: 

- A box, indicating the Interquartile Range (IQR), bounded by the values $Q_ {1}$ and $Q_ {3}$;
- The median, or $Q_ {2}$, represented by the line drawn within the box;
- The “whiskers,” extending out of the box, which can be defined in a number of ways. Commonly, the whiskers are 1.5 times the length of the IQR from either $Q_ {1}$ or $Q_ {3}$; 
- Outliers, presented as small circles or dots, and are values in the data that are not present within the bounds set by either the box or whiskers.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/img/boxPlot.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Just like histograms, boxplots can also illustrate the skew of a data. In a histogram, the skewed was named after the location of the tail and in a boxplot, this corresponds to the side with a longer whisker. Here we can see histograms and boxplots for various distributions of data.
</div>

- - -

The variance and the standard deviation are numerical summaries which quantify how spread out the distribution is around its mean. 

We have two kinds of variances: `sample variance` and `population variance`. The difference between sample variance and population variance lies in how they are calculated and what they represent in the context of statistical analysis.

**Population Variance**:

Population variance measures how much the members of a population differ from the population mean. It is denoted by $\sigma^2$. If you have a population with $N$ members and population values $x_1, x_2, ..., x_N$, the population variance $\sigma^2$ is calculated as:
  $$ \sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2 $$
  where $\mu$ is the population mean. Note that $\mu$ is not the mean of some measured data, it is supposed to be given by some theoretical model. Population variance is used when you have access to all the data points in the population.

**Sample Variance**

Sample variance measures how much the members of a sample (a subset of the population) differ from the sample mean. It is an estimator of the population variance. Sample variance is denoted by $s^2$. If you have a sample of size $n$ with values $x_1, x_2, ..., x_n$, the sample variance $s^2$ is calculated as:
  $$ s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \overline{x})^2 $$
  where $\overline{x}$ is the sample mean.
  
Key Differences:

1. **Purpose:** Population variance describes the variability within an entire population, while sample variance estimates the population variance from a subset of the population.
2. **Formula:** The population variance formula divides by $n$ (the total number of population members), whereas the sample variance formula divides by $n-1$ (one less than the sample size).
3. **Bias Correction:** The use of $n-1$ in the sample variance formula, known as Bessel's correction, corrects for the bias in the estimation of population variance from a sample.

When we calculate the variance of a sample, we typically use the sample mean $\overline{x}$ as an estimate of the true population mean. However, using the sample mean introduces a bias because it is based on the same data points that we are using to calculate the variance. This means the sum of the squared deviations $(x_i - \overline{x})^2$ tends to be smaller than it would be if we used the true population mean, leading to an underestimate of the true population variance.

To correct for this bias, we use $n-1$ in the denominator instead of $n$. This adjustment is known as Bessel's correction. The rationale behind it is that when estimating variance from a sample, we lose one degree of freedom because we have estimated the mean from the same data set. Using $n-1$ effectively compensates for this loss, making the sample variance an unbiased estimator of the true population variance.

In summary, the factor $\frac{1}{n-1}$ is used instead of $\frac{1}{n}$ to make the sample variance an unbiased estimator of the population variance, accounting for the fact that the sample mean is used in the variance calculation.

The standard deviation, denoted as $s$, is a function of variance. Recall that the mean is not a robust outlier and is highly sensitive to skew or the presence of outliers. Consequently, the variance and the standard deviation are also very sensitive.

- - -

The regression method is a statistical technique used to model and analyze the relationships between a dependent variable and one or more independent variables. The primary goal of regression is to predict the value of the dependent (or `response`) variable based on the values of the independent (or `predictor`) variables. It is widely used in various fields such as economics, finance, biological sciences, and social sciences for forecasting, estimating, and determining causal relationships.

There are several types of regression methods, each suited to different types of data and relationships:

1. **Linear Regression**: The simplest form of regression, linear regression uses a linear approach to model the relationship between the dependent variable and one or more independent variables. The model assumes that the relationship can be described by a straight line in the form $y = \beta_0 + \beta_1x_1 + \epsilon$, where $y$ is the dependent variable, $x_1$ is the independent variable, $\beta_0$ is the y-intercept, $\beta_1$ is the slope of the line, and $\epsilon$ represents the error term.

2. **Multiple Linear Regression**: An extension of simple linear regression, this method involves two or more independent variables. The model is expressed as $y = \beta_0 + \beta_1x_1 + \beta_2x_2 + ... + \beta_nx_n + \epsilon$, where $x_1, x_2, ..., x_n$ are the independent variables.

3. **Logistic Regression**: Used when the dependent variable is categorical, typically binary. Logistic regression models the probability that the dependent variable belongs to a particular category, using a logistic function.

4. **Polynomial Regression**: A form of regression where the relationship between the independent variable and the dependent variable is modeled as an nth degree polynomial. Polynomial regression fits a nonlinear relationship between the value of x and the corresponding conditional mean of y.

5. **Ridge and Lasso Regression**: These are types of linear regression that include regularization. Regularization adds a penalty on the size of coefficients to prevent overfitting. Ridge regression adds a squared magnitude of the coefficient as a penalty term to the loss function, while Lasso regression adds the absolute value of the magnitude of the coefficient as a penalty term.

6. **Non-linear Regression**: Used when the data cannot be modeled using linear methods due to a non-linear relationship between the dependent and independent variables. Non-linear regression can fit complex curves to data.

Regression analysis involves selecting the appropriate model for the data, estimating the model parameters (usually through methods like least squares), evaluating the model's adequacy (checking for goodness-of-fit, residuals, etc.), and interpreting the results to make inferences or predictions.

In practice, the choice of regression method depends on the nature of the dependent variable, the shape of the relationship, and the distribution of the residuals, among other factors. Proper model selection, diagnostic testing, and validation are crucial steps in ensuring that the regression model provides reliable and accurate predictions or insights.

# Basic Statistical Methods

## t-Test and ANOVA (Analysis of Variance)

My time is really limited here so I'll direct jump to a short review of some mostly commonly used statistical methods. 

The basic $t$-test is used to compare two independent samples. The t-statistic on which the test is based is the difference between the two sample averages, divided by the standard error of that difference. The t-test is designed to work in small samples, whereas Z-tests are not. 

- - -

Below is the gist of the derivation of the t-distribution. Assume we have a population that follows a normal distribution with mean $\mu$ and standard deviation $\sigma$. We take a random sample of size $n$ from this population, and we calculate the sample mean $\bar{x}$. The sample mean $\bar{x}$ is also normally distributed (due to the Central Limit Theorem) with mean $\mu$ and standard deviation $\sigma / \sqrt{n}$. We standardize $\bar{x}$ to transform it into a standard normal variable $Z$:

$$
Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}
$$

In practice, $\sigma$ (the population standard deviation) is often unknown and must be estimated from the sample. We use the sample standard deviation $s$ as an estimate for $\sigma$, where $s$ is calculated from the sample data. We replace $\sigma$ with $s$ in the standardization formula, but this introduces additional variability because $s$ is an estimate:

$$
T = \frac{\bar{x} - \mu}{s / \sqrt{n}}
$$

This ratio $T$ does **not** follow a standard normal distribution anymore due to the uncertainty introduced by using $s$ instead of $\sigma$. Instead, the variable $T$ follows a distribution that is similar to the normal distribution but with heavier tails. This is the t-distribution. *The exact shape of the t-distribution depends on the sample size $n$ through the degrees of freedom, which is $n - 1$ in this context*. The degrees of freedom account for the additional uncertainty introduced by estimating the population standard deviation. 

The t-distribution is formally defined through its probability density function (pdf), which is more complex than that of the normal distribution and involves the Gamma function. The pdf of the t-distribution for a given $t$ value and $v$ degrees of freedom (where $v = n - 1$) is given by:

$$
f(t; v) = \frac{\Gamma((v+1)/2)}{\sqrt{v\pi}\Gamma(v/2)} \left(1 + \frac{t^2}{v} \right)^{-(v+1)/2}
$$

where $\Gamma$ is the Gamma function, a generalization of the factorial function to complex numbers.

In short, remember the following:

- The t-distribution accounts for the additional uncertainty in estimating the population mean when the population standard deviation is unknown and the sample size is small.
- As the sample size increases, the t-distribution approaches the standard normal distribution because the estimate $s$ becomes more accurate, reducing the extra uncertainty.

- - -

In the context of the t-test and statistical hypothesis testing, "significance" refers to the degree to which the test results allow us to reject the null hypothesis. The null hypothesis typically proposes that there is no effect or no difference between groups or conditions. When we say a result is "statistically significant," it means that the observed data are unlikely to have occurred under the null hypothesis, suggesting that there is a real effect or difference.

The significance level, denoted as $\alpha$, is a threshold set by the researcher before conducting the test, which defines the probability of rejecting the null hypothesis when it is actually true (a type I error). Common values for $\alpha$ are 0.05, 0.01, and 0.10, with 0.05 being the most widely used. Setting $\alpha$ at 0.05 means that there is a 5% risk of concluding that a difference exists when there is no actual difference.

The p-value is a key metric derived from the t-test that indicates the probability of observing the test results, or more extreme results, if the null hypothesis were true. A p-value that is less than or equal to the significance level ($p \leq \alpha$) indicates that the observed data are unlikely under the null hypothesis, leading to the rejection of the null hypothesis. In simpler terms, a low p-value (typically ≤ 0.05) suggests that the evidence against the null hypothesis is strong enough to consider the results statistically significant.

**Interpretation of Significance**

- **Statistically Significant**: If the test result is statistically significant, it suggests that the evidence is strong enough to reject the null hypothesis. This typically means there is a meaningful difference between the groups being compared, which is not likely to have occurred by chance.

- **Not Statistically Significant**: If the result is not statistically significant, it suggests that the evidence is not strong enough to reject the null hypothesis. This could mean that there is no meaningful difference between the groups, or that the study did not have enough power (e.g., sample size was too small) to detect a difference if one exists.

It's important to note that *statistical significance does not necessarily imply practical or clinical significance*. A result can be statistically significant but still be of little practical value if the observed effect or difference is too small to be of interest or use in a practical context.

- - -

### Two-sided Hypothesis Test

In biostatistics, the two-sided t-test (also known as the two-tailed t-test) is commonly used to determine whether there is a significant difference between the means of two groups, *without specifying the direction of the difference*. This type of test is employed when the research question is concerned with whether there is any difference at all, rather than predicting which group will have a higher or lower mean.

Biostatistics often involves comparing biological measurements or outcomes across different groups. For instance, one might compare the efficacy of two different medications, the impact of a treatment versus a placebo, or physiological measurements (like blood pressure) between two groups with different dietary habits. In these cases, researchers might not have a strong hypothesis about which group will have higher or lower means, or they may wish to test for the possibility of a difference in either direction. The two-sided t-test is ideal for these scenarios because it allows for the detection of significant differences regardless of their direction.

The formula for the t-statistic in a two-sided t-test is similar to that of a one-sided t-test, but the *interpretation of the p-value and the critical value from the t-distribution is different*.

For an independent two-sample t-test, the formula for the t-statistic remains:

$$ t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{s^2 \left(\frac{1}{n_1} + \frac{1}{n_2}\right)}} $$

However, in a two-sided t-test, you're interested in differences in both directions, so you consider both tails of the distribution when determining the critical t-value or when interpreting the p-value.

The hypotheses for a two-sided t-test are formulated as follows:

- Null Hypothesis ($H_0$): There is no difference between the group means ($\mu_1 = \mu_2$).
- Alternative Hypothesis ($H_a$): There is a difference between the group means ($\mu_1 \neq \mu_2$).

In a two-sided t-test, the p-value represents the probability of observing a test statistic as extreme as, or more extreme than, the one observed, in either direction, assuming the null hypothesis is true. If this p-value is less than or equal to the chosen significance level ($\alpha$), the null hypothesis is rejected, indicating a statistically significant difference between the two group means.

A significant result in a two-sided t-test suggests that there is enough evidence to conclude that a difference exists between the two group means, but it does not indicate which group has the higher mean. This approach is particularly useful in biostatistics, where establishing the existence of a difference can be crucial for further research, clinical decisions, or policy-making, even before the direction of the difference is fully understood.

- - -

Suppose that we need to compare sample averages across the arms of a clinical trial with multiple treatments, or more generally across more than two independent samples. For this purpose, one-way analysis of variance (ANOVA) and the F-test take the place of the t-test. F-test technique extends the t-test, which compares only two means, by allowing comparisons among multiple groups simultaneously, thus providing a holistic view of the data.

In the context of $F$-test, the *null hypothesis is that the mean values of the outcomes from all the populations sampled from are the same*, against the alternative that the means differ in at least two of the samples. 


The F-test is based on the F-distribution and uses an F-statistic to test the null hypothesis. *The test essentially compares the variance between the groups to the variance within the groups*; a higher ratio suggests that the group means differ significantly.

Key Concepts of One-Way ANOVA are

- `Between-Group Variability`: Differences among the group means, which reflect the effect of the independent variable.
- `Within-Group Variability`: Variations within each group, attributed to random error or individual differences not due to the treatment effect.
- `F-Statistic`: A ratio of the between-group variability to the within-group variability. A larger F-statistic indicates a greater likelihood that significant differences exist among the group means.

F-test assumes that:

1. **Independence of Observations:** The data in different groups should be independent of each other.
2. **Normality:** The distribution of the residuals (errors) should be approximately normally distributed for each group.
3. **Homogeneity of Variances:** The variances among the groups should be approximately equal.

Imagine a researcher wants to investigate the effect of different teaching methods on student performance. The researcher divides a group of 90 students into three equal groups, each subjected to a different teaching method: Method A (traditional), Method B (interactive), and Method C (technology-assisted). After a semester, the researcher measures the performance of each student on a standardized test.

The research question is: "Do the three teaching methods result in different student performance levels?"

To address this question using one-way ANOVA, the researcher would:

1. **Calculate the group means:** Find the average performance score for students in each teaching method group.
2. **Compute the ANOVA statistics:** Determine the between-group and within-group variances and calculate the F-statistic.
3. **Compare the F-statistic to a critical value from the F-distribution:** The critical value depends on the level of significance (usually set at 0.05) and the degrees of freedom for the numerator (between-groups, $k - 1$, where $k$ is the number of groups) and the denominator (within-groups, $N - k$, where $N$ is the total number of observations).

If the computed F-statistic is greater than the critical value, the null hypothesis is rejected, suggesting that there is a significant difference in student performance across at least two of the teaching methods. The researcher might then conduct post-hoc tests to identify specifically which groups differ from each other.

- - -

### Robustness 

We have assumed normal distribution for the distribution of random variables. However, both the t-test and the F-test are pretty robust to violations of the normality assumption, especially in large samples, similar to the central limit theorem. *By robust we mean that the type-I error rate, which is the mistake of rejecting the null hypothesis when it actually holds, is not seriously affected.* They are, however, primarily sensitive to outliers, which will mess up the variation. 