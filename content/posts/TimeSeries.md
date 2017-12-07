---
layout: post
title: "Time Series"
description: "Here is how to make a time series in Rstudio"
tags: [sample post, link post]
date: 2013-08-12
comments: true
link: 
---
This is the code used in Rstudio to make a time series using the lahman data set. 

 # extracting the data---------------------------

query<- "SELECT yearID,HR
FROM Batting
WHERE playerID = 'ruthba01'"

result<- sqldf(query)

 # visualize the data----------------------------

ggplot()+
  geom_line(data=result,aes(x=yearID,y=HR))+
  geom_point(data=result,aes(x=yearID,y=HR))+
  ggtitle("Ruth's homerun Totals Through the Years")+
  xlab("year")+
  ylab("homeruns")
