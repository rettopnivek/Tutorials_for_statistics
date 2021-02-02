## Probability axioms

Introduction

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Kolmogorov's origional probability axioms</a>
2. <a href="#S02">Current axiomatic foundations</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Kolmogorov's axioms of probability

Paraphrasing from an excellent blog post by John Mount titled [Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told ](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told), we have two major questions regarding probabilities:

1. **What do probabilities mean?**
2. **What kind of calculations (e.g., addition, multiplication) can we perform on/with probabilities?**

Kolmogorov (1933), relying on set theory, laid out **6 axioms** (propositions to be taken as true) to attempt to answer *question 2*. As per a 2018 translation of Kolmogorov (1933), with slight notational changes:

Let &Omega; (the *sample space*) be a collection of elements e<sub>1</sub>, e<sub>2</sub>, e<sub>3</sub>, ..., dubbed *elementary events*, and let &#120021; be a set of subsets of &Omega;, where the elements of &#120021; are called *random events*. Then...

1. &#120021; is a *field of sets* \[now known as a **set-algebra**\].
2. &#120021; contains &Omega;.
3. To each set E<sub>i</sub> in &#120021;, a non-negative real number P(E<sub>i</sub>) is assigned. The number P(E<sub>i</sub>) is called the probability of event E<sub>i</sub>.
4. P(&Omega;) equals 1.
5. If set E<sub>i</sub> and E<sub>j</sub> have no element in common (E<sub>i</sub> &cap; E<sub>j</sub> = &empty;), then P(E<sub>i</sub> &cup; E<sub>j</sub>) = P(E<sub>i</sub>) + P(E<sub>j</sub>).
6. If E<sub>1</sub> &#8839; E<sub>2</sub> &#8839; ... is a countably infinite decreasing sequence of events from &#120021; with &#8898;<sup>&#8734;</sup><sub>i = 1</sub> E<sub>i</sub> = &#8709;, then lim<sub>i &#8594; &#8734;</sub> P( E<sub>i</sub> ) = 0.

**Axioms 1 - 2**: These axioms provide some useful groundwork in preparation of defining probability. Important implications are:

- The *field of sets*, or a **set-algebra**, indicates that if sets E<sub>i</sub> and E<sub>j</sub> are in &#120021;, then E<sub>i</sub> &cup; E<sub>j</sub>, E<sub>i</sub> &cap; E<sub>j</sub>, and the set differences E<sub>i</sub> &cap; E<sub>j</sub><sup>c</sup> and E<sub>i</sub><sup>c</sup> &cap; F<sub>j</sub> are also all in &#120021;.
- In other words, a set-algebra is **closed under the boolean operations complement, union, and intersection**.

**Axioms 3 - 5**: These are the *key axioms that define probability*. These axioms (or variants thereof) are what you will typically see reported in textbooks and introductory statistics courses. Several useful collaries can be derived from them:

- **Complement rule** - For any event A, P(A<sup>c</sup>) = 1 - P(A).
- **Inclusion-Exclusion** - For two arbitrary events A and B, P( A &cup; B ) = P(A) + P(B) - P( A &cap; B).

**Axiom 6**: This axiom ensures the definition of probability works both for finite and continuous variables.

*Note: Others have laid out their own formulations to address question 2, but Kolmogorov's axioms are the most well-known and successful.*

##### References:

* John Mount (2020, September 19). Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told [Blog post]. [&rarr;](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told)
* Kolmogorov, A. N. (2018). *Foundations of the Theory of Probability* (N. Morrison, Trans.; 2nd edition). Dover. (Original work published 1933).[&rarr;](https://store.doverpublications.com/0486821595.html)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 1. Current axiomatic foundations

1. The probability of an event E is a non-negative real number: P(E) &#8805; 0 and P(E) &#8712; &#8477;.
2. The probability of at least one event occuring is 1: P(F) = 1.
3. Countable additivity (or &sigma;-additivity): For all countable collections of pairwise disjoint sets in F: P( &cup;<sup>&#8734;</sup><sub>i = 1</sub> E<sub>i</sub>) = &sum;<sup>&#8734;</sup><sub>i = 1</sub> P( E<sub>i</sub> ).

```R
# Example R code
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
[Probability](C01_P000_Probability.md);
[Sections](C00_P002_Chapters.md);
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)
