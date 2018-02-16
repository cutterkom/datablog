---
title: How to load data from Google Spreadsheets into R
author: kbrunner

date: 2015-12-10T08:35:35+00:00
url: /2015/12/10/how-to-load-data-from-google-spreadsheets-into-r/
categories:
  - R
tags:
  - Google Spreadsheets
  - Import
  - Import Data

---

# How to load data from Google Spreadsheets into R

The [googlesheets package][1] from statistics professor Jennifer Bryan at the University of British Columbia is by far the most convenient way.

``` R
    library(dplyr)
    library(googlesheets)

    # load all sheets in google drive by authentication (new browser tabs with 
    all_my_sheets_in_drive <- gs_ls()

    # show all sheets in R
    my_sheets

    # get a specific sheet
    d <- gs_title("Name of Googlesheet")

    # get worksheet 
    d <-  d %>% gs_read(ws="worksheet 1")
``` 

 [1]: https://github.com/jennybc/googlesheets
