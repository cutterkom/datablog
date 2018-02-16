---
title: Count observations with dplyr
author: kbrunner

date: 2015-08-21T12:03:54+00:00
url: /2015/08/21/count-observations-with-dplyr/
categories:
  - R
tags:
  - code
  - dplyr

---
Suppose you have this dataset and you want to count how often each country appears:

    country, somedata
    Germany, 2
    Germany, 3
    Germany, 4
    Italy, 4
    Italy, 3


Code with dplyr:
  
1. group the countries
  
2. count with helper function n()


library(dplyr)
data %>% group_by(country) %>% summarize(count=n())`
