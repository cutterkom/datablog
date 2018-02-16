---
title: Install Hugo
author: Katharina Brunner

date: 2016-12-16
url: /post/install-hugo
categories:
  - Snippets
tags:
  - CMS
  - blog

---



[Hugo](htpp://www.gohugo.io) is a static site CMS

A [great tutorial in German](http://privat.albicker.org/blog/tags/hugo/)

- Install Hugo
    
   
`brew install hugo`

`hugo new site blog`

- Install a theme, e.g. `cocoa`

`git clone https://github.com/nishanths/cocoa-hugo-theme.git themes/cocoa`

- Activate the theme

`hugo -t cocoa`

- Change the date format depeding on the theme, e.g. `cocoa`: look up correct date format in the `config`-file of your [theme](https://github.com/nishanths/cocoa-hugo-theme/blob/master/exampleSite/config.toml). Use that information in your `config.toml` as a parameter

`[params]`

`dateform = "Jan 2, 2006"`

`dateformfull = "Mon Jan 2 2006 15:04:05 MST"`

- Upload the files to a server or Github

