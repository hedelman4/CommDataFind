# Bikeshare Data Exploration
## by Harry Edelman


## Dataset
I used the Ford GoBike dataset. The source file was provided in CSV format, and contained 183,412 rows with 16 colums of data. The start and end-times were in string format, so I converted them to datetime for easier manipulation. Additionally, the birth year data was a float type where integers would be sifficient. I also added member age and distance between station columns based on member birth year and station coordinate data found in the source file. Finally, I excluded some age, distance and duration outliers that either seemed erroneous or were severely skewing the data for my analysis.

## Summary of Findings
The main exploratory concept I wanted to focus on was to relate user types, genders, originating/terminating stations and age with distance and duration of rides. My initial expectation was that young male subscribers would ride the longest and farthest. Instead, young male subscribers turned out to represent the largest conglomerate of users, but didn't necessarily ride the farthest/longest.

In general, both duration and distance data distributions were right-skewed with extreme outliers. Log-normalizing the duration data showed a mode of ~500 seconds per ride. Eliminating outliers for distance displays that the majority or rides were 2 km or less.

The most frequent ages are in the late 20's through the mid 30's. Males represent nearly triple the users than females and other genders combined. Subscribers outnumber customers by nearly 8 times.

Notable bivariate correlation pairs include the following:
- start_station_id / end_station_id
- start_station_longitude / end_station_longitude
- start_station_latitude / end_station_latitude
- start_station_latitude / end_station_longitude
- start_station_longitude / end_station_latitude

There turned out not to be a deep correlation between distance and duration, which was surprising. This must mean that there are a number of rentals that are not strictly for commuting purposes.

Across the different age brackets, the medians, means and quartiles of duration and distance are not extraordinarily dissimilar. However, the age brackets from 21-60 all have disproportionate numbers of outliers.

Finally, it appears that female and other gender have less concentration compared with males when it comes to distance and duration of bike rentals.

## Key Insights for Presentation
- The majority of users are young male subscribers
- Zooming in on distance vs duration shows there is surprisingly little influence of one variable on the other
- The only meaningful correlations demonstrate the start and end stations are oftened paired up
- Across the different age brackets, the medians, means and quartiles of duration and distance are not extraordinarily dissimilar. However, the age brackets from 21-60 all have disproportionate numbers of outliers.
- Female and other gender have less concentration compared with males when it comes to distance and duration of bike rentals.