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


The formula for the simple linear regression model is

$$
y_i = \beta_0 + \beta_1 x_i + \epsilon_i
$$

where $\epsilon \sim \text{N}( 0, \sigma^2 )$.

In other words, the residual $\epsilon_i$ follows a normal distribution with a mean of 0 and a variance of $\sigma^2$. An equivalent way of writing this is

$y_i \sim \text{N}( \mu_i, \sigma^2 )$

where $\mu_i = \beta_0 + \beta_1 x_i$. This formulation helps to emphasizes key assumptions for the simple linear regression model:

* The dependent variable is assumed to follow a normal distribution;
* The variance of the distribution is fixed irrespective of the values of *y* or *x* (homoscedasticity);
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

