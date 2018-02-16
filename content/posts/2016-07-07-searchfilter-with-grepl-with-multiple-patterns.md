---
title: Search/Filter with grepl with multiple patterns
author: kbrunner

date: 2016-07-07T08:43:50+00:00
url: /2016/07/07/searchfilter-with-grepl-with-multiple-patterns/
categories:
  - R
tags:
  - filter
  - grepl
  - pattern
  - string

---
Goal: Filter a dataframe, that contains parts of strings, that are in another dataframe.

    # dataframe that contains strings
    d1 <- c("halloauch", "hieronymus", "grüßdich", "hello", "hi", "hallo")
    d1 <- data.frame(d1)
    # dataframe that contains patterns
    d2 <- c("hi", "hallo")
    d2 <- data.frame(d2)



`grepl` can&#8217;t search through a dataframe. It needs a vector with the `or`-operator

# convert patterns to vector
d2 <- as.vector(as.matrix(d2))
# combine patterns to a single element
d2 <- paste(d2, collapse="|")


check, if dataframe contains patterns and filter these elements: 

library(dplyr)
d %>% filter(grepl(d2, d1$name))
