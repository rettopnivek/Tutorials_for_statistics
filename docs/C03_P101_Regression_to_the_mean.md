<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
## Regression to the mean

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Section 1</a>
2. <a href="#S02">Section 2</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Section 1

Statistical model:

For individuals \( i = \{ i, ..., n \} \) and runs \( t = \{ 1, 2 \} \), let us assume the statistcal model for a hypothetical 1-mile run time is:

$$run_{i,t} = \beta_0 + \eta_i + \epsilon_{i,t}$$,

where \( \eta_i \sim N( 0, \sigma^{\eta} ) \) and \( \epsilon_{i,t} \sim N( 0, \sigma^{\epsilon} ) \).

```R
# install.packages( 'dplyr' )
library( dplyr )

# Fix RNG seed for reproducibility
set.seed( 100 )

B0 = 9 # Mean time to run a mile (minutes)
sigma = 1 # Standard deviation

# Standard deviation for subject-level differences
sigma_eta = .5
# Standard deviation for differences between 
# runs (i.e., residual variation)
sigma_epsilon = sqrt( (sigma^2) - sigma_eta^2 )

# Sample size
n = 100

# Initialize data frmae
dtf = data.frame(
  ID = rep( 1:n ),
  # Subject-level deviations
  eta = NA,
  # Residual deviations 
  epsilon_1 = NA,
  epsilon_2 = NA,
  # Intervention (based on performance on first run)
  Intervention = 'Criticize',
  x = NA, # Dummy code for intervention
  # Observed 1-mile run time (minutes)
  run_1 = NA,
  run_2 = NA,
  stringsAsFactors = F
)

# Simulate subject-level deviations in run time 
# (i.e., individual differences in performance,
#  constant over run 1 and 2)
dtf$eta = rnorm( n, 0, sigma_eta )

# Simulate independent residual variation 
# between run 1 and 2
dtf$epsilon_1 = rnorm( n, 0, sigma_epsilon )
dtf$epsilon_2 = rnorm( n, 0, sigma_epsilon )

# Simulate run times (no effect of intervention)
dtf$run_1 = B0 + dtf$eta + dtf$epsilon_1
dtf$run_2 = B0 + dtf$eta + dtf$epsilon_2

# Specify intervention type based on 
# performance on run 1

# Above-average performance gets praise
dtf$Intervention[ dtf$run_1 > B0 ] = 'Praise'
# Dummy coded version
dtf$x = as.numeric( dtf$run_1 > B0 )

# Correlation between runs 1 and 2
# (i.e., stability between subjects)
cor( dtf$run_1, dtf$run_2 )

dtf %>% 
  group_by( 
    Intervention
  ) %>% 
  summarise( 
    Mean_change = round( mean( run_2 - run_1 ), 2 ), 
    .groups = 'drop'
  )

#   Intervention Mean_change
# 1 Criticize          0.53
# 2 Praise            -0.48
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
