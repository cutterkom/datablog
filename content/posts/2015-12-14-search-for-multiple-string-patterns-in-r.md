---
title: Search for multiple string patterns in R
author: kbrunner

date: 2015-12-14T13:07:32+00:00
url: /2015/12/14/search-for-multiple-string-patterns-in-r/
categories:
  - R
tags:
  - dplyr
  - grep
  - pattern
  - string
  - stringr

---
make a string pattern vector, then search for strings by combining patterns with OR operator 

    library(dplyr)
    library(stringr)
    string_patterns <- c("stringpattern1", "stringpattern2")
    df %>% filter ( str_detect ( col_with_strings, paste ( string_patterns, collapse = '|' )))
