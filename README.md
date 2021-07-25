## Module 14: New York City Bike Sharing Analysis using Tableau Public


![image](https://user-images.githubusercontent.com/82583576/126883517-e3d16349-be14-40a1-a173-b4ca89c2ba7b.png)




## Overview

The objective of this project is to create visualizations in Tableau Public to present information to investors with regards to a potential bike sharing project in Des Moines, Iowa.

The visualizations presented to the investors will include:

- Length of time bikes are checked out by each gender
- Number of bike trips by all users and each gender for each day of the week
- Number of bike trips for each type of user and gender for each day of the week

## Results of the Analysis

The data from the two datasets pertaining to the New York City bike sharing program for the month of August 2019 will be used for the visualizations.

However, prior to creating the worksheets in Tableau Public, the following needs to be done:

- Convert the trip duration provided as an integer in the dataset to  datetime datatype by using Pandas and Python;
- Within Tableau, convert the Gender from ineteger to a string to display "Male, Female or Unknown".

There are two datasets that were used in the analysis:

- citi_bike.csv: amongst other data, includes data with regards to riders gender, trip duration, usage relative to time of day.
- 201908-citibike-tripdata: amongst other data contains the August 2019 data with regards to number of rides, starting locations, ending locations.

The visualizations (worksheets, dashboards and story board) can be found in Tableau Public by clicking [here](https://public.tableau.com/app/profile/binoy.luckoo/viz/NYC_DesMoines_CitiBikes/NewYorkCityBikeRides?publish=yes).

Below is a summary of the visualizations.

**1. Demographics of the bike users**

As illustrated in the dashboard below, the total number of users were 2,344,224, 81% of which are subscribers to the service.
Also to be noted that 65% of total users are males.

![image](https://user-images.githubusercontent.com/82583576/126883629-8f3bcfd8-4c8a-4a5a-8ea4-fe42ee00059e.png)
##
##
**2. Trip Location Summary**

Most ride starts and ends are located in central Manhattan with peak hours being between 8:00 am to 10:00 am and 5:00 pm to 7:00 pm.
The top 10 start stations are also close to Grand Central Station.

![image](https://user-images.githubusercontent.com/82583576/126883636-f710d64a-9bda-4a1b-b35e-59c1e18d0d39.png)
##
##
**3. User Trips Information**

The majority of riders were born between 1980 and 2000 with maximum duration of trips being around 15 minutes irrespective of gender.
The highest number of rentals are during the peak hours for most of the weekdays except for Wednesday, where the afternoon, i.e. 5:00 pm to 7:00 pm, is not as busy as the other days of the workweek.
During the week-ends, Saturday is quite busy from 10:00 am till 6:00 pm.

![image](https://user-images.githubusercontent.com/82583576/126883657-944fc035-b777-4c73-a152-421c3ad79c3c.png)
##
##
**4. User Trips by Gender**

From the dashboard below, it is very evident that male subscribers make up the majority of the ridership. 

![image](https://user-images.githubusercontent.com/82583576/126883668-494ff42a-37d3-47c8-af22-da6413287780.png)
##
##
**Summary**
- Male subscribers to the bike sharing service are the majority of the ridership in New york City.
- The main duration of rides is less than 20 minutes with peak times being on weekdays between 8:00 am to 10:00 am and between 5:00 pm and 7:00 pm.
- Busiest bike stations are close to the train station.
- The common rider was born between 1980 and 2000. 
  . owever, the dataset may need some further investigation and clean up with regards to birth years. The data contains some riders with birth years from 1880 to early 1900's.     Not convinced that people of that age will be riding bikes in 2019.

- To keep the rideship happy, a maintenance program for the bikes must be in place. One way toschedule the bike maintenance is to consider their utilization.
The folliwng bubble chart illustrates the bikes that have the highest utilizations - the size of the bubbles are relative to the utilization level of each bike.
##
![image](https://user-images.githubusercontent.com/82583576/126883679-b9e14356-9507-421b-9ae6-5819aea801b6.png)
##
##

**Further Analysis & Recommendations**
For Des Moines, need to gather some data and create visualizations regarding:
- The gender ratio of the urban centres.
- Locations of train or subway stations.
- Marketing campaigns targetted at converting users to subscribers.
- Survey geared towards female ridership to find out if the bikes are attractive and safe for to the female riders.
- Marketing campaigns to encourage female ridership.
- Marketing campaigns geared towards increasing ridership during the week-ends - may be reduced rates or more bike stations closer to tourist attractions. 


