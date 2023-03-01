<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
## Probability axioms

Paraphrasing from an excellent blog post by John Mount titled [Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told ](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told), we have two major questions regarding probabilities:

1. What do probabilities mean?
2. What kind of calculations (e.g., addition, multiplication) can we perform on/with probabilities?

An **axiomatic definition of probability** (axioms are propositions to be taken as true) allows us to answer *question 2*. The most well-known axiomatic approach is based on Kolmogorov (1933), who laid out 6 axioms based on [set theory](C01_P001_Set_theory.md). The final 3 axioms, with some reformulation, provide the core definition of probability reported in modern textbooks today.

*Note: Others have laid out their own formulations to address question 2, but Kolmogorov's axioms are the most well-known and successful.*

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">The Kolmogorov axioms</a>
2. <a href="#S02">Current axiomatic foundations</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. The Kolmogorov axioms

Kolmogorov (1933) set forth 6 axioms to define probabilities. Based on a 2018 translation of his work, with slight notational changes:

Let &Omega; (the <a href="https://rettopnivek.github.io/Tutorials_for_statistics/docs/C01_P001_Set_theory.html#S01">sample space</a>) be a collection of elements e<sub>1</sub>, e<sub>2</sub>, e<sub>3</sub>, ..., dubbed *elementary events*, and let &#120021; be a set of subsets of &Omega;, where the elements of &#120021; are called *random events*. Then...

1. \\( \mathcal{F} \\) is a *field of sets* (now known as a set algebra).
2. \\( \mathcal{F} \\) contains \\( \Omega \\).
3. To each set \\( E_{i} \\) in \\( \mathcal{F} \\), a non-negative real number \\( P(E_{i}) \\) is assigned. The nunber \\( P(E_{i}) \\) is called the probability of event \\( E_{i} \\).
4. \\( P(\Omega) \\) equals 1.
5. If set \\( E_{i} \\) and \\( E_{j} \\) have no element in common (\\( E_{i} \cap E_{j} = \emptyset \\)), then \\( P(E_{i} \cup E_{j}) = P(E_{i}) + P(E_{j}) \\).
6. If \\(E_{1} \supseteq E_{2} \supseteq \dots \\) is a countably infinite decreasing sequence of events from \\( \mathcal{F} \\) with \\( \bigcap_{i=1}^{\infty} E_{i} = \emptyset \\) then \\( lim_{i \to \infty} P(E_{i}) = 0 \\).

**Axioms 1 - 2**: These axioms provide some useful groundwork in preparation of defining probability. Important implications are:

- The *field of sets*, or a **set-algebra**, indicates that if sets E<sub>i</sub> and E<sub>j</sub> are in &#120021;, then E<sub>i</sub> &cup; E<sub>j</sub>, E<sub>i</sub> &cap; E<sub>j</sub>, and the set differences E<sub>i</sub> &cap; E<sub>j</sub><sup>c</sup> and E<sub>i</sub><sup>c</sup> &cap; F<sub>j</sub> are also all in &#120021;.
- In other words, a set-algebra is **closed under the boolean operations complement, union, and intersection**.

**Axioms 3 - 5**: These are the *key axioms that define probability*. These axioms (or variants thereof) are what you will typically see reported in textbooks and introductory statistics courses. Several useful collaries can be derived from them:

- **Complement rule** - For any event A, P(A<sup>c</sup>) = 1 - P(A).
- **Inclusion-Exclusion** - For two arbitrary events A and B, P( A &cup; B ) = P(A) + P(B) - P( A &cap; B).

**Axiom 6**: This axiom ensures the definition of probability works both for finite and continuous variables.

##### References:

* John Mount (2020, September 19). Kolmogorov’s Axioms of Probability: Even Smarter Than You Have Been Told [Blog post]. [&rarr;](https://win-vector.com/2020/09/19/kolmogorovs-axioms-of-probability-even-smarter-than-you-have-been-told)
* Kolmogorov, A. N. (2018). *Foundations of the Theory of Probability* (N. Morrison, Trans.; 2nd edition). Dover. (Original work published 1933).[&rarr;](https://store.doverpublications.com/0486821595.html)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 2. Current axiomatic foundations

Standard textbooks on probability reformulate the axioms proposed by Kolmogov, providing some groundwork from set theory and then presenting three axioms. First, we define a **&sigma;-algebra** or **Borel field** (&#120017;) as a collection of subsets of a sample space &Omega; with the following 3 properties:
 
1. &empty; &#8712; &#120017; (the empty set is an element of &#120017;).
2. If E &#8712; &#120017; then E<sup>c</sup> &#8712; &#120017; (&#120017; is closed under complementation).
3. If E<sub>1</sub>, E<sub>2</sub>, ... &#8712; &#120017; then &cup;<sup>&#8734;</sup><sub>i = 1</sub> E<su>i</sub> &#8712; &#120017; (&#120017; is closed under countable unions).

Given a sample space &Omega; and an associated sigma;-algebra &#120017;, a probability function is therefore a function P with domain &#120017; that satisfies:

1. P(E) %ge; 0 (The probability of any event must be non-negative).
2. P(&Omega;) = 1.
3. If E<sub>1</sub>, E<sub>2</sub>, ... &#8712; &#120017; are pairwise disjoint.

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
