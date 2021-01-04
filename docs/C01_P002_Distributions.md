## Probability distributions

Introduction

<a name="TOC"></a>
### Table of contents

1. <a href="#S01">The cumulative distribution function</a>

<a name="S01"></a>
#### 1. The cumulative distribution function

A *complete probabilstic description* of a random variable **X** for a single observation (or series of independent observations) is the probability that **X** is less than or equal to a real value x. or F(x) = P(**X** &leq; x). One can write this as a function, known as the *cumulative distribution function* or **CDF**:

F(x) = F(**X** &leq; x).

A function must meet 3 requirements to be a **CDF**:

1. Monotonicity: if x<sub>1</sub> < x<sub>2</sub>, then F(x<sub>1</sub>) < F(x<sub>2</sub>).
2. As x approaches positive infinity (or the highest allowable value), F(x) approaches 1.
3. As x approaches negative infinity (or the lowest allowable value), F(x) approaches 0.

#### 2. The density function

##### References:

* Luce, R. D. (1986). *Response times: Their role in inferring elementary mental organization*. Oxford University Press. [&rarr;](https://oxford.universitypressscholarship.com/view/10.1093/acprof:oso/9780195070019.001.0001/acprof-9780195070019)

```R
# Example R code
```

*Note: Advanced content.*

[Return to sections](C00_P002_Chapters.md)


