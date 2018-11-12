---
layout: post
title: Introductory Statistics
date: 2018-11-05 19:30
description:
categories:
 - statistics
tags:
---
__Statistics__ is the science of learning from data and involves collecting, presenting, analysing and interpreting data. The primary objective of the statistician is to obtain information about a _target population_ (all relevant subjects of interest), using a _sample_ (a manageable subset of the target population, selected to make the study feasible).

## Data Classification

Data can be classified as either categorical or numerical:
* Categorical - variables for which each observation falls into one of a number of groups.
  * Nominal - named variables with no inherent ordering (e.g. favourite colour - red, green, blue)
  * Ordinal - grouped variables with some ordering (e.g. grade attained in unit - A, B, C)
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
* The median and quartiles can be located using the following formula:
<br>
$$
m = n \times \frac{P}{100} \\
\text{where:} \\
m: \text{positional variable} \\
n: \text{sample size} \\
P: \text{percentile (median = 50; LQ = 25; UQ = 75)} \\
$$
  * If `m` is not an integer, then round up to the next whole number and this number gives you the position of the Pth percentile.
  * If `m` is an integer, then you will find the Pth percentile half way between the value in the mth position and the value in the (m+1)st position.
* Defining __fences__ allows us to determine whether the data set has any outliers (unusually large or small values). These are located at:
  * `Lower Fence = LQ - 1.5 * IQR`
  * `Upper Fence = UQ + 1.5 * IQR`
* The __whiskers__ extend from each quartile to the furthest data value __inside or on__ the corresponding fence.
* __Outliers__ are data values which are outside the fences.

## Population Distributions

