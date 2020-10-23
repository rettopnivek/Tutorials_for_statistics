## Probability (Concepts)

A core foundation of statistics is probability. To make inferences about a large group based on a smaller sample, or to predict future events, or to weigh how much the evidence from messy data supports a theory, we rely on probability.

<a name="TOC"></a>
### Table of contents

1. <a href="#S01">What is a random variable?</a>
2. <a href="#S02">Types of random variables</a>
3. <a href="#S03">Set theory</a>
5. <a href="#S04">The Kolomogorov axioms of probability</a>
6. <a href="#S06">Interpreting probabilities</a>

<a name="S01"></a>
#### 1. What is a random variable?

* **Random variable**: A variable that can randomly take on one of several possible numeric values.
* **Outcome**: The observed value for a random variable.
* **Sample space**: The list of all possible outcomes (can also be called the population).
* **Event**: A collection of outcomes, a subset of the sample space. A event can consist of a single outcome, or multiple outcomes. Furthermore, the same outcome can appear in different events.
* **Experiment**: An opportunity to observe a outcome or event.

Consider the result of rolling a numbered six-sided die. This is a random variable, as the numbered side that ends up facing upward can be any value between 1 to 6, and can change each time you roll the die. The upward-facing number is an outcome, and the values 1 through 6 are the sample space, as this describes all possible outcomes. This sample space can be divided into many different possible events, from singular outcomes (1, 2, 3, etc.), to combinations ( 1 or 2, 1 or 3, 2 or 3, etc.). The act of rolling the die and observing which value ends up facing upwards is an experiment.

<img src="C01_P001_I001.png" alt="Figure 1.1" width="500" height="500"/>

##### References:

