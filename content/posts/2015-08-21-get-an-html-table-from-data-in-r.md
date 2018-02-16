---
title: Get an HTML table from data in R
author: kbrunner

date: 2015-08-21T11:48:55+00:00
url: /2015/08/21/get-an-html-table-from-data-in-r/
categories:
  - R

---
[Knitr package][1] outputs R data in many different formats, e.g. HTML or LaTex

From a dataframe to an HTML table for embedding on a website:

    install.packages("knitr")

    library(knitr)

    kable((data), format = 'html', table.attr = "class=nofluid")


 [1]: https://cran.r-project.org/web/packages/knitr/knitr.pdf
