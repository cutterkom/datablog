---
title: Create Rank Variable with dplyr
author: kbrunner

date: 2016-06-08T07:31:55+00:00
url: /2016/06/08/create-rank-variable-with-dplyr/
categories:
  - R
tags:
  - dplyr
  - rank

---
```
library(dplyr)
df <- df %>% mutate(rank = dense_rank(desc(variable_to_be_ranked)))
```
