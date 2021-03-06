---
title: "2. Estimates and ggplot2"
author: "jsg"
date: "Last compiled on 02 July, 2022 12:59"
output:
  html_document:
    toc: true
    toc_float: true
    keep_md: true
    self_contained: true
---


Remember you should

* add code chunks by clicking the *Insert Chunk* button on the toolbar or by
pressing *Ctrl+Alt+I* to answer the questions!
* **knit** your file to produce a markdown version that you can see!
* save your work often 
  * **commit** it via git!
  * **push** updates to github

## Using ggplot2
Let’s return to the mammal sleep dataset that we left off with last week. 
Load the dataset

```r
sleep <- read.csv("https://raw.githubusercontent.com/jsgosnell/CUNY-BioStats/master/datasets/sleep.csv", stringsAsFactors = T)
#need to use stringsAsFactors to make characters read in as factors
```
Last time you used the built-in plot functions to do some plots. Let’s replace 
those with ggplot2 and do some practice.

1. First plot how TotalSleep is explained by BrainWt (remember the issues with 
the data).  Use ggplot2 to plot the relationship.

2. Next color code each plot point by whether or not its a primate.  In order 
to do this you can use the Primate column or (following class code) make a new 
column called Taxa to represent the information (hint:search for “ revalue”). 
Make sure axes are well-labeled.

3. Let’s work with histograms.
* What type of variation do we see in total time spent sleeping? Create a 
histogram to explore this issue.
* Facet the graph you created based on whether or not the animal is a primate 
(Primate column).
* Now only graph the data for primates.

4. Develop a properly-labeled bar graph with error bars to explore how total 
sleep changes with 
* Primate (relabeled as yes/no as Primate/Non-Primate; note 
there are multiple ways to do this!) – use a 95% confidence interval for the bar
* Predation risk (as a factor!) – use 1 standard error for the bar. Note the difference!
