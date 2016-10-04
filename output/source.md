<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Practical 1</a>
<ul>
<li><a href="#sec-1-1">1.1. Question 1</a></li>
<li><a href="#sec-1-2">1.2. Question 2</a></li>
<li><a href="#sec-1-3">1.3. Question 3</a></li>
</ul>
</li>
<li><a href="#sec-2">2. Practical 2</a>
<ul>
<li><a href="#sec-2-1">2.1. Which age occurs most often?</a></li>
<li><a href="#sec-2-2">2.2. Find out what’s the mean, the median, the mode, the range and the standard deviation of the Proficiency Score in your data.</a></li>
<li><a href="#sec-2-3">2.3. Find out what is the minimum age, the maximum age, the mean age and the standard deviation.</a></li>
<li><a href="#sec-2-4">2.4. What is the most frequently occurring proficiency score</a></li>
<li><a href="#sec-2-5">2.5. What is the z-score of Participant 13?</a></li>
<li><a href="#sec-2-6">2.6. Which group has higher proficiency scores, the male or the female participants?</a></li>
<li><a href="#sec-2-7">2.7. Which group scored more homogeneously?</a></li>
<li><a href="#sec-2-8">2.8. Boxplots</a></li>
<li><a href="#sec-2-9">2.9. Part B</a></li>
</ul>
</li>
<li><a href="#sec-3">3. Practical 3</a>
<ul>
<li><a href="#sec-3-1">3.1. Part A</a>
<ul>
<li><a href="#sec-3-1-1">3.1.1. Descriptives and graphs for groups</a></li>
<li><a href="#sec-3-1-2">3.1.2. Which performed best? And which group performed most homogeneously?</a></li>
<li><a href="#sec-3-1-3">3.1.3. Which teacher performed best?</a></li>
<li><a href="#sec-3-1-4">3.1.4. Boxplot</a></li>
<li><a href="#sec-3-1-5">3.1.5. Grades</a></li>
<li><a href="#sec-3-1-6">3.1.6. How many students passed?</a></li>
<li><a href="#sec-3-1-7">3.1.7. Checking for normality</a></li>
<li><a href="#sec-3-1-8">3.1.8. Zscores</a></li>
<li><a href="#sec-3-1-9">3.1.9. Impressions about teacher gorup</a></li>
<li><a href="#sec-3-1-10">3.1.10. The Null hypothesis</a></li>
<li><a href="#sec-3-1-11">3.1.11. Defining the variables</a></li>
<li><a href="#sec-3-1-12">3.1.12. Running the test</a></li>
</ul>
</li>
<li><a href="#sec-3-2">3.2. Part B</a></li>
</ul>
</li>
<li><a href="#sec-4">4. Practical 4</a>
<ul>
<li><a href="#sec-4-1">4.1. Applying the t-test</a>
<ul>
<li><a href="#sec-4-1-1">4.1.1. What are the dependent and independent variables?</a></li>
<li><a href="#sec-4-1-2">4.1.2. What kind of measures (nominal, ordinal or interval / scale) are used for the variables?</a></li>
<li><a href="#sec-4-1-3">4.1.3. How many levels does the independent variable have?</a></li>
<li><a href="#sec-4-1-4">4.1.4. Formulate the statistical hypothesis</a></li>
<li><a href="#sec-4-1-5">4.1.5. Select an alpha level suitable for this study</a></li>
<li><a href="#sec-4-1-6">4.1.6. Which statistical test could be used ?</a></li>
<li><a href="#sec-4-1-7">4.1.7. Enter the data</a></li>
<li><a href="#sec-4-1-8">4.1.8. Provide the following descriptive statistics for both groups: means, range, minimum, maximum, standard deviations.</a></li>
<li><a href="#sec-4-1-9">4.1.9. What are your first impressions about the difference between the boys and the girls?</a></li>
<li><a href="#sec-4-1-10">4.1.10. Create a box plot to visualise the results.</a></li>
<li><a href="#sec-4-1-11">4.1.11. Test the statistical significance of this experiment</a></li>
</ul>
</li>
<li><a href="#sec-4-2">4.2. What can you say about the meaningfulness of this outcome?</a></li>
<li><a href="#sec-4-3">4.3. Consider the following data</a>
<ul>
<li><a href="#sec-4-3-1">4.3.1. What would be H<sub>0</sub> if we want to test the relationship between reading and listening comprehension?</a></li>
<li><a href="#sec-4-3-2">4.3.2. Make a plot of the results.</a></li>
<li><a href="#sec-4-3-3">4.3.3. At face value, do you think Reading and Listening , as plotted in the graph, are related?</a></li>
<li><a href="#sec-4-3-4">4.3.4. We want to know if we can conclude that reading skills and listening comprehension are significantly related.</a></li>
<li><a href="#sec-4-3-5">4.3.5. Report</a></li>
<li><a href="#sec-4-3-6">4.3.6. <span class="todo __TODO">☛ TODO</span> Cronbach's Alpha</a></li>
</ul>
</li>
<li><a href="#sec-4-4">4.4. testing the normality of the distribution</a></li>
</ul>
</li>
</ul>
</div>
</div>


