# baltimore-water-supply


## Background Information

Recent water tests conducted by the Environmental Working Group, a leading environmental non-profit, revealed [alarmingly high levels of contaminants in the Maryland water supply](https://baltimore.cbslocal.com/2019/12/04/maryland-water-systems-found-to-contain-worrying-levels-of-nitrate-arsenic-and-other-chemicals-nonprofit-says/), including Baltimore water utilities. Nitrates, nitrite, and nitrogen were found to exceed EWG guidelines and Baltimore utility levels slightly exceeded the state and national averages. Common sources of nitrates, nitrite, and nitrogen are agricultural and urban runoff, wastewater discharge, and septic tank leaks, which are all common in industrial and urban settings. Nitrates, nitrite, and nitrogen exposure can cause many types of cancer and oxygen deprivation in infants, therefore it is extremely important to regulate their abundance in water supplies. Current EPA guidelines allow up to 10ppm of nitrates, nitrite, and nitrogen, however given signfiicant associated health risks, the [EWG has proposed a new value of 0.14ppm](https://www.epa.gov/ground-water-and-drinking-water/national-primary-drinking-water-regulations) to accurately reflect the risk of nitrates, nitrite, and nitrogen water contamination.  Given this recent change in allowable limits for nitrates, nitrite, and nitrogen, it is particularly salient to examine Baltimore water stations to understand the extent of nitrates, nitrite, and nitrogen contamination in water sources and identify any trends that may have developed over time. 

 

## Business Question

_**How do nitrate/nitrite/nitrogen levels differ throughout the water supply in Baltimore, Maryland?**_

## Open Data
This analysis uses open data from the Baltimore City Open Data platform and the Maryland GIS Data Catalog. The [Surface Water Quality Data Since 1995](https://data.baltimorecity.gov/datasets/surface-water-quality-data-since-1995/geoservice) was the primary dataset used in the cluster analysis, time series analysis, and geospatial analysis. The dataset includes water quality test results for various parameters (water contaminants) for water stations throughout Baltimore and includes testing dates, geographic coordinates, and the laboratory that performed the test. The [Maryland Archived American Community Survey Census Tracts 2009 to 2013](https://data.imap.maryland.gov/datasets/maryland-archived-american-community-survey-census-tracts-2009-to-2013?geometry=-81.224%2C38.070%2C-73.313%2C39.568&selectedAttribute=POV_POP) dataset was the secondary dataset used in the geospatial analysis and provided census tract delineations and median household income by census tract within Baltimore. 


## Data Analysis Questions
Microsoft Office Excel and MapBox will be used to conduct a cluster analysis, time series analysis, and geospatial analysis to answer the following data questions:
1. How can Baltimore water stations be organized into clusters based on the presence of nitrate/nitrite/nitrogen levels?
2. How do the average observed levels of nitrate/nitrite/nitrogen compare between each of the clusters over time?
3. Where are water stations located throughout Baltimore?
4. How do nitrate/nitrite/nitrogen levels vary between water stations given median household income by census tract? 


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
### Where are water stations located throughout Baltimore?
### How do nitrate/nitrite/nitrogen levels vary between water stations given median household income by census tract? 


## Business Answer

The cluster analysis, time series analysis, and geospatial analysis compared different water stations throughout Baltimore. Based on the cluster analysis, a majority of water stations contain 1-2 mg/L of nitrate/nitrite/nitrogen (Cluster 2). Based on the data provided by the EPA in the background information, these levels are below the legal limit of 10 PPM (mg/L). However, the levels are above the national averages which are below 1 mg/L and are around the state averages of 1.5 mg/L. Cluster 1 has nitrate/nitrite/nitrogen between 0-1 mg/L which is below the legal, national, and state levels. Cluster 3 is below the legal level, but it is above the state and national averages. The geospatial analysis reveals that most water stations with nitrate/nitrite/nitrogen levels >1.99ppm are located in census tracts with high median household income ($60,000+) compared to most water stations with nitrate/nitrite/nitrogen levels <1.99ppm located in census tracts with lower median household income ($20,000-$40,000). 

This information is useful to scientists who are regulating water quality and identifying toxic contaminents. Further analysis is needed to identify if the legal limit of nitrate/nitrite/nitrogen is actually the safe limit; the state and national averages are much lower than the legal limit, so safety measures should be analyzed beyond this project. Scientists can take this information to test the water in Cluster 3 to identify any potential hazards due to the higher nitrate/nitrite/nitrogen levels in comparison to other water staions in Baltimore. The information can be used to prioritize examinations of water stations that may need more attention than others. This analysis can be conducted again with different chemicals to further analyze the components of the water. Additionally, further research to examine structural differences in water stations in high median household income census tracts compared to lower median household income census tracts may provide useful guidance for improving water system infrastructure and general knowledge regarding water safety for Baltimore residents. 




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
### Geospatial Analysis 
1. Filtered the filtered data from step 2 of Data Collection to separate stations with results >1.99ppm and <1.99ppm, and to include labelled longitude and latitiude coordinates
3. Converted file to CSV and uploaded file to MapBox 
4. Created one layer showing stations with values >1.99ppm and changed style color to black 
5. Created another layer showing stations with values<1.99ppm and changes style color to red 
6. Uploaded Maryland Archived American Community Survey Census Tracts 2009 to 2013 shapefile to Mapbox 
7. Used 'style across data range' to Selected medhhdata and create layer with only lines 
8. Repeated step 7 to create another layer but selected fill to create gradients 
9. Added stops with $20,000 ranges from $0-$140,000 and one range from $140,000-$250,000, and gave each stop a unique color in ROYGBV order 
10. Adjusted opacity and reordered layers so station points and lines were visible and exported visualization as a PNG
11. Created legend for symbols and income range colors using Canva 