* A __measure of centre__ tells us where we can find the 'middle' of the data - that is, roughly, the 'middle' of the histogram.
* A __measure of spread__ tells us how spread out the histogram is.
* These measures don't tell us about the __shape__ of the data however.
* A __distribution__ is determined by the centre, spread and shape of the histogram of numerical data. In the case of a _continuous population distribution_, we represent it as a smooth curve rather than a histogram as our population distribution is often  theoretical model with an infinite number of observations.
* Some common population distributions include:
![](http://www.math.montana.edu/hayes/powerpoint-lectures/l1/images/v3_master31_image062.gif)
__Source:__ [Montana State University](http://www.math.montana.edu/hayes/powerpoint-lectures/l1/32.html)
* Examples include:
  * Uniform distribution: last two digits of 50 telephone numbers
  * Normal distribution: heights of daffodils; GPAs of students
  * Multimodal: speed of wind
  * U-shaped: daily hours of sunshine
  * Left skewed: marks on an easy test
  * Right skewed: salaries of workers
  * Zero component + right skewed: workers' income taxes

## Summarising Numerical Data

* Statistical studies are concerned with using samples to learn about the population from which they have been drawn.
* Sample statistics are calculated to estimate population parameters.
* We expect histograms of large samples to more closely resemble the parent population distribution than histograms of small samples.

### Measures of Centre

* The __median__ is a measure of the centre of a set of numerical data defined on an interval. It is the middle value or the average of the middle two values, if the sample size n is even) of a data set which has been sorted.
* The __mean__ is another measure of centre. It is defined as the arithmetic average.
* Both the median and the mean summarise numerical data, using a single value to give an indication of the overall location of the measurements. They are not the same unless the distribution is symmetric. The median is not as sensitive to outliers as the mean, so it is a more robust measure of centre than the mean (less easily influenced by outliers).

| Measure | Sample Statistic | Population Parameter |
| Median  | $$\tilde{y}$$    | $$\tilde{\mu}$$      |
| Mean    | $$\bar{y}$$      | $$\mu$$              |

### Measures of Spread

* The __interquartile range__ is the difference between the upper and lower quartiles. It therefore gives the range of the middle 50% of a set of data.
* The __range__ is the difference between the maximum value and the minimum value in the data. Unlike the IQR, this will be influenced by large or small outliers in the data.
* The __standard deviation__ is another measure of spread. it is defined in terms of the deviation of the data (called residuals) from the mean and gives a measure of how much the data is spread out around the mean. It is the square root of the average squared residual.
<br>
$$
Residual = y_i - \bar{y} = \text{observed value - sample mean} \\
s = \sqrt{\frac{(y_1-\bar{y})^2+(y_2-\bar{y})^2+...+(y_n-\bar{y})^2}{n-1}} \\
$$
* The IQR, like the median, is a more robust measure of spread than the range or standard deviation.

| Measure            | Sample Statistic | Population Parameter |
| Standard Deviation | $$s$$            | $$\sigma$$           |
| Variance           | $$s^2$$          | $$\sigma^2$$         |

## Summarising Categorical Data

* To summarise a categorical variable, construct a table showing:
  * the variable name;
  * the name of each category;
  * the count;
  * proportion and/or percentage of observations in each category; and
  * total sample size

## The Normal Distribution

* A __probability__ is a measure of the expectation that an event will occur and lies between 0 nd 1.
* The __normal distribution__ is a symmetric "bell shaped" distribution with an unlimited range. It is described by two parameters:
  * $$\mu$$ (a measure of centre), which determines the "bell's" position along the horizontal axis; and
  * $$\sigma$$ (a measure of spread), which determines the height and width of the "bell"
* The __standard normal distribution__ is a special kind of normal distribution with a mean of 0 and standard deviation of 1.
![](https://www.statisticshowto.datasciencecentral.com/wp-content/uploads/2013/09/standard-normal-distribution.jpg)
__Source:__ University of Virginia via Data Science Central
* In any normal distribution:
  * 68.3% of the values lie within one standard deviation of the mean;
  * 95.4% of the values lie within two standard deviations of the mean;
  * 99.7% of the values lie within three standard deviations of the mean.
* A __z-score__ is the number of standard deviations that a value, y, is away from its population mean, $$\mu$$.
  * If the y value is greater than the mean ($$y > \mu$$), then the z-score is positive.
  * If the y value is less than the mean ($$y < \mu$$), then the z-score is negative.
<br>
$$
z = \frac{y - \mu}{\sigma} \\
$$
* Common questions to solve include:
  * Proportion probability problems (e.g. what proportion of population has IQ greater than 130?)
  * Calculating y value from a given z-score, area or percentile

## Sampling Distributions

* As the number of samples taken increases, the shape becomes more "normal", the mean remains the same and the standard deviation decreases.
* The standard error ($$se_\bar{y}$$ or $$\sigma_\bar{y}$$) can be thought of as the standard deviation of the samples.
* The standard error decreases at a rate of $$\frac{\sigma}{\sqrt{n}}$$ so it requires a quadrupling of the sample size to double the accuracy.
* These characteristics are also found in populations which are not symmetric or normal.

### Central Limit Theorem

* The __Central Limit Theorem__ states that: _If we take random samples of the same size n from  population which is not normally distributed, then the sample means will follow a normal distribution provided n, the sample size, is large enough._
* If the original population is not too far from normal, an n of 25 will be 'large enough' to assume an approximate normal distribution for sample means.
* If the original population is a normal distribution, then sample means will follow an exact normal distribution regardless of sample size.
* Examination of a histogram could be useful to determine how far the population is from normal.
* To find the z-score of sample means:
<br>
$$
\text{Sample Means: } z = \frac{\bar{y} - \mu}{\frac{\sigma}{\sqrt{n}}} \\
$$

### Sample Proportions

* The Central Limit Theorem also applies to sample proportions.
* $$\pi$$ is the population proportion and p represents the sample proportion.
* In the context of sample proportions, n is large enough if: $$n\pi >= 5 \text{ and } n(1-\pi) >= 5 \\ $$
* The standard error of sample proportions is:
<br>
$$
\sigma_p = se_p = \sqrt{\frac{\pi(1-\pi)}{n}} \\
$$
* To find the z-score of sample proportions:
<br>
$$
\text{Sample Proportions: } z = \frac{p - \pi}{\sqrt{\frac{\pi(1-\pi)}{n}}}
$$

## Confidence Intervals

* Confidence intervals represent an estimate of a range of believable values and associated confidence of the estimate.
* There are three different ways of calculating confidence intervals depending on what information is available:
  * Confidence interval for a population mean $$\mu$$ where $$\sigma$$ is known.
  * Confidence interval for a population mean $$\mu$$ where $$\sigma$$ is unknown.
  * Confidence interval for a population proportion $$\pi$$.
* For CI to give valid estimates, the following conditions must apply:
  * The measurements recorded must be independent of each other.
  * The sample mean is from a normal distribution (e.g. rely on CLT, examine the histogram etc)
* CI allow us to draw conclusions about the population mean (not the sample mean as this is known).

### CI where population standard deviation is known

* In real life, this rarely happens as it is unlikely that you will know the population standard deviation, but not the population mean.

$$
\text{95% CI for } \mu \text{: } (\bar{y} - 1.96 \times \frac{\sigma}{\sqrt{n}}, \bar{y} + 1.96 \times \frac{\sigma}{\sqrt{n}}) \\
$$

### CI where population standard deviation is unknown

* When the population standard deviation is unknown, we cannot use the z-distribution and have to use the (student's) t-distribution instead.

$$
\text{95% CI for } \mu \text{: } (\bar{y} - t_\text{crit} \times \frac{s}{\sqrt{n}}, \bar{y} + t_\text{crit} \times \frac{s}{\sqrt{n}}) \\
$$

* Heavier tailed than the standard normal distribution, the t-distribution has an extra parameter, $$\nu$$, the degrees of freedom (df) which depends on the sample size: $$\nu = n - 1$$.
* As $$\nu \to \infty$$ the t-distribution approaches the normal distribution.
* Where $$\nu$$ is in between two values in the t-table (e.g. 75 being in between 70 and 80), take the lower one to be conservative.

### CI for a population proportion

$$
\text{95% CI for } \pi \text{: } (p - 1.96 \times \sqrt{\frac{p(1-p)}{n}}, p + 1.96 \times \sqrt{\frac{p(1-p)}{n}}) \\
$$

## Study Design and Review

* The general study design process involves:
  * Formulating the question of interest
  * Specifying a target population
    * The target population should be well defined.
  * Determining the measurements to be collected (the variables)
    * Ideally, the observations should be independent of each other.
    * Variables can be classified as:
      * Outcomes (responses) or
      * Determinants (may influence responses)
  * Defining the method of data collection
    * The sample should be representative of the target population (not biased), and large enough to give accurate information about the population.
    * One way to ensure that a sample is representative of the target population is to obtain a random sample.
    * A simple random sample, of a given size n, is one in which each set of that size has the same change of being selected from the target population. However, it is often difficult, or even impossible, to obtain a simple random sample (e.g. tuna fishing in different parts of the world).
    * A random sample is one where each member of the population has the same chance of being selected.
    * A representative sample should have characteristics which represent those of the target population without bias.
* Types of studies can be split into:
  * Deductive (non-empirical studies)
  * Inductive (empirical studies - involves collecting data)
    * Qualitative (unstructured)
    * Quantitative (structured)
      * Observational - no intervention by the investigator nor is there any treatment imposed.
        * Example: Study of association between use of mobile phones and eye cancer. 118 subjects with the eye cancer were compared to 475 subjects who did not have the eye cancer. Subjects with eye cancer had significantly higher mobile phone use.
        * Example: A researcher takes blood samples from students to measure blood alcohol levels during Monday morning lectures in Week 1 of semester.
      * Experimental - investigator has some control over the determinant.
        * Example: 22,071 male physicians between the ages of 40 and 84 were randomly assigned into one of two groups taking either aspirin or a placebo. In a follow up, heart attack rates were compared in the two groups.
        * Example: A researcher randomly assigns law students into two groups. Members of one group are all given an alcoholic drink. Each student is asked to argue on a topic and the quality of their arguments are rated. Ratings are compared for the two groups.
* __Bias__ may be defined as any systematic error (i.e. not occurring randomly) which results in an incorrect estimate of a parameter or an incorrect association between variables in a study. These include:
  * __Selection bias:__ refers to any systematic differences in the way that subjects are selected for a study (e.g. to estimate the proportion of 18 to 25 year old in Australia who have private health insurance. If we select a sample from a student database could produce a biased result, since the proportion of students with private health insurance may differ from the proportion of other young adults with private health insurance)
  * __Measurement bias:__ refers to systematic differences in the measurement of variables (e.g. in a comparison of flu rates among people with and without chronic illnesses, the responses for people with chronic illnesses may be more accurate as their past illnesses may be better documented and/or recalled)
  * __Response bias:__ can occur when the response rate is too low (e.g. responding to postal survey). Ideally, the response rate should be at least 75% to ensure that a study is not significantly affected by response bias.
* A __confounder__ is a variable that distorts the apparent effect of one variable (determinant) on another (outcome). For example, an increase in ice-cream sales seems to be associated with an increase in drownings, but it is confounded by the fact that higher temperature results in more people going to the beach and buying ice-cream.

### Sample Size

* A sample needs to be sufficiently large to give an accurate representation of the target population.
* The accuracy of a sample for determining a population characteristic depends on two factors:
  * the sample size (n) used for the study
  * the variability (spread) of the measurements - a small sample may be sufficient when the population is homogenous (i.e. where it doesn't vary much)
* The accuracy of a sample does not depend on the population size.
* The sample size needed depends on the kind of data which are of interest:
  * For a __proportion__: most opinion polls are based on surveys of at least 500 persons. We need this number to ensure a reasonable degree of accuracy.
  * For a __mean__: smaller samples are often sufficient for estimating characteristics of populations of numerical (measured) data.

## Hypothesis Testing

* Hypothesis testing is the process of determining the probability that a given hypothesis is true.

### General steps in Hypothesis Testing

* __Hypothesis:__ State the null and alternative hypotheses in terms of the parameter of interest.
* __Assumptions:__ Check the underlying assumptions of the test.
* __Test Statistic:__ Calculate the test statistic.
* __P-Value:__ Obtain the p-value for the test from the distribution of the test statistic.
  * Note that when looking up the area in the z-table, the area value will need to be doubled if it is a two-tailed hypothesis test.
  * Note that the z-test is used where the population standard deviation is known and the t-test where it is unknown.
* __Decision:__ If the p-value is less than 0.05 (the significance level), reject the null hypothesis. If the p-value is not less than 0.05, do not reject the null hypothesis.
* __Conclusion:__ Write a conclusion to the original research question in terms of the target population.

### Example: Stopping Distances using Z-Test

__Research Question:__ Is the average stopping distance of school buses travelling at 75km/h equal to 80m as claimed by public transport authorities? The standard deviation of stopping distances at that speed is known to be 1.2m. Automotive engineers tested a randomly selected sample of 20 school buses and found that the average stopping distance for this sample, when travelling at 75 km/h, was 80.74m.

__Hypothesis:__
<br>
$$
H_0: \mu = 80 \\
H_1: \mu \neq 80 \\
$$

__Assumptions:__
<br>
From the histogram, the normality assumption appears reasonable: the sample appears to be drawn from a normally distributed population.

__Test Statistic:__
<br>
$$
z = \frac{\bar{y} - \mu}{\frac{\sigma}{\sqrt{n}}} = \frac{80.74-80}{\frac{1.2}{\sqrt{20}}} = 2.76 \\
$$

__P-Value:__<br>
P-Value = 0.0029 x 2 = 0.0058

__Decision:__<br>
Since p-value < 0.05, reject $$H_0$$.

__Conclusion:__<br>
There is evidence to suggest that the average stopping distance for all school buses is more than 80m.

### Example: CI view of Hypothesis Tests

* A CI can be used to test a null hypothesis: if the CI does not include the null value, the decision is to reject the null hypothesis; and if the CI does include the nul value, the decision is to not reject the null hypothesis.
* For the stopping distances example examined above:
<br>
$$
\text{95% CI for } \mu \text{: } (80.74 - 1.96 \times \frac{1.2}{\sqrt{20}}, 80.74 + 1.96 \times \frac{1.2}{\sqrt{20}}) = (80.2, 81.3)\\
$$
* The null hypothesis is rejected as 80m does not lie between the 95% CI of (80.2m, 81.3m).

### Example: Newspaper Recycling using T-Test

__Research Question:__ Is the average weekly weight of recycle newspaper equal to 0.91kg per household, on average? A random sample of 148 households in the are found that the average weight of the households sampled was 0.989kg with a sample standard deviation of 0.445kg.

__Hypothesis:__<br>
$$
H_0: \mu = 0.91 \\
H_1: \mu \neq 0.91 \\
$$

__Assumptions:__<br>
From the histogram and a sample size of 148, CLT will apply and the normality assumption appears reasonable: the sample appears to be drawn from a normally distributed population.
<br>

__Test Statistic:__<br>
$$
t = \frac{\bar{y} - \mu}{\frac{\sigma}{\sqrt{n}}} = \frac{0.989-0.91}{\frac{0.445}{\sqrt{148}}} = 2.16 \text{ with 147 df} \\
$$

__P-Value:__<br>
0.02 < p-value < 0.05

__Decision:__<br>
Since p-value < 0.05, reject $$H_0$$

__Conclusion:__<br>
There is evidence to suggest that the average weekly weight of recycled newspaper is more than 0.091kg per household.

## Comparing Population Means

### Paired T-Test

* A __paired t-test__ (i.e. a one sample t-test on the difference between pairs) is used to compare the average scores for two sets of matched measurements recorded on a target population. The test assumption is that the differences between the pairs are drawn from a normal population. An example is the before and after weight of one sample of participants who were part of a weight loss program.
* The null and alternative hypotheses for paired t-test are:<br>
$$
H_0: \mu_d = 0 \\
H_1: \mu_d \neq 0 \\
$$
* The test statistic for paired t-test is:<br>
$$
t = \frac{\bar{y} - \mu}{\frac{\sigma}{\sqrt{n}}} \\
\text{with n-1 degrees of freedom, where n is the number of differences} \\
\text{where } \bar{y}_d \text{ is the mean of the differences (calculated from the sample of differences) and } s_d \text{ is the standard deviation of the sample of differences.} \\
$$
* The 95% CI will be based on differences as well.

### Two Sample T-Test

* A __two sample t-test__ is used to compare the average scores in two independent populations. The assumptions are that both samples are drawn from the normal populations and that the two populations have the same standard deviation. It is used where there is no meaningful way to match up subjects in two samples drawn from independent populations. This allows for testing of whether there is a significant difference between two samples if the number of observations from each sample is different as well.
* The null and alternative hypothesis for two sample t-test are:<br>
$$
H_0: \mu_1 = \mu_2 \\
H_1: \mu_1 \neq \mu_2 \\
$$
* The assumptions are:
  * Both samples are drawn from normal distributions; and
  * Both samples are drawn from populations with equal spread (i.e. assume $$\sigma_1 = \sigma_2$$)
* The test statistic is:<br>
$$
t = \frac{\bar{y}_1 - \bar{y}_2}{s_p\sqrt{\frac{1}{n_1} + \frac{1}{n_2}}} \\
\text{with df = } n_1 + n_2 - 2 \\
\text{and where } s_p \text{ is the pooled standard deviation.} \\
$$
* The __pooled standard deviation__ is a weighted average of the two sample standard deviations. We use this because we are assuming the two samples are from populations with the same standard deviation i.e. we assume $$\sigma_1 = \sigma_2$$:<br>
$$
s_p = \sqrt{\frac{s_1^2(n_1 - 1) + s_2^2(n_2 - 1)}{n_1 + n_2 - 2}}
$$
* The 95% CI to estimate the aerage difference between two populations is given by:<br>
$$
\text{95% CI for } \mu_1 - \mu_2 = (\bar{y}_1 - \bar{y}_2) \pm t_\text{crit} \times s_p\sqrt{\frac{1}{n_1} + \frac{1}{n_2}}
$$

## Simple Linear Regression

* A scatter plot can be used to visualise associations between two variables.
* The y variable is usually the outcome/response variable while the x variable is the predictor/determinant variable.
* Remember that causation does not equal correlation.

### The Least Squares Regression Line

* Linear regression is the process of fitting the best straight line to summarise the relation between two numerical variables.
* Regression Line: $$\hat{y} = a + bx$$
* The least squares regression line is the line that makes the total squared residual distances as small as possible.
* The residuals are the distances between the points and the line. They are obtained by subtracting the predicted values from the responses. Residual = $$y_i - \hat{y}_i$$
* The best line will be the line which has the:
  * Sum of its squared residuals as a minimum: $$\Sigma_i(y_i - \hat{y}_i)^2$$ ; and
  * Sum of its residuals equal to zero: $$\Sigma_i(y_i - \hat{y}_i) = 0$$
* Assumptions for a linear model:
  * The relation in the population is linear.
    * To check this, look at the scatter plot to see whether a linear model is a sensible model for the data.
    * The scatter plot should indicate whether a linear model is appropriate and may also indicate whether there are other problems with the model.
    * Outliers may have an 'undue influence' on the regression line.
    * Clustering, or 'groups of points', may be some reason for fitting separate models for different groups.
  * The residuals (errors) are drawn from a normal distribution.
    * To check this, look at the histogram of the residuals which can be obtained from Minitab.
  * The residuals (errors) in y (i.e. the deviations from the line in the y direction) have a constant standard deviation.
    * To check this, look at a plot of the residuals showing the spread of the residuals round zero. Minitab calls this plot 'Residuals vs fits' and plots the residuals against the fitted values (i.e. the predicted values). If the residuals have a constant standard deviation, the spread of the residuals around zero (the horizontal line in the plot) will be constant across the range of the predicted values.

| Measure         | Sample Statistic     | Population Parameter     |
| Linear Equation | $$\hat{y} = a + bx$$ | $$Y = \alpha + \beta X$$ |
| Slope           | $$b$$                | $$\beta$$                |

### Hypothesis Testing for a Linear Relation

* The test statistic is given by:<br>
$$
t = \frac{b}{se_b}
$$
* Remember to state conclusions in terms of the population, not the sample.

__Hypothesis:__<br>
$$
H_0: \beta = 0 \\
H_1: \beta \neq 0 \\
$$

__Assumptions:__<br>
The scatter plot indicates the relation may be linear in the population. The histogram indicates the residuals could be from a normal distribution. The residuals vs fits plot indicates the residuals could have a constant standard deviation.

__Test Statistic:__<br>
$$
t = \frac{b}{se_b} = \frac{-1.31}{0.1276} = -10.23 \text{, with n - 2 = 28 df}
$$

__P-Value:__<br>
p-value approximately 0

__Decision:__<br>
Since p-value < 0.05, reject $$H_0$$

__Conclusion:__<br>
There is evidence of a negative linear relation between the price and age of used Toyota Corollas. For each extra year in age, price decrease by $1310, on average.

### 95% CI for Linear Relations

* The 95% CI for linear relations is given by:<br>
$$
\text{95% CI for } \beta = b \pm t_\text{crit} \times se_b \\
\text{where n - 2 df is used for } t_\text{crit} \\
$$

### Making valid predictions

* A statistically significant relation must exist (i.e. $$H_0: \beta = 0$$ has been rejected)
* Any prediction that we make must be within the range of the x-values we used to obtain the regression line.
* Model will only give valid predictions when we predict Y (the outcome) from X (the determinant). We cannot use the model to predict X from Y.

### Goodness-of-fit statistic

* The __goodness-of-fit statistic ($$r^2$$)__ is a measure of how well our data fit the least squares regression model. It measures the proportion of variation in the dependent variable that can be explained by the independent variable.
* The __correlation coefficient (r)__ is a measure of the strength and direction of the linear relation between the two numerical variables. The value of `r` always lies between -1 and 1. To calculate this, take the goodness-of-fit statistic, square it and then take the same sign as `b`.
* $$R^2$$ is usually represented as a percentage; and $$r$$ as a decimal.

## Categorical Data Analysis

### Comparing Two Categorical Variables

If we wish to compare categorical variables, the research question will concern population proportions, rather than means.

__Hypothesis:__<br>
$$
H_0: \pi = \pi_0 \\
H_1: \pi \neq \pi_0
$$

__Assumptions:__<br>
We need to ensure that sample proportions follow a normal distribution through checking that the Central Limit Theorem (CLT) applies. Both $$n\pi$$ and $$n(1-\pi)$$ need to be $$\geq5$$.

__Test Statistic:__<br>
For this test, we use:
<br>
$$
z = \frac{p-\pi}{\sqrt{\frac{\pi(1-\pi)}{n}}}
$$
<br> where `p` is the sample proportion.

__p-value:__<br>
We obtain the p-value from the two tails of the z distribution.
Note: We need to include both tails and usually this will involve doubling the p-value provided from the table directly.

__Decision:__<br>
We will continue to use  significance level of $$\alpha=0.05$$. We will only reject $$H_0$$ when the p-value is <0.05. When the p-value is >= 0.05, we do not reject $$H_0$$.

### Example: Handedness with two outcomes

__Research Question:__<br>
Is the proportion of artists who are left-handed any different to the proportion of left-handers in the general population? 150 artists were sampled and 18 were found to be left-handed. It is generally claimed that the proportion of left handers in the general population is 10%.

__Hypothesis Test:__<br>
$$
H_0: \pi = 0.1 \\
H_1: \pi \neq 0.1 \\
$$
Check assumptions:

Check test statistic:
<br>
$$
z = \frac{p-\pi}{\sqrt{\frac{\pi(1-\pi)}{n}}} = \frac{p-0.1}{\sqrt{\frac{0.1(1-0.1)}{150}}} = 0.82
$$

p-value = 2 x 0.2061 = 0.4122

Since the p-value is >= 0.05, we do not reject $$H_0$$.

10% of all artists could be left handed. We do not have enough evidence to suggest that the proportion of left handers is different among artists than among the general population.

95% CI is the same as sample proportion.

$$
\text{95% CI for } \pi \text{: } (p - 1.96 \times \sqrt{\frac{p(1-p)}{n}}, p + 1.96 \times \sqrt{\frac{p(1-p)}{n}}) \\
$$

Because p is used instead of $$\pi$$, there is a chance that CI will be slightly different to the results of the hypothesis.

### Comparing Three Or More Categorical Variables

When the hypothesis we wish to test involves proportions in three or more categories (e.g. left-handed/right-handed/ambidextrous) we need to use the chi square ($$\chi^2$$) goodness-of-fit test.

### Example: Handedness with three outcomes

__Research Question:__<br>
Are 80% of people right-handed, 12% left-handed and the remainder ambidextrous? 635 adults from various professions were sampled and their handedness recorded. 536 are predominantly right handed, 67 predominantly left handed and the remainder ambidextrous.

__Hypothesis:__<br>
$$
H_0: \pi_R = 0.80, \pi_L = 0.12, \pi_A = 0.08 \\
H_1: \text{The proportions are not as stated in the null hypothesis.}
$$

__Assumptions:__<br>
$$
n\pi_R = 635 * 0.80 = 508 \\
n\pi_L = 635 * 0.12 = 76.2 \\
n\pi_A = 635 * 0.08 = 50.8 \\
$$
<br>
Given that all proportions >= 5, CLT applies and we can use the chi square goodness-of-fit test.

__Test:__<br>
$$
\chi^2 = \Sigma\frac{(O_i - E_i)^2}{E_i} \\
\chi^2 = \frac{(536-508)^2}{508} + \frac{(67-76.2)^2}{76.2} + \frac{(32-50.8)^2}{50.8} \\
\chi^2 = 9.61 \\
$$

Number of categories - 1 degrees of freedom = 3 - 1 = 2 df
0.005 < p-value < 0.01
Since the p-value is below the 0.05 significance level, we reject $$H_0$$.

__Conclusion:__<br>
The proportions are not as claimed by the researcher. There appears to be a lower proportion of ambidextrous people than the researcher has claimed.

### Chi-Square Test of Independence

* If we take a sample from some target population and we record information on each of two categorical variables for each subject in the sample, we can carry out a chi-square test of independence to determine whether the two variables are dependent or independent.
* We can use this test to answer questions such as:
  * Is occupation independent of education level among people between 40 and 50 years of age?
  * Is the proportion of male students who own cars different to the proportion of female students who own cars?
  * Among shift workers, is there an association between the day on which an employee is absent from work and the shift on which they are rostered?

### Example: e-Cigarettes vs Nicotine Patches

* Note that in this example, the population "theoretical" proportion is unknown.

__Research Question:__<br>
Are e-cigarettes and nicotine patches equally effective in quitting smoking? 584 smokers wanting to quit were randomised into groups with 289 allocated to the nicotine patch group. After six months of treatment, abstinence from smoking was verified for 21 of the nicotine e-cigarette group and 17 of the nicotine patch group.

__Hypothesis:__<br>
$$H_0:$$ There is no association between the method used to quit smoking and its effectiveness.
$$H_1:$$ There is an association between the method used to quit smoking and its effectiveness.

__Assumptions:__<br>
_Work out the expected values for each cell in the table._
_Shortcut is: exepected value = (row total x column total)/grand total_

|             | e-Cig       | Patches      | Total |
| Quit        | 21 (18.8)   | 17 (19.2)    | 38    |
| Didn't Quit | 268 (270.2) | 278 (275.8)  | 546   |
| Total       | 289         | 295          | 584   |

We have calculated the expected value for each of the four cells in the table and since they are all at least 5, the test is valid.

__Test:__<br>
$$
\chi^2 = \Sigma\frac{(O_i - E_i)^2}{E_i} \\
\chi^2 = \frac{(21-18.8)^2}{18.8} + \frac{(17-19.2)^2}{19.2} + \frac{(268-270.2)^2}{270.2} + \frac{(278-275.8)^2}{275.8} \\
\chi^2 = 0.543 \\
$$

Number of df = (rows-1)(columns-1) = (2-1)(2-1) = 1 df

0.2 < p-value < 0.5

Since the p-value >= 0.05 we do not reject $$H_0$$.

__Conclusion:__<br>
We have not found any evidence of an association between the method used to quite smoking and its effectiveness among people who want to quit smoking. The proportion of all people who quit using e-cigarettes could be the same as the proportion who quit using patches.

### What if any of the expected values are <5?

* A chi-square test will not give valid results if any of the expected values are less than 5. This is the case for both a chi square goodness-of-fit test and for a chi-quare test of independence.
* To overcome this problem, we could group smaller categories together in a logical manner (e.g. vegetarian, vegan) in order to meet the expected value of >=5 required.

## Summary of Graphical Summaries and Analyses

![](/assets/images/stat670_summary_of_graphs_and_tests.jpg)

![](/assets/images/stat670_flowchart_of_graphs_and_tests.jpg)
