---
title: Create a long-form dataset with tidyr or reshape2
author: kbrunner

date: 2015-08-22T13:45:17+00:00
url: /2015/08/22/create-a-long-form-dataset-with-tidyr-or-reshape2/
categories:
  - R
tags:
  - data wrangling
  - packages
  - reshape2
  - tidyr

---
There are at least two packages, which let you create data in a long-format. This a step in the process of getting tidy data. For many functions you need your data in this format, for example when creating a chart with multiple lines in ggplot2 in R.

When do you need this?

When your data is stacked:

    year 1  2
    2013 54 65
    2014 34 90
    2015 89 100

This form violates two thirds of [Hadley Wickham&#8217;s rules for tidy data][1]:

> 1. Each variable forms a column
  
> 2. Each observation forms a row
  
> 3. Each data set contains information on only one observational unit of analysis (e.g., families, participants, participant visits)

The same data in the best practice longform:

    year treatment result
    2013 1 54
    2013 2 65
    2014 1 34
    2014 2 90
    2015 1 89
    2015 2 100

Now, every variable has its column, every observation is a row.

## Two packages to get long-form data

  1. Reshape2
  2. Tidyr

### Reshape2

The central function in [reshape2][2] is called `melt()`

Example with dataset above:

    library(reshape2)
    data_long <- melt(data, id.vars="year", measure.vars=c("treatment a", "treatment b"), variable.name="treatment", value.name="result")

`measure.vars`: which columns need to be packed in melted into one column

`variable.name`: how is this new column called?

`value.name`: how is the value column called? default: value

Learn more about reshape2 in a tutorial: [An Introduction to reshape2][3]

### Tidyr

The function with tidyr is gather

    library(tidyr)
    gather(year, result, 1:2)

Suppose you have 5 different treatments and the header row of your stacked data looks like this:
  
`year 	1 	2 	3 	4 	5`

The code is then:
  
`gather(year, result, 1:5)`

A tutorial for tidyr: [Data Processing with dplyr & tidyr][4]

Both packages are by [Hadley Wickham][5], they can do much more than making stacked data long.

 [1]: http://vita.had.co.nz/papers/tidy-data.pdf
 [2]: https://cran.r-project.org/web/packages/reshape2/reshape2.pdf
 [3]: http://seananderson.ca/2013/10/19/reshape.html
 [4]: https://rstudio-pubs-static.s3.amazonaws.com/58498_dd3b603ba4fb4b469bb1c57b5a951c39.html
 [5]: http://ddj.katharinabrunner.de/2015/08/21/dplyr-package-for-data-wrangling/
