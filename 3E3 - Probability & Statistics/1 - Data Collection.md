---
tags:
- Quantative
- Qualitative
- Ordinal
- Nominal
- Interval
- Ratio
---
### Glossary:
- [[#Classification of Different Data Types]]
- [[#Scale of Measurement]]
- [[#Sampling]]
- [[#Parameters and Statistics]]
- [[#Accuracy of Estimates]]
	- [[#Bias & Precision]]
	- [[#Non-sampling Bias]]

&nbsp;

---
# Classification of Different Data Types

###### <u>Data can be classified in two ways:</u>

- ###### __Quantative Data:__ ^726f4a
	- __Numeric Data__ that indicates how much or how many. e.g _height, mass, number of children_
	- Types:
		- __Continuous Variables:__ variables can take any value in a certain range. They are usually measured according to some scale. e.g _age, height, mass_ (measured to a given accuracy, i.e age in closest year)

		- __Discrete Variables:__ variables take values from a set that can be listed (commonly integer values). Such variables are often counted. e.g _number of children/subjects passed at leaving cert_ (when a discrete variable takes in a very large number of values, may be treated as continuous)

&nbsp;

- ###### __Qualitative Data:__ ^891e66
	- Normally __classifications__ or __groupings.__ e.g _gender, university department, social class_


----
# Scale of Measurement

- ###### [[#^891e66|Qualitative Data]] may be further split into: ^5afe74
	- __Nominal Classifications:__ Data defined by a _pure classification_, in which the _order_ of the classes has _no practical_ interpretation. e.g _discipline:_ ^a66ec0
		1. Civil
		2. Electronic
		3. Biomedical
		4. Mechanical
	- __Ordinal Classifications:__ _Order_ of classification is _important_. e.g:
		1. Non-smoker
		2. Light smoker
		3. Heavy smoker ^168b3f
		- i.e the higher a number, the more an individual smokes.

&nbsp;

- ###### [[#^726f4a|Quantitative Data]] may be further split into: 
	- __Interval Classifications:__ Like ordinal except we can say the intervals between each value are equally split. e.g:
		- <u>Temperature:</u> where the _difference_ between 29-30 celsuis is the same magnitude as the difference between 78-79 celsius. As zero temperature (0C/0F) are defined based on convention, there is no absolute zero.
		- <u>Time:</u> where we cannot say when the time started.
	- __Ratio Classifications:__ Interval data with an absolute zero point. e.g:
		- <u>Duration:</u> ratio since 0 duration is meaningful
		- <u>Temperature (Kelvin):</u> ratio since 0 Kelvin is an absolute value.

&nbsp;

|__Scale__|__Order__|__Distance__|__Relative Zero__|__Absolute Zero__|
|---|:---:|:---:|:---:|:---:|
|_Nominal_|❌|❌|❌|❌|
|_Ordinal_|✅|❌|❌|❌|
|_Interval_|✅|✅|✅|❌|
|_Ratio_|✅|✅|✅|✅|

Nominal is weakest, Ratio is strongest.

---
# Sampling

Suppose we wish to study a _particular group of individuals_ (or items), e.g. Irish voters, European students or all the bulbs manufactured in a company. 

> The __population__ in a study is the _entire group_ of individuals (or items) that we wish to investigate (as above).  

Since it is _impractical to observe all_ the individuals in a population, we _observe a sample_ of the population in question.  

> A __unit__ is any individual member of the population

![[Pasted image 20230209191726.png|400]]

&nbsp;

> A __sampling frame__ is a list of members of a population. It may be used to choose a sample.  

A sampling frame __may be incomplete or inaccurate__. For example, the Irish electoral register will be a complete sampling frame for the population of eligible voters in Ireland. However, it will not be a complete sampling frame for the population of adult Irish residents.

Choice of an _inappropriate sampling frame_ may well lead to _systematic errors in estimates_ obtained from sampling (__bias__).

If I tried to measure the mean IQ (or height) of the whole Irish population by _just observing a sample of Irish students_, I would _tend to overestimate_ this population mean.

---
# Parameters and Statistics

> A __parameter__ is a _numeric characterisation of the population_ (its value is usually unknown), e.g. 13% of all recent immigrants have professional occupations.  

> A __statistic__ is a _numeric characterisation of the sample_ (observed), e.g. 12.4% of individuals in our sample have professional occupations.  

_Statistics_ can be _used to estimate the parameters_ of the population, e.g. here we would estimate that 12.4% of all recent immigrants have professional occupations.

![[Pasted image 20230209192615.png|400]]

---
# Accuracy of Estimates

## Bias & Precision

As described above, if we use an _inappropriate sampling frame_, our estimates of parameters may have a _systematic bias_. Bias that results from our method of sampling is called _sampling bias_. Other sources of bias exist ([[#-Non-sampling Bias|See later]]). 

Also, we have _random errors_ depending on the sample actually observed. This determines the precision of a study.

&nbsp;

> __Bias__ shows us hows close a measured value (e.g an estimate) is to its actual true value.

>__Precision__ shows us how close the measured values are to eachother.

&nbsp;

![[Pasted image 20230209193319.png|400]]

&nbsp;

## Non-sampling Bias

> This is a form of bias that occurs when _certain groups_ of individuals have a tendency to give _inaccurate responses_ or _not give_ an answer.

The _wording_ of a questionnaire, _who_ the interviewer is and what the interviewee _perceives_ to be the “right” answer in a given situation may also _lead to bias_.  

-  _Example_, it was noticed that UK political _polls_ systematically _underestimated_ the _support of the conservative party_ in the 80s and 90s.  This may well have been due to the fact that conservative supporters were _more likely to hide their preferences_ than supporters of other parties.
- _Example_, suppose a questionnaire is carried out on how willing people are to _pay extra_ for “_ecologically friendly goods_”. Such a survey will _tend to overestimate_ the proportion of individuals willing to pay extra, as it is _politically correct_ to express such a willingness.

---