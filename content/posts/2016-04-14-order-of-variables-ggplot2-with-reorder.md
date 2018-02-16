---
title: Order of variables ggplot2 with reorder()
author: kbrunner

date: 2016-04-14T08:39:28+00:00
url: /2016/04/14/order-of-variables-ggplot2-with-reorder/
categories:
  - R
  - Visualization
tags:
  - ggplot2
  - plot
  - reorder

---
The order of appearance is controlled in the [ggplot aesthetics via redorder()][1]

    p <- ggplot(
      
    data = d, aes(x = variable, y = reorder(film, index), fill = value, colour=&#8221;white&#8221;))

    # sort my films depending on the index variable
    ggplot(d, aes(x = variable, y = reorder(film, index))

    # descending
    ggplot(d, aes(x = variable, y = reorder(film,desc(index))


 [1]: http://stackoverflow.com/questions/3744178/ggplot2-sorting-a-plot
