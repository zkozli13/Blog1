---
layout: post
title: "Barplot"
description: "Here is how to make a barplot using Rstudio"
tags: [sample post, video]
date: 2013-06-25
---

This is the code used used in Rstudio to make a barplot using the lahman data set.

standing<-c('sophmore','sophmore','junior','freshman','junior','senior')
standing<-factor(standing,levels=c('freshman','sophmore','junior','senior'))

 #Extracting the data-------------------------

query<-"SELECT name,HR
FROM Teams
WHERE yearID=1980
ORDER BY HR"

result<-sqldf(query)

 #visualizing the data------------------------


ggplot()+
  geom_bar(data=result,aes(x=name,y=HR),stat='identity',color='blue',fill='white')+
  coord_flip()+
  ylab('homeruns')+
  xlab('team')+
  ggtitle('1980 Team Homerun Distrubtion')

result$name<-factor(result$name,levels=result$name)

