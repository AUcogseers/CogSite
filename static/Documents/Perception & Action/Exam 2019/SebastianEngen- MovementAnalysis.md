---
title: "Movement Analysis"
author: "Sebastian"
date: "6/3/2019"
output: word_document
---





```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
#Loading necessary packages
library(tidyverse)
library(signal)
#Setting Working Directory
getwd()
setwd("/Users/FlowersnIce-cream/Google Drev/Hogwarts/4/Models for perception and action/Exam/Exam/")
```

## Get Data Setup
```{r cars}
#Load data -> Read TXT
data <- read.table("timsigF_211_1_1_1_short.txt", header = FALSE, sep = ",", dec = ".")
#Rename the columns to sample, time, x, y, z.
names(data) <-  c("sample", "time", "x", "y", "z")
```

## Correct the z dimension by flipping all values so that more positive ones are shown
# I use the abs() function as all points were negative and would therefore just be turned into positive
```{r pressure, echo=FALSE}
#Plot without flipping
ggplot(data) +
  geom_point( aes(x,z)) +
  labs(x = "Trajectory", y = "Height") # add axis titles
#Moving On
#Make Z into absolute numbers
data$z2 <- abs(data$z)

#Then we center the data to make it look more intuitive
# center the data by substracting the minimum values
data$xc <-  data$x - min(data$x)
data$yc <-  data$y - min(data$y)
data$z2c <-  data$z2 - min(data$z2)

#plot x and z
ggplot(data) +
  geom_point( aes(xc,z2c)) +
  labs(x = "Trajectory", y = "Height") # add axis titles

```
#Calculate z velocity and plot it against time.
```{r}
# Calculating velocity
data$velocity <- c(0,diff(data$z2c) / diff(data$time))

ggplot(data) +
  geom_line( aes(time,velocity)) +
  labs(x = "time", y = "velocity") # add axis titles

```
#Apply a Butterworth filter to z velocity with reasonable parameters. Plot the filtered velocity on top of the unfiltered one.
```{r}
# For reasonable parameters, I use the same as in the original study (Vesper, C., Schmitz, L., & Knoblich, G. (2017))
butter <- butter(4, 0.1, type ='low')
data$velocity2 <- filtfilt(butter,data$velocity)
# Green unfiltered, Red filtered
ggplot(data) +
  geom_line( aes(time,velocity)) + geom_line( aes(time,velocity2, color ="red")) +
  labs(x = "time", y = "velocity (Red is the filtered)") # add axis titles

```
#Make a final plot with z and the nicely filtered velocity over time.
```{r}
ggplot(data) + geom_line( aes(time,velocity2, color = "red")) + geom_line( aes(time,z2c))  +
  labs(x = "time", y = "velocity = Red, z = black") # add axis titles

```
#Describe (= text, not code) what relation z velocity has to z and how z velocity can be used to extract the maximal vertical extension. [5%]
finger was kept a bit above the table
2 samples every second 120HZ - time in second
Movement Amplitude Exagerations

