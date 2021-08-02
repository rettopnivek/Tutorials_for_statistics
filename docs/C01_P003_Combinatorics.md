<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

## Combinatorics

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Concepts</a>
2. <a href="#S02">Multiplication rule</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Concepts

- **Unordered sample**
  - Definition.
  - <span style="color: #ADD8E6">For example, ...</span>
- **Ordered sample**
  - Definition.
  - For example, ...
- **Sampling with replacement**
  - When sampling with.
  - For example, ...
- **Sampling without replacement**
  - When sampling without replacement, each sample unit has only one chance of being included in the sample. If a sample unit is included in a sample, that unit cannot be in subsequent samples drawn from the population.
  - For example, consider the set *S* = \{*a*, *b*, *c*\}. When sampling a single element without replacement, if *a* is sampled from *S*, then in a subsequent draw only \{*b*, *c*\} are available - *a* is excluded.
- **Permutation**
  - Given a set *A* with *n* elements, consider an experiment that consists of selecting *k* elements from *A* without replacement. Let each outcome consist of the *k* elements *in the order selected*. Then each outcome is called a **permutation** of **n elements taken k at a time**.
  - For example, suppose you have the set *A* = \{ *a*, *b*, *c*, *d* \}. A draw of \{ *b*, *a* \} from *A* is a permutation of 4 elements taken 2 at a time. Possible outcomes for the remaining draw from *A* would consist only of \{ *c*, *d* \} or \{ *d*, *c* \}, as per sampling without replacement. Furthermore, the elemens \{ *a*, *b* \} versus \{ *b*, *a* \} are different permutations, since they have *different orderings*.
- **Combination**
  - Consider a set *A* with *n* elements. Each subset *A*<sub>i</sub> with *k* elements (*k* < *n*) is called a **combination** of **n elements taken k at a time**.
  - For example, suppose you have the set *A* = \{ *a*, *b*, *c*, *d* \}. Then the subset *A*<sub>1</sub> = \{ *a*, *b* \} is an example of a combination of 4 elements taken 2 at a time. Note that the permutations \{ *a*, *b* \} and \{ *b*, *a* \} are the same subset, and therefore are a single combination - in other words, for combinations, the *order of the elements does not matter*.

##### References:

* DeGroot, M. H., & Schervish, M. J. (2012). *Probability and statistics* (4th ed.). Boston, MA: Addison-Wesley. [&rarr;](https://www.pearson.com/us/higher-education/product/De-Groot-Probability-and-Statistics-4th-Edition/9780321500465.html)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 2. Number of permutations

Content.

```R
# Example R code
```

*Note: Advanced content.*

##### References:

* Reference &rarr;

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S03"></a>
#### 3. Multiplication rule

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

<a href="#TOC">&#129145;</a>

<a name="END"></a>
Return to:
[Probability](C01_P000_Probability.md);
[Sections](C00_P002_Chapters.md);
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)
