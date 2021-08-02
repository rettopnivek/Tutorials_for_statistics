<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

## Combinatorics

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Concepts</a>
2. <a href="#S02">Number of possible permutations</a>
3. <a href="#S03">Number of possible combinations</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Concepts

- **Sampling with replacement**: Elements are randomly selected from a population, and the population remains unchanged after each sample is drawn.
- **Sampling without replacement**: Elements are randomly selected from a population, and elements included in a sample are removed from the population prior to subsequent sampling.
- **Permutation**: Given a set *A* with *n* elements, consider an experiment that consists of selecting *k* elements from *A*. Let each outcome consist of the *k* elements **in the order selected** Then each outcome is called a **permutation** of **n elements taken k at a time**.
- **Combination**: Consider a set *A* with *n* elements. Each subset *A*<sub>i</sub> with *k* elements (*k* < *n*) is called a **combination** of **n elements taken k at a time**.

```{r}
# Consider a sample space
S = c( "A", "B", "C", "D", "E", "F" )

set.seed( 212 ) # For reproducibility

### Sampling with replacement ###

# Each sample draws two elements 
# from S
J = 1:6
sample_1 = sample( J, size = 2 )
sample_2 = sample( J, size = 2 )
sample_3 = sample( J, size = 2 )

# For each sample, population 
# J remains unchanged, so 
# elements can appear in 
# multiple samples
S[ sample_1 ] # [1] "F", "C"
S[ sample_2 ] # [1] "A", "B"
S[ sample_3 ] # [1] "A", "E"

### Sampling without replacement ###

# Each sample draws two elements 
# from S
sample_1 = sample( J, size = 2 )
# Remove elements from population
J = J[ !J %in% sample_1 ]  
sample_2 = sample( J, size = 2 )
J = J[ !J %in% sample_2 ]  
sample_3 = sample( J, size = 2 )

# After each sample, population is 
# updated to only have unsampled 
# elements - therefore, each 
# element only appears once 
# across samples
S[ sample_1 ] # [1] "D", "A"
S[ sample_2 ] # [1] "E", "F"
S[ sample_3 ] # [1] "C", "B"
```

##### References:

* DeGroot, M. H., & Schervish, M. J. (2012). *Probability and statistics* (4th ed.). Boston, MA: Addison-Wesley. [&rarr;](https://www.pearson.com/us/higher-education/product/De-Groot-Probability-and-Statistics-4th-Edition/9780321500465.html)
* Dodge, Y. (2008). *The concise encyclopedia of statistics*. New York, NY: Springer. [&rarr;](https://link.springer.com/referencework/10.1007/978-0-387-32833-1)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 2. Number of possible permutations

Content.

```R
# Example R code
```

*Note: Advanced content.*

##### References:

* Reference &rarr;

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S03"></a>
#### 3. Number of possible combinations

Assume an experiment (e.g., a dice roll, a coin flip, etc.):
- has k parts (*k* &#8805; 2);
- the i<sup>th</sup> part of the experiment can have n<sub>i</sub> outcomes;
- all of the outcomes in each part can occur irrespective of what occurred in other parts (i.e., <a href="#S01_R01">sampling with replacement</a>).

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
