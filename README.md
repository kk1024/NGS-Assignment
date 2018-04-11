---
title: "NGS lecture 4 Written assignment"
author: "Jack"
date: "2018年4月10日"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown

The data used in this assignment are from genome biology paper "[New reference genome sequences of hot pepper reveal the massive evolution of plant disease-resistance genes by retroduplication](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-017-1341-9)"



```{r}
library(xlsx)
table<-read.xlsx(file = "D:\\transfer/NGS/plot.xlsx",sheetIndex = "supplement table",startRow = 1,endRow = 315)

summary(table)
```


## Making Plots


```{r pressure}
plot(table)

#look into individual part

library(ggplot2)
qplot(Leaf,Root,data=table)
qplot(Leaf,Stem,data=table)
qplot(Stem,Root,data=table)
qplot(Leaf,Flower,data=table)
qplot(Flower,Root,data=table)
qplot(Flower,Stem,data=table)

```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
