---
title: Turn dataframe upside down in R / Flip dataframe
author: kbrunner

date: 2016-01-04T17:04:23+00:00
url: turn-dataframe-upside-down-in-r-flip-dataframe/
categories:
  - R
tags:
  - reshape
  - wrangle

---
    # start
        [,1] [,2]
     [1,]    1   10
     [2,]    2    9
     [3,]    3    8
     [4,]    4    7
     [5,]    5    6
     [6,]    6    5
     [7,]    7    4
     [8,]    8    3
     [9,]    9    2
    [10,]   10    1


    #result
        [,1] [,2]
     [1,]   10    1
     [2,]    9    2
     [3,]    8    3
     [4,]    7    4
     [5,]    6    5
     [6,]    5    6
     [7,]    4    7
     [8,]    3    8
     [9,]    2    9
    [10,]    1    10

    # df = dataframe
    df[nrow(df):1,]
