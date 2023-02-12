---
tags:
- Qualitative
---


### Glossary:
- [[#Numerical Methods]]
	- [[#Notation and Measures of Centrality]]
	- [[#The Sample and Popoulation Means]]
	- [[#The Sample Median]]
	- [[#The Sample Mode]]
	- [[#Outliers]]
	- [[#Trimmed Mean]]
	- [[#Symmetry and Skewness]]
	- [[#Measures of Variability]]
	- [[#Grouped Data]]
	- [[#Percentiles & Quartiles]]
	- [[#Box Plots]]

&nbsp;

#### Formulas:
- Sum of Data [[#^15edd5| .1]]
- Sample Mean [[#^1ebce1| .2]]
- Population Mean [[#^2a8dfb| .3]]
- Trimmed mean ($p\%$) [[#^28e174| .4]]


&nbsp;

--- 

# Numerical Methods

##### [[3 - Describing Data#Organizing and Summarizing Qualitative Data|Organizing and Summarizing Qualitative Data]]
> The most common measures (statistics) used to describe numerical variables can be classified into two categories.
> $\quad$ 1. Measures of #Centrality , i.e _measure of the **centre** of the distribution_.
> $\quad$ 2. Measures of #Variability , i.e _the **spread**, **dispersion** of the data_.

&nbsp;

## Notation and Measures of Centrality

- Let $x$ denote a particular numerical variable, e.g _height_.
- Considering $n$ observation of this variable ( in the same sequence as they are observed ),
- $$x_{1} , \, x_{2} , \, . . . \, , \, x_{n} ,$$
- then $n$ ordered observations are denoted by:
- $$x_{(1)} , \, x_{(2)} , \, . . . \, , \, x_{(n)} ,$$
- where  $x_{(1)} \leq x_{(2)} \leq \, . . . \leq x_{(n)}$. This is simply a list of the obervations from the smallest to the largest.
- If a value appears $k$ times in the sample, it must appear $k$ times in this ordered list.
- In this case, the __*index is the rank of the obersvation*__.

&nbsp;

## The Sample and Popoulation Means


>The __*Sum of the Data*__ is denoted by:
> $$\sum_{i=1}^{n}x_{i} =  x_{1} , \, x_{2} , \, . . . \, , \, x_{n}.$$

^15edd5

> The #Sample_Mean (which we _observe_) is given by $\bar{x}$, where:
> $$\bar{x} = \frac{1}{n} \sum_{i=1}^{n}x_{i}$$

^1ebce1

> The #Population_Mean (which we _do not observe_) is given by $\mu$, where:
> $$\mu = \frac{1}{N} \sum_{i=1}^{N}x_{i}$$
> where $N$ is the [[1 - Data Collection#^a9f7af|population]] size.

^2a8dfb

&nbsp;

## The Sample Median

- When $n$ is __odd__, the #Sample_Median , denoted by _'Med'_, is the observation that appears in the _middle of the list_ of ordered observations.
- When $n$ is __even__, the #Sample_Median is the _average_ of the two observations in the middle of the list.

- That is to say,
	1. For __odd__ values of $n$, the #Median has rank $\frac{n+1}{2}$.
	2. For __even__ values of $n$, the #Median is the average of the two observations with ranks $\frac{n}{2}$ and  $\frac{n}{2} + 1$.

>__*NOTE:*__ Half the data are less than or equal to the median and the other half the data are __*strictly greater*__ than the median.

&nbsp;

## The Sample Mode

> The #Mode is useful when we are dealing with [[1 - Data Collection#^ede962|discrete]] or _categorised_ data. (__*not*__ [[1 - Data Collection#^b37fbc|continuous]] data)
> The mode is the _observation_ (or category, as appropriate) that occurs most frequently in a sample.

&nbsp;

### Examples: Mean, Median, Mode

> __*EXAMPLE 1:*__
> The number of children in 14 fmilies is given below:
> $\quad \quad \quad$ 4, 2, 0, 0, 4, 3, 0, 1, 3, 2, 1, 2, 0, 6.
> 
> Calculate: 
> $\quad$ 1. the mean;
> $\quad$ 2. the median;
> $\quad$ 3. the mode,
> of the number of children.

>__*SOLUTION*__
>1. the mean:
>$$\bar{x} = \frac{4+2+0+0+4+3+0+1+3+2+1+2+0+6}{14} = 2$$
>
>2. the median:
>Since $n=14$, the median will be the average of the observations with rank $7$ and $8$. Ordering these observations, we obtain:
>$$0,0,0,0,1,1,2,2,2,3,3,4,4,6$$
>The $7^{th}$ and $8^{th}$ observations in this list are both $2$. Thus, the Median is 2.
>
>3. the mode:
>0 appears most frequently, 4 times, thus the mode is 0.

&nbsp;

## Outliers

The #Mean is much more sensitive to _extreme values_ or errors in data, i.e. #Outliers , then the #Median .

![[Pasted image 20230212153240.png|600]]

> For Example:
> 
> |**Data Set 1:** 3.7, 4.6, 3.9, 3.7, 4.1$\: \: \: \: \: \:\: \: \:$|**Data Set 2:** 37, 4.6, 3.9, 3.7, 4.1$\: \: \: \: \: \:\: \: \:$|
> |---|---|
> |median: 3.9 $\: \: \: \: \: \:\: \: \:$mean: 4           |median: 4.1$\: \: \: \: \: \:\: \: \:$mean: 10.66|
> 
> __*Note:*__ Outliers are a real problem for data analysts. If a population truly contains outliers, but they are deleted from the sample, the sample will not characterise the population correctly.

&nbsp;

##### Use of Median for #Asymmetric Distributions 

> If the distribution ([[3 - Describing Data#Histogram|histogram]]) is #Symmetric or close to symmetric, then;
> $$\bar{x} \approx Median$$
> In this case, the sample might contain a #Outliers . Either measure may be used, (the #Mean is normally used as it has _nicer statistical properties_).
> If the distribution is _clearly_ #Asymmetric these measures will be _significantly_ different.
> In this case, the #Median should be used as a measure of #Centrality , since there will be outliers which have a large influence on the mean.
> 
>![[Pasted image 20230212154329.png]]

&nbsp;

## Trimmed Mean 
$\,$
Like the #Median , the #Trimmed_Mean is a _measure of center_ that is designed to be _unaffected_ by #Outliers .
$\,$
The trimmed mean is computed by arragning the [[1 - Data Collection#Sampling|sample]] values in order, __*"trimming"*__ an _equal_ number of them from each end,
	- e.g: $p\%$, which is called __$p\%$ trimmed mean__.
$\,$
There are no hard-and-fast rules on how many _values to trim_. The most _commonly used trimmed means_ are the $5\%, 10\%$ and $20\%$ trimmed means.
$\,$
Since the number of data points trimmed __must be a whole number__, it is impossible in many cases to trim the _exact percentage_ of data.
$\,$
In this case, the simplest thing to do is to round $\frac{n \cdot p}{100}$ to the nearest whole number and trim that amount. (where $n$ is the sample size.) ^28e174

&nbsp;

>__*EXAMPLE 2:*__
> In this article "__Evaluation of Low-Temperature Properties of HMA Mixtures__" (P. Sebaaly, A. Lake, and J. Epps, Journal of Transportation Engineering, 2002: 578–583), the following values of _fracture stress_ (in _mega pascals_) were measured for a sample of $24$ mixtures of hot-mixed asphalt (_HMA_).
> $$30 \: \quad 75 \: \quad 79 \: \quad 80 \: \quad 80 \: \quad 105 \quad 126 \quad 138 \quad 149 \quad 179 \quad 179 \quad 191$$
> $$223 \quad 232 \quad 232 \quad 236 \quad 240 \quad 242 \quad 245 \quad 247 \quad 254 \quad 273 \quad 384 \quad 470$$
> Compute the _mean_, _median_, and the $5\%, 10\%$ and $20\%$ trimmed means.

>__*SOLUTION*__
>- [[#^1ebce1|Mean]] is found by averaging all numbers as $195.42$
>$$\,$$
>- Since $n=24$, the [[#The Sample Median|Median]] is the average of the observations with rank $12$ and $13$, i.e. $\frac{(191+223)}{2} = 207$
>$$\,$$
>- To calculate the $5\%$ #Trimmed_Mean , we must drop $5\%$ of the data from each end, i.e. $\frac{5 \times 24}{100} = 1.2$ which is rounded off to $1$.
>- Similiary, to compute $10\%$ and $20\%$ trimmed mean values, we round off $\frac{10 \times 24}{100} = 2.4$ and $\frac{20 \times 24}{100} = 4.8$ to $2$ & $5$ respectively.
>- __Thus__, the $5\%, 10\%$ and $20\%$ trimmed means can be found as $190.45$, $186.55$ and $194.07$, respectively.

&nbsp;

## Symmetry and Skewness



&nbsp;


## Measures of Variability
```
Examples:
 - Sample Range
 - Variance
 - Standard Deviation
``` 

$\quad$
## Grouped Data
$\quad$
## Percentiles & Quartiles
$\quad$
## Box Plots
$\quad$





![[Pasted image 20230209180125.png]]

---