# Practical 1<a id="sec-1" name="sec-1"></a>

Firs we begin be importing our dataset. We have to use an additional library to read an \*.xlsx file. After that we assign names to the columns. And we take a look at the first rows of the dataset to see what it looks like.

    data <- read.csv("./data/p1.csv")
    names(data) <- c("id","age","sex","profs")
    head(data)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="right">16</td>
<td class="right">1</td>
<td class="right">91</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">20</td>
<td class="right">2</td>
<td class="right">58</td>
</tr>


<tr>
<td class="right">3</td>
<td class="right">24</td>
<td class="right">1</td>
<td class="right">52</td>
</tr>


<tr>
<td class="right">4</td>
<td class="right">22</td>
<td class="right">2</td>
<td class="right">45</td>
</tr>


<tr>
<td class="right">5</td>
<td class="right">18</td>
<td class="right">1</td>
<td class="right">78</td>
</tr>


<tr>
<td class="right">6</td>
<td class="right">14</td>
<td class="right">2</td>
<td class="right">88</td>
</tr>
</tbody>
</table>

## Question 1<a id="sec-1-1" name="sec-1-1"></a>

*Does the proficiency score increase or decrease with age?*

To answer this question we might simply plot both age and proficiency score and see if there is any clear indication.

    plot(data$age,data$profs)

![img](1.png)

Well, yes, from the scatter plot we built we can see that as the age increases the proficiency decreases.

## Question 2<a id="sec-1-2" name="sec-1-2"></a>

*Is there a difference in proficiency score between female and male participants?*

    aggregate(data$profs, by=list(Category=data$sex), FUN=mean)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="right">75.5333333333333</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">63.6666666666667</td>
</tr>
</tbody>
</table>

## Question 3<a id="sec-1-3" name="sec-1-3"></a>

*Is there an overall difference in age between male and female participants?*

    m <- data$age[data$sex == 1]
    f <- data$age[data$sex == 2]
    boxplot(m,f)

    aggregate(data$age, by=list(Category=data$sex), FUN=mean)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="right">20.1333333333333</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">20.5333333333333</td>
</tr>
</tbody>
</table>

# Practical 2<a id="sec-2" name="sec-2"></a>

    data <- read.csv("./data/p1.csv")
    names(data) <- c("id","age","sex","profs")
    str(data)

## Which age occurs most often?<a id="sec-2-1" name="sec-2-1"></a>

    which.max(tabulate(data$age))

    16

## Find out what’s the mean, the median, the mode, the range and the standard deviation of the Proficiency Score in your data.<a id="sec-2-2" name="sec-2-2"></a>

    mean(data$profs)

    69.6

    median(data$profs)

    69

    which.max(tabulate(data$profs))

    59

    range(data$profs)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">33</td>
</tr>


<tr>
<td class="right">97</td>
</tr>
</tbody>
</table>

    sd(data$profs)

    16.4434244273069

## Find out what is the minimum age, the maximum age, the mean age and the standard deviation.<a id="sec-2-3" name="sec-2-3"></a>

    min(data$age)

    14

    max(data$age)

    27

    mean(data$age)

    20.3333333333333

    sd(data$age)

    3.56547944576335

    sd(data$age)

    3.56547944576335

## What is the most frequently occurring proficiency score<a id="sec-2-4" name="sec-2-4"></a>

    which.max(tabulate(data$profs))

    59

## What is the z-score of Participant 13?<a id="sec-2-5" name="sec-2-5"></a>

    scale(data$profs,center=TRUE, scale=TRUE)[13]

    -0.462190830966998

## Which group has higher proficiency scores, the male or the female participants?<a id="sec-2-6" name="sec-2-6"></a>

    aggregate(data$profs, by=list(Category=data$sex), FUN=mean)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="right">75.5333333333333</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">63.6666666666667</td>
</tr>
</tbody>
</table>

## Which group scored more homogeneously?<a id="sec-2-7" name="sec-2-7"></a>

    aggregate(data$profs, by=list(Category=data$sex), FUN=sd)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="right">14.2421239721502</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">16.7871833197092</td>
</tr>
</tbody>
</table>

## Boxplots<a id="sec-2-8" name="sec-2-8"></a>

    m <- data$profs[data$sex == 1]
    f <- data$profs[data$sex == 2]
    boxplot(m,f,names=c("M","F"))

