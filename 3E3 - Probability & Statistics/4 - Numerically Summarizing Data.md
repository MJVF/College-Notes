---
tags:
- Qualitative
- Histograms
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
	- [[#Measures of Variability (Dispersion)]]
	- [[#Grouped Data]]
	- [[#Percentiles & Quartiles]]
	- [[#Box Plots]]

&nbsp;

#### Formulas:
- Sum of Data [[#^15edd5| .1]]
- Sample Mean [[#^1ebce1| .2.1]] & [[#^0cfe0b| .2.2]]
- Population Mean [[#^2a8dfb| .3]]
- Trimmed mean ($p\%$) [[#^28e174| .4]]
- Sample Variance ($s^2$) [[#^90b40a| .5.1]] & [[#^a80352| .5.2]]
- Standard Deviation ($s$) [[#^12dce8| .6.1]] & [[#^a80352| .6.2]]
- Coefficient of Variation (CV) [[#^981bb1| .7]]


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
> of the number of children. ^049e73
> ---
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
> ---
>__*SOLUTION:*__
>- [[#^1ebce1|Mean]] is found by averaging all numbers as $195.42$
>$$\,$$
>- Since $n=24$, the [[#The Sample Median|Median]] is the average of the observations with rank $12$ and $13$, i.e. $\frac{(191+223)}{2} = 207$
>$$\,$$
>- To calculate the $5\%$ #Trimmed_Mean , we must drop $5\%$ of the data from each end, i.e. $\frac{5 \times 24}{100} = 1.2$ which is rounded off to $1$.
>- Similiary, to compute $10\%$ and $20\%$ trimmed mean values, we round off $\frac{10 \times 24}{100} = 2.4$ and $\frac{20 \times 24}{100} = 4.8$ to $2$ & $5$ respectively.
>- __Thus__, the $5\%, 10\%$ and $20\%$ trimmed means can be found as $190.45$, $186.55$ and $194.07$, respectively.

&nbsp;

## Symmetry and Skewness

> - A [[3 - Describing Data#Histogram|histogram]] is perfectly #Symmetric if its right half is a _mirror image_ of its left half.
> ![[Pasted image 20230212200316.png|250]]

&nbsp;

> - Histograms that are not symmetric are reffered to as #Skewed . In practice, no [[2 - Sampling|sample]] has a perfectly symmetric histogram.

$\,$

> - A histogram with a long _right-hand_ tail is said to be __*skewed to the right*__, or __*Positively Skewed*__.
> ![[Pasted image 20230212200902.png|250]]
> - For a histogram that is _skewed to the right_, the __mean is greater than the median__ as the mean is near the #center-of-mass of the histogram.


$\,$

> - A histogram with a long _left-hand_ tail is said to be __*skewed to the left*__, or __*Negatively Skewed*__.
> ![[Pasted image 20230212201151.png|250]]



&nbsp;


## Measures of Variability (Dispersion)

> The following measures show the amount of #Dispersion in the variable. Dispersion is the degree to which the data are __spread out__.

&nbsp;

1. ###### Range
The #Range, $R$, is the _difference between_ the _largest_ and the _smallest_ values in a sample. i.e:
$$R = x_{(n)} - x_{(1)}$$
This is simple to calculate, but is very _sensitive to **extreme values**_.
Since it depends only on the two extreme values, it is _rarely used_, as it provides _no information_ about the rest of the sample. ^142d94

&nbsp;

2. ###### Sample Variance
The #Sample_Variance measures how closely the data are placed around the mean.
If all the data are _equal_, then the _variance will be zero_. The more dispersed data around the mean, the greater the variance.
The sample variance is given by $s^2$, where:
$$s^{2} = \frac{1}{n-1} \sum_{i=1}^{n} (x_{i} - \bar{x} )^{2} = \frac{1}{n-1} \big{(}\sum_{i=1}^{n} x_{i}^{2} - n \bar{x}^{2} \big{)}$$
It is a measure of the average squared __deviations__ from the #Mean . ^90b40a
> __*Note:*__ A serious _drawback_ of the sample variance as  a #Measure_of_Spread is that its _units are different_ than the sample values, i.e. they are the squared units.

&nbsp;

3. ###### Standard Deviation
To obtain a #Measure_of_Spread whose units are _the same_ as those of the sample values, we simply take the _square root of the variance_. This quantity is known as the __*Sample #Standard_Deviation*__, $s$, where:
$$s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_{i} - \bar{x} )^{2}} = \sqrt{ \frac{1}{n-1} \big{(}\sum_{i=1}^{n} x_{i}^{2} - n \bar{x}^{2} \big{)}}$$
It is _preferred_ to the variance as a descriptive measure, since it is a measure of the _average distance_ of an observation from the mean.
It is thus measured in the _same units_ as the observations themselves.
>__*Note:*__ On scientific calculators the standard deviation is noted as $s_{n-1}$ or $\sigma_{n-1}$ ^12dce8

&nbsp;

4. ###### Coefficient of Variation
The #Coefficient_of_Variation (CV) is a measure that allows for comparison in spread between two or more data sets by describing the amount of _spread per unit mean_.
$$CV = \frac{s}{\bar{x}}$$
CV is calculated by dividing the [[#^12dce8|standard deviation]] by the [[#^1ebce1|sample mean]]. The sample with the largest CV has the largest __relative spread__.
A major advantage of the coefficient of variation is that it is _unitless_ and thus, it is _inensitive to units_. ^981bb1

&nbsp;

&nbsp;

> __*EXAMPLE 3:*__
> For the following data sets, calculate the Coefficient of Variation:
> $$
> \mathcal{D}_{1} = \{ 100, 100, 100 \} \quad \quad
> \mathcal{D}_{2} = \{  90, 100, 110 \} \quad \quad
> \mathcal{D}_{3} = \{ 8, 10, 12, 14, 16, 18, 20 \}
> $$
> ---
>__*SOLUTION:*__
> 1. Since all the data in $\mathcal{D}_{1}$ is constant, its _standard deviation_ is 0, and its average is 100. Thus,  $CV_{1}\% = 100 \times (\frac{0}{100}) = 0\%$
> 2. The data in $\mathcal{D}_{2}$ has more _variability_. Its _standard deviation_ is 10 and its average is 100. Thus, $CV_{2}\% = 100 \times (\frac{10}{100}) = 10\%$
> 3. The data in $\mathcal{D}_{3}$ has more _variability_ again. Its _standard deviation_ is approximately 4.32, and its average is 14. Thus, $CV_{3}\% = 100 \times (\frac{4.32}{14}) \approx 30.85\%$

&nbsp;

>__*EXAMPLE 4:*__
>Consider the data set in [[#^049e73|Example 1]]:
>$$0,0,0,0,1,1,2,2,2,3,3,4,4,6$$
>Calculate the #Sample_Variance , #Standard_Deviation , #Range , and #Coefficient_of_Variation .
> ---
>__*SOLUTION:*__
> 1. In Example 1, we calculated $\bar{x} = 2$, thus, the [[#^90b40a|sample variance]] can be obtained as:
> $$\begin{eqnarray}
 s^{2} &=& \frac{1}{n-1} \sum_{i=1}^{n} (x_{i} - \bar{x} )^{2}  \\
 &=& \frac{4\cdot(0-2)^{2} + 2\cdot(1-2)^{2} + 3\cdot(3-2)^{2} + 2\cdot(4-2)^{2} + (6-2)^{2}}{13} \\
 &=& \frac{44}{13} \approx 3.3846
 \end{eqnarray}$$
 > 2. The [[#^12dce8|standard deviation]] is given by:
 > $$s = \sqrt{s^{2}} = \sqrt{3.3846} \approx 1.8397$$
 > 3.  As the largest and smallest observations are 6 and 0 respectively the [[#^142d94|range]] is given by:
 > $$R = 6 - 0 = 6$$
 > 4. The [[#^981bb1|coefficient of variance]] is given by:
 > $$CV = \frac{1.8397}{2} \approx 0.9199$$

^1f7186

&nbsp;


## Grouped Data

Data from a [[1 - Data Collection#^ede962|discrete]] distribution may well be displayed in tabular form, e.g. the data from the [[#^1f7186|previous]] example may be presented as:

| | | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|Number of children|0|1|2|3|4|5|6|
|Number of families|4|2|3|2|2|0|1|
| | | | | | |

- The _first row_ gives the _value_ of the observation $x_{i}$ (here, no. of children).
- The _second row_ gives the _frequency_ of each observation $n_{i}$ (no number of observations of $x_{i}$ children). The _sum_ of these numbers is the total number of observations.
- Since $3$ families have $2$ children, these families account for $3 \times 2 = 6$ children (in mathematical notation $n_{3} \times 2$, where $n_{3}$ is the number of time $2$ children were observed).
$\,$
- It can be seen that summing $x_{i} \cdot n_{i}$ over all the possible observations of the variable (number of children), we obtain the sum of the observations.
- It follows that the #Sample_Mean is given by:
$$\bar{x} = \frac{\sum x_{i} \cdot n_{i}}{\sum n_{i}}$$ ^0cfe0b
- Similiarly, the #Sample_Variance and #Standard_Deviation are given by:
$$
s^{2}= \frac{\sum_{i} (x_{i} - \bar{x})^{2} \cdot n_{i}}{(\sum_{i} n_{i}) - 1},
\quad \quad \quad \quad \quad \quad \quad \quad
s^{2}= \sqrt{\frac{\sum_{i} (x_{i} - \bar{x})^{2} \cdot n_{i}}{(\sum_{i} n_{i}) - 1}}
$$ 
^a80352
- where $n = \sum_{i} n_{i}$ is the total numbr of observations. 




&nbsp;

## Percentiles & Quartiles
$\quad$
## Box Plots
$\quad$





![[Pasted image 20230209180125.png]]

---