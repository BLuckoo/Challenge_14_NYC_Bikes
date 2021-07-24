## Module 14: New York City Bike Sharing Analysis using Tableau Public

<p align="center">
![image](https://user-images.githubusercontent.com/82583576/126883061-ef0ddc9e-6b89-4981-b1dd-1e7f9444666b.png)
</p>


[Please click here to get to the Tableau Dashboard](https://public.tableau.com/app/profile/binoy.luckoo/viz/NYC_DesMoines_CitiBikes/NewYorkCityBikeRides?publish=yes)

## Overview

The objective of this project is to create visualizations in Tableau Public to present information to investors with regards to a potential bike sharing project in Des Moines, Iowa.

The data from the two datasets pertaining to the New York City bike sharing program will be used for the visualizations.

However, prior to creating the worksheets in Tableau Public, the following needs to be done:

- Convert the trip duration provided as an integer in the dataset to  datetime datatype by using Pandas and Python;
- Within Tsbleau, convert the Gender from ineteger to a string to display "Male, Female or Unknown".


There are two datasets that were used in the analysis

Ride Data from New Jersey (September 21 2015 - June 30 2018), a light dataset for the tests.
Ride Data from New York (July 20 2017 - June 30 2018), a Public version of Tableau has a limit of 15 millions rows for a single dataset, therefore this dataset has a smaller time span.

Tableau workbook description
Overview dashboard:
Time period can be choosen with the range of dates.

Any station can be chosen for a deeper analysis.

All data below is actual for the choosen period of time and station.

Map shows all the stations with outgoing trips.

Overall information about total number of trips, average duration and number of unique bikes.

% of subscribers and customers.

9 bikes with the longest travel time.

Trips length divided in 5 categories.

Month to month growth or decrease in a number of rides.

Most and less popular time of the day.

Age and gender distribution.

Top and bottom 10 station for outgoing trips.

Single bike dashboard:
Gives an information about a particular bike.

Map shows all the station where the bike has ever been and the number of it's rides from that stations.

Overall information about total number of rides, duration and average trip length.

Age distribution by age groups.

Customer type.

Trips by duration.

Other sheets:
Map with outgoing trips.

Trips by length depending on the day and time.

Station popularity by month.

Top/Bottom 10 end stations.

Rides by age by station.

Bikes rotation by station.

Duration by age.

Steps
1. Data loading and cleaning


2. Visualization in Tableau

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

Data Cleaning
Before doing any visualizations, I first used Python and the Pandas library to clean the data. In a Jupyter Notebook, I concatenated monthly data files into one, and then dropped rows where the trip duration was under 90 seconds and the starting and ending stations were the same. This was done to weed out any instances of a faulty bike.

Then, trip duration was converted from seconds to minutes, which is personally easier to understand at first glance, and all trips over 24 hours (1440 minutes) dropped. Under CitiBike’s current pricing model, bikes can be used an unlimited amount of times (under the day passes and subscriptions) but in 30- or 45-minute intervals. Trips longer than that, are charged an extra $2.50 or $4.00 every 15 minutes. Therefore, all bikes that were not docked for over 24-hours were most likely stolen, and not legitimate rides. This was still a conservative assumption, as bike rides up to 24 hours would still cost the user between $232.50 and $376.

Next, I converted the gender column (which was originally numerically coded) into strings using a list comprehension, and added an extra column for ride id to uniquely identify each ride. Then, I calculated the distance for each trip, and the ages of each rider. Finally, I dropped all rows where riders were above the age of 90, assuming these were fake ages (some riders even gave ages over 130), and divided the riders into age bins. Like trip duration, I again made a conservative estimate, as it is unlikely that users in their 80s would be riding bikes in a large city.

In a separate notebook, I reshaped the cleaned data. Originally, each row represented one ride, with the starting and ending information in one row. Because I wanted to visualization each bike path, I need to plot two sets of coordinates at the same time. So, I divided the data so that the starting information and ending information would be in separate rows. Though visualizations were made with this data, it was not included in the final analysis.

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
