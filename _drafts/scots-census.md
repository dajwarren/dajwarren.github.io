---
layout: post
title: "Aberdeen, Scots and the 2011 census"
thumbnail: bar-chart
---
For the first time, the census in 2011 in Scotland asked a series of questions about people's use of Scots. While the data is available through the [census website](http://www.scotlandscensus.gov.uk/census-results), here I'm working with the datasets released on the CDRC site as they come with ```.shp``` files for plotting maps which saved me having to track them down separately. While I'm sceptical of the results for enough reasons to fill another blog post (I should really write that sometime), I couldn't resist the opportunity to make some pretty graphics of them. They'll probably find their way into my thesis as well because everyone likes maps, and by 'everyone' I might just mean me...

It's also worth noting these maps are for 'data zones' [which need to be explained]


## Method
Everything was done in R. For each data zone, I calculated the percentage of the population that answered yes to each Scots-related question and then grouped them in 5% bins (except for the lowest group of 0-10%). I also created a 'total Scots ability' category, combining those who claimed to be able to read, write and speak Scots with those who could only speak it and those who could speak, read but not write it.


I used the R packages ```ggmap``` and ```maptools``` for producing the visualisations.

## Aberdeen City
[![Scots ability in Aberdeen City]({{ site.baseurl }}/assets/images/aberdeen_scots.png)]({{ site.baseurl }}/assets/images/aberdeen_scots.png)


# Aberdeenshire

[![Scots ability in Aberdeenshire]({{ site.baseurl }}/assets/images/aberdeenshire_scots.png)]({{ site.baseurl }}/assets/images/aberdeenshire_scots.png)
