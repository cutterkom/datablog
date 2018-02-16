---
title: Change multiple columns to as.numeric from factor
author: kbrunner

date: 2015-09-10T08:37:00+00:00
url: /2015/09/10/change-multiple-columns-to-as-numeric/
categories:
  - R
tags:
  - as.numeric
  - type

---
```
    # look for the columns in the data matrix. In this case: columns 4 to 11
    data[,4:11]
    # Then change them as to numeric
    data[,4:11] <- sapply(data[,4:11], as.numeric(as.character(data[,4:11])))      
```

[Source][1]

 [1]: https://everydropr.wordpress.com/2013/05/20/how-to-convert-a-range-of-variables-from-factor-to-numeric-in-r/
