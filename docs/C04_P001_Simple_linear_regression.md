<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> 

## Simple linear regression

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Formulation</a>
2. <a href="#S02">Section 2</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Formulation

Given a predictor **x** = \\(\\{x_1, x_2, ..., x_n\\}\\) (or independent variable) and a outcome **y** = \\(\\{y_1, y_2, ..., y_n\\}\\) (or dependent variable), the formula for the simple linear regression model is

$$
y_i = \beta_0 + \beta_1 x_i + \epsilon_i
$$

where \\(\epsilon_i \sim \text{N}( 0, \sigma_{\epsilon}^2 )\\).

In other words, the residuals \\(\epsilon\\) follows a normal distribution with a mean of 0 and a variance of \\(\sigma{\epsilon}^2\\). An equivalent way of writing this is

$$
y_i \sim \text{N}( \mu_i, \sigma^2 ) \text{ with } \mu_i = \beta_0 + \beta_1 x_i.
$$

This formulation helps to emphasizes some key assumptions for the simple linear regression model:

* The dependent variable is assumed to follow a normal distribution;
* As indicated by a lack of a subscript i on \\(\sigma^2\\), the variance of the distribution is fixed irrespective of the values of **y** or **x** (homoscedasticity);
* The expected value for \\(y_i\\) is a linear combination of an intercept and \\(x_i\\);
* Observations are independent and identically distributed (i.i.d.).

```R
# Example R code
```

*Note: Advanced content.*

<a name="S03"></a>
#### 3. Decomposition of the variance for **y**

In the simple linear model, the variance for the outcome **y** can be decomposed into

$$
\sigma_{y}^2 = \sigma_{\text{R}}^2 + \sigma_{\epsilon}^2.
$$

The first term to on the right-hand side of the equation refers to the variance accounted by the predictor **x**, which is

$$
\sigma_{R}^2 = \beta_1^2 \sigma_{x}^2,
$$

where \\(\sigma_{x}^2\\) is the variance for the predictor **x**.

Therefore, the proportion of variance of the outcome **x** accounted for by its linear relation with the predictor **x**, a metric known as \\(R^2\\), is

$$
R^2 = \frac{\sigma_{R}^2}{\sigma_{y}^2}
$$

which is equivalent to

$$
R^2 = 1 - \frac{\sigma_{\epsilon}^2}{\sigma_{y}^2}.
$$

$$
\sigma_{\epsilon}^2 = \frac{\beta_1^2 \sigma_{x}^2(1 - R^2 )}{R^2}
$$


#### ?. Estimation

DISCUSS "Least-squares solution".

The sampling distribution for the parameter \\(\beta_1\\) is N(\\(\beta_1\\), \\(\sigma_{\beta_1}^2\\)), where

$$
\sigma_{\beta_1}^2 = \frac{1}{n - 1} \lgroup \frac{\sigma_y}{\sigma_x} \rgroup (1 - R^2).
$$

Here, \\(sigma_y\\) and \\(\sigma_x\\) refer to the standard deviation of **y** and **x** (in the population).

##### References:

* Reference &rarr;

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 1. Section 2

Content.

```R
# Example R code
```

*Note: Advanced content.*

##### References:

* Reference &rarr;

<a href="#TOC">&#129145;</a>

<a name="END"></a>
Return to:
Chapter;
[Sections](C00_P002_Chapters.md);
[Index](C0_P000_Alphabetical.md); 
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)

