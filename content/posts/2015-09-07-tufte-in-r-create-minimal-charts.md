---
title: 'Tufte in R: Create minimal charts'
author: kbrunner

date: 2015-09-07T13:13:14+00:00
url: /2015/09/07/tufte-in-r-create-minimal-charts/
categories:
  - R
tags:
  - package
  - plot

---
Edward Tufte, the inventor of the boxplot, was an advocate for simple charts. [Lukasz Piwek brings his rules to R (with code examples)][1].

> The idea behind Tufte in R is to use R &#8211; the most powerful open-source statistical programming language &#8211; to replicate excellent visualisation practices developed by Edward Tufte.

How to remove all superflousus information in R? With a combination of ggplot2 (or other plotting packages) and [ggthemes][2]:

ggplot default design:

[<img src="https://i2.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default-295x300.png?resize=295%2C300" alt="ggplot2 default" class="alignnone size-medium wp-image-34" srcset="https://i1.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default.png?resize=295%2C300 295w, https://i1.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default.png?w=542 542w" sizes="(max-width: 295px) 85vw, 295px" data-recalc-dims="1" />][3]

`ggplot(bg_long, aes(x = jahr, y = value, group = variable, colour = variable)) +geom_line(size=2)`

ggplot2 and the tufte theme:
  
[<img src="https://i1.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme-295x300.png?resize=295%2C300" alt="ggplot2 tufte theme" class="alignnone size-medium wp-image-35" srcset="https://i0.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme.png?resize=295%2C300 295w, https://i0.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme.png?w=542 542w" sizes="(max-width: 295px) 85vw, 295px" data-recalc-dims="1" />][4]

``Edward Tufte, the inventor of the boxplot, was an advocate for simple charts. [Lukasz Piwek brings his rules to R (with code examples)][1].

> The idea behind Tufte in R is to use R &#8211; the most powerful open-source statistical programming language &#8211; to replicate excellent visualisation practices developed by Edward Tufte.

How to remove all superflousus information in R? With a combination of ggplot2 (or other plotting packages) and [ggthemes][2]:

ggplot default design:

[<img src="https://i2.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default-295x300.png?resize=295%2C300" alt="ggplot2 default" class="alignnone size-medium wp-image-34" srcset="https://i1.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default.png?resize=295%2C300 295w, https://i1.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default.png?w=542 542w" sizes="(max-width: 295px) 85vw, 295px" data-recalc-dims="1" />][3]

`ggplot(bg_long, aes(x = jahr, y = value, group = variable, colour = variable)) +geom_line(size=2)`

ggplot2 and the tufte theme:
  
[<img src="https://i1.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme-295x300.png?resize=295%2C300" alt="ggplot2 tufte theme" class="alignnone size-medium wp-image-35" srcset="https://i0.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme.png?resize=295%2C300 295w, https://i0.wp.com/data.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme.png?w=542 542w" sizes="(max-width: 295px) 85vw, 295px" data-recalc-dims="1" />][4]

``

 [1]: http://motioninsocial.com/tufte/#minimal-line-plot
 [2]: https://cran.r-project.org/web/packages/ggthemes/vignettes/ggthemes.html
 [3]: https://i0.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-default.png
 [4]: https://i0.wp.com/ddj.katharinabrunner.de/wp-content/uploads/2015/09/ggplot2-tufte-theme.png
