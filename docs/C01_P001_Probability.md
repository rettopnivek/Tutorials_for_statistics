## Probability

The foundations of statistics is probability. To make inferences about a large group based on a smaller sample, or to predict future events, or to weigh how much the evidence from messy data supports a theory, we rely on probability. This sections provides a brief summary of concepts, notation, and rules that form an important foundation for statistical testing.

### Table of contents

1. Useful concepts, terms, and notation
2. Probability axioms
4. Rules

#### 1. Useful concepts, terms, and notation

In this section, I will work through several foundational concepts and terms for probability, and detail the notation typically used to represent them.

* **Random variable**: A variable that can randomly take on one of several possible numeric values.
* **Outcome**: The observed value for a random variable.
* **Sample space**: The list of all possible outcomes.
* **Event**: A collection of outcomes, a subset of the sample space. A event can consist of a single outcome, or multiple outcomes. Furthermore, the same outcome can appear in different events.

Consider the result of rolling a numbered six-sided die. This is a random variable, as the numbered side that ends up facing upward can be any value between 1 to 6, and can change each time you roll the die. The upward-facing number is an outcome, and the values 1 through 6 are the sample space, as this describes all possible outcomes. This sample space can be divided into many different possible events, from singular outcomes (1, 2, 3, etc.), to combinations ( 1 or 2, 1 or 3, 2 or 3, etc.).

Random variables can be further categorized as:

* **Discrete**: A random variable that takes on a countable number of distinct values.
* **Continuous**: A random variable that can take on an infinite number of values.

Rolling a six-sided die is an example of a discrete random variable, as only six distinct values are possible. In contrast, the resulting decimal value for the angle of the arrow for a spinner/picker wheel is an example of a continuous variable.

*Note: The concepts of discrete versus continuous random variables are more malleable than they may first seem. For example, it is possible to have a discrete random variable that in theory can take on an infinite number of integer values (i.e., being countably infinite). Furthermore, what we often label as continuous random variables in reality are discrete variables with a very large sample space (e.g., if we measure people who can range between 1 and 2 meters in height with a ruler to reads accurately to a millimeter, technically we have a discrete random variable with a set of 1,001 possible outcomes). In reality, we cannot measure anything with infinite precision!*

The typical notation for a random variable is a boldface capital letter, like **X** or **Y**. A distinction is made between a random variable and its observed value, the latter of which is represented by standard lower-case letters like x or y. So we can write:

**X** = x,

which means the observed value for the random variable **X** is x.

#### 2. Notation

P( X = x )

#### 3. Probability axioms

1. The probability of an event is a non-negative real number.
2. The probability that at least one event in the sample space will occur is 1.
3. 

A probability must be
between 0

#### 4. Rules



```R
# Example R code
```


*Note: Advanced content.*

[Return to sections](C00_P002_Chapters.md)