![img](3.png)

## Part B<a id="sec-2-9" name="sec-2-9"></a>

Provide the mean, the mode, the median, the range and the standard deviation.

    a <- c(3, 4, 5, 6, 7, 8, 9)
    b <- c(6, 6, 6, 6, 6, 6, 6)
    c <- c(4, 4, 4, 6, 7, 7, 10)
    d <- c(1, 1, 1, 4, 9, 12, 14)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
</tr>


<tr>
<td class="right">1</td>
</tr>


<tr>
<td class="right">1</td>
</tr>


<tr>
<td class="right">4</td>
</tr>


<tr>
<td class="right">9</td>
</tr>


<tr>
<td class="right">12</td>
</tr>


<tr>
<td class="right">14</td>
</tr>
</tbody>
</table>

    MySummary <- function(dataset) {
      m = mean(dataset)
      mode = which.max(tabulate(dataset))
      med = median(dataset)
      stdde = sd(dataset)
      results <- c(m,mode,med,stdde)
      return(results)
    }

    MySummary(a)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">3</td>
</tr>


<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">2.16024689946929</td>
</tr>
</tbody>
</table>

    MySummary(b)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">0</td>
</tr>
</tbody>
</table>

    MySummary(c)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">4</td>
</tr>


<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">2.23606797749979</td>
</tr>
</tbody>
</table>

    MySummary(d)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">6</td>
</tr>


<tr>
<td class="right">1</td>
</tr>


<tr>
<td class="right">4</td>
</tr>


<tr>
<td class="right">5.59761854124889</td>
</tr>
</tbody>
</table>

# Practical 3<a id="sec-3" name="sec-3"></a>

## Part A<a id="sec-3-1" name="sec-3-1"></a>

As always, we begin by importing the data and taking a quick look at the first rows to see what it looks like.

    data <- read.csv("./data/p3a.csv",na="",header=TRUE)
    head(data)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="left" />

<col  class="left" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="left">A</td>
<td class="left">1A</td>
<td class="right">10</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">7</td>
<td class="right">4</td>
<td class="right">2</td>
<td class="right">4</td>
<td class="right">14</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">4</td>
<td class="right">12</td>
</tr>


<tr>
<td class="right">2</td>
<td class="left">A</td>
<td class="left">1A</td>
<td class="right">12</td>
<td class="right">5</td>
<td class="right">4</td>
<td class="right">8</td>
<td class="right">4</td>
<td class="right">4</td>
<td class="right">5</td>
<td class="right">18</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">4</td>
<td class="right">17</td>
</tr>


<tr>
<td class="right">3</td>
<td class="left">A</td>
<td class="left">1A</td>
<td class="right">10</td>
<td class="right">4</td>
<td class="right">5</td>
<td class="right">6</td>
<td class="right">2</td>
<td class="right">3</td>
<td class="right">0</td>
<td class="right">8</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">4</td>
<td class="right">11</td>
</tr>


<tr>
<td class="right">4</td>
<td class="left">A</td>
<td class="left">1A</td>
<td class="right">18</td>
<td class="right">5</td>
<td class="right">6</td>
<td class="right">8</td>
<td class="right">5</td>
<td class="right">3</td>
<td class="right">4</td>
<td class="right">15</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">4</td>
<td class="right">12</td>
</tr>


<tr>
<td class="right">5</td>
<td class="left">A</td>
<td class="left">1B</td>
<td class="right">20</td>
<td class="right">5</td>
<td class="right">6</td>
<td class="right">7</td>
<td class="right">5</td>
<td class="right">4</td>
<td class="right">4</td>
<td class="right">19</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">13</td>
</tr>


<tr>
<td class="right">6</td>
<td class="left">A</td>
<td class="left">1A</td>
<td class="right">16</td>
<td class="right">5</td>
<td class="right">6</td>
<td class="right">8</td>
<td class="right">6</td>
<td class="right">3</td>
<td class="right">1</td>
<td class="right">19</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">5</td>
<td class="right">0</td>
<td class="right">0</td>
<td class="right">4</td>
<td class="right">11</td>
</tr>
</tbody>
</table>

