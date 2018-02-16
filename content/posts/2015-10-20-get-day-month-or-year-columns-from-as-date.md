---
title: Get day, month or year columns from as.Date()
author: kbrunner

date: 2015-10-20T14:20:36+00:00
url: /2015/10/20/get-day-month-or-year-columns-from-as-date/
categories:
  - R
tags:
  - as.Date()
  - date
  - day
  - month
  - year

---
Suppose you have a data frame (df) with [a date column][1]:
  


    x    date
    10    2015-10-01
    22    2014-09-16

Now you want three new columns &#8211; one for the day, one for the month, one for the year:

    # get the year
    df$year <- format(df$date, format = "%Y")
    # 2 ways to get the months
    df$month <- format(df$date, format = "%m")
    df$month <- months(df$date) 
    # get the day
    df$day <- format(df$date, format = "%d")

The resulting dataframe:

    x    date    year    month    day
    10    2015-10-01    2015    10    01
    11    2014-09-16    2014    09    16

[All date format options.][1]

 [1]: http://www.statmethods.net/input/dates.html
