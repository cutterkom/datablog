---
title: Sum up with group_by in R and dplyr
author: kbrunner

date: 2015-08-21T12:09:44+00:00
url: /2015/08/21/sum-up-with-group_by-in-r-and-dplyr/
categories:
  - R
tags:
  - code
  - dpylr

---
Suppose you have this dataset and you want to add up each countries values:

    country, somedata
    Germany, 2
    Germany, 3
    Germany, 4
    Italy, NA
    Italy, 3
France, 2

With dpylr:

- group observations
- sum `somedata` and exclude missing values


    library(dplyr)
    data %>% group_by(country) %>% summarize(data_by, total=sum(somedata, na.rm=TRUE))
