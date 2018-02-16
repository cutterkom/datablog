---
title: Merge two spatial datasets in R
author: kbrunner

date: 2015-12-30T10:52:19+00:00
url: /2015/12/30/merge-two-spatial-datasets-in-r/
categories:
  - GIS
  - R
tags:
  - GIS
  - Merge geodata
  - spatial data

---
Merging two spatial data has two caveats:
  
1. make sure the datasets have the same projections. <´Whereas ArcGIS and QGIS do this on their own, R is not.
  
2. the `over`-command is looking only for the first intersection. If there are multiple intersection, [you have to options to merge][1]

    library(rgdal)

    # load two datasets with spatial data
    geodata1 <- readOGR("shapefiles", "geodata1")
    geodata2 <- readOGR("shapefiles", "geodata2")

    #check if the same projection
    stopifnot(proj4string(geodata1) == proj4string(geodata2)) 

    proj4string(geodata1)
    proj4string(geodata2)

    # look at projections: if different decide for one and reproject
    # get projection of geodata1
    geodata1_CRS <- CRS(proj4string(geodata1))
    # reproject geodata2 with projection of geodata1
    geodata2_reprojected <- spTransform(geodata2, geodata1_CRS)

    # now merge: 
    merged_geodata <- over(geodata2_reprojected, geodata1)

[Source][1]

 [1]: http://www.nickeubank.com/wp-content/uploads/2015/10/RGIS2_MergingSpatialData_part1_Joins.html
