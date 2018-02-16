---
title: Merge spatial data and dataframe in R
author: kbrunner

date: 2015-12-30T10:45:29+00:00
url: /2015/12/30/merge-spatial-data-and-dataframe-in-r/
categories:
  - GIS
  - R
tags:
  - Merge geodata
  - spatial data

---
# merge just like two dataframes with merge command

    worldCountries <- merge(worldCountries, countryData, by.x = "id-number", by.y = "countryID")
