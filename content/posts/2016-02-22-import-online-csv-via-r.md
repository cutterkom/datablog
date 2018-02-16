---
title: Import online csv via R
author: kbrunner

date: 2016-02-22T10:33:57+00:00
url: /2016/02/22/import-online-csv-via-r/
categories:
  - R
tags:
  - Import
  - import csv
  - Import Data
  - RCurl

---
    library(RCurl)
    url <- getURL("http://www.adress.com/data.csv")
    d <- read.csv(text = url)
