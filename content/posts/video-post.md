---
layout: post
title: "Barplot"
description: "Here is how to make a barplot using Rstudio"
tags: [sample post, video]
date: 2013-06-25
---

Data Visualization is an important concept in data science. Here we will be using a bar plot as an example of data visualization. A bar chart or bar graph is a chart or graph that presents categorical data with rectangular bars with heights or lengths proportional to the values that they represent.

First we will install the necessary packages for this example:

In this example we will be looking at all of the homerun totals of all of the teams in the MLB during the 1980's:

This part of the example allows us to order the bar plot in any way we want:

geom_bar allows us to make the height of the bar proportional to the number of cases in each group coord_flip() flips the axis of the plot
