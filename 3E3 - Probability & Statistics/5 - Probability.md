---
tags:
- Quantitative
- Random_Experiment
- Sample_Space
- Set
- Sample_Set
- Element
- Event
- Sample_Point
- Elementary_Event
- The_Law_of_Large_Numbers
- Subset
- Union
- Intersection
- Complement
- Mutually_Exclusive
- Probability
- Axioms
- Addition Rule
- Permutation
- Conditional_Probability
- Law_of_Total_Probability
- Tree_Diagrams
---

### Glossary:
- [[#Probability]]
- [[#Combining Events]]
- [[#Mutually Exclusive Events]]
- [[#Frequency Interpretation of Probability]]
- [[#Axioms of Probability]]
- [[#The Addition Rule]]
- [[#Counting Methods]]
	- [[#Permutations]]
	- [[#Combinations]]
- [[#Conditional Probability]]
- [[#Independant Events]]
- [[#The Multiplication Rule]]
- [[#The Law of Total Probability]]
- [[#Bayes' Theorem]]
- [[#Application to Reliability Analysis]]

&nbsp;

#### Formulas:
- Mutually Exclusive [[#^6f35b9| .1]]
- Addition Rule [[#^6e895a| .2]]
- Permutations [[#^f30062| .3]]
- Combinations [[#^477096| .4]]
- Conditional Probability [[#^6e6ea1| .5]]
- Independant Events [[#^bb853a| .5.1]] [[#^4ccd06| .5.2]]
- Intersection of Events (Conditional) [[#^555ae9| .6]]
- Intersection of Events (Independant) [[#^2b06dc| .7.1]] [[#^0cb1d9| .7.2]]


&nbsp;

---

# Probability

```ad-important
title: Definition

> #Probability is a [[1 - Data Collection#^726f4a|quantitative]] measure of how likely a __random phenomenon__ is to occur.
> A #Random_Experiment has an _unknown outcome_, but a well defined set of _possible outcomes_, $S$. The #Set $S$ is caled the #Sample_Set or #Sample_Space for the experiment.
```

```ad-important
title: ###### The Law of Large Numbers
> #The_Law_of_Large_Numbers states that: As the number of _repetitions_ of a probability experiment _increases_, the proportion with which a certain outcome is observed _get closer_ to the probability of the outcome, e.g, _flipping a coin_.

- An #Element of the _sample space_, $S$, is called a #Sample_Point ( #Elementary_Event ).
- An #Event can be described by a collection of sample points, i.e. _a subset of a sample space_.
```

&nbsp;

```ad-example
> For example, if we roll a die,
> $$S = \{1, 2, 3, 4, 5, 6 \}$$
> i.e there are 6 _sample points_.
> - Let A be the event that the result is _even_. Then A can be described by the set;
> $A = \{2, 4, 6 \}$
> Any even can be represented by a #Subset of the sample set.
```


&nbsp;

---
# Combining Events

```ad-important
title: Definition
We often _construct events_ by combining simpler events or we describe new events from _combinations_ of existing events.
- The #Union of two event, $E_1$ and $E_2$, denoted $E_1 \cup E_2$, is the set of outcomes that belong __either__ to $E_1$, to $E_2$, or to _both_, i.e. "$E_1$ __or__ $E_2$"
- The #Intersection of two events $E_1$ and $E_2$, denoted $E_1 \cap E_2$, is the set of outcomes that belong both to $E_1$ and to $E_2$, i.e. "$E_1$ __and__ $E_2$"
- The #Complement of an event $E$, denoted; $E^C$, $\bar{E}$, or $\neg E$, is the set of outcomes that __do not belong__ to E, i.e. "Not $E$"
$\,$
![[Pasted image 20230215143247.png|400]]
```


&nbsp;

---

# Mutually Exclusive Events

```ad-important
title: Definition
The events $E_1$ and $E_2$ are said to be #Mutually_Exclusive if they have _no outcomes_ in common.
More generally, a collection of events $E_1, \, E_2, \, \dots \, , \, E_n$ is said to be mutually exclusive if _no two_ of them have any outcomes in common.
$\,$
![[Pasted image 20230215143648.png|250]]
```

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

```ad-important
title: ###### Axioms of Probability
The probability theory is built based on _three commons sense rules_, known as #Axioms .
$\,$
> 1. Given the sampe sapce $S$, $P(S) = 1$.
> 2. For any vent $E$, $0 \leq P(E) \leq 1$.
> 3. If $E_1$ and $E_2$ are #Mutually_Exclusive events, i.e $(E_1 \cap E_2) = \emptyset$, then $P(E_1 \cup E_2) = P(E_1) + P(E_2)$. And more generally, if $E_1, \, E_2, \, \dots \, , \, E_k$, then $P(E_{1} \, \cup \, \dots \cup E_{k}) = P(E_{1}) + \dots + P(E_{k})$.
```
^180053

These axioms imply the following results: 
$$\begin{array}

P(E^C) = 1 - P(E), \\
\, \\
P( \emptyset ) = 0

\end{array}$$ 
^05edc8

&nbsp;


```ad-example
title: EXAMPLE 1
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
```

&nbsp;

When the model of _equally likely outcomes_ is assumed, the probabilites are chosen to be _equal_.
> If $S$ is a #Sample_Space containing $N$ equally likely outcomes, and if $E$ is an event containing $k$ outcomes, then:
> $$P(E) = \frac{k}{N}$$
> _Whenever a sample space consists of N possible outcomes that are equally likely, the probability of each outcome is $\frac{1}{N}$_

&nbsp;

```ad-example
title: EXAMPLE 2
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
> $$P(\text{too short}) = \frac{10 + 3 + 5}{1000} = \frac{18}{1000} = 0.018$$
```

^1bd154

&nbsp;

---

# The Addition Rule

```ad-note
if $E_1$ and $E_2$ are #Mutually_Exclusive events, then $P(E_1 \cup E_2) = P(E_1) + P(E_2)$
```

^6f35b9

&nbsp;

```ad-example
title: EXAMPLE 3
> Refer to [[#^1bd154|Example 2]], if a rod is sampled at random, what is the probability that it is either too short or too thick?
> 
> ---
> __*SOLUTION 1:*__
> Of the 1000 outcomes, the number that are either too short or too thick is: 
> $$10+3+5+4+13 = 35$$
> Thus:
> $$P(\text{too short or too thick}) = \frac{35}{1000}$$
> ---
> 
>__*SOLUTION 2:*__
> $$\begin{array}
> .P(\text{too short}) = \frac{18}{1000}, \quad \quad P(\text{too thick}) = \frac{22}{1000}, \quad \quad P(\text{ too short and too thick}) = \frac{5}{1000} \\ \\
> \, \\
> P(\text{too short or too thick}) \, = \, P(\text{too short}) \, + \, P(\text{too thick}) \,  - \, P(\text{too short and too thick}) \\
> = \frac{18}{1000} + \frac{22}{1000} - \frac{5}{1000} = \frac{35}{1000}
> \end{array}$$
```

&nbsp;

```ad-important
title: ###### Addition Rule
The probability of #Union of the events $E_1$ and $E_2$ is:
$$P(E_1 \cup E_2) = P(E_1) + P(E_2) - P(E_1 \cap E_2)$$
```

^6e895a

````ad-abstract
title: Proof
```ad-note
Note first that $E_1 \cup E_2$ can be decomposed into two _disjoint_ events $E_1$ and $E_1^C \cap E_2$ and thus,
$$P(E_1 \cup E_2) = P(E_1) + P(E_1^C \cap E_2)$$
```
Similiarly, $E_2$ is union of the two disjoint events $E_1 \cap E_2$ and $E_1^C \cap E_2$. Hence:
- $P(E_2) = P(E_1 \cap E_2) + P(E_1^C \cap E_2)$ which can be rearranged as:
- $P(E_1^C \cap E_2) = P(E_2) - P(E_1 \cap E_2)$ and then subsituted into the formula in the note above to obtain the formula of the #Addition_Rule

````

&nbsp;

---

# Counting Methods

When computing probabilties, it is sometimes necessary to determine the number of outcomes in a #Sample_Space .

$\,$

````ad-example
title: EXAMPLE 4
> A certain make of automobile is available in any of three colours: red, blue, or green, and comes with either a large or small engine. In how many ways can a buyer choose a car?
> 
> | | |__*Red*__|__*Blue*__|__*Green*__|
> |---:|---|:---:|:---:|:---:|
> || ||||
> |__*Large*__| |Red, Large|Blue, Large|Green, Large|
> |__*Small*__| |Red, Small|Blue, Small|Green, Small|

```ad-note
If an operation can be performed in $n_1$ ways, and if for each of these ways, a second operation can be performed in $n_2$ ways, then the total number of ways o perform the two operations is $n_1 \times n_2$.
```
````

&nbsp;

```ad-example
title: EXAMPLE 5: (Counting with Repetition)
> How many unique passwords can be made with 4 digits?
> 
> ---
> __*SOLUTION:*__
> $10 \times 10 \times 10 \times 10 = (10)^4$
```

$\,$

```ad-example
title: EXAMPLE 6: (Counting without Repetition)
> Three members from a 20-member cimmittee are to be randomly selected to serve as chair, vice-chair, and secretary.
> The first person selected is the chair, the second is the vice-chair, and the third is the secretary.
> How many different committee structures are possible?
> 
> ---
> __*SOLUTION:*__
> $20 \times 19 \times 18 = 6840$
```
^8a785a

&nbsp;

## Permutations

````ad-important
title: ###### Permutations
> A #Permutation is an ordering of a collection of objects.
- The fundamental principle of counting can be used to determine the number of _permutations_ of any set of objects.
- For example, there are six permutations of the set of letters $\{ A,B,C \}: ABC, \, ACB, \, BAC, \, BCA, \, CAB, \,, CBA$
- Therefore, the number of permutations for $n$ _distinct objects_ can be obtained as:
$$n(n-1) \dots (3)(2)(1)$$

```ad-note
For any positive integer $n \geq 0$, the __*factorial symbol*__, $n!$, is defined as follows;
$$n! = n(n-1) \dots (3)(2)(1) \quad \quad \quad \quad \quad \quad \quad \quad 0! = 1, \quad \text{and} \quad 1! = 1.$$
```
````


- In [[#^8a785a|Example 6]], we found the number of ways that we can randomly choose three memebrs from a 20-member committee to serve as chair, vice-chair, and secretary.
- The reasoning that we used to solve this problem can be generalised to the case where we want to choose $k$ objects in an _ordered_ arrangement from $n$ different objects as:
$$\begin{array}
(n)(n-1) \dots (n-k+1) &=& \frac{n(n-1) \, \dots \, (n-k+1)(n-k) \, \dots \, (2)(1)}{(n-k) \, \dots \, (2)(1)} \\
&=& \frac{n!}{(n-k)!}
\end{array}$$

```ad-note
The number of permutations of $k$ objects chosen from a group of $n$ objects is:
$$\frac{n!}{(n-k)!}$$
```

^f30062

## Combinations

- In some cases, when choosing a set of objects from a larger set, we _do not_ care about the ordering of the chosen objects.
- Each distinct group of objects that can be selected, without regard to order, is called a #Combination 

```ad-important
title: Combinations
__Number of Combinations of__ $k$ __Objects Chosen from__ $n$ __Objects:__
The number of different arrangements of $k$ objects chosen from $n$ objects, in which:
1. The _order_ is not important
2. The $n$ objects are _distinct_
3. Repetition of objects is not allowed

is given by:
$$\begin{pmatrix}
n \\
k
\end{pmatrix}
= \frac{n!}{k!(n-k)!}$$
```

^477096


&nbsp;

> Sometimes we are interested in counting the number of ordered sequences for objects that are _not at all different_.

```ad-example
title: EXAMPLE 7
> Assume that in a class of 12 students, a project is assigned in which the students will work in groups. Three groups are to be formed, consisting of 5, 4, and 3 students. Calculate the number of ways in which the groups can be formed.
>
> ---
> __*SOLUTION:*__
> The process of dividing the class into 3 groups is performed _sequentially_, as follows:
> 1. First, we choose 5 students from the total 12 students that can be done in, $\begin{pmatrix}12 \\ 5 \end{pmatrix} = \frac{12!}{5!7!}$ different ways.
> 2. Second, we choose 4 students from the remaining, $12 - 5 = 7$, students to form the second group. This can be done in, $\begin{pmatrix}7\\4\end{pmatrix} = \frac{7!}{4!3!}$, different ways.
> 3. Third, we choose 3 students from the remaining, $7-4=3$, students to form the third group. This can be done in $\begin{pmatrix}3\\3\end{pmatrix}=\frac{3!}{3!0!}$, diferent ways.
> 
> The third step above is not necessary as group 3, automatically consists of 3 students onc groups 1 and 2 have ben formed.
> 
> Notice that the _numerator_ in the final answer is the _factorial of the total group size_, while the denominator is the product of the factorials of teh sizes and groups chosen from it. This holds in general.

```ad-note
The number of ways of dividing a group of $n$ objects into groups of $k_1, \dots , k_{\mathcal{l}}$ objects, where $k_1 + \dots + k_{\mathcal{l}} = n$, is:
$$\frac{n!}{k_1! \dots k_{\mathcal{l}}!}$$
```

&nbsp;

---


# Conditional Probability

> That the #Sample_Space, $S$, contains all the possible outcomes of an experiment.
> Sometimes, we obtain some additional information about an experiment telling us that the outcome comes from a #Subset of $S$.
> Thus, the probability of an event is based on the _outcomes in a subset_ of $S$.

```ad-important
title: Definition
A probability that is based on a part of a #Sample_Space is called a #Conditional_Probability .
```

> In [[#^1bd154|Example 2]], we discussed a population of 1000 aluminium rods where each rod was classified as too short, too long, or OK, and the diameter was classified as too thin, too thick, or OK. We calculated $P(\text{too short})$ considering the entire sample space. This probability is called #Unconditional_Probability.

- Now, in [[#^1bd154|Example 2]], assume that a rod is sampled, and its length is measured and found to meet specification. What is the probability that the diameter _also_ meets the specification.
- The knowledge that the __*length meets the specification*__ reduces the sample space to 942 rods.

- Of the 942 rods in this sample space, 900 of them meet the diameter specification. Thus, $P(\text{diameter OK, {GIVEN}, length OK}) = \frac{900}{942}$.
- Hence the #Conditional_Probability that the rod meets the diameter specification __given__ that it meets the length specification is represented as;
$$P(\text{diameter OK | length OK})=\frac{900}{942}$$

&nbsp;

```ad-example
title: EXAMPLE 8
> Compute the _conditional probability_ $P(\text{diameter OK | length too long})$. Is this the same as the _unconditional probability_ $P(\text{diameter OK})$?
> 
> ---
> __*SOLUTION*__
> Of the 40 outcomes, 25 meet the diameter specification, thus:
> $$P(\text{diameter OK | length too long}) = \frac{25}{40}$$.
> The unconditional probability is $P(\text{diameter OK}) = \frac{928}{1000}$.
> The _denominator_ of the conditional probability, $\frac{25}{40}$, represents the number of outcomes that satisfy the condition that <u>the rod is too long</u>. While the _numerator_, $25$, represents the number of outcomes that satisfy both the condition that <u>the rod is too long __and__ that the diameter is OK.</u>
> $$\begin{array}
.P(\text{diameter OK | length too long}) &=& \frac{\frac{25}{1000}}{\frac{40}{1000}}  \\
&=& \frac{P(\text{diameter OK and length too long})}{P(\text{length too long})}
\end{array}$$

Based on this resoning, we can construct a definition for the #Conditional_Probability that holds for __any__ #Sample_Space .

```ad-note
title: Definition
Let $E_{1}$ and $E_{2}$ be events with $P(E_{2}) \neq 0$. The conditional probability of $E_1$ given $E_2$ is:
$$P(E_{1} | E_{2}) = \frac{P(E_{1} \cap E_{2})}{P(E_{2})}$$
```

^6e6ea1

&nbsp;

---

# Independant Events

- Sometimes the knowledge that one event has occured does not change the probability that another event occurs.
- Thus, _conditional_ and _unconditional_ probabilites are the smae, and such events are said to be __#Independant__. This implies that $P(E_{1} \cap E_{2} = P(E_{1})\cdot P(E_{2})$.

```ad-important
title: Defintion
Two events $E_1$ and $E_2$ are independant, if the probability of each event remains the same whether or not the other one occurs.
If $P(E_1) \neq 0$ and $P(E_2) \neq 0$, then $E_1$ and $E_2$ are independant if:
$$P(E_1 | E_2) \, = \, P(E_1 | E_2^C) \, = \, P(E_1) \quad \quad \text{or,} \quad \quad P(E_2 | E_1) \, = \, P(E_2 | E_1^C) \, = \, P(E_2)$$
If either $P(E_1) = 0$ or $P(E_2) = 0$, then $E_1$ and $E_2$ are independant. 
```

^bb853a

&nbsp;

```ad-important
title: Definition
- Events $E_1 , \, E_2, \, \dots, \, E_n$ are independant if the probability of each remains the same no matter which of the others occur.
- Events $E_1 , \, E_2, \, \dots, \, E_n$ are independant if and _only if_ for any subset of these events $E_{i_{1}} , \, E_{i_{2}}, \, \dots, \, E_{i_{k}}$, 
$$P(E_i | E_{i_{1}} \cap \, \dots \, \cap E_{i_{k}} = P(E_{i})$$
and,
$$P(E_{i_{1}} \cap E_{i_{2}} \cap \, \dots \, \cap E_{i_{k}}) = P(E_{i_{1}}) \times P(E_{i_{2}}) \times \, \dots \, \times P(E_{i_{k}})$$
```

^4ccd06

&nbsp;

```ad-warning
title: Exercise:
Find $P(\text{too long})$ and $P(\text{too long | too thin})$ in [[#^6e6ea1|Example 8]].
	- Are these probabilites different?
Comment on the independance of the events $E_1$, the rod being too long, and $E_2$, the rod being too short.
```

&nbsp;

---
# The Multiplication Rule

Sometimes, we know $P(E_{1}|E_{2})$ or $P(E_{2}|E_{1})$, and we wish to find $P(E_{1}\cap E_{2})$. Using the formula for [[#^6e6ea1|conditional probability]], given that $P(E_1) \neq 0$ and $P(E_2) \neq 0$,
$$P(E_{1}\cap E_{2}) \, = \, P(E_{2})\cdot P(E_{1}|E_{2}) \, = \, P(E_{1})\cdot P(E_{2}|E_{1})$$ ^555ae9

If events $E_1$ and $E_2$ are #Independant:
$$P(E_{1} \cap E_{2}) = P(E_{1}) \cdot P(E_{2})$$ ^2b06dc

This result can be extended to any number of independant events $E_1 , \, E_2, \, \dots, \, E_n$, i.e,
$$P(E_{1} \cap E_{2} \cap \, \dots \, \cap E_{n}) = P(E_{1})  P(E_{2}) \, \cdots \, P(E_{n})$$ ^0cb1d9

&nbsp;

---
# The Law of Total Probability

> Consider the #Sample_Space in the figure below that contains the #Mutually_Exclusive events $A$ and $A'$.
> 
> ![[Pasted image 20230216230251.png|200]]
>
>From this figure, it is clear that the events $B \cap A$ and $B \cap A'$ are also #Mutually_Exclusive and their union forms the event $B$. Therefore,
>$$\begin{array}
.P(B) = P[(B \cap A) \cup (B \cap A')] &=& P(B \cap A) + P(B \cap A')  \\
&=& P(B|A) \cdot P(A) \, + \, P(B|A') \cdot P(A')
\end{array}$$

$\,$

> Given the mutually exclusive sets, $E_1 , \, E_2, \, \dots, \, E_n$, this result can be generalised as:
> $$\begin{array}
.P(B) &=& P(B\cap E_{1}) + \, \cdots \, + P(B \cap E-n) \\
&=& \sum_{i=1}^{n} P(B|E_{i}) \cdot P(E_{i})
\end{array}$$
>![[Pasted image 20230216231059.png|200]]

&nbsp;

```ad-example
title: EXAMPLE 9

```

> Customers who purchase a certain make of car can order an engine in any of three _small, medium and large_ sizes. The percentage of sold cars with different engine sizes together with the failure rate in emissions test within two years of purchase are presented in the table below. 
> - What is the probability that a randomly chosen car will fail an emissions test within two years?
> 
> ||||
> |:---:|:---:|:---:|
> |__*Engine Size*__|__*Percentage of all cars sold*__|__*Emission test failure rate*__|
> ||||
> |Small|45%|10%|
> |Medium|35%|12%|
> |Large|20%|15%|
> ||||
> 
> ---
>__*SOLUTION:*__
> Let $B$ denote the event that a car _fails_ emissions test, and $A_1$, $A_2$, and $A_3$ denote the events that a car has a small, medium, or large engine size respectively. Thus, $P(A_1) = 0.45$, $P(A_2) = 0.35$, and $P(A_3) = 0.20$
> 
> The probabilities that a car fails a test given different engine sizes are stated in the problem, i.e $P(B|A_1) = 0.10$, $P(B|A_2) = 0.12$, and $P(B|A_3) = 0.15$. Thus, using #Law_of_Total_Probability, we have:
> $$\begin{array}
P(B) \, &=& \, \sum_{i=1}^{3} P(B|A_{1}) \cdot P(A_{1}) \\
&=& (0.10)(0.45) + (0.12)(0.35) + (0.15)(0.20) = 0.117
\end{array}$$
>
> ---
> __*Alternate Solution:*__
> Sometimes, problems like this example are solved using #Tree_Diagrams 
> 
> ![[Pasted image 20230216233257.png|300]]

---
# Bayes' Theorem
---
# Application to Reliability Analysis
---
