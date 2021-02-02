## Probability distributions

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">The cumulative distribution function</a>
2. <a href="#S02">The probability density function</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. The cumulative distribution function

A *complete probabilstic description* of a random variable **X** for a single observation (or series of independent observations) is the probability that **X** is less than or equal to a real value x. or F(x) = P(**X** &leq; x). One can write this as a function, known as the *cumulative distribution function* (**CDF**):

F(x) = F(**X** &leq; x).

A function must meet 3 requirements to be a **CDF**:

1. Monotonicity: if x<sub>1</sub> < x<sub>2</sub>, then F(x<sub>1</sub>) < F(x<sub>2</sub>).
2. As x approaches positive infinity (or the highest allowable value), F(x) approaches 1.
3. As x approaches negative infinity (or the lowest allowable value), F(x) approaches 0.

```R
# Example code
```

*Note: Advanced content.*

##### References:

* Luce, R. D. (1986). *Response times: Their role in inferring elementary mental organization*. Oxford University Press. [&rarr;](https://oxford.universitypressscholarship.com/view/10.1093/acprof:oso/9780195070019.001.0001/acprof-9780195070019)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 2. The density function

Assuming the cumulative distribution function is differentiable, we can compute the first derivate with respect to the value x to get the *probability density function* (**PDF**):

f(x) = *d* F(x) / *d*x.

As such, one can also compute the cumulative distribution function by taking the integral of the probability density function:

F(x) = &#8747;<sub>-&#8734;</sub><sup>z</sup> f(x) *d*x.

```R
# Example R code
```

*Note: Advanced content.*

##### References:

* Luce, R. D. (1986). *Response times: Their role in inferring elementary mental organization*. Oxford University Press. [&rarr;](https://oxford.universitypressscholarship.com/view/10.1093/acprof:oso/9780195070019.001.0001/acprof-9780195070019)

<a href="#TOC">&#129145;</a>

<a name="END"></a>
Return to:
[Probability](C01_P000_Probability.md);
[Sections](C00_P002_Chapters.md);
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)
