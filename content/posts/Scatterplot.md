---
layout: post
title: Scatterplot
description: "Here is how to make a scatterplot in Rstudio"
date: 2013-08-16
lastmod: 2016-09-05
tags: [sample post, code, highlighting]
image:
  feature: 
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

This is the code used in rstudio to make barplots using the lahman dataset. 

 extracting the data-------------------------------------

query<- "SELECT playerID,sum(HR) as career_HR,sum(SO) as career_SO
FROM Batting
GROUP BY playerID
HAVING sum(HR)>=400"

result<- sqldf(query)

 visualizing the data------------------------------------

ggplot()+
  geom_point(data=result,aes(x=career_SO,y=career_HR,color="blue"))+
  ggtitle("Career Strikeouts VS Homeruns for Great Hitters")+
  xlab("Career Strikeouts")+
  ylab("Career Homeruns")


[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>