Now we define the type of variables for `teacher` and `group`. More precisely, we want to define them as *factors*.

    data$group <- as.factor(data$group)
    data$teacher <- as.factor(data$teacher)
    str(data)

     id age sex profs
    1  1  16   1    91
    2  2  20   2    58
    3  3  24   1    52
    4  4  22   2    45
    5  5  18   1    78
    6  6  14   2    88
     null device 
              1
     
     Category        x
    1        1 75.53333
    2        2 63.66667
     null device 
              1
     
     Category        x
    1        1 20.13333
    2        2 20.53333
     'data.frame':  30 obs. of  4 variables:
     $ id   : int  1 2 3 4 5 6 7 8 9 10 ...
     $ age  : int  16 20 24 22 18 14 15 17 19 21 ...
     $ sex  : int  1 2 1 2 1 2 1 2 1 2 ...
     $ profs: int  91 58 52 45 78 88 90 86 83 62 ...
    [1] 16
    [1] 69.6
    [1] 69
    [1] 59
    [1] 33 97
    [1] 16.44342
    [1] 14
    [1] 27
    [1] 20.33333
    [1] 3.565479
    [1] 3.565479
    [1] 59
    [1] -0.4621908
     
     Category        x
    1        1 75.53333
    2        2 63.66667
     
     Category        x
    1        1 14.24212
    2        2 16.78718
     null device 
              1
    [1] 6.000000 3.000000 6.000000 2.160247
    [1] 6 6 6 0
    [1] 6.000000 4.000000 6.000000 2.236068
    [1] 6.000000 1.000000 4.000000 5.597619
     
     Student. teacher group Q1 Q2 Q3 Q4 Q5 Q6 Q7 Q8 Q9 Q10 Q11 Q12 Q13 Q14 Q15 Q16
    1        1       A    1A 10  5  5  7  4  2  4 14  5   5   5   0   5   0   0   4
    2        2       A    1A 12  5  4  8  4  4  5 18  5   0   5   0   0   5   0   4
    3        3       A    1A 10  4  5  6  2  3  0  8  0   5   5   0   5   0   0   4
    4        4       A    1A 18  5  6  8  5  3  4 15  5   5   5   0   5   0   5   4
    5        5       A    1B 20  5  6  7  5  4  4 19  5   5   5   0   5   0   0   5
    6        6       A    1A 16  5  6  8  6  3  1 19  0   0   5   0   5   0   0   4
      Q17
    1  12
    2  17
    3  11
    4  12
    5  13
    6  11
    'data.frame':   130 obs. of  20 variables:
     $ Student.: int  1 2 3 4 5 6 7 8 9 10 ...
     $ teacher : Factor w/ 2 levels "A","B": 1 1 1 1 1 1 1 1 1 1 ...
     $ group   : Factor w/ 5 levels "1A","1B","1C",..: 1 1 1 1 2 1 1 1 1 1 ...
     $ Q1      : int  10 12 10 18 20 16 10 7 20 11 ...
     $ Q2      : int  5 5 4 5 5 5 3 4 4 5 ...
     $ Q3      : int  5 4 5 6 6 6 4 6 6 5 ...
     $ Q4      : int  7 8 6 8 7 8 8 6 6 7 ...
     $ Q5      : int  4 4 2 5 5 6 5 3 6 6 ...
     $ Q6      : int  2 4 3 3 4 3 3 2 3 3 ...
     $ Q7      : int  4 5 0 4 4 1 3 0 4 2 ...
     $ Q8      : int  14 18 8 15 19 19 16 14 17 17 ...
     $ Q9      : int  5 5 0 5 5 0 0 0 5 5 ...
     $ Q10     : int  5 0 5 5 5 0 5 0 5 5 ...
     $ Q11     : int  5 5 5 5 5 5 5 5 5 5 ...
     $ Q12     : int  0 0 0 0 0 0 5 0 0 0 ...
     $ Q13     : int  5 0 5 5 5 5 5 0 5 0 ...
     $ Q14     : int  0 5 0 0 0 0 0 0 0 0 ...
     $ Q15     : int  0 0 0 5 0 0 0 0 5 0 ...
     $ Q16     : num  4 4 4 4 5 4 2 5 4 4 ...
     $ Q17     : int  12 17 11 12 13 11 11 2 8 12 ...

### Descriptives and graphs for groups<a id="sec-3-1-1" name="sec-3-1-1"></a>

Adding a `TOTAL_score` variable.

    data$TOTAL_score <- rowSums(data[,4:20])
    str(data$TOTAL_score)

    num [1:130] 87 96 68 105 108 89 85 54 103 87 ...

### Which performed best? And which group performed most homogeneously?<a id="sec-3-1-2" name="sec-3-1-2"></a>

    best <- aggregate(data$TOTAL_score, by=list(data$group), FUN=mean)
    best$Group.1[which.max(best$x)]

    1B

    more_homo <- aggregate(data$TOTAL_score, by=list(data$group), FUN=sd)
    more_homo$Group.1[which.min(more_homo$x)]

    1C

### Which teacher performed best?<a id="sec-3-1-3" name="sec-3-1-3"></a>

    byteacher <- aggregate(data$TOTAL_score, by=list(data$teacher), FUN=mean)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="left">A</td>
