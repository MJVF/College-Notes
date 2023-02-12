---
tags:
- Descriptive_Statistics
- Graphical_Methods
- Numerical_Methods
- Frequency_Distribution
- Frequency
- Relative_Frequency
- Qualitative
- Bar_Graphs
- Pie_Charts
- Histograms
- Stem_and_Leaf_Plots
- Dot_Plots
---


### Glossary:
- [[#Overview]]
- [[#Describing Data]]
	- [[#Use of Graphical and Numerical Methods]]
	- [[#Graphical Methods]]
	- [[#Organizing and Summarizing Qualitative Data]]
	- [[#Constructing Bar Graphs]]
	- [[#Constructing Pie Charts]]
	- [[#Histogram]]
		- [[#Constructing a Histogram]]
	- [[#Stem-and-Leaf Plots]]
	- [[#Dot Plots]]

&nbsp;

#### Formulas:
- Relative Frequency [[#^00a149| .1]]
- Pie chart angle [[#^9e268a| .2]]
- Width of Histogram intervals [[#^3f14cc| .3]]
- Density of Histogram classes [[#^ab7d62| .4]]


&nbsp;

---
# Overview

- __*Remember*__, statistics is a process.
- So far, we dealt with the _first two steps_ in the statistical process:
	1. The research objective identification ([[1 - Data Collection]])
	2. Collecting data to answer the questions in the research objective ([[2 - Sampling]])

> The focus of the following is on _organising, summarising, and presenting_ the data collected.
> This step is called #Descriptive_Statistics 

&nbsp;

---
# Describing Data

We consider:
	- #Graphical_Methods 
	- #Numerical_Methods 

&nbsp;

## Use of Graphical and Numerical Methods

> [[#Graphical Methods|Graphical methods]] can be used to visually and [[1 - Data Collection#^891e66|qualitatively]] present data and compare variables and samples.
>
> They can be used to __illustrate conclusions__, but __*not to draw conclusions*__, since they lack qualitative detail.
> 
> #Numerical_Methods can be used to quantitatively present data and compare variables and samples (giving a mental picture).

&nbsp;
 
## Graphical Methods

- Consider the following graphical methods
	1. To illustrate the distribution of a variable
		1. For [[1 - Data Collection#^891e66|qualitative]] variables: #Pie_Charts , #Bar_Graphs 
		2. For [[1 - Data Collection#^726f4a|quantative]] variables: #Histograms , #Stem_and_Leaf_Plots , #Dot_Plots , #Box_Plots
	2. To illustrate the relationship between _two variables_, when we have pairs of observations (e.g. _the height and weight of a group of people_): #Scatter_Plots 

&nbsp;

## Organizing and Summarizing Qualitative Data

- __*Qualitative Data*__ provide measures that categorize or classify an individual.
- __*Qualitative Data*__ summaries are created by:
	 1.  Organising qualtitative data in tables
	 2. Constructing bar graphs or pie charts

- When raw qualitative data are collected, we often first determine the number of indivduals within each category.


> ##### DEFINITION
>A #Frequency_Distribution lists each category of data and the number of occurrences for each category of data.

&nbsp;

&nbsp;

> __*EXAMPLE 1:*__
> In an event organised by the School of Engineering for the third year students, _data was collected_ upon registration, by _asking the stream_ of each student.
> $\quad$The tally shows that $22, 30, 34, 41, 33,$ and $40$ Biomedical, Civil, Computer, Electronic and Computer, Electronic, and Mechanical Engineering students, respectively, attended the event. Construct a #Frequency_Distribution table showing the stream of the attendees.
>
> |__*Stream*__||__*Frequency*__|
> |---|---|:---:|
> ||||
> |Biomedical||22|
> |Civil||30|
> |Computer||34|
> |Electronic & Computer||41|
> |Electronic||33|
> |Mechanical||40|

^6558db

&nbsp;

In any _frequency distribution_, it is a good idea to add up the frequency column to make sure that it equals the number of observations.
Often, we want to know the _relative frequency_ , rather than the frequency.

&nbsp;

> ##### DEFINITION
>The #Relative_Frequency is the _proportion_ (or percent) of observations within a category and is found using the formula:
> $$Relative \: frequency = \frac{frequency}{sum \: of \: all \: frequencies}$$
>
>A __*relative frequency distribution*__ lists each category of data together with the relative frequency.

^00a149

&nbsp;

> __*EXAMPLE 2:*__
> Using the summarised data in the table of [[#^6558db|Example 1]], find the _relative frequency distribution_.
>
> |__*Stream*__||__*Frequency*__|__*Relative Frequency*__|
> |---|---|:---:|:---:|
> |||||
> |Biomedical||22|0.11|
> |Civil||30|0.15|
> |Computer||34|0.17|
> |Electronic & Computer||41|0.205|
> |Electronic||33|0.165|
> |Mechanical||40|0.2|
> |||||
> |__TOTAL__||__200__|__1__|

^e17086

&nbsp;

 
## Constructing Bar Graphs

Once raw data are organised in a table, we can create graphs, as a _graphical representation_ of data in a more powerful message than tables!

__A picture representing the collected data, is worth a thousand words!__

&nbsp;

> ##### DEFINITION
> #Bar_Graphs are constructed by labeling each category of data o either the horizontal or vertical axis and the #Frequency or #Relative_Frequency of the category on the other axis. _Rectangles_ of equal width are drawn for each category. The height of each rectangle represents the category's _frequency_ or _relative frequency_.

&nbsp;

> __*EXAMPLE 3:*__
> Use the data summarised in the table of [[#^e17086|Example 2]] to construct a _**frequency** bar graph and a **relative frequency** bar graph_.
>
> ![[Pasted image 20230211150904.png|600]]

&nbsp;
 
## Constructing Pie Charts

#Pie_Charts are typically used to present the relative frequency of [[1 - Data Collection#^891e66|qualitative]] data. In most cases the data are [[1 - Data Collection#^5afe74|nominal]] but [[1 - Data Collection#^5afe74|orindal]] deata can also be displayed in a _pie chart_.

&nbsp;

> ##### DEFINITION
> A __*Pie Chart*__ is a circle divided into _sectors_. Each sector represents a category of data. The _area_ of each sector is proportional to the #Frequency of the category.
>
>The _angle_ made by a piece of pie representing a given _category_, $i$, in the pie chart is:
>$$a_{i} = 3.6 \, \cdot \, f_{i}$$
>where $f_{i}$ is the #Relative_Frequency of category $i$.

^9e268a

&nbsp;

> __*EXAMPLE 4:*__
> Use the data summarised in the table of [[#^e17086|Example 2]] to construct a _pie chart_.
> 
> ![[Pasted image 20230211153941.png|500]]

&nbsp;
 
## Histogram

- #Histograms are used to estimate the distribution of a variable based on a [[1 - Data Collection#Sampling|sample]].
- _Histogram_ are graphs simliar to the #Bar_Graphs that gives an idea of the _"shape"_ of a sample, indicating regions where the sample points are concentrated and regions where they are sparse.
- In order to do this, data must first be split into _intervals_ (classes).
- It is good to have more _intervals/classes_ rather than fewer, but it is also good to have large numbers of _sample points_ in the intervals/classes.
> If we have $n$ observations, then the number of intervals/classes used, $k$, should be approximately $\sqrt{n}$. Hence, if we have $20$ observations, it is best to use $4$ or $5$ classes ( i.e $k=4$ or $k=5$).

&nbsp;

- The _endpoints_ of the intervals used to define the classes should be _nice numbers_ (i.e _consecutive integers_, multiples of 2, 5, 10, 20, 50, 100, etc.. depending on the values of the observations).

> Let $a$ be the value of the __largest *"nice"*__ number smaller than any of the observations and $b$ the value of the __smallest *"nice"*__ greater than any of the observations. Then the _width_ of the intervals $w$ is:
> $$w = \frac{b-a}{k},$$
> where $k$ is the number of classes.
> The values of $a$, $b$, $k$ and $w$ can be fine tuned.

^3f14cc

&nbsp;

### Constructing a Histogram

- To construct #Histograms , we need to take the following steps:
	1. Choose _boundary points_ for the class intervals.
	2. Compute the #Frequency and #Relative_Frequency for each class. (_Relative frequency_ is optional if the classes all have the same width)
	3. Compute the _density_ for each class, according to the formula: $$\rho = \frac{f_{i}}{w},$$ where $\rho$ represents the density and $f_{i}$ is the _relative frequency_. (_This step is optional if the classes all have the same width._) ^ab7d62
	4. Draw a _rectangle_ for each class. 
		- If the classes all have the _same width_, the heights of the rectangles may be set equal to the _frequencies_, the _relative frequencies_, or the _densities_. 
		- If the classes __*do not*__ all have the _same width_, the hieghts of the rectangles must be set equal to the _densities_.

&nbsp;

> __*EXAMPLE 5:*__
> To investigate factors affecting diesel vehicle emissions, data on emissions of _particulate matter_ (PM) for a sample of _62_ vehicles driven at _high altitude_ (approximately one mile above sea level) were collected. All the vehicles were manufactured between 1991 and 1996.
> 
>The samples contained roughly equal proportions of _high_ and _low mileage_ vehicles. The observed data, in units of _grams of particulate per gallon_ (g/gal) of fuel consumed, are present in the following.
>
>||||||||||||||
>|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
>|7.59|6.28|6.07|5.23|5.54|3.46|2.44|3.01|13.63|13.02|23.38|9.24|3.22|
>|2.06|4.04|17.11|12.26|19.92|8.50|7.81|7.18|6.95|18.64|7.10|6.04|5.66|
>|8.86|4.40|3.57|4.35|3.84|2.37|3.81|5.32|5.84|2.89|4.68|1.85|9.14|
>|8.67|9.52|2.68|10.14|9.20|7.31|2.09|6.32|6.53|6.32|2.01|5.91|5.60|
>|5.61|1.50|6.46|5.29|5.64|2.07|1.11|3.32|1.83|7.56||||
>||||||||||||||
>
> Construct a [[#Histogram]] represetning this data.
> 
> ---
>__*SOLUTION*__
>The first step is to choose the _boundary points_ for the class intervals. To this end, since we have $62$ items, we choose the number of classes as $\sqrt{62} \approx 8$.
>The data may vary within the range from $1.11$ g/gal to $23.38$ g/gal. Since we have $8$ classes, we choose the range from $1$ -> $25$ g/gal that leads to the [[#^3f14cc|interval width]] of $w = \frac{25-1}{8} = 3$. Now we can construct the _frequency table_.
>
>|__*Class Interval, $E$ (g/gal)*__|Frequency|Relative Frequency|Density|
>|:---:|:---:|:---:|:---:|
>|||||
>|$1 \leq E \lt 4$|19|0.3064|0.1021|
>|$4 \leq E \lt 7$|22|0.3548|0.1183|
>|$7 \leq E \lt 10$|13|0.2097|0.0699|
>|$10 \leq E \lt 13$|2|0.0322|0.0107|
>|$13 \leq E \lt 16$|2|0.0322|0.0107|
>|$16 \leq E \lt 19$|2|0.0322|0.0107|
>|$19 \leq E \lt 22$|1|0.161|0.0053|
>|$22 \leq E \lt 25$|1|0.161|0.0053|
>|||||
>
>__*NOW*__, using the information in the _frequency table_, the __*histogram*__ can be drawn as:
>
>![[Pasted image 20230211170149.png|600]]


&nbsp;

## Stem-and-Leaf Plots

- #Stem_and_Leaf_Plots are a simple way to summarise a data set. In a _stem-and-lead plot_ (stem plot), we use the _one or two digits_ to the left of the rightmost digit for the __stem__. Each rightmost digit forms a __leaf_. 


>__*EXAMPLE 6:*__
>The geyser "Old Faithful", in Yellowstone National Park, alternates periods of eruption, which typically last from _1.5_ to _4_ minutes, with periods of dormancy, that last longer. The data in the _table below_ present the durations, in minutes, of 60 dormant periods.
>The list has been sorted into numeric order.
>
>|||||||||||
>|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
>|42|45|49|50|51|51|51|51|53|53|
>|55|55|56|56|57|58|60|66|67|67|
>|68|69|70|71|72|73|73|74|75|75|
>|75|75|76|76|76|76|76|79|79|80|
>|80|80|80|81|82|82|82|83|83|84|
>|84|84|85|86|86|86|88|90|91|93|
>||||||||||| ^73ecf1
> ---
>__*SOLUTION*__
> Stem-and-Leaf plot of the geyser data is shown below, where the stem consists of the _tens digit_ and the leaf consists of the _ones digit_. Each line of the stem-and-leaf plot contains all of the sample items with a given stem.
> 
> ![[Pasted image 20230211174824.png|400]]
>  &nbsp;
>  The stem-and-leaf plot is a compact way to represent the data. It also gives some indication of its shape.
>  
>For the geyser data, we can see that there is relatively few durations in the _60-69_ minute interval, compared with the _50-59_, _70-79_, or _80-89_ minute intervals.

&nbsp;

## Dot Plots

> #Dot_Plots are graphs that can be used to give a rough impression of the shape of a sample.

- To construct a dot plot, for each value in the sample, a vertical column of dots is drawn, with the number of dots in the column equal to the number of times the value appears in the sample.
- The dot plot gives a good indication of where the sample values are concentrated and where the gaps are. A _Dot Plot_ for the geyser data in [[#^73ecf1|Example 6]] is constructed as:

&nbsp;

![[Pasted image 20230211180128.png]]

&nbsp;

---