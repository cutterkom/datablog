---
title: Start x-axis and y-axis at 0
author: kbrunner

date: 2016-07-04T11:13:16+00:00
url: /2016/07/04/start-x-axis-and-y-axis-at-0/
categories:
  - R
tags:
  - axis
  - ggplot2

---
    d %>% ggplot(aes(x = x, y=y) + geom_line() + expand_limits(y = 0, x = 0)

