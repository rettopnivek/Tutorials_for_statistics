## Simple linear regression

Introduction

### Table of contents
1. Formulation

#### 1. Formulation

The formula for the simple linear regression model is

![y_i = \beta_0 + \beta_1 x_i + \epsilon_i,](https://render.githubusercontent.com/render/math?math=y_i%20%3D%20%5Cbeta_0%20%2B%20%5Cbeta_1%20x_i%20%2B%20%5Cepsilon_i%2C)

where

![\epsilon_i \sim N( 0, \sigma^2 ).](https://render.githubusercontent.com/render/math?math=%5Cepsilon_i%20%5Csim%20N(%200%2C%20%5Csigma%5E2%20).)

In other words, ![\epsilon_i](https://render.githubusercontent.com/render/math?math=%5Cepsilon_i) follows a normal distribution with a mean of 0 and a variance of ![\sigma^2](https://render.githubusercontent.com/render/math?math=%5Csigma%5E2). An equivalent way of writing this is

![y_i \sim N( \mu_i, \sigma^2 ),](https://render.githubusercontent.com/render/math?math=y_i%20%5Csim%20N(%20%5Cmu_i%2C%20%5Csigma%5E2%20)%2C)

where

![\mu_i = \beta_0 + \beta_1 x_i.](https://render.githubusercontent.com/render/math?math=%5Cmu_i%20%3D%20%5Cbeta_0%20%2B%20%5Cbeta_1%20x_i.)

This formulation helps to emphasizes key assumptions for the simple linear regression model:

* The dependent variable is assumed to follow a normal distribution;
* The variance of the distribution is fixed irrespective of the values of *y* or *x* (homoscedasticity);
* The predicted value for *y* is a linear combination of *x*;
* Observations are independent and identically distributed (i.i.d.).

```R
# Example R code
```

*Note: Advanced content.*

[Return to sections](C00_P002_Chapters.md)


