---
layout: post
title: Testing R for Jekyll
date: 2018-09-27 21:00
description:
categories:
 - R
tags:
---
After some Googling, I have finally managed to get my .Rmd files converted to .md for use with Jekyll + GitHub Pages. It still requires a manual step to move the images to the right place, but I am sure that there is a way to automate that as well. In short, it involves having this in the meta-data at the top of the .Rmd file to tell it to retain the .md file that is generated as part of the knitting process:
```
output:
  html_document:
    keep_md: true
```
Here is what the default .Rmd template looks like after being converted:

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


```r
summary(cars)
```

```
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
```

## Including Plots

You can also embed plots, for example:

![](/assets/images/2018-09-27-testing-R-for-jekyll/figure-html/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
