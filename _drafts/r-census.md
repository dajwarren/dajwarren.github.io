---
layout: post
title: "Plotting census data with R"
thumbnail: code
---
*Note: This is only for the UK 2011 census, using the CDRC datasets.*

About six months back I discovered the fantastic interactive maps on the CDRC website (careful: they're computationally intensive and your browser might freeze). However, they offer fewer data overlays for Scotland, which made me realise that if I wanted to look at some sociodemographic maps for Aberdeen I'd have to find the data and plot it myself.

As it turns out, the CDRC make a lot of data sets publicly available, including the 2011 UK census (by data zones, not individuals) and package them with shapefiles for plotting maps (I admit I'm still slightly excited about that)! A bit of playing around with R later, and we have things like this:

[IMAGE]

That's a plot of Scots speakers expressed as a percentage of the population of each of the data zones within the boundaries of Aberdeen City.

```R
# Here are the libraries we're going to be using
library(dplyr)
library(scales)
library(ggplot2)
library(ggmap)
library(gpclib)
library(maptools)
library(mapproj)
library(Cairo)
library(RColorBrewer)
library(Hmisc)

# Read the relevant file into R
scotsfile <- read.csv('~/Documents/geodata/aberdeen/census/tables/KS206SC_dz11.csv')

# Using dplyr and piping (yay!), save columns 1 (datazone id), 2 (datazone population) and the variable of interest (in this case answers to a Scots usage question (column 7))
scots <- scotsfile %>%
  select(.,c(1:2,7))

names(scots) <- c('id', 'pop', 'scots')

# Create new column ($percent) and calculate the percentage of Scots users for each data zone.
scots <- scots %>%
                mutate(percent = (scots/pop)*100) %>%
                mutate(percent = round(percent, 0))

# Bin each percentage in intervals of 5%
scots <- scots %>%
  mutate(bin = cut(percent, breaks = c(10,15,20,25,30,35,40,45,50,55,60),
                   labels = c('10-14', '15-19', '20-24', '25-29', '30-34',
                              '35-39', '40-44', '45-49', '50-54', '55-60')))

# Open file choice dialogue to select correct shapefile, then reformat it so it can be used by ggplot2
area.dz <- readShapePoly(file.choose())
gpclibPermit()
plot.dz <- fortify(area.dz, region='DataZone')

# Combine both data frames
plot.scots <- left_join(plot.dz, scots)

# Create the colour palette
palette.scots <- c('#4575b4','#74add1','#abd9e9','#e0f3f8','#ffffbf',
'#fee090','#fdae61','#f46d43','#d73027')

# Plot the map with ggplot2
plot1 <- ggplot() +
  geom_polygon(data = plot.scots, aes(x = long, y = lat, group = group,
  fill = percentages), color = "black", size = 0.25) +
  coord_equal() +
  scale_fill_manual(values = palette.scots) +
  theme_nothing(legend=TRUE) +
  guides(fill = guide_legend(reverse = TRUE))

# Save the output to a file
ggsave(plot1, file = "plot1.png", width = 20, height = 21, type = "cairo-png")
```
