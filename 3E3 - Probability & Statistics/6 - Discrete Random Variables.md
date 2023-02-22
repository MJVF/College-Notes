---
tags:
- Mean
- Expected_Value
- Expectation
- Variance
- Standard_Deviation
---


### Glossary:
- [[#Discrete Random Variables and Probability Distributions]]
	- [[#-Random Variables]]
	- [[#-Probability Distribution and Probability Mass Function]]
	- [[#-Cumulative Ditribution Function]]
	- [[#-Mean and Variance]]
	- [[#-The Expected Value of a Function]]
	- [[#-Expected Value and Variance Properties]]
	- [[#-Distribution of Discrete Random Variables]]

$\quad$


---

# Discrete Random Variables and Probability Distributions

## -Random Variables

A #Random_Variable is a function that assigns a _real number_ to each outcome in the #Sample_Space of a #Random_Experiment .
A randome variable is represented by an uppercase letter such as $X$ and the particular value of the corresponding random variable is denoted by a lowercase letter.
The notation $X(s) = x$ means that $x$ is the value associated with the outcome $s$ by the random variable $X$.
More formally, a random variable is a function whose domain is the sample space and whose [[4 - Numerically Summarizing Data#^142d94|range]] is the set of _real numbers_.
![[Pasted image 20230222144004.png|350]]

### Types of Random Variables

#### Continuous Random Variables
#Continous_Random_Variables are _random variables_ with an interval (either _finite or infinite_) of real numbers for its range while no possible value of the random variable has a positive probability, i.e $P(X=x_{0}) = 0$.
Some examples of the continuous random variables include:
	- _electrical current, length, pressure, temperature, time, voltage, weight._

&nbsp;

#### Discrete Random Variables
#Discrete_Random_Variables are _random variables_ with a _finite_ (or _countably infinite_) range.
Some examples of the discrete random variables include:
	- _number of transmitted bits received in error in a communication system, number of scratches on a surface, proportion of defective parts among 100 tested._

_also see:_ [[1 - Data Collection#^b9aa0d|Types of variables]]

&nbsp;

```ad-example
title: EXAMPLE 1
> Computer chips often contain surface imperfections. For a certain type of computer chip, 9% contain no imperfections, 22% contain 1 imperfection, 26% contain 2 imperfections, 20% contain 3 imperfections, 12% contain 4 imperfections, and the remaining 11% contain 5 imperfections.
> Let $X$ represent the number of imprfections in a randomly chosen chip. What are the possible values for $X$? Is $X$ _discrete or continuous_? Find $P(X=x)$ for each possible value $x$.
> 
> ---
> __*SOLUTION:*__
> The possible values for $X$ are the integers $0,1,2,3,4,5$. The random variable $X$ is _discrete_, as it takes only integer values. 9% of the outcomes in the sample space are assigned the value 0. Thus:
> 1. $P(X=1)=0.22$
> 2. $P(X=2)=0.26$
> 3. $P(X=3)=0.20$
> 4. $P(X=4)=0.12$
> 5. $P(X=5)=0.11$
```

^fa2be0

&nbsp;

---

## -Probability Distribution and Probability Mass Function

- The list of possible values for the random variable $X$ in the _previous example_, along with the probabilities for each, provide a complete description of the population from which $X$ is drawn.
- This description is called the #Probability_Mass_Function or the #Probability_Distribution

```ad-important
title: Definition
For a __Discrete Random Variable__ $X$ with possible values $X_1, X_2, \, \dots \, , X_n$, a probability mass function (PMF) is a function such that:
1. $f(x_i) = P(X=X_i)$
2. $f(x_i) \ge 0$
3. $\sum_{i=1}^{n} f(x_i) = 1$
```

&nbsp;

---

## -Cumulative Ditribution Function


In [[#^fa2be0|Example 1]], we might be interested in the probability of _three or fewer_ imperfections, i.e, $P(X \le 3)$.
Since the event $X \le 3$ is the union of the events $\{ X=0 \}, \, \{ X=1 \}, \, \{ X=2 \},$ and $\{ X=3 \},$
$$\begin{array}
P(X \le 3) &=& P(X=0) + P(X=1) + P(X=2) + P(X=3) \\
&=& 0.09 + 0.22 + 0.26 + 0.20 = 0.77
\end{array}$$
If we have a function that specifies the probability that a random variable is less than or equal to a given value, we can use this function to calculate the probability of different events, e.g, $P(X=3) = P(X \le 3) - P(X \le 2)$.
This function is called the #Cumulative_Distribution_Function 

&nbsp;

```ad-important
title: Definition
The __Cumulative Distribution Funciton (CDF)__ of a discrete random variable $X$, denoted as $F(x)$, is:
$$F(x) = P(X \le x) = \sum_{x_{i} \le x} f(x_{i})$$
This function satisfies the following properties.
1. $F(x) = P(X \le x) = \sum_{x_{i} \le x} f(x_{i}) = \sum_{x_{i} \le x} P(X=x_{i})$
2. $0 \le F(x) \le 1$
3. If $x \le y$, then $F(x) \le F(y)$

```

```ad-example
title: EXAMPLE 2
> The system below contains two components, $A$ and $B$, connected in series. The system will function only if both componenets function. The probability that $A$ and $B$ function is given by $P(A) = 0.96$, and $P(B) = 0.92$, respectively.
> Assume that $A$ and $B$ function _independantly_. Define a #Random_Variable $X$ for the system and find the corresponding __PMF__ and __CDF__ functions. 
> ![[Pasted image 20230222183016.png|250]]
>
> ---
> __*SOLUTION*__
> > Let us define $E_A$ as the event that the first device functions and $E_B$ as the event that the second device functions. There are 3 possible outcomes:
> 1. Both devices function.
> 2. Only one of the devices functions.
> 3. None of the devices function.
> 
> Which we map to $X=0$, $X=1$, and $X=2$, respectively. Thus, the __PMF__ is obtained by finding the probabilities $P(X=0)$, $P(X=1)$, and $P(X=2)$. Using these probabilites, we can also calculate the __CDF__.
> 1. $P(X=0) = P(E_{A} \cap P_{B}) = (0.96)(0.92) = 0.8832$
> 2. $P(X=0) = P(E_{A}^{C} \cap E_{B}) + P(E_{A} \cap P_{B}^C) = (1−0.96)(0.92)+ (0.96)(1−0.92) = 0.1136$
> 3. $P(X=2) = P(E_{A}^C \cap E_{B}^C) = (1 − 0.96)(1 − 0.92) = 0.0032$
> $$f(x) = \begin{cases}
0.8832, & X=0 \\
0.1136, & X=1 \\
0.0032, & X=3
\end{cases}$$
> #Cumulative_Distribution_Function $F(x)$ can be obtained as:
> 
> $$\begin{array}
.F(X = 0) = P(X \le 0) = 0.8832 \quad \quad \quad \quad \quad \quad \quad \quad \\
F(X = 1) = P(X \le 1) = 0.8832 + 0.1136 = 0.9968  &&&& F(x) = \begin{cases}
\mbox{0.8832}, & X=0 \\
\mbox{0.9968}, & X=1 \\
\mbox{1}, & X=2 
\end{cases} \\
\quad \, \, \, F(X = 2) = P(X \le 2) = 0.8832 + 0.1136 + 0.0032 = 1
\end{array}$$



```

&nbsp;

---

## -Mean and Variance

Left off here



&nbsp;

---

## -The Expected Value of a Function
$\quad$
## -Expected Value and Variance Properties
$\quad$
## -Distribution of Discrete Random Variables

$\quad$

---