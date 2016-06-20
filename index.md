---
title       : Hits and Run!!!
subtitle    : Data Visualization for All-Time Hits in MLB
author      : Mike Shih
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
ext_widgets : {rCharts: libraries/nvd3}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
--- 
## All-Time Hits in MLB
- The purpose of the project is to visualize all-time hits record in Major League Baseball.

- Lahman’s Baseball Database

- From 1871 to 2015

- Formats: csv, MS Access, SQL

- Database includes players' information (Master.csv) and career batting record (Batting.csv)

---

## Data Preparation - 1

- Covert middle names to abbreviation (names.R)

- Data proccessing (data_processing.R) 

1. merges Master.csv and Batting.csv
        
2. generates cumulative hits record, cumulative AB and seniority

3. removes the multiple data in the same year due to the transfering (remove_dup.R).   

---
## Data Preparation - 2

- User will input the maximum and minimun counts of hits on the sidebar panel. 

- The input values will pass to server.R and use funtion "careerhit" (in careerhit.R) to select players satisfied the criteria. 

---
## Ploting by rCharts NVD3


```r
library(rCharts)
library(dplyr)
```

Players with hits over 3500.

<iframe src=' figure/nvd3plot2-1.html ' scrolling='no' frameBorder='0' seamless class='rChart nvd3 ' id=iframe- chart3e1631d0ee1e ></iframe> <style>iframe.rChart{ width: 100%; height: 400px;}</style>

