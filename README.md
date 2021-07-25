## Module 14: New York City Bike Sharing Analysis using Tableau Public


![image](https://user-images.githubusercontent.com/82583576/126883517-e3d16349-be14-40a1-a173-b4ca89c2ba7b.png)


[Please click here to get to the Tableau Dashboard](https://public.tableau.com/app/profile/binoy.luckoo/viz/NYC_DesMoines_CitiBikes/NewYorkCityBikeRides?publish=yes)

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

![image](https://user-images.githubusercontent.com/82583576/126883668-494ff42a-37d3-47c8-af22-da6413287780.png)

##
##

![image](https://user-images.githubusercontent.com/82583576/126883679-b9e14356-9507-421b-9ae6-5819aea801b6.png)


##



Tableau workbook description
Overview dashboard:


Conclusions

The further the station is from the city center the longer the average trip duration is.

More than 95% of all users are annual subscribers.

The common rider is a man around 30 years old. Women rides are only 25% of total (in average).

The main usage of the bikes for all ages are the trips shorter than 10 minutes.

On weekend bikes are mostly used from 10 am to 6 pm, while on weekdays the rush hours are 8 am and 5-6pm.

From May to October there is a peak in a rides number. From December to March the rides are significantly decreasing (more than 50%).

The average trip on weekend is longer than on weekday.

ableau CitiBike: January 2019 - August 2019
Goal
Analyze CitiBike data between January and August 2019 for trends and visualize them using Tableau Public. View the Tableau Public workbook here (it may take a moment to load).




Analysis
My analysis focused on user types (customer or subscriber) and gender (male, female, unknown). Though annual subscribers make up over 90% of total riders, customers (1-day and 3-day rentals) have a higher growth rate (1718%) than subscribers (113%). This could signal a growing interest in short-term rentals for users who want to experience the CitiBike product without being tied down for a whole year, or perhaps even a growing tourist market.



Despite efforts to filter out fraudulent records from the data set, I still found possible evidence of user fraud. Looking at age and gender, males make up the majority of users, and most users are between the ages of 30-33. However, you’ll see a large spike in the amount of users aged 50, with over 82% of those users identifying as “unknown”. This deviates greatly from the rest of the user demographic trends. Filtering out those users, females show a higher growth rate than males.



Recommendations
Continue marketing campaigns to encourage short-term rentals.
Continue marketing campaigns to encourage female ridership.
Check all bikes with trip durations under 90 seconds and the same starting and ending stations for any needed repairs.
There is steady ridership growth across user types and gender, suggesting a healthy demand for CitiBikes. Current year-to-date growth rates also suggest a growing market for short-term rentals and female users. Therefore, recommendations would be to focus marketing campaigns towards those users.

Assuming that users use a day pass or annual subscription to its max capacity (48 rides in 24 hours for day pass users, 11,680 rides per year for subscribers), each ride costs $0.25 under a day pass, and $0.01 under an annual subscription. Therefore, short-term users are more profitable per ride, especially when also considering that “time overages” are also charged at a higher rate ($4 per 15 minutes) than subscribers ($2.50 per 15 minutes).

Females also make up 51% of the Jersey City population source. Yet, only 40% of Jersey City females use CitiBike, leaving over 80,000 potential local users.

Further Analysis
For further analysis, I would look at the bike and station ids of all the rows that were dropped from this data set for any trends. Are the same bikes being stolen? Or are bikes being stolen from the same station? Do either these bikes or stations need to be serviced to prevent theft? I would also look into why there are so many “unknown” 50-year old users. Are these just default parameters of the app (gender set to unknown and birth year set to 1969)? Or are there and commonalities in the records of these users?
