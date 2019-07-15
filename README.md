# Lyft Bay Wheels Data Exploration
## by Wakana Morlan


## Dataset

Bay Wheel is a bike-sharing service available in the San Francisco Bay area operated by Lyft. It was formerly known as "Ford GoBike", however, the company behind the service, Motivate was acquired by Lyft. After the acquisition, the system was subsequently renamed to Bay Wheels in June 2019. 

This document explores a dataset containing 94802 trip records of BayWheels in January 2018.  The original data is available to download from [here](https://www.lyft.com/bikes/bay-wheels/system-data).


## Summary of Findings

In the exploration, I found out that subscribers are purpose-driven riders. As most of their tips are short, mostly within 30minutes, and made around downtown, they use BayWeel for commuting. On the other hand, customers are casual riders. Since they enjoy riding, they tend to make longer duration and distance trip.

- When I created a histogram of trip duration with a whole dataset, the plot was scaled up quite a lot because of many outliers. So I created a new histogram to explore the frequency of the usage by hour. 
- From this histogram, I saw that most of the trips lasted less than 1 hour. So through the investigation, I decided to compare 2 types of trips; trips lasted less than 1 hour and trips lasted over 1 hour, I'm going to used pandas query function to create 2 sub-data frames that contain data of each type of trip.

- Majority of the rides are made by subscribers. This totally makes sense that subscribers have an unlimited ride for up to 45 minutes. I wish I could identify the individual users so that I can understand each user's frequency of the service use. Unfortunately, such information is not available in this dataset.

- Subscribers tend to have a shorter duration and slightly longer distance trip than customers for the trip lasted for less than 1 hour.
- Even though subscribers have an unlimited ride for 45 minutes, the majority of their trips are within 30 minutes. 
- Customers tend to have a longer duration and longer distance trip than subscriber for the trip lasted for over 1 hour, even though it cost customers more than what costed subscribers.
- Customers tend to ride the bike for a  longer period of time. 

- 2207 trips, which of 2.3% of the total trips are round trips (These are the trips started and ended at the same station.)
- Both subscribers and customers made round trips, however, the purpose of the round trip differed by user type.
- The stations used the most for roundtrips by customers  are The Embacadero at Sansome St station and Central Ave at Fell St station and both are located near sightseeing or bike riding spots. 


Outside of the main variables of interest, I investigated the most used start and end stations. The trend of the most used start and end station for subscribers and customers is similar. San Francisco Caltrain, San Francisco Ferry Building is the most used station for both start and end station. This makes sense because these locations are transit stations for commuters. Users use BayWheel to get to their office from their primary commute transportation (Caltrain or Ferry) and ride to their office and vise verse.


## Key Insights for Presentation

For the presentation, I focus on the usage of Bay Wheel by user type. First I will introduce the overall relationship between trip duration and distance by user type. Then I will break it down to trips lasted for less than 1 hour and trips lasted over 1 hour. 

Also, I am going to show the stations most used for roundtrips by user type to explain the difference of the service usage by user type.