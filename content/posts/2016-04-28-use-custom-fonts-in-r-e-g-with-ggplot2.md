---
title: Use custom fonts in R, e.g. with ggplot2
author: kbrunner

date: 2016-04-28T08:46:11+00:00
url: /2016/04/28/use-custom-fonts-in-r-e-g-with-ggplot2/
categories:
  - R
  - Visualization
tags:
  - font
  - ggplot2

---
The [showtext package][1] can import .otf font files, that can be used with ggplot2 theme options.

    library(showtext)
    font.add("NameOfFont", "NameOfFont.otf")
    showtext.auto() 

    library(ggplot2)
    ggplot(d, aes(x = x, y = y)) +
    geom_point() +
    theme(text = element_text(family="NameOfFont")) 



Alternativly, there is [extrafont][2]. The downside: It can only use .ttf files.

 [1]: https://github.com/yixuan/showtext
 [2]: https://www.r-project.org/nosvn/pandoc/extrafont.html
