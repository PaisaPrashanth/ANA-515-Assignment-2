# ANA-515-Assignment-2
Data Loading and Describing Biopic Dataset


---
title: "ANA 515 Assignment 2"
author: Prashanth Paisa
output: html_document
date: "2022-09-17"
---

The chosen dataset biopic dataset is collected from IMDb where various information is collected about various Biopics released by various countries in different years. The set of information is having 762 numbers of rows of information which are actually belongs to 14 numbers of class label information. 

```{r}
biopic_data <- read.csv("biopics.csv")
biopic_data
```
```{r}
library("dplyr")
biopic_data <- rename(biopic_data, "website" = "site")
biopic_data
```
```{r results = TRUE}

text_tbl <- data.frame( 
Names = c(biopic_data$title, biopic_data$website, biopic_data$country), 
Description = c("This column describes the title of the biopics", "This column describes the IMDb website URL", "This column describes the country where the biopics are made")
) 
text_tbl 


```
```{r}

myvars <- c("year_release", "number_of_subjects", "box_office")
newdata <- biopic_data[myvars]

Summarytable <- summary(newdata)
Summarytable

```


