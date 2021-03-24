<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

## Combinatorics

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Multiplication rule</a>
2. <a href="#S02">Section 2</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Concepts

- Combination
- Permutation
- Unordered sample
- Ordered sample
- Sampling with replacement
- Sampling without replacement

<a name="S02"></a>
#### 2. Multiplication rule

Assume an experiment (e.g., a dice roll, a coin flip, etc.):
- has k parts (*k* &#8805; 2);
- the i<sup>th</sup> part of the experiment can have n<sub>i</sub> outcomes;
- all of the outcomes in each part can occur irrespective of what occurred in other parts (i.e., *sampling with replacement*).

The total number of unique combinations of outcomes over parts is then:

$$\prod_{i=1}^k n_i $$.

Using R, we can easily run a Monte Carlo simulation that demonstrates this. Consider rolling a 6-sided die 3 times:

```R
# Function to simulate rolling a 6-sided die 3 times
roll_dice_3_times <- function() {
  # Sample space
  S <- 1:6
  # Simulate 3 rolls of die
  output <- sample( S, size = 3, replace = T )
  return( output )
}

# Monte Carlo simulation of 10,000 rolls
mc_sim <- sapply(
  1:10000,
  function(i) roll_dice_3_times()
)

# Convert column vectors with separate outcomes
# for each roll into character strings in order to
# easily identify unique combinations
terms <- apply( mc_sim, 2, paste, collapse = ',')

# Extract all unique combinations of outcomes
unq <- unique( terms )

# Total number of unique outcome combinations
print( length( unq ) ) # 216

# Using multiplication rule

# 6 possible outcomes for each roll
n <- c( 6, 6, 6 )

# Product of number of outcomes for each part
print( prod( n ) ) # 216
```

##### References:

* DeGroot, M. H., & Schervish, M. J. (2012). *Probability and statistics* (4th ed.). Boston, MA: Addison-Wesley. [&rarr;](https://www.pearson.com/us/higher-education/product/De-Groot-Probability-and-Statistics-4th-Edition/9780321500465.html)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 2. Permutations

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
[Probability](C01_P000_Probability.md);
[Sections](C00_P002_Chapters.md);
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)
