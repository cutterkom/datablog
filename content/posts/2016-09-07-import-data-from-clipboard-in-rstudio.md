---
title: Import data from clipboard in RStudio
author: kbrunner

date: 2016-09-07T08:57:21+00:00
url: /2016/09/07/import-data-from-clipboard-in-rstudio/
categories:
  - R
tags:
  - clipboard
  - Import
  - import csv

---
Copy your data, use the snippet below. Ready.

    df <- read.table(pipe("pbpaste"), sep="\t", header=T)