<td class="right">78.4</td>
</tr>


<tr>
<td class="left">B</td>
<td class="right">69.2928571428571</td>
</tr>
</tbody>
</table>

Teacher A

### Boxplot<a id="sec-3-1-4" name="sec-3-1-4"></a>

    teacherA <- data$TOTAL_score[data$teacher == "A"]
    teacherB <- data$TOTAL_score[data$teacher == "B"]
    boxplot(teacherA,teacherB)

![img](teacher.png)

### Grades<a id="sec-3-1-5" name="sec-3-1-5"></a>

    data$grade <- trunc(((data$TOTAL_score/143)*100)/10)
    str(data$grade)

    [1] 1B
    Levels: 1A 1B 1C 1D 1E
    [1] 1C
    Levels: 1A 1B 1C 1D 1E
     null device 
              1
     num [1:130] 6 6 4 7 7 6 5 3 7 6 ...

### How many students passed?<a id="sec-3-1-6" name="sec-3-1-6"></a>

    table(data$grade >= 6)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="left">FALSE</td>
<td class="right">86</td>
</tr>


<tr>
<td class="left">TRUE</td>
<td class="right">44</td>
</tr>
</tbody>
</table>

### Checking for normality<a id="sec-3-1-7" name="sec-3-1-7"></a>

    x <- data$grade
    h<-hist(x, breaks=10, col="red", xlab="Grade", main="Histogram with normal curve of grades")
    xfit<-seq(min(x),max(x),length=40)
    yfit<-dnorm(xfit,mean=mean(x),sd=sd(x))
    yfit <- yfit*diff(h$mids[1:2])*length(x)
    lines(xfit, yfit, col="blue", lwd=2)

![img](normality.png)

### Zscores<a id="sec-3-1-8" name="sec-3-1-8"></a>

    zgrades <- scale(data$grade,center=TRUE, scale=TRUE)
    round(zgrades[c(11,33,44,55)],2)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">0.8</td>
</tr>


<tr>
<td class="right">-1.58</td>
</tr>


<tr>
<td class="right">1.99</td>
</tr>


<tr>
<td class="right">0.8</td>
</tr>
</tbody>
</table>

### Impressions about teacher gorup<a id="sec-3-1-9" name="sec-3-1-9"></a>

It seems to me that teacher A is a better one.

### The Null hypothesis<a id="sec-3-1-10" name="sec-3-1-10"></a>

*There is no difference between the two groups.*

### Defining the variables<a id="sec-3-1-11" name="sec-3-1-11"></a>

`teacher` is the independent variable.

### Running the test<a id="sec-3-1-12" name="sec-3-1-12"></a>

The default R's function assumes that there is non equal variance between the two groups. So we first check if that's the case, and in case the variance is equal, then we pass an additional argument to the function.

    var(teacherA)

    481.871186440678

    var(teacherB)

    554.467339544513

Well, at this point I don't know if this difference can be considered large enough to justify the use of the Welsh test. I'll run both.

    t.test(teacherA,teacherB, var.equal=TRUE)$p.value

    0.0250141709914793

    t.test(teacherA,teacherB)$p.value

    0.02426194067448

It is safe to reject the null hypothesis.

## Part B<a id="sec-3-2" name="sec-3-2"></a>

    data <- read.csv("./data/p3b.csv",na="")
    colnames(data) <- c("partecipant","motivation","score")
    str(data)

    FALSE  TRUE 
       86    44
     null device 
              1
    [1]  0.80 -1.58  1.99  0.80
    [1] 481.8712
    [1] 554.4673
    [1] 0.02501417
    [1] 0.02426194
    'data.frame':   424 obs. of  3 variables:
     $ partecipant: int  1 2 3 4 5 6 7 8 9 10 ...
     $ motivation : Factor w/ 2 levels "High","Low": 2 2 1 2 2 2 2 1 1 1 ...
     $ score      : int  22 28 28 26 18 31 22 25 20 25 ...

Let's define Motivation as factor.

    data$motivation <- as.factor(data$motivation)
    str(data$motivation)

    Factor w/ 2 levels "High","Low": 2 2 1 2 2 2 2 1 1 1 ...

Ok, now we group the scores by motivation level.

    bymotivation <- aggregate(data$score, by=list(data$motivation), FUN=mean)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="left">High</td>
<td class="right">23.8842592592593</td>
</tr>


<tr>
<td class="left">Low</td>
<td class="right">22.8653846153846</td>
</tr>
</tbody>
</table>

