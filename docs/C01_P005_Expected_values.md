## Expected value

Introduction

### Table of contents
1. Definition
    1.1. Discrete random variables
    1.2. Continuous random variables
2. Properties
3. Relation to the sample mean

#### 1. Definition

##### 1.1. Discrete random variables

Let **X** be a discrete random variable with a set of possible values *D* and a probability mass function *p(x)*. Then the expected value for **X** is:

![E\[X\] = \sum_{x \in D} x \cdot p(x)](https://render.githubusercontent.com/render/math?math=E%5BX%5D%20%3D%20%5Csum_%7Bx%20%5Cin%20D%7D%20x%20%5Ccdot%20p(x)).

*Note: The equation given above handles both finite cases and countably infinite cases.*

**Examples**:

A) Consider a fair six-sided die. The probability mass function is simply *p(x)* = 1/6. We can then write the expected value as:

*E*[ **X** ] = 1 &middot; 1/6 + 2 &middot; 1/6 + 3 &middot; 1/6 + 4 &middot; 1/6 + 5 &middot; 1/6 + 6 &middot; 1/6.

Hence, the expected value for the die is 3.5.

B) Now consider rolling this die four times, and counting values greater than 4 (i.e., 5 and 6) as a "success", and values 4 and under as a "failure". Observations of successes then follow a binomial distribution with a probability parameter ![\theta](https://render.githubusercontent.com/render/math?math=%5Ctheta) set to 2/6 and number of trials fixed to 4. We can use R to easily compute the expected value of number of successes over four die rolls:
```r
n <- 4 # Number of trials
x <- 0:n # Number of possible successes
# Use R's built-in density function for the binomial distribution
p_x <- dbinom( x, n, 2/6 )
# Compute expected value
E_x = sum( x * p_x )
```
The expected value is 1.33 (rounded to two decimal places), or more accurately, 1 and 1/3.

##### 1.2. Continuous random variables

Let **X** be a continuous random variable with values from the set of real numbers, ![\Re](https://render.githubusercontent.com/render/math?math=%5CRe), and with a density function *f*(*x*). Then the expected value for **X** is:

![E\[X\] = \int_{\Re} x f(x) dx](https://render.githubusercontent.com/render/math?math=E%5BX%5D%20%3D%20%5Cint_%7B%5CRe%7D%20x%20f(x)%20dx).

**Examples**:

A) Consider a random variable **U** that follows the uniform distribution with a lower limit ![\alpha](https://render.githubusercontent.com/render/math?math=%5Calpha) = 0 and an upper limit ![\beta](https://render.githubusercontent.com/render/math?math=%5Cbeta) = 2. The density function for uniform distribution is given as:

![f(x) = 1/(\beta - \alpha)](https://render.githubusercontent.com/render/math?math=f(x)%20%3D%201%2F(%5Cbeta%20-%20%5Calpha)).

For our current parameters, this simplifies to *f*(*x*) = 1/(2-0) = 0.5. The expected value is then:

![E\[X\] = \int .5 x dx](https://render.githubusercontent.com/render/math?math=E%5BX%5D%20%3D%20%5Cint%20.5%20x%20dx).

This is a straightforward integral to solve:

![\int .5 x dx = .25 x^2](https://render.githubusercontent.com/render/math?math=%5Cint%20.5%20x%20dx%20%3D%20.25%20x%5E2).

Hence, the expected value for **X** is:

![E\[X\] = .25 (2)^2 - .25 (0)^2 = 1](https://render.githubusercontent.com/render/math?math=E%5BX%5D%20%3D%20.25%20(2)%5E2%20-%20.25%20(0)%5E2%20%3D%201).

B) We can also use R's built-in function for unidimensional numerical integration to solve this problem:

```r
# Define function that computes x * f(x)
x_fx <- function( x ) x * dunif( x, 0, 2 )
# Use R's built-in numerical integration function
E_x <- integrate( x_fx, lower = 0, upper = 2 )
```

#### 2. Properties

If you multiply a random variable **X** by a scalar *a*, then:

E[ *a* **X** ] = *a* E[ **X** ].

If you have a set of random variables, **X**<sub>1</sub>, **X**<sub>2</sub>, ..., **X**<sub>K</sub>, then:

![E\[ \sum_{i=1}^K X_i \] = \sum_{i=1}^K E\[X_i\]](https://render.githubusercontent.com/render/math?math=E%5B%20%5Csum_%7Bi%3D1%7D%5EK%20X_i%20%5D%20%3D%20%5Csum_%7Bi%3D1%7D%5EK%20E%5BX_i%5D).

#### 3. Relation to the sample mean




```R
# Example R code
```

*Note: Advanced content.*

[Return to sections](C00_P002_Chapters.md)


