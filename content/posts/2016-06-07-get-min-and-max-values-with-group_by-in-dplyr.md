---
title: Get min and max values with group_by in dplyr
author: kbrunner

date: 2016-06-07T07:19:22+00:00
url: /2016/06/07/get-min-and-max-values-with-group_by-in-dplyr/
categories:
  - R
tags:
  - dplyr
  - group
  - group_by
  - max
  - min

---
    library(dplyr)
    df %>% group_by(group_variable) %>% filter(value == max(value)) 

    df %>% group_by(group_variable) %>% filter(value == max(value))

[via stackoverflow][1]

 [1]: http://stackoverflow.com/questions/24237399/how-to-select-the-rows-with-maximum-values-in-each-group-with-dplyr