Good. There is a difference. Now we have to understand if this difference is significative or not.

    low <- data$score[data$motivation == "Low"]
    high <- data$score[data$motivation == "High"]
    t.test(low,high)

            Welch Two Sample t-test
    
    data:  low and high
    t = -2.0046, df = 421.24, p-value = 0.04565
    alternative hypothesis: true difference in means is not equal to 0
    95 percent confidence interval:
     -2.01795621 -0.01979307
    sample estimates:
    mean of x mean of y 
     22.86538  23.88426

    round(t.test(low,high)$p.value,digits=3)

    0.046

Yes, with this *p* value the difference can be considered significative.

# Practical 4<a id="sec-4" name="sec-4"></a>

Inductive statistics

## Applying the t-test<a id="sec-4-1" name="sec-4-1"></a>

A researcher wants to find out whether boys or girls are more intelligent. Eleven girls and eight boys (randomly selected) participated in an experiment in which scores were involved ranging 1-20 (interval).

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="right">Girls</th>
<th scope="col" class="right">Boys</th>
</tr>
</thead>

<tbody>
<tr>
<td class="right">17</td>
<td class="right">16</td>
</tr>


<tr>
<td class="right">16</td>
<td class="right">15</td>
</tr>


<tr>
<td class="right">14</td>
<td class="right">13</td>
</tr>


<tr>
<td class="right">19</td>
<td class="right">19</td>
</tr>


<tr>
<td class="right">18</td>
<td class="right">15</td>
</tr>


<tr>
<td class="right">17</td>
<td class="right">14</td>
</tr>


<tr>
<td class="right">16</td>
<td class="right">13</td>
</tr>


<tr>
<td class="right">15</td>
<td class="right">12</td>
</tr>


<tr>
<td class="right">16</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="right">15</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="right">19</td>
<td class="right">&#xa0;</td>
</tr>
</tbody>
</table>

We begin by building the dataframe.

    partecipant <- seq(1,19)
    score <- c(17,16,16,15,14,13,19,19,18,15,17,14,16,13,15,12,16,15,19)
    gender <- c(1,2,1,2,1,2,1,2,1,2,1,2,1,2,1,2,1,1,1)
    gender <- as.factor(gender)
    levels(gender) <- c("F", "M")
    df = data.frame(partecipant,gender,score)
    df
    str(df)

Here we load some libraries that we are going to use later on. The first one is a plotting library, while the second contains skewness and kurtosis functions. The car packages contains Levene's test.

    library(ggplot2)
    library(moments)
    library(car)

### What are the dependent and independent variables?<a id="sec-4-1-1" name="sec-4-1-1"></a>

Gender is the independent variable and the score is the dependent one

### What kind of measures (nominal, ordinal or interval / scale) are used for the variables?<a id="sec-4-1-2" name="sec-4-1-2"></a>

Gender is a nominal, while score is a scale variable.  

### How many levels does the independent variable have?<a id="sec-4-1-3" name="sec-4-1-3"></a>

Two, `boys` and `girls`. For readability in the output I have renamed these to `M` and `F` respectively.

### Formulate the statistical hypothesis<a id="sec-4-1-4" name="sec-4-1-4"></a>

-   Null: there is no difference in the two groups
-   H1: there is a difference: boys do better than girls
-   H2: there is a difference: girls do better than boys

### Select an alpha level suitable for this study<a id="sec-4-1-5" name="sec-4-1-5"></a>

0.5

### Which statistical test could be used ?<a id="sec-4-1-6" name="sec-4-1-6"></a>

The t-test. But we have first to check for the normality of the distribution and the homogenity.

### Enter the data<a id="sec-4-1-7" name="sec-4-1-7"></a>

*Tip*: carefully consider this step – the two columns (Girls and Boys) in the data are not necessarily the variable columns. Remember that the columns in the dataset represent variables, not levels of variables!

    head(df)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="left" />

<col  class="right" />
</colgroup>
<tbody>
<tr>
<td class="right">1</td>
<td class="left">F</td>
<td class="right">17</td>
</tr>


<tr>
<td class="right">2</td>
<td class="left">M</td>
<td class="right">16</td>
</tr>


<tr>
<td class="right">3</td>
<td class="left">F</td>
<td class="right">16</td>
</tr>


<tr>
<td class="right">4</td>
<td class="left">M</td>
<td class="right">15</td>
</tr>


<tr>
<td class="right">5</td>
<td class="left">F</td>
<td class="right">14</td>
</tr>


<tr>
<td class="right">6</td>
<td class="left">M</td>
<td class="right">13</td>
</tr>
</tbody>
</table>

