---
title: Create variable with repeating values
author: kbrunner

date: 2015-09-21T11:02:16+00:00
url: /2015/09/21/variable-with-repeated/
categories:
  - R
tags:
  - repeat

---
What I want: A vector with years from 1990 to 2000 with each year appearing 10 times, then 2001 to 2010 5 times per year.

    years_1 <- rep(1990:2000, each=10) 
    years_2 <- rep(2001:2010, each=5) 
    # take them together 
    years <- append(years_1, years_2)

&nbsp;
