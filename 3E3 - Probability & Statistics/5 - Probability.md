---
tags:
- Quantitative
---

### Glossary:
- [[#Probability]]
- [[#Combining Events]]
- [[#Mutually Exclusive Events]]
- [[#Frequency Interpretation of Probability]]
- [[#Axioms of Probability]]
- [[#The Addition Rule]]
- [[#Counting Methods]]
- [[#Independant Events]]
- [[#The Multiplication Rule]]
- [[#The Law of Total Probability]]
- [[#Bayes' Theorem]]
- [[#Application to Reliability Analysis]]

&nbsp;

#### Formulas:
- 


&nbsp;

---

# Probability

> #Probability is a [[1 - Data Collection#^726f4a|quantitative]] measure of how likely a __random phenomenon__ is to occur.
> A #Random_Experiment has an _unknown outcome_, but a well defined set of _possible outcomes_, $S$. The #Set $S$ is caled the #Sample_Set or #Sample_Space for the experiment.

> #### The Law of Large Numbers
> #The_Law_of_large_Numbers states that: As the number of _repetitions_ of a probability experiment _increases_, the proportion with which a certain outcome is observed _get closer_ to the probability of the outcome, e.g, _flipping a coin_.

- An #Element of the _sample space_, $S$, is called a #Sample_Point ( #Elementary_Event ).
- An #Event can be described by a collection of sample points, i.e. _a subset of a sample space_.

&nbsp;

> __*EXAMPLE:*__
> For example, if we roll a die,
> $$S = \{1, 2, 3, 4, 5, 6 \}$$
> i.e there are 6 _sample points_.
> - Let A be the event that the result is _even_. Then A can be described by the set;
> $A = \{2, 4, 6 \}$
> Any even can be represented by a #Subset of the sample set.


&nbsp;

---
# Combining Events

We often _construct events_ by combining simpler events or we describe new events from _combinations_ of existing events.
- The #Union of two event, $E_1$ and $E_2$, denoted $E_1 \cup E_2$, is the set of outcomes that belong __either__ to $E_1$, to $E_2$, or to _both_, i.e. "$E_1$ __or__ $E_2$"
- The #Intersection of two events $E_1$ and $E_2$, denoted $E_1 \cap E_2$, is the set of outcomes that belong both to $E_1$ and to $E_2$, i.e. "$E_1$ __and__ $E_2$"
- The #Complement of an event $E$, denoted; $E^C$, $\bar{E}$, or $\neg E$, is the set of outcomes that __do not belong__ to E, i.e. "Not $E$"
$\,$
![[Pasted image 20230215143247.png|400]]

&nbsp;

---

# Mutually Exclusive Events

The events $E_1$ and $E_2$ are said to be #Mutually_Exclusive if they have _no outcomes_ in common.
More generally, a collection of events $E_1, \, E_2, \, \dots \, , \, E_n$ is said to be mutually exclusive if _no two_ of them have any outcomes in common.
$\,$
![[Pasted image 20230215143648.png|300]]

&nbsp;

---

# Frequency Interpretation of Probability

We often use th eletter $P$ to stand for #Probability .
Suppose an experiment is repeated $n$ times, where $n$ is very large, (effectively infinite), and event '$E$' occurs $r$ times,. Then:
$$P(E) = \frac{r}{n}$$
It follows from this interpretation that:
1. $0 \leq P(E) \leq 1$
2. $P(E) = 0$ if th event of '$E$' is impossible.
3. $P(E) = 1$ if th event of '$E$' is sure to happen.

&nbsp;

- In many situations, the only way to _estimate_ the probability of an event is to _repeat the experiment_ many times and determine the _proportion_ of times that the event occurs, e.g:
	- If it is desired to estimate the probability that a printed circuit board manufactured by a certain process is defective.
- In some cases, probabilities can be determined through _knowledge_ of the _physical nature_ of the experiment, e.g:
	- If it is known that the shape of a die is nearly a perfect cube, and that its mass is distrbuted nearly uniformly, it may be assumed that each of the six faces is equally likely to land upward when the die is tossed.


&nbsp;

---

# Axioms of Probability

The probability theory is built based on _three commons sense rules_, known as #Axioms .
$\,$ ^c65007
> #### Axioms of Probability
> 1. Given the sampe sapce $S$, $P(S) = 1$.
> 2. For any vent $E$, $0 \leq P(E) \leq 1$.
> 3. If $E_1$ and $E_2$ are #Mutually_Exclusive events, i.e $(E_1 \cap E_2) = \emptyset$, then $P(E_1 \cup E_2) = P(E_1) + P(E_2)$. And more generally, if $E_1, \, E_2, \, \dots \, , \, E_k$, then $P(E_{1} \, \cup \, \dots \cup E_{k}) = P(E_{1}) + \dots + P(E_{k})$.

^180053

These axioms imply the following results: 
$$\begin{array}

P(E^C) = 1 - P(E), \\
\, \\
P( \emptyset ) = 0

\end{array}$$ 
^05edc8

&nbsp;


>__*EXAMPLE 1:*__
> The following table presents _probabilities_ for the number of times that a certin computer system will crash in the course of a week. Let $A$ be the event that there are more than _two crashes_ during the week, and let $B$ be the event that the system crashes _at least onece_. 
> - Find a #Sample_Space.
> - Then find the #Subset of the sample space that correspond to the events $A$ and $B$.
> - Then find $P(A)$ and $P(B)$.
>
>  |__Number of Crashes__|__Probability__|
>  |:---:|:---:|
>  |||
>  |0|0.60|
>  |1|0.30
>  |2|0.05|
>  |3|0.04|
>  |4|0.01|
> ---
>__*SOLUTION:*__
> The _sample space_ for the experiment is the set $S = \{ 0,1,2,3,4 \}$. 
> 
> The events are $A = \{ 3, 4 \}$ and $B = \{ 1, 2, 3, 4 \}$.
> 
> To find $P(A)$, notice that $A$ is the event that either _3_ or _4_ crashes happen. The events "_3 crashes appen_" and "_4 crashes happen_" are #Mutually_Exclusive. Therefore, using [[#^180053|Axiom 3]]:
> $$\begin{array}
> 
> . P(A) &=& P(\text{3 crashes happen or 4 crashes happen}) \\
> &=& P(\text{3 crashes}) + P(\text{4 crashes}) \\
> &=& 0.04 + 0.01 = 0.05 
> 
> \end{array}$$
> 
> As $B^C$ is the event that no crashes happen. Therefore using the ([[#^05edc8|above formula]]):
> $$\begin{array}
> . P(B) &=& 1 - P(B^C) \\
> &=& 1 - P(\text{0 crashes}) \\
> &=& 1 - 0.6 = 0.4
> \end{array}$$

&nbsp;

When the model of _equally likely outcomes_ is assumed, the probabilites are chosen to be _equal_.
> If $S$ is a #Sample_Space containing $N$ equally likely outcomes, and if $E$ is an event containing $k$ outcomes, then:
> $$P(E) = \frac{k}{N}$$
> _Whenever a sample space consists of N possible outcomes that are equally likely, the probability of each outcome is $\frac{1}{N}$_

&nbsp;

> __*EXAMPLE 2:*__
> An extrusion die is used to produce aluminium rods. Specifications are given for the _length and diameter_ of the rods. For each rod, the length is classified as _too short_, or _too thick_, or _OK_. In a population of 1000 rods, the number of rods in each class is as follows:
> 
> ||||*__Diameter__*||
> |:---:|:---:|:---:|:---:|:---:|
> ||||||
> |__Length__||__Too Thin__|__OK__|__Too Thick__|
> ||||||
> |__Too Short__||10|3|5|
> |__OK__||38|900|4|
> |__Too Long__||2|25|13|
>  - A rod is sampled at _random_ from this population. What is the probability that it is _too short_?
> ---
> __*SOLUTION:*__
> We can think of each of th 1000 rods as an outcome in a sample space. Each of the 1000 outcomes is equally likely. We'll solve the problem by counting the number of outcomes that correspond to the event:
> $$P(\text{too short}) = \frac{10 + 3 + 5}{1000} = \frac{18}{1000}$$

---

# The Addition Rule
---
# Counting Methods
---
# Independant Events
---
# The Multiplication Rule
---
# The Law of Total Probability
---
# Bayes' Theorem
---
# Application to Reliability Analysis
---
