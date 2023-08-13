# Uber_data_analysis
The Uber dataset contains 31 million rows of data from September 2014 to August
2015, including information about trip origin, destination, pickup and drop-off
dates/times, trip distance and duration. The data allows for estimating Uber's revenue
per trip in NYC, but the pickup and drop-off locations are anonymized and grouped as
taxi zones for privacy. The dataset is 1.4 GB in size and although it can be worked on a
laptop with 16 GB RAM, some transformations may require efficient handling.
Here, I did an EDA on the uber dataset, which consisted of data from rides booked in
NYC over the course of one year, from September 2014 to August 2015, and eventually
computed the income of Uber in one year as well as the revenue trend during the year.
This dataset was limited to around 31 million rows and columns of origin, destination,
pickup date and time, travel distance and duration.
Used Pandas data frame to check for the presence of null values in the dataset and
discovered that the destination column had 1.3 million missing data but that the
corresponding data in other columns such as origin, trip duration, trip distance, pickup
date and time data were present for these missing data, implying that we cannot
remove these missing rows from our dataset because they have a significant impact on
Uber's total revenue. Because the destination column was categorical, I utilized the
mode imputation approach to address missing values. There were some missing values
in the trip length and trip distance columns as well, so I used the mean imputation
approach to address these.
Also, feature engineering was used to construct several columns that can help with
analysis and expand the area of study. As a result, I made distinct columns for the year,
month, and day of the trip. These columns were then utilized to determine the data's
monthly trend. Also included a column for trip revenue, which was used to determine
total revenue and average revenue. The revenue consisted of various components like:
Base fare = 2.55
Per minute = 0.35
Per mile = 1.75
Minimum fare = 8
