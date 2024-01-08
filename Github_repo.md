# Table of Contents

* [Introduction](#1)
   
* [Ask](#2)
  
* [Prepare](#3)
 
* [Process](#4)
  
    * [Cleaning](#5)
    
    
* [Analyze/Queries](#6)

    * [Review](#7)
    
    
* [Share/Visualizations](#8)

    
<a id="1"></a> <br>
# Introduction

As part of the Google Data Analytics Certification capstone project, I will perform data analysis for a fictional bike-share company, Cyclistic, in order to help them attract more members through digital media marketing. Along the way, I will perform numerous real-world tasks of a junior data analyst by following the steps of the data analysis process: *Ask, Prepare, Process, Analyze, Share, and Act*. Using the [Case Study Roadmap](https://d3c33hcgiwev3.cloudfront.net/aacF81H_TsWnBfNR_x7FIg_36299b28fa0c4a5aba836111daad12f1_DAC8-Case-Study-1.pdf?Expires=1680393600&Signature=eI5fpYqVfi7Dv79AWmJCruuCnDYi7Ky24zn9kJE~CC-kD29tNaM9p5lqKnnoyZY6El3cIa8QFL1Az9FDmxgZZJvJKNzt0jPL7dKwUNl5rB9lM0DXqZe31~LQH1ysLT3TKuKggj7bahaGtJtY4AEvubGy9yHmHFh7nQ~5DV5Ez~0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A 'Case Study Roadmap') tables provided on Coursera, I will use guiding questions and key tasks to stay on the right path.


### Scenario

"You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations."


### Characters and teams

● **Cyclistic**: "A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day."

● **Lily Moreno**: "The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels."

● **Cyclistic marketing analytics team**: "A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy learning about Cyclistic’s mission and business goals — as well as how you, as a junior data analyst, can help Cyclistic achieve them."

● **Cyclistic executive team**: "The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program."

<a id="2"></a> <br>
# Ask


#### Business Task (Marketing Questions for the Team):

 **How do annual members and casual riders use Cyclistic bikes differently?** (our assignment from Moreno) 

With our assignment, we will create a report with the following deliverables:
1. A clear statement of the business task
2. A description of all data sources used
3. Documentation of any cleaning or manipulation of data
4. A summary of your analysis
5. Supporting visualizations and key findings
6. Top three recommendations based on your analysis


### Guiding Questions
* **What is the problem you are trying to solve?**

The problem the team is trying to solve is how to convert more casual riders into annual members. My specific task is to determine how casual riders and members use Cyclistic's service differently.

* **How can your insights drive business decisions?**
  
By understanding the differences between these two types of riders, we can gain insight into their similarities and differences and create new marketing strategies to convert more casual riders to annual members.

#### Key Tasks

* **Identify the business task**
* **Consider key stakeholders**

#### Deliverable

* **A clear statement of the business task**

Find the differences between casual riders and annual members and create recommendations on how digital media marketing can be used to increase membership.

<a id="3"></a> <br>
# Prepare

#### Guiding Questions

**1. Where is your data located?**

The data is housed in an AWS bucket with links directly from the Coursera course.The data can be accessed through the following link: https://divvy-tripdata.s3.amazonaws.com/index.html.

**2. How is the data organized?**

The data is organized chronologically, grouped first by month, then year, then by quarters.

**3. Are there issues with bias or credibility in this data? Does your data ROCCC?**

There is no reason to suspect bias or credibility issues with this data as it is reliable, original, comprehensive, current and cited.

**4. How are you addressing licensing, privacy, security, and accessibility?**

The company has licensing over their own data, but this data has been made public and has no identifying information about any of the riders.

**5. How did you verify the data’s integrity?**

All of the files are consistently organized and labeled, with some missing data in specific columns

**6. How does it help you answer your question?**

It provides data on bike type, rider type, locations, durations, and times that should help to determine some differences between riders.

**7. Are there any problems with the data?**

A few of the monthly datasets I downloaded are missing some station information, which could help to determine distances traveled.

#### Key Tasks

1. Download data and store it appropriately.
2. Identify how it’s organized.
3. Sort and filter the data.
4. Determine the credibility of the data.

#### Deliverable

* **A description of all data sources used**

I have used 12 csv files of rider data dating from Jan. 2023-Dec. 2023, all obtained from the bucket site.The data can be accessed through the following link: https://divvy-tripdata.s3.amazonaws.com/index.html.

<a id="4"></a> <br>
# Process
#### Guiding Questions

**1. What tools are you choosing and why?**

For this case study, I will be using **SQL(BigQuery)** for much of the cleaning, organization, and analysis while I use **Tableau** for the visualization. This will enable me reinforce what I have learned during my course and showcase my skills to job recruiters for employment.

**2. Have you ensured your data’s integrity?**

Data is consistent, with queries to filter and calculate helpful information from the data.

**3. What steps have you taken to ensure that your data is clean?**

After combining the data in BigQuery, I have run queries to check for missing/duplicate data as well as finding and removing outliers.

**4. How can you verify that your data is clean and ready to analyze?**

The queries that have been run serve to remove duplicate/missing/irrelevant/outlier rows/columns and ensure that all columns are of the correct type. 

**5. Have you documented your cleaning process so you can review and share those results?**

This notebook serves as the documentation for all processes of the case study.



#### Key Tasks

**[1]Check the data for errors.**

**[2] Choose your tools.**

**[3] Transform the data so you can work with it effectively.**

**[4] Document the cleaning process.**


#### Deliverable

**Documentation of any cleaning or manipulation of data**

Shown below

#### **Note**
_Because some of the months from the 12 .csv files were >100MB,  However, I found a workaround by creating a Google Cloud Storage trial account (good for 90 days) that lets me upload much larger files and transfer into BigQuery without size restriction issues._

<a id="17"></a> <br>

<a id="5"></a> <br>
## Queries

### Combining All Data


>SELECT *</br>
&emsp;FROM (</br>
    &emsp;SELECT *</br>
        &emsp;FROM `capstone.tripdata_202301`</br>
    &emsp;UNION ALL</br>
    &emsp;SELECT *  </br>
        &emsp;FROM `capstone.tripdata_202302`  </br>
    &emsp;UNION ALL  </br>
    &emsp;SELECT *    </br>
        &emsp;FROM `capstone.tripdata_202303` </br>
    &emsp;UNION ALL  </br>
    &emsp;SELECT *    </br>
  &emsp;FROM `capstone.tripdata_202304`  </br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202305`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202306`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202307`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202308`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202309`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202310`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202311`</br>
  &emsp;UNION ALL</br>
    &emsp;SELECT *</br>
  &emsp;FROM `capstone.tripdata_202212`</br>
) AS combined_data</br>


__5,677,610 results
saved as new table `combined_data` in BigQuery__

#### Prior to the procesing the data,I created a destination for the new combine_data table so I can query it. I create columns for _trip_duration_ and _day_of_week_ the trips started at in order to perform some analyses using these columns.

## Creating columns for trip_duration and day_of_week

>SELECT *,</br>
  &emsp;TIMESTAMP_DIFF(ended_at, started_at, second) AS trip_duration,</br>
  &emsp;EXTRACT(DAYOFWEEK FROM started_at) AS day_of_week</br>
FROM `capstone.combine_data`</br>

</br>
</br>

#### Next, I check for rows with trips that need to be removed in order to filter the combine_data table.

## Checking for duplicates

>SELECT ride_id,</br> 
&emsp;COUNT(*)</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY ride_id</br>
HAVING </br>
&emsp;COUNT(*) >1</br>

__0 results. meaning, there are no duplicate rides. This is good__

## Checking for rides with 0 duration

>SELECT *</br>
FROM `capstone.tripdata_combined_filtered`</br>
WHERE trip_duration = 0</br>

__966 rows with rides that have 0 duration will be removed__

## Checking for rides with negative duration

>SELECT *</br>
FROM `capstone.tripdata_combined_filtered`</br>
WHERE trip_duration < 0</br>

__262 rows with rides that are negative duration will be removed__

## Checking for rides lasting <1 minute 

>SELECT *</br>
FROM `capstone.tripdata_combined_filtered`</br>
WHERE trip_duration/60 < 1</br>

__1,228 rows with rides that are < 1 minute will be removed.__</br>
*I chose 1 minute arbitrarily as a way to gather trips that are real, not negative, and not excessively short for any reason.*

## Checking for rides lasting >12 hours

>SELECT *</br> 
FROM `capstone.tripdata_combined_filtered`</br> 
WHERE trip_duration/60 > 720</br> 

__42,216 rows with rides that are > 12 hours (720 minutes) and will be removed__</br>
*12 hours was also chosen arbitrarily as a way to limit the number of excessively long rides and durations that are possibly the result of mistakes.*

## Tallying all rows to be removed

>SELECT *</br> 
FROM `capstone.tripdata_combined.filtered`</br>
WHERE trip_duration/60 > 720</br>
OR trip_duration/60 < 1</br>
OR trip_duration < 0</br>
OR trip_duration = 0</br>

__158,809 rows to be removed from the table__

### How many of these entries are from members or casual riders? .

>SELECT member_casual,</br>
  &emsp;COUNT(trip_duration) AS number_entries</br>
FROM `capstone.tripdata_combined_filtered`</br>
WHERE trip_duration/60 > 720</br>
OR trip_duration/60 < 1</br>
OR trip_duration < 0</br>
OR trip_duration = 0</br>
GROUP BY</br>
  &emsp;member_casual</br>


|      | number_entries |
|------|----------------|
|member| 97921 |
|casual| 60888|

__The number of outliers from members outnumbers casual riders, signaling that experience with the service does not necessarily reduce outliers.__

### Next I will remove all rows with zero duration, negative duration, very short trips (<1 minute), and very long trips (>12 hours) to have a table with data ready to analyze for typical users.

>DELETE FROM `capstone.tripdata_combined_filtered`</br>
WHERE trip_duration/60 > 720</br>
OR trip_duration/60 < 1</br>
OR trip_duration < 0</br>
OR trip_duration = 0</br>

__158,809 rows removed, 5,518,801 rows remain__

## Next,removal of outlier data.
## Approximating quantiles in seconds, and standard deviation (filtered)

>SELECT</br>
   APPROX_QUANTILES(trip_duration, 4) AS q_values,</br>
   STDDEV(trip_duration) AS stddev_trip</br>
FROM `capstone.tripdata_combined_filtered`</br>

60 - __MIN trip duration__ (1 minute)</br>
340 - __1st Quartile (25th percentile)__ (5.66 minutes)</br>
585 - __2nd Quartile (50th percentile)__ (9.75 minutes)</br>
1030 - __3rd Quartile (75th percentile)__ (17.16 minutes)</br>
43166 - __MAX trip duration__ (719.43 minutes)</br>
1293.5036185795 - __Standard Deviation__ (21.55 minutes)</br>

## Using IQR to find data at upper and lower Outliers Gates.

__IQR:__ 1030 - 340 = 690 (11.50 minutes)</br>
__Lower Outlier Gate:__ 340 - (1.5 * 690) = 340 - 1035 = -695(-11.58 minutes)</br>
__Upper Outlier Gate:__ 1030 + (1.5 * 690) = 1030 + 1035 = 2070 (34.5 minutes)</br>

*Using the filtered data, I will look for values in the dataset that are below the lower gate (11.58 minutes) or above the upper gate (34.5 minutes). All values fall between these two gates. Boxplots typically use this method to identify outliers and display asterisks when they exist to decide which values should not be included in the analysis.*

__NULL values in the filtered,cleaned and combined dataset for station names and id's are not vital for how riders use the service and will be left out of my analysis involving location since this will not affect my findings.__

<a id="6"></a> <br>
# Analyze

This phase is where we will start to run some analyses to gather information about the riders and how they use the bikes. We will perform some basic queries to gather information on ride lengths, days of the week, rider types, months, time of day, and others to better understand how member and casual riders differ in how they use the service. 

>Note: All analysis and visualization will be performed with `filtered` data, removing all data with rides <60 seconds and >12 hours.

>Some tables are modified for ease of use

## Longest Trip Duration

>SELECT </br>
&emsp;MAX(trip_duration)/3600 AS trip_hours</br>
FROM `capstone.tripdata_combined_filtered`</br>

__11.99 hours is the max trip duration after filtering out rides >12 hours__

## Shortest Trip Duration
>SELECT</br>
&emsp;MIN(trip_duration)</br>
FROM `capstone.tripdata_combined_filtered`</br>

__60 seconds is the min trip duration after filtering out all rides <1 minute__

## Average Trip Duration

>SELECT </br>
&emsp;(AVG(trip_duration)/60) AS trip_minutes</br>
FROM `capstone.tripdata_combined_filtered`</br>

__15.03 minutes average trip duration within trips >1 minute and <12 hours__

## Average trip duration by rider type

>SELECT</br>
&emsp;AVG(trip_duration)/60 AS trip_minutes, </br>
  &emsp;member_casual</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY member_casual</br>

__20.1 minute avg trip duration for casual riders__</br>
__12.12 minute avg trip duration for members__

## Average trip duration by day of week

>SELECT</br>
  &emsp;AVG(trip_duration/60) AS trip_minutes,</br> 
  &emsp;day_of_week</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY day_of_week</br>
ORDER by day_of_week</br>

| day_of_week | trip_minutes |
|-----------------|-------------------|
| Sunday    | 18.020321523090015|
| Monday    | 14.244841195179893 |
| Tuesday   | 13.59155118023631|
| Wednesday | 13.252256304114082|
| Thursday  | 13.522030862342595|
| Friday    |14.84729199289468|
| Saturday  |17.890757343529412|


__weekends has the most riding days of the week, with Sunday barely edging out Saturday__

## Rider type average trip duration by day of the week: 

>SELECT</br>
   &emsp;AVG(trip_duration/60) AS trip_minutes, </br>
    &emsp;day_of_week,</br>
    &emsp;member_casual</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY day_of_week, member_casual</br>
ORDER by day_of_week</br>

|  | Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday |
|--|--------|--------|---------|-----------|----------|--------|----------|
| casual | 23.407406777161377|19.830126031187522 | 18.021686570256271| 17.076892979321617| 17.438406856879496 | 19.505854674397579| 22.879802416359841|
| member | 13.57357749219792| 11.586862632108591 | 11.696188011766344 | 11.619527580936508 | 11.719709193573751 | 12.088935772138226 | 13.528481650401115 |



__Here we can see that both members and casual riders tend to ride longer on the weekends, but members tend to ride longer on Saturdays while casual riders ride longer on Sundays__

## Bike Type Preference

>SELECT rideable_type,</br>
  &emsp;member_casual,</br>
  &emsp;COUNT(rideable_type)</br>
FROM `capstone.tripdata_combined_filtered` </br>
GROUP BY rideable_type, member_casual</br>
ORDER BY rideable_type</br>

| member_casual | classic_bike | docked_bike | electric_bike |
|---------------|--------------|-------------|---------------|
| member | 1765396 | | 1761892 |
| casual | 851683 | 77183| 1062647 |


__Interestingly, there are zero uses of docked bikes for members__

## Number of rides by day of the week

>SELECT</br>
  &emsp;COUNT(ride_id),</br>
  &emsp;day_of_week,</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY day_of_week</br>
ORDER by day_of_week</br>

| Weekday | Trips |
|---------|-------|
| Sundays | 714775|
| Mondays | 706895 | 
| Tuesdays | 800094 | 
| Wednesdays | 804435 |
| Thursdays | 835279|
| Fridays | 807845|
| Saturdays | 849478|


__Saturdays are the most common day to ride followed, interestingly, by Thursdays__

## Number of rides by month

>WITH</br>
  &emsp;month AS (</br>
    &emsp;&emsp;SELECT</br>
      &emsp;&emsp;&emsp;ride_id,</br>
      &emsp;&emsp;&emsp;started_at,</br>
      &emsp;&emsp;&emsp;EXTRACT (month FROM started_at) AS ride_month</br>
    &emsp;&emsp;FROM `capstone.tripdata_combined_filtered`</br>
  &emsp;)</br>
SELECT</br>
  &emsp;ride_month,</br>
  &emsp;COUNT(*) AS month_count</br>
FROM </br>
  &emsp;month AS month_ct</br>
INNER JOIN</br>
  &emsp;`capstone.tripdata_combined_filtered` AS trips</br>
ON </br>
  &emsp;month_ct.ride_id = trips.ride_id</br>
GROUP BY</br>
  &emsp;ride_month</br>
ORDER BY</br>
  &emsp;ride_month</br>

| Month | Trips |
|-------|---------|
| January | 183929 | 
| February | 184253 | 
| March | 249352 | 
| April | 411006| 
| May | 586010 | 
| June | 699663 | 
| July | 745982 | 
| August | 751675 | 
| September | 650915 | 
| October | 524559 | 
| November | 354598 | 
| December | 176859 |

__the busiest months for rides are in summer with August seeing the most trips.__

## Aggregated trip duration for the filtered data (Limited to 10 rows Screenshot) ##

![image.png](attachment:e677ba58-ff24-4b21-9480-a07a0beb6114.png)

__Link to complete aggregate data here:__ [Aggregate Data](https://docs.google.com/spreadsheets/d/1RE9RyAjw5V0MrjwsDWJFnwdnT-4zJIxVWmDYs28QMVE/edit?usp=drive_link)

![image.png](attachment:9edc18d7-9a61-4fd5-a3cb-fa3020f82f28.png)

## Top 10 Most Common Starting Stations

>SELECT start_station_name,</br>
  &emsp;COUNT(start_station_name) AS ride_count</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY</br>
  &emsp;start_station_name</br>
ORDER BY</br>
  &emsp;ride_count DESC</br>
LIMIT 10</br>

| start_station_name | ride_count |
|---------|-------|
| Streeter Dr & Grand Ave | 61392 |
| DuSable Lake Shore Dr & Monroe St | 39020 |
| Michigan Ave & Oak St | 36266 |
| DuSable Lake Shore Dr & North  | 34942 |
| Clark St & Elm St | 34782 |
| Kingsbury St & Kinzie St| 33776 |
| Wells St & Concord Ln | 32696 |
| Clinton St & Washington Blvd| 31414 |
| Wells St & Elm St | 29545 |
| Theater on the Lake | 29240 |

## Top 10 Most Common Ending Stations

>SELECT end_station_name,</br>
  &emsp;COUNT(end_station_name) AS ride_count</br>
FROM `capstone.tripdata_combined_filtered`</br>
GROUP BY</br>
  &emsp;end_station_name</br>
ORDER BY</br>
  &emsp;ride_count DESC</br>
LIMIT 10</br>

| end_station_name | ride_count |
|------------------|------------|
| Streeter Dr & Grand Ave | 29240 |
| DuSable Lake Shore Dr & North Blvd | 38574 |
| Michigan Ave & Oak St | 37077|
| DuSable Lake Shore Dr & Monroe St | 36989 |
| Clark St & Elm St | 34027 |
| Wells St & Concord Ln | 33417 |
| Kingsbury St & Kinzie St | 33274 |
| Clinton St & Washington Blvd | 30235|
| Millennium Park | 32414 |
| Theater on the Lake | 29951 |

## Trips by Hour of the Day
>WITH</br>
  &emsp;hour AS (</br>
    &emsp;&emsp;SELECT</br>
      &emsp;&emsp;&emsp;ride_id,</br>
      &emsp;&emsp;&emsp;started_at,</br>
      &emsp;&emsp;&emsp;EXTRACT (hour FROM started_at) AS ride_hour</br>
    &emsp;&emsp;FROM `capstone.tripdata_combined_filtered`</br>
  &emsp;)</br>
SELECT</br>
  &emsp;ride_hour,</br>
  &emsp;member_casual,</br>
  &emsp;COUNT(*) AS trip_ct</br>
FROM </br>
 &emsp; hour AS hour_ct</br>
INNER JOIN</br>
  &emsp;`capstone.tripdata_combined_filtered` AS trips</br>
ON </br>
  &emsp;hour_ct.ride_id = trips.ride_id</br>
GROUP BY</br>
  &emsp;ride_hour, member_casual</br>
ORDER BY</br>
  &emsp;ride_hour</br>

| ride_hour | member | casual |
|-----------|--------|--------|
| 12:00am | 34089 | 35212 |
| 1:00am | 20294 | 22864 |
| 2:00am | 11824 | 13802 |
| 3:00am | 7672 | 7643|
| 4:00am | 8467 | 5785 |
| 5:00am | 32913 | 11063 |
| 6:00am | 101765 | 29401 |
| 7:00am | 188643 | 51632 |
| 8:00am | 236244| 68855 |
| 9:00am | 158645 | 67779 |
| 10:00am | 142776 | 83777 |
| 11:00am | 169747 | 107040 |
| 12:00pm | 192249 | 126631 |
| 1:00pm | 190507| 132071 |
| 2:00pm | 193339 | 137787 |
| 3:00pm | 236891 | 154100 |
| 4:00pm |318966 | 176690 |
| 5:00pm | 348671 | 193090 |
| 6:00pm | 374684 | 166471|
| 7:00pm | 297384| 148775 |
| 8:00pm | 210767 | 123159 |
| 9:00pm | 146526 | 88886 |
| 10:00pm | 84916 |65966 |
| 11:00pm | 54221 | 47333|

<a id="7"></a> <br>
#### Guiding Questions

* **How should you organize your data to perform analysis on it?**

    All data was combined into two separate CSV files for analysis and visualization. One CSV for unfiltered data with no changes and the other CSV is beng filtered in the following process:
1. Checked Rides with zero duration : 966 rides have 0 duration were removed
2.  Checked Rides with negative duration: 262 rides with negative duration. This must be unreal rides and were removed.
3.	Checked Rides lasting less than one minute: 1228 rides were discovered and can be real covering a very short distance.
4.	Checked for rides lasting more-than twelve hours (720 minutes): 42,216 rides were removed. This is an excessively long rides that could be a mistake
5.	Rows removed: Total of 158,809 rows were removed while 5,518,801 remain. rows removed are:
* _trip duration/60 < 1 minutes_
* _trip duration/60 > 720 minutes_
* _trip duration < 0_
* _trip duration = 0_

    
* **Has your data been properly formatted?**
    
    All column datatypes are in correctly formatted.
    **Outliers** from the rows removed above, for members is greater than that for casual riders. Member riders with long experience with the services do not equate reduction in outliers from my observation
    
* **What surprises did you discover in the data?**

    There were a few surprises in the data that I found when analyzing:
    - In all **5,677,610m** unfiltered rides, _every_ ride that lasted >26 hours was from a casual rider and each month saw at least one trip from a casual rider lasting >7 days with 28 days being the longest 
    - 262 rides with negative duration (My hypothesis suggest the started_at and ended_at columns were switched for these rides somehow or these were possibly refunded rides but since I wasnt sure, these rides were removed for the filtered data).
    - In the unfiltered data, casual riders tended to take trips that were >2x as long as members on every day of the week (this is less extreme in the filtered data, but still consistently longer for casual riders than members)
    - Thursdays are the second most common day to ride, behind Saturdays as most common.
    - Streeter Dr & Grand Ave is the most frequent starting and ending station (DuSable Lake Shore Dr & North Blvd, DuSable Lake Shore Dr & Monroe St, Michigan Ave & Oak St and Millennium Park also highly popular starting and ending stations).
    - Casual riders outnumber members between the late night hours of 12:00am and 2:00am, while members outnumber casual riders for all other hours of the day.
    - There are zero rides from members for docked bikes 
    
    
* **What trends or relationships did you find in the data?**

    - Casual riders tend to use the bikes longer than members.
    - Summer months are the most popular months to ride, and the longest rides.
    - Weekends tend to be the most popular days to ride, and the longest rides.
    - Members tend to use the bikes more often and at more consistent durations.
    - Members ride more during the week, signifying that it is frequently used for work commuting.
    - Members prefer classic bikes over electric, while casual riders prefer electric bikes over classic bikes.
    
    
* **How will these insights help answer your business questions?**
    
    These trends and relationships allow us to see some differences between casual riders and members that we can then use to start to formulate some recommendations for marketing at specific times of the week, and months to specific riders.

#### Deliverable

* A summary of your analysis

<a id="8"></a> <br>
# Share

Embedded in this notebook are the visualizations I carried out in tableau.In the meantime I have provided a link to the dasboards in my Tableau Public with all data for this visualization accessible there.

__Link to the Dashboard visualizations on Tableau__
https://public.tableau.com/app/profile/elijah.agom/vizzes
