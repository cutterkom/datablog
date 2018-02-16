---
title: Split string in characters and numbers
author: kbrunner

date: 2015-09-17T08:23:07+00:00
url: /2015/09/17/split-string-in-characters-and-numbers/
categories:
  - R
tags:
  - as.numeric
  - string
  - stringr

---
Data:
  
    China 91 km  91
    Iran 921 km 921
    Pakistan 2,670 km
    Tajikistan 1,357 km
    Turkmenistan 804 km
    Uzbekistan 144 km

I want the information of the numeric border length in a new columns. S[olution via stringr library][1] 


    # extract the numbers and create new variable named new_var
    df$new_var <- as.numeric(str_extract(df$column_to_split, "[0-9]+"))

  
    extract the characters and create new variable named country
    df$country <- (str\_extract(df$column\_to_split, "[aA-zZ]+"))</code>

 [1]: http://stackoverflow.com/a/9756409/2646974
