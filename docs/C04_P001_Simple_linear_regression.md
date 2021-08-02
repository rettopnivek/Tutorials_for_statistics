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

Given an independent variable/predictor \\(text{\textbf{x}} = \{x_1, x_2, ..., x_n\}\\) and a dependent variable/outcome \\(text{\textbf{y}} = \{y_1, y_2, ..., y_n\}\\), the formula for the simple linear regression model is

$$
y_i = \beta_0 + \beta_1 x_i + \epsilon_i
$$

where \\(\epsilon_i \sim \text{N}( 0, \sigma^2 )\\).

In other words, the residuals \\(\epsilon\\) follows a normal distribution with a mean of 0 and a variance of \\(\sigma^2\\). An equivalent way of writing this is

$$
y_i \sim \text{N}( \mu_i, \sigma^2 ) \text{ with } \mu_i = \beta_0 + \beta_1 x_i.
$$

This formulation helps to emphasizes some key assumptions for the simple linear regression model:

* The dependent variable is assumed to follow a normal distribution;
* As indicated by a lack of a subscript i on \\(\sigma^2\\), the variance of the distribution is fixed irrespective of the values of *y* or *x* (homoscedasticity);
* The predicted value for *y* is a linear combination of *x*;
* Observations are independent and identically distributed (i.i.d.).

```R
# Example R code
```

*Note: Advanced content.*

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

