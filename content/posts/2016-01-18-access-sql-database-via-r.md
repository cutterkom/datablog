---
title: Access SQL-Database via R
author: kbrunner

date: 2016-01-18T10:05:19+00:00
url: /2016/01/18/access-sql-database-via-r/
categories:
  - R
tags:
  - database
  - Import
  - import sql
  - sql

---
[RMySQL][1] is a handy package to import data from a sql database in R. 

One caveat: if the location is on localhost, [the host needs to be][2] `host = "127.0.0.1"`, instead of `host = "localhost"`

    library(RMySQL)

    # if database on localhost
    db = dbConnect(MySQL(), user='root', password='root', host = "127.0.0.1", port=8888, dbname="table_name")

    # look at tables in database
    dbListTables(db)

    # variables in a table
    dbListFields(db, 'table_name')

    # sql query to get all data in a table
    query = dbSendQuery(db, "SELECT * FROM table_name")

    # save as dataframe
    df = fetch(query, n=-1)

    head(df)


 [1]: https://cran.r-project.org/web/packages/RMySQL/RMySQL.pdf
 [2]: http://stackoverflow.com/questions/31136701/cant-connect-to-local-mysql-server-through-socket-error-when-using-ssh-tunel
