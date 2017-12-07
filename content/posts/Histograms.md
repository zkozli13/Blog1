---
layout: post
title: Histograms
description: "Here is how to make a histogram in Rstudio"
tags: [sample post]
date: 2013-10-26
background: /images/triangular.png
---
This is the code used in Rstudio to make a Histogram using the lahman data set. 


 # extracting the data-----------------------------------

query<- "SELECT weight
FROM Master"

result<- sqldf(query)

 # visualize the data------------------------------------

ggplot()+
  geom_histogram(data=result,aes(x=weight,color="blue",fill="white"))+
  ggtitle("Baseball Player Weight Distribution")



