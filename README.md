# Crashes in Melbourne
## An interactive map for visual thinking

The interactive map aims to create an interface using different techniques and tools in Geovisualisation. Users could interact with the map to investigate the information in public dataset of crashes in the last five years in Melbourne from VicRoads. The map implementation follows exploratory data analysis and visualisation pipelines strictly and provides an ideal interface with visual thinking.

## Summary

1 - Data Modelling and Selection
Crash_Last_Five_Years dataset has been used as primary data, which combine with the Greater Melbourne boundary data sourced from the ABS website. In the data selection process, crashes out of Melbourne boundary has been removed. In the data modelling process, formatted data includes the change rate of each year in each LGA area.

2 - Visual Mapping
In visual mapping stage, choropleth map, proportional map and heatmap have been added in the interface. The colour scheme has been selected carefully. For the choropleth map, the diverging colour scheme represents the change rate of crashes each year in each area. Moreover, sequential colour represents the density and count of total persons in the heatmap and proportional map.

3 - Visualisation
The map includes zoom, pan, switch layer, and setting time for users. When users zoom to a larger scale, the proportional plan will replace heatmap, and users could check summary information by clicking each crash circle. Users could also switch from the heatmap to choropleth map. Moreover, the map provides a time slider for users to check information for the different financial year. Figure 1 shows the console of the map. Users could find the distribution and changing patterns for crashes in the Greater Melbourne area by interacting with this good design and intuitive interface.
Figure 1 Iteration Interface

## Appendix
1. Crash_Last_Five_Years datasets from VicRoads
https://discover.data.vic.gov.au/dataset/crashes-last-five-years

2. SA2 boundary shapefile from ABS
https://www.abs.gov.au/browse?opendocument&ref=topBar
