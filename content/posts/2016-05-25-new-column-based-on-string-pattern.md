---
title: New column based on string pattern
author: kbrunner

date: 2016-05-25T09:10:13+00:00
url: /2016/05/25/new-column-based-on-string-pattern/
categories:
  - R
tags:
  - dataframe
  - replace
  - string

---
    # Find a string pattern in a column. Create a new column
    df$new_column[df$colum_with_pattern %in% c("abc", "def")] <- "string in new column"

    # alternative with pattern vector
    patterns <- c("abc", "def")

    df$new_column[df$colum_with_pattern %in% patterns] <- "string in new column"
