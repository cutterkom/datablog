---
title: Import csv with 2 pairs of locations coordinates in QGIS
author: kbrunner

date: 2015-09-23T15:41:20+00:00
url: /2015/09/23/import-csv-with-2-pairs-of-locations-coordinates-in-qgis/
categories:
  - QGIS
tags:
  - csv
  - Geodata

---
What I have: A csv-table with two pairs of lat/long. QGIS can import only one pair &#8211; except when the two pairs of coordinates are reshaped to [WKT, Well Known Text][1].

A new colum named wkt is needed.

    LINESTRING(long1 lat1, lat2 long2)

# example

    first_row, wkt
    1,LINESTRING(51.210021 6.786209,6.786209 51.213942)
    2,LINESTRING(51.213942 6.761064,6.761064 51.270831)

First choose wkt when importing, then line &#8211; and done.

 [1]: https://en.wikipedia.org/wiki/Well-known_text