### Provide the following descriptive statistics for both groups: means, range, minimum, maximum, standard deviations.<a id="sec-4-1-8" name="sec-4-1-8"></a>

    f <- df$score[df$gender == "F"]
    m <- df$score[df$gender == "M"]
    summary(m)
    summary(f)
    mean(m)
    mean(f)
    range(m)
    range(f)
    sd(m)
    sd(f)

    [1] 0.046
     
      partecipant gender score
    1            1      F    17
    2            2      M    16
    3            3      F    16
    4            4      M    15
    5            5      F    14
    6            6      M    13
    7            7      F    19
    8            8      M    19
    9            9      F    18
    10          10      M    15
    11          11      F    17
    12          12      M    14
    13          13      F    16
    14          14      M    13
    15          15      F    15
    16          16      M    12
    17          17      F    16
    18          18      F    15
    19          19      F    19
    'data.frame':   19 obs. of  3 variables:
     $ partecipant: int  1 2 3 4 5 6 7 8 9 10 ...
     $ gender     : Factor w/ 2 levels "F","M": 1 2 1 2 1 2 1 2 1 2 ...
     $ score      : num  17 16 16 15 14 13 19 19 18 15 ...
     
     partecipant gender score
    1           1      F    17
    2           2      M    16
    3           3      F    16
    4           4      M    15
    5           5      F    14
    6           6      M    13
       Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
      12.00   13.00   14.50   14.62   15.25   19.00
       Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
      14.00   15.50   16.00   16.55   17.50   19.00
    [1] 14.625
    [1] 16.54545
    [1] 12 19
    [1] 14 19
    [1] 2.199838
    [1] 1.634848

### What are your first impressions about the difference between the boys and the girls?<a id="sec-4-1-9" name="sec-4-1-9"></a>

Let's take a look.

    boxplot(f,m,names=c("Girls","Boys"))

![img](boysgirls.png)

It seems that girls score better than the boys.

### Create a box plot to visualise the results.<a id="sec-4-1-10" name="sec-4-1-10"></a>

Done in the previous section.

### Test the statistical significance of this experiment<a id="sec-4-1-11" name="sec-4-1-11"></a>

Find out which group has a distribution that most resembles the normal distribution.

What do the values of skewness and kurtosis represent again ?  How can they help you in determining whether a dataset resembles a normal distribution?  Check the “How To Check Assumptions NEW” on Nestor as well.

In our dataset we have 19 observations. So, we are going to run the Shapiro-Wilk test.

    shapiro.test(m)
    shapiro.test(f)

     null device 
              1
    
            Shapiro-Wilk normality test
    
    data:  m
    W = 0.9228, p-value = 0.453
    
            Shapiro-Wilk normality test
    
    data:  f
    W = 0.94182, p-value = 0.5422

Both groups resembles a normal distribution. We now take a look at skewness and kurtosis.

    skewness(m)
    kurtosis(m)
    skewness(f)
    kurtosis(f)

    [1] 0.8540259
    [1] 3.008633
    [1] 0.203529
    [1] 2.014369

The `boys` group presents higher values for both skewness and kurtosis when compaird to `girls`. So `girls` has a more normal distribution.

1.  Do  the Independent samples t-test.

    Why do you have to use this test rather than the one sample t-test or the paired samples t-test ?
    
        t.test(m,f)
    
                Welch Two Sample t-test
        
        data:  m and f
        t = -2.0856, df = 12.357, p-value = 0.05838
        alternative hypothesis: true difference in means is not equal to 0
        95 percent confidence interval:
         -3.92030824  0.07939915
        sample estimates:
        mean of x mean of y 
         14.62500  16.54545

2.  Carefully study the output

3.  Leven's test

    Taking Levene’s test into account, what is the value of “t”?  Which degrees of freedom are applied to this test?  What is the level of significance of these samples ?  Compare this to the alpha level you set in e) above.  Can you reject H 0 ?

