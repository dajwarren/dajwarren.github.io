---
layout: post
title: "Aberdeen, Scots and the 2011 census"
thumbnail: code
---
For the first time, the 2011 census in Scotland asked a series of questions about Scots usage. While the data is available through the [census website](http://www.scotlandscensus.gov.uk/census-results), the datasets on the CDRC site come with ```.shp``` files for plotting maps, which I might have got a little over-excited about. While I'm sceptical of the results for enough reasons to fill another blog post (I should really write that sometime), I couldn't resist the opportunity to make some pretty graphics of them. They'll probably find their way into my thesis as well because everyone likes maps.

It's also worth noting these maps are for 'data zones' [which need to be explained]

## Method
Everything was done in R. For each data zone, I calculated the percentage of the population that answered yes to each Scots-related question and then grouped them in 5% bins (except for the lowest group of 0-10%). I used the R packages ```ggmap``` and ```maptools``` for producing the visualisations.

## Aberdeen
