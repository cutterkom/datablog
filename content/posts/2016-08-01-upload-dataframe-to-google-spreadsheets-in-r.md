---
title: Upload dataframe to Google Spreadsheets in R
author: kbrunner
date: 2016-08-01T08:30:45+00:00
url: /2016/08/01/upload-dataframe-to-google-spreadsheets-in-r/
categories:
  - R
tags:
  - Google Spreadsheets

---


    library(googlesheets)

    # dataframe
    df <- data.frame(x = c(1,2), y=c(2,3))

    # access googlesheets
    all_my_sheets_in_drive <- gs_ls()

    # access spreadheet
    gs <- gs_title("my spreadsheet")

    # create worksheet
    gs_ws <- gs_ws_new(gs, ws_title = "new worksheet")
     
    # upload dataframe to worksheet "new worksheet"
    gs_edit_cells(gs, ws="new worksheet", input = df, trim = TRUE)
