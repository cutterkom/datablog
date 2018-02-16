---
title: Delete \r\n\t in string in R
author: kbrunner

date: 2015-09-21T13:33:03+00:00
url: /2015/09/21/delete-rnt-in-string/
categories:
  - R
tags:
  - remove
  - string

---
If you scrape a website, it is possbile that you extract some hidden text, e.g. \n = newline, \r = carriage return or \t = tab.

This is how you remove them from a string:

    # data
    # \r\n some_text
     
    gsub('[\r\n\t]', '', data)

    # result: 
    # some_text
