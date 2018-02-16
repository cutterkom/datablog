---
title: Delete n rows at top or bottom of a dataframe in R
author: kbrunner

date: 2016-07-07T10:49:44+00:00
url: /2016/07/07/delete-n-rows-at-top-or-bottom-of-a-dataframe-in-r/
categories:
  - R
tags:
  - dataframe
  - head
  - tail

---
Example 1: Delete the first 20 rows of a dataframe
  
    tail(d, -3)

Example 2: Delete the last 20 rows of a dataframe
  
    head(d, -3)
