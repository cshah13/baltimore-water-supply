# baltimore-water-supply


## Background Information



## Business Question

_**How do nitrate/nitrite/nitrogen levels differ throughout the water supply in Baltimore, Maryland?**_

## Open Data
This analysis uses open data from...

The following data set was used for this analysis...

The original data set can be viewed here...

## Data Analysis Questions
Microsoft Office Excel and MapBox will be used to conduct a cluster analysis, time series analysis, and geospatial analysis to answer the following data questions:
1. How can Baltimore water stations be organized into clusters based on the presence of nitrate/nitrite/nitrogen levels?
2. How do the average observed levels of nitrate/nitrite/nitrogen compare between each of the clusters over time?
3. 


## Data Answer 1
### How can Baltimore water stations be organized into clusters based on the presence of nitrate/nitrite/nitrogen levels?

The Microsoft Office Excel Solver tool was used to identify three clusters representing the data. The water stations were grouped based on the calculated z-scores for the presense of nitrate/nitrite/nitrogen in each water station. Cluster 1 consists of nitrate/nitrite/nitrogen levels that are below average in relation to the other stations; there are 17 stations in this cluster, and the cluster node is Warner and Alluvion. The levels of nitrate/nitrite/nitrogen in Cluster 1 are between 0-1 mg/L. Cluster 2 is defined by the stations that have z-scores that are close to zero, indicating that the nitrate/nitrite/nitrogen levels are around average in relation to other stations; there are 20 stations in this cluster, and the cluster node is Stony Run. The levels of nitrate/nitrite/nitrogen in Cluster 2 are between 1-2 mg/L. Finally, Cluster 3 is defined as the stations which have above average nitrate/nitrite/nitrogen levels in relation to the other stations; there is only one station in this cluster, the cluster node, Lombard St. The levels of nitrate/nitrite/nitrogen in Cluster 3 are above 5 mg/L. 

The full analysis can be found [here](https://github.com/cshah13/baltimore-water-supply/blob/main/Cluster%20Analysis%20.xlsx). The graph below identifies the number of stations that correlate with each cluster.

![alttext](https://github.com/cshah13/baltimore-water-supply/blob/main/Cluster%20Graph.png)

## Data Answer 2
### How do the average observed levels of nitrate/nitrite/nitrogen compare between each of the clusters over time?

In order to explore trends in the relationship between the average levels of nitrate/nitrite/nitrogen among the 3 clusters, a time series analysis was conducted over the 24 years for which data was available for all three clusters (1997-2020). Each point on the line represents the average quantity of the pollutants observed across all stations in the associated cluster during the year in reference. For example, the first point on the cluster 2 average line in the graph below represents the average result in mg/L of nitrate/nitrite/nitrogen for all reporting stations included in cluster 2 for 1997. 

![Picture1](https://user-images.githubusercontent.com/78438582/112257789-c02bff00-8c3b-11eb-863a-416c1375b4de.png)

The graphs reveal a strikingly consistent result gap between clusters 1 and 2, with the average observed values for the stations in cluster 2 about 0.401 mg/L higher than the average observed values for the stations in cluster 1. The line displaying the average observed values for cluster 3 exhibits somewhat more volatility, which is to be expected given the fact that only one station is included in the cluster. Of particular interest is the spike in average result for cluster 3 during the mid-to-late 2000s, where the average level of nitrate/nitrite/nitrogen in cluster 3 was nearly twice that of cluster 2. This seems to suggest that a few anomolous measurements are driving the higher than average nitrate/nitrite/nitrogen level observed in cluster 3.

## Data Answer 3
### Insert question


## Business Answer

Based on the cluster analysis, a majority of water stations contain 1-2 mg/L of nitrate/nitrite/nitrogen (Cluster 2). Based on the data provided by the EPA in the background information, these levels are below the legal limit of 10 PPM (mg/L). However, the levels are above the national averages which are below 1 mg/L and are around the state averages of 1.5 mg/L. Cluster 1 has nitrate/nitrite/nitrogen between 0-1 mg/L which is below the legal, national, and state levels. Cluster 3 is below the legal level, but it is above the state and national averages. This information is useful to scientists who are regulating water quality and identifying toxic contaminents. Further analysis is needed to identify if the legal limit is actually the safe limit; the state and national averages are much lower than the legal limit, so safety measures should be analyzed beyond this project.



## Step by Step Instructions
### Data Collection
1. Downloaded original data from
2. Filtered the original data to include nitrate/nitrite/nitrogen levels from the first water collection at each station in 2020
### Cluster Analysis
1. Used Excel functions to calculate z scores for the nitrate/nitrite/nitrogen levels
2. Identified three sample cluster nodes, used VLOOKUP to identify the cluster node names, and calculated the distance squared for each value
3. Calculated the minimum for each distance squared value, used the MATCH function to identify clusters, and calculated the sum of the minimums
4. Used the Excel Solver function to minimize the sum of minimums, identifying three new cluster rods
5. Moved clusters into a visualization to identify the number of water stations in each cluster 