4.  Reporting

    > On average, the girls showed a higher level of intelligence (M=14.63, SE= &#x2026; )  than the boys(M=14.63. , SE= &#x2026; ). This difference was not significant t(df=12.36,t=-2.09, p > 0.05).

## What can you say about the meaningfulness of this outcome?<a id="sec-4-2" name="sec-4-2"></a>

Is there any additional information you’d like to have about this study ?

Not much. I would like to have more data

## Consider the following data<a id="sec-4-3" name="sec-4-3"></a>

8 students have participated in a reading test and a listening comprehension test.  Reading ability and listening comprehension are operationalised by the variables R and L respectively. Both variables are measured on an interval scale. The results have been summarised in the table below. Build a dataframe.

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="right" />

<col  class="right" />

<col  class="right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="right">Student</th>
<th scope="col" class="right">R</th>
<th scope="col" class="right">L</th>
</tr>
</thead>

<tbody>
<tr>
<td class="right">1</td>
<td class="right">20</td>
<td class="right">65</td>
</tr>


<tr>
<td class="right">2</td>
<td class="right">40</td>
<td class="right">69</td>
</tr>


<tr>
<td class="right">3</td>
<td class="right">60</td>
<td class="right">73</td>
</tr>


<tr>
<td class="right">4</td>
<td class="right">80</td>
<td class="right">77</td>
</tr>


<tr>
<td class="right">5</td>
<td class="right">100</td>
<td class="right">80</td>
</tr>


<tr>
<td class="right">6</td>
<td class="right">120</td>
<td class="right">84</td>
</tr>


<tr>
<td class="right">7</td>
<td class="right">140</td>
<td class="right">89</td>
</tr>


<tr>
<td class="right">8</td>
<td class="right">160</td>
<td class="right">95</td>
</tr>
</tbody>
</table>

    partecipant <- seq(1,8)
    r <- c(20,40,60,80,100,120,140,160)
    l <- c(65,69,73,77,80,84,89,95)
    df = data.frame(partecipant,r,l)

### What would be H<sub>0</sub> if we want to test the relationship between reading and listening comprehension?<a id="sec-4-3-1" name="sec-4-3-1"></a>

Reading and listening do not interfere.  

### Make a plot of the results.<a id="sec-4-3-2" name="sec-4-3-2"></a>

Tip: Make a scatter plot and define the X-and Y-axis.

    plot(df$r,df$l,xlab="Reading",ylab="Listening")

![img](correlation.png)

### At face value, do you think Reading and Listening , as plotted in the graph, are related?<a id="sec-4-3-3" name="sec-4-3-3"></a>

Yes

### We want to know if we can conclude that reading skills and listening comprehension are significantly related.<a id="sec-4-3-4" name="sec-4-3-4"></a>

To determine this, you will have to calc ulate a Pearson r (or r xy ). Make sure the computer calculates the Pearson correlation for a two-tailed test.  What is the value of r xy ? Is this a strong correlation? What is the chance of incorrectly rejecting your H 0 ? What do you decide?

    cor(df$r,df$l,method="pearson")

    0.996229128491916

### Report<a id="sec-4-3-5" name="sec-4-3-5"></a>

> A correlation analysis showed that Reading Skills and Listening Skills were &#x2026;. [significantly or not significantly] related (r =0.99, p &#x2026; [ fill in < 0.05 or > 0.05 or whichever α you’ve selected] ) ”

### ☛ TODO Cronbach's Alpha<a id="sec-4-3-6" name="sec-4-3-6"></a>

&#x2026;we shortly discussed reliability, and that Cronbach’s Alpha was a good measure to check for reliability of a test. The teachers from the data in Practical 3A are interested in the reliability of their exam. They have decided to use Cronbach’s Alpha to check this
1.  Open the data for Prac3A t o check the reliability of a 17-item phonetics test
2.  Decide whether the test is reliable by going to Analyze > Scale > Reliability Analysis.  Put all the Qu estions in the Items (and not the Total and the Grade), and choose Alpha next to Model . Click OK. The Output will give you a correlation coefficient.  Do you think this is a reliable test?
3.  Now we will check the individual items. Go to Analyze > Scale > Reliability Analysis.  Click on Statistics. Check Inter-Item Correlations and Descriptives for Scale if item deleted. Click OK. The output will give you the correlations between items and will give you all the Cronbach’s Alpha values without a particular item. With the deletion of which item do you get the highest reliabil

## testing the normality of the distribution<a id="sec-4-4" name="sec-4-4"></a>

One of the assumptions of the t-test (apart from the equality of the variances in the groups) is that the data are distributed according to the normal distribution. You could of course simply run Explore and look at the Skewness and the Kurtosis. If Skewness and Kurtosis is very close to 0, or at least between- 1 and 1, you can assume that the distribution is approximately normal. However, some of you may want to know what the chance is that you go wrong in assuming the normal distribution. This can be established by applying the Kolmogorov-Smirnov test. We’ll apply this test in SPSS using the data from Practical 2.

Please note: if you want to test for normality in an experiment with more than one group, you’ll have to run separate analyses for the each group. It’s important the distribution of each group is normal, rather than the distribution of the scores of the two groups taken together.

    data <- read.csv("./data/p3a.csv",na="",header=TRUE)
    ks.test(data$Q1,data$Q2,"pnorm")

     null device 
              1
    [1] 0.9962291
    
            Two-sample Kolmogorov-Smirnov test
    
    data:  data$Q1 and data$Q2
    D = 0.73846, p-value < 2.2e-16
    alternative hypothesis: two-sided
    
    Warning message:
    In ks.test(data$Q1, data$Q2, "pnorm") :
      p-value will be approximate in the presence of ties