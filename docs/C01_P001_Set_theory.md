## Set theory

Set theory provides several fundamental tools used to lay out the rules and logic of probability. Set theory provides a formal mathematical way of describing collections of elements.

<a name="TOC"></a>
### Table of contents
1. <a href="#S01">Sets</a>
2. <a href="#S02">Elementary set operations</a>

<a href="#END">&#129147;</a>

<a name="S01"></a>
#### 1. Sets

* **Set**: A collection of objects (called **elements**, **members**) regarded as a single object.
     * The sides of a die (1 to 6) are an example of a set.
     * A specific side (i.e., the side labeled "1") is an element/member of the set.

Consider the set &Omega; = \{ 1, 2, 3, 4, 5, 6 \}. There are several **operators** we can use to indicate whether elements are in a set or not:
* 1 &isin; &Omega; - the number 1 is an elment of the the set &Omega;.
* 7 &notin; &Omega; - the number 7 is not an elment of the the set &Omega;.
* \{ 1, 3, 5 \} &sub; &Omega; - the set of numbers 1, 3, and 5 form a **subset** of the larger set &Omega;.
* 

There are several special sets worthy of note:
* The **empty set**, or &empty; - a set with no elments or members.
* **Real numbers**, or &#8477; - the set of all rational or irrational (e.g., ) numbers, either positive, negative, or zero.
* **Natural numbers**, or &#8469; - the set of whole numbers (either starting from 0 or 1, depending on the field).
* **Integers**, or &#8484; - the set with whole numbers, negative whole numbers, and zero.

In the context of probability theory, set theory is applied to the outcomes that can result from conducting an experiment. Consider the result of rolling a numbered six-sided die. The act of rolling the die is an **experiment**; the value on the side of the die facing upward is an **outcome**. Two key concepts are then:

* **Sample space**: The set of all possible outcomes that could occur.
* **Event**: Any collection of possible outcomes in the experiment; any subset of the sample space.

<img src="C01_P001_I001.png" alt="Figure 1.1" width="500" height="500"/>

##### References:

* Luce, R. D. (1986). *Response times: Their role in inferring elementary mental organization*. Oxford University Press. [&rarr;](https://oxford.universitypressscholarship.com/view/10.1093/acprof:oso/9780195070019.001.0001/acprof-9780195070019)

<a href="#TOC">&#129145;</a> <a href="#END">&#129147;</a>

<a name="S02"></a>
#### 1. Section 2

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
[Home page](https://rettopnivek.github.io/Tutorials_for_statistics/)
