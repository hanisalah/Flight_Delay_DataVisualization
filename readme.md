# Airline On-Time Performance
## by Hani Salah


## Dataset

1. This data consists of flight arrival and departure details for all commercial flights within the USA, from October 1987 to April 2008. This is a large dataset: there are **nearly 120 million records** in total, and takes up 1.6 gigabytes of space compressed and 12 gigabytes when uncompressed.  
2. Should all data be examined, tools other than **pandas** will be required (e.g. **dask**) to be able to wrangle *12GB* worth of data. For the sake of simplicity, **years 1990, 1995, 2000, 2005 will be the only ones considered with 23.4 Million records.**

## Summary of Findings

1. There are 7 Carriers **(DL, WN, US, AA, UA, NW, CO)** that operated more than ***1.5 million flights each***. We can call those the big players.  
2. It is seen that there are 11 airports **(ATL, ORD, DFW, LAX, PHX. DEN, IAH, DTW, STL, MSP, SFQ)** that have more than ***1 million flights each***.  
3. There is a ***strong positive relation between Departure and Arrival delays***. We can almost see the regression line drawn by overplotting scatter points.  
4. We observed interesting relation between the carrier operating volume and their departure delays. Particularly for DL, WN, UA; where **DL** tend to be the jiant going down the slippery road, **WN** earn thumbs up for being a big player and having minimum delays, **UA** on the other hand may need consultation to strengthen its volume and minimize its delays.  
5. With this dataset, we can only attibute an airport to a departure delay. ***Arrival delays cannot be explained*** by the selected dataset due to the random selection of years as well as its cleaning. This is further statistically evident from the strong positive relation ship between Departure and Arrival delays.
6. The top operating airports **(ATL, ORD, DFW)** have ***spectacular operations*** to keep their departure delays less than 15 minutes.
7. When we expand the chronological view of departure delays, we further strengthened the ability to conclude that chronologically there was tendancy to have ***increased number of flights with negative delays (depart earlier than scheduled)***. This might go against the flow of belief that increasing security checks at airports tend to result in more delays.
8. **CKB** airport ranked first in the ***top departure delays***. Interestingly enough, the multivariate heatmap show that this top average delay occured by single air line **(OH)**.

## Key Insights for Presentation

While exploring, we made the plots substantially complete and asthetic in a way that it does not require more polishing to fit for explanatory purposes except for two minor areas:
1. Markdown cells: Text has been reduced from the original notebook to better suit a presentation environment.
2. The last heatmap has been split in separate subslides to fit the presentation size. The original heatmap has 310 rows and as such it was sliced in 52-row dataframes, and each dataframe was separately plotted and assigned as a subslide.

## [Creating slide decks presentation](Slide_Decks Command.md)
