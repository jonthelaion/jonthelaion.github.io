---
layout: post
title: Introductory Statistics
date: 2018-11-05 19:30
description:
categories:
 - statistics
tags:
---
Statistics is the science of learning from data and involves collecting, presenting, analysing and interpreting data. The primary objective of the statistician is to obtain information about a _target population_ (all relevant subjects of interest), using a _sample_ (a manageable subset of the target population, selected to make the study feasible).

## Data Classification

Data can be classified as either categorical or numerical:
* Categorical - variables for which each observation falls into one of a number of groups.
  * Nominal - named variables with no inherent ordering (e.g. favourite colour)
  * Ordinal - grouped variables with some ordering (e.g. grade attained in unit)
  * Binary/Dichotomous - variables which can only fall into one of two groups (e.g. nominal - gender; ordinal - <20 years, >= 20 years)
* Numerical - measured variables
  * Discrete - variables that take discrete values (e.g. number of students in class)
  * Continuous - variables which can assume any value, usually within a certain range (e.g. height, weight)

## Graphing Data

The following table summarises the appropriate graphical display to be used based on the data type.

|                 | __Categorical__          | __Numerical__         |                          |
| __Categorical__ | Clustered Bar Charts     | Comparative Box Plots | Bar Charts or Pie Charts |
| __Numerical__   | Comparative Box Plots    | Scatter Plots         | Histograms               |
|                 | Bar Charts or Pie Charts | Histograms            |                          |

Graphs need:
* a title
* clearly labelled axes
* an explanatory comment
* to be clear and uncluttered

### Medians, Quartiles, Fences and Outliers

* The __median__ is the value which divides the sample in half.
* The __lower quartile (LQ)__ separates the smallest 25% of data values from the rest of the data set i.e. the lower quartile is the 25th percentile.
* The __upper quartile (UQ)__ separates the largest 25% of data values from the rest o the data set i.e. the upper quartile is the 75th percentile.
* The __interquartile range (IQR)__ is the difference between the upper and lower quartiles: `IQR = UQ - LQ`.
* The meidan and quartiles can be located using the following formula:
<br>
$$
m = n \times \frac{P}{100} \\
\text{where:} \\
m: \text{positional variable}
n: \text{sample size} \\
P: \text{percentile (median = 50; LQ = 25; UQ = 75)} \\
$$
  * If `m` is not an integer, then round up to the next whole number and this number gives you the position of the Pth percentile.
  * If `m` is an integer, then you will find the Pth percentile half way between the value in the mth position and the value in the (m+1)th position.
* Defining __fences__ allows us to determine whether the data set has any outliers (unusually large or small values). These are located at:
  * `Lower Fence = LQ - 1.5 * IQR`
  * `Upper Fence = UQ + 1.5 * IQR`
* The __whiskers__ extend from each quartile to the furthest data value __inside or on__ the corresponding fence.
* __Outliers__ are data values which are outside the fences.

## Simple Linear Regression

* The __goodness-of-fit statistic ($$r^2$$)__ is a measure of how well our data fit the least squares regression model. It measures the proportion of variation in the dependent variable that can be explained by the independent variable.
* The __correlation coefficient (r)__ is a measure of the strength and direction of the linear relation between the two numerical variables.

## Categorical Data Analysis

### One Sample z-test for a Population Proportion

If we wish to compare categorical variables, the research question will concern population proportions, rather than means.

#### General Steps

__Hypothesis:__
<br>
$$
H_0: \pi = \pi_0 \\
H_1: \pi \neq \pi_0
$$

__Assumptions:__
<br>
We need to ensure that sample proportions follow a normal distribution through checking that the Central Limit Theorem (CLT) applies. Both $$n\pi$$ and $$n(1-\pi)$$ need to be $$\geq5$$.

__Test Statistic:__


#### Example

## Chi Square ($$\chi^2$$) Goodness-of-Fit Test

When the hypothesis we wish to test involves proportions in three or more categories (e.g. left-handed/right-handed/ambidextrous) we need to use the chi square ($$\chi^2$$) goodness-of-fit test.

#### Example: Handedness

__Research Question:__
<br>
Are 80% of people right-handed, 12% left-handed and the remainder ambidextrous?

__Info:__
<br>
635 adults from various professions were sampled and their handedness recorded. 536 are predominantly right handed, 67 predominantly left handed and the remainder ambidextrous.

__Hypothesis:__
<br>
$$
H_0: \pi_R = 0.80, \pi_L = 0.12, \pi_A = 0.08 \\
H_1: \text{The proportions are not as stated in the null hypothesis.}
$$

__Assumptions:__
<br>
$$
n\pi_R = 635 * 0.80 = \\
n\pi_L = 635 * 0.12 = \\
n\pi_A = 635 * 0.08 = \\
$$
<br>
Given that all proportions >= 5, CLT applies and we can use the chi square goodness-of-fit test.

__Conclusion:__
<br>
The proportions are not as claimed by the researcher. There appears to be a lower proportion of ambidextrous people than the researcher has claimed.