* Luce, R. D. (1986). *Response times: Their role in inferring elementary mental organization*. Oxford University Press. [&rarr;](https://oxford.universitypressscholarship.com/view/10.1093/acprof:oso/9780195070019.001.0001/acprof-9780195070019)

<a href="#TOC">&#10548;</a>

<a name="S02"></a>
#### 2. Types of random variables

Random variables can be further categorized as:

* **Discrete**: A random variable that takes on a countable number of distinct values.
* **Continuous**: A random variable that can take on an infinite number of values.

Rolling a six-sided die is an example of a discrete random variable, as only six distinct values are possible. In contrast, the resulting decimal value for the angle of the arrow for a spinner/picker wheel is an example of a continuous variable.

*Note: The concepts of discrete versus continuous random variables are more malleable than they may first seem. For example, it is possible to have a discrete random variable that in theory can take on an infinite number of integer values (i.e., being countably infinite). Furthermore, what we often label as continuous random variables in reality are discrete variables with a very large sample space (e.g., if we measure people who can range between 1 and 2 meters in height with a ruler to reads accurately to a millimeter, technically we have a discrete random variable with a set of 1,001 possible outcomes). In reality, we cannot measure anything with infinite precision!*

<a href="#TOC">&#10548;</a>

<a name="S03"></a>
#### 3. Set theory

Set theory provides several fundamental tools that can be used to describe random variables and is a core part of Kolomogorov's axioms of probability. Set theory provides a formal mathematical way of describing collections of elements. The concepts and notation useful for discussing probability later on are easiest to introduce in the context of **finite sets**, when there are a finite collection of elements to describe.

* **Set**: A collection of objects (called **elements** or **members**) regarded as a single object.
     * The sides of a die (1 to 6) are an example of a set.
     * A specific side (i.e., the side labeled '1') is an element/member of the set.

Consider the set &Omega; = \{ 1, 2, 3, 4, 5, 6 \}. There are several **operators** we can use to indicate whether elements are in a set or not:
* 1 &isin; &Omega; - the number 1 is an elment of the the set &Omega;.
* 7 &notin; &Omega; - the number 7 is not an elment of the the set &Omega;.
* \{ 1, 3, 5 \} &sub; &Omega; - the set of numbers 1, 3, and 5 form a **subset** of the larger set &Omega;.

There are several special sets worthy of note:
* The **empty set**, or &empty; - a set with no elments or members.
* **Real numbers**, or &#8477; - the set of all rational or irrational (e.g., ) numbers, either positive, negative, or zero.
* **Natural numbers**, or &#8469; - the set of whole numbers (either starting from 0 or 1, depending on the field).
* **Integers**, or &#8484; - the set with whole numbers, negative whole numbers, and zero.

To describe how sets do or do not overlap, four useful concepts are: 
* The **complement** of a set;
     * All elements not in a set.
     * Written as A' or A<sup>c</sup>.
* The **union** of two sets;
     * For sets A and B, their union refers to the set of elements contained in either A or B, irrespective of overlap.
     * Written as A &cup; B.
* The **intersection** of two sets;
     * For sets A and B, their intersection refers to the set of elements contained in both A or B, only overlapping elements.
     * Written as A &cap; B.
* **Mutually exclusive** or **disjoint** sets;
     * Sets A and B are mutually exclusive/disjoint when no elements in either set overlap.
     * Written as A &cap; B = &empty;.

<img src="C01_P001_I002.png" alt="Figure 1.2" width="500" height="500"/>

<a href="#TOC">&#10548;</a>

<a name="S04"></a>
#### 4. The Kolmogorov axioms of probability

Paraphrasing from an excellent blog post by John Mount titled [Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told ](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told), we have two major questions regarding probabilities:

1. **What do probabilities mean?**
2. **What kind of calculations (e.g., addition, multiplication) can we perform on/with probabilities?**

Kolmogorov (1933), relying on set theory, laid out **5 axioms** (propositions to be taken as true) to attempt to answer *question 2*. As per a 2018 translation of Kolmogorov (1933), with slight notational changes:

Let E (the *sample space*) be a collection of elements e<sub>1</sub>, e<sub>2</sub>, e<sub>3</sub>, ..., dubbed *elementary events*, and let F be a set of subsets of E, where the elements of F are called *random events*. Then...

1. F is a *field of sets* \[now known as a **&sigma;-algebra**\].
2. F contains E.
3. To each set F<sub>i</sub> in F, a non-negative real number P(F<sub>i</sub>) is assigned. The number P(F<sub>i</sub>) is called the probability of event F<sub>i</sub>.
4. P(E) equals 1.
5. If set F<sub>i</sub> and F<sub>j</sub> have no element in common (F<sub>i</sub> &cap; F<sub>j</sub> = &empty;), then P(F<sub>i</sub> &cup; F<sub>j</sub>) = P(F<sub>i</sub>) + P(F<sub>j</sub>).

Additional notes...

**Axiom 1**: The *field of sets*, or a **&sigma;-algebra**, indicates that if sets F<sub>i</sub> and F<sub>j</sub> are in F, then F<sub>i</sub> &cup; F<sub>j</sub>, F<sub>i</sub> &cap; F<sub>j</sub>, the set differences F<sub>i</sub> &cap; F<sub>j</sub><sup>c</sup> and F<sub>i</sub><sup>c</sup> &cap; F<sub>j</sub> are also all in F. In other words, a &sigma;-algebra is **closed under the boolean operations complement, union, and intersection**.

**Axiom 3**: This is an application of the **law of total probability**.

**Axioms 3 - 5**: These axioms define probabililty, and several useful collaries can be derived from them:

* **Complement rule** - For any event A, P(A<sup>c</sup>) = 1 - P(A).
* **Inclusion-Exclusion** - For two arbitrary events A and B, P( A &cup; B ) = P(A) + P(B) - P( A &cap; B).

*Note: Others have laid out their own formulations to address question 2, but Kolmogorov's axioms are the most well-known and successful.*

##### References:

* John Mount (2020, September 19). Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told [Blog post]. [&rarr;](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told)
* Kolmogorov, A. N. (2018). *Foundations of the Theory of Probability* (N. Morrison, Trans.; 2nd edition). Dover. (Original work published 1933).[&rarr;](https://store.doverpublications.com/0486821595.html)

<a name="S02_P02"></a>
### 4. Notation for random variables and probability

The typical notation for a random variable is a capital letter, like X or Y. A distinction is made between a random variable and its observed value, the latter of which is represented by lower-case letters like x or y. So we can write:

X = x,

which simply means the observed value for the random variable X is x. Combining this with the notation for probability, we can then represent the probabiliy that the random variable X will equal the observed value x as:

P(X = x).

Additionally, we can combine this with inequalities. So we can write:

P(X &#x2264; x),

which denotes the probability that a random variable will be less than or equal to an observed value x.

<a href="#TOC">&#10548;</a>

#### 5. Types of probability

While the probability axioms lay out the rules that determine what constitutes a valid probability, this does not solve *how to interpret probabilities*. What does it mean for P(X = x) = 0.1? One straightforward way to think of probability is that it is the ratio of the actual number of occurences divided by the total number of possible occurences. However, there are a few different ways to assign probabilities to outcomes, typically divided into three types:

1. **Classical** probability.

This type of probability assumes that outcomes are equally probable, and assigns probabilities as the ratio of the number of specified outcomes over the number of outcomes in the sample space. We can again use the fair six-sided die as an example of this type of probability. There are six possible outcomes, so each outcome has a 1 in 6 chance of occurring.

This type of probability is intuitive and easy to work with, but of course hinges on equally probable outcomes, which does not have to be the case. For example, a dice with some of the corners rounded is not fair - the rounded corners make it harder for some numbers to end up facing upward.

2. **Frequentist** or **empirical** probability.

This type of probability is based on the number of times a outcome (or event) occurs with repeated (independent) experiments. The classic example for this type of probability is flipping a coin. If you want to know the probability that a coin will come up heads when flipped, you can flip the coin repeatedly and count the number times it comes up heads, divided by the number of times you flipped the coin. This will give you an estimate of the probability of the coin coming up heads.

Frequentist probability has been a mainstay of statistics for a long time. There are nuances to how it is used though, that can be non-intuitive.

* Frequentist probability is built around *asymptotic behavior*. Consider the coin flip. The more you flip the coin, the better your estimate of the probability that it will come up heads will be, and if you fipped this coin an infinite number of times, then you would obtain the actual probability. The nuance here is that the probability is based on a thought experiment, as we could never actually flip the coin an infinite number of times.
* Frequentist probability is only valid for a *repeatable* event. Flipping a coin is clearly something that can be easily repeated. However, other types of events once again often require thought experiments. Conducting a complicated scientific study is typically difficult to replicate many times. So again, one must instead *imagine* the possible outcomes that could result from repeating the study many times, rather than actually repeating the study. However, some events are not repeatable. For instance, if a doctor wants to know the probability that their current patient has a specific illness, this type of event is too specific for frequentist probability.

3. **Subjective** or **evidential** probability.

This type of probability gives the measure of an individual person's belief that an event will happen. In other words, a person can assign values to whether events will occur (e.g., I there's a 80% chance it will rain tomorrow), and as long as they meet the requiremets based on the three axioms of probability, you have a valid subjective probablity.

This type of probability is part of the basis for Bayesian statistics, which has gain popularity in recent years. However, the fact that different individuals can assign different probabilities to events unnerves many people. Furthermore, it can be hard to convert an individual's beliefs into valid probabilities.

*Note: These types of probabilities overlap - they are not mutually exclusive!*

<a href="#TOC">&#10548;</a>

[Return to sections](C00_P002_Chapters.md)


