# GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY

![CYCLIST](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/4c67e00d-1f38-46b6-bc6d-cba585a2147d)

INTRODUCTION

I have completed the Google Data Analytics courses on Coursera and would like to demonstrate the knowledge and skills I have learnt through this case study. In this case study, I will perform a real-world task as a junior data analyst and follow the steps of the data analysis process: ask, prepare, process, analyze, share, and act.

Background

I am a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

Cyclistic is a bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day.

About the Company

In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a very good chance to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs.

Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.


![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/52597d65-0bd5-4234-9d9c-2370b0d06b91)




Phase 1: Ask

Business Task
To identify the difference between annual members and casual riders in using Cyclistic bikes and provide recommendations to convert casual riders into annual members.

Key Stakeholders
Lily Moreno: The director of marketing and your manager.
Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide the Cyclistic marketing strategy
Cyclistic executive team: The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.


PHASE 2: PREPARE

Data Source Description
The data used was supplied by Google and can be found in the link: [12 months of Cyclistic trip data.](https://ride.divvybikes.com/data-license-agreement) It is public data on the fictional company called Cyclistic provided by Motivate International Inc. under this license. Data for March 2021 to February 2022 has been selected for use.

Data Location: HTML link supplied above

Data Organization: data was supplied as CSV files which were zipped according to their respective months.

Data’s Relevance to the Problem: Booking information on rides, membership types, duration of trips, etc. are part of the information supplied which will be used to show helpful insights into the rider’s pattern

Problems with the Data: Blank or null values. As riders’ personally identifiable information is prohibited, no pass purchases will be able to connect to credit card numbers to determine if casual riders live in the Cyclistic service area or have purchased multiple single passes.

Phase 3: Process

I have used Microsoft Excel for data validation and cleaning.

Some steps I have done in the validation and cleaning part are:-

I decided to convert the files from the .csv format to .xlsx and opted to analyze each month separately in Microsoft Excel.

In each file the information is sorted under the following 12 columns:

· Column A — ride_id: Unique ID assigned to each individual ride

· Column B — rideable_type: Type of bicycle (classic, docked, or electric)

· Column C — started_at: Date and time at the start of the trip

· Column D — ended_at: Date and time at the end of the trip

· Column E — start_station_name: Name of the station the trip started at

· Column F — start_station_id: ID number of the station the trip started at

· Column G — end_station_name: Name of the station the trip ended at

· Column H — end_station_id: ID number of the station the trip ended at

· Column I — start_lat: Latitude of starting location

· Column J — start_lng: Longitude of the start location

· Column K — end_lat: Latitude of ending location

· Column L — end_lng: Longitude of ending location

· Column M — member_casual: Type of membership (Casual or Cyclistic Member)

STEP 1: I deleted a column called ‘ride_id’. I don’t believe we need ride_id for analyzing this data, so I deleted.

STEP 2: I copied a column called ‘started_at’ twice and then edited it to ‘start_hour’ and ‘start_date’. I changed the ‘start_hour’ format to time and ‘start_date’ format to date only.

STEP 3: I copied a column called ‘ended_at’ twice and then edited it to ‘end_hour’ and ‘end_date’. I changed the ‘end_hour’ format to time and ‘end_date’ format to date only.

STEP 4: I created a column called ‘trip_duration’ and then extracted ‘end_hour’ from ‘start_hour’ and they are in the format of minutes

STEP 5: I created a column called ‘start_day’ and then applied a formula ‘=text(start_day, ‘DDD’). We created this column to extract day of each trip, so that we can figure out which day has the most customer.

STEP 6: Filtered the ‘start_station’ and deleted the blank rows in excel.

STEP 7: Filtered the ‘trip_duration’ and deleted the rows which contain less than 5 seconds.

STEP 8: Created a column called ‘month_start’ and extracted the month of each trip.

STEP 9: Searched for duplicates with the built-in function in excel, and no duplicates were found in the individual month sheets.

STEP 10: Searched for blank cells on the columns that include the most important information for our study, and none were found.

STEP 11: Looked for extra spaces and misspelling in my cells.

STEP 12: Used the built-in filter for all the columns and manually checked for unexpected values.

Phase 4: Analyze

Now that I have some clean data, I will be organizing and performing calculations on it to identify key trends and relationships.

I have used ‘Pivot table’ for exploring the data. Following are some of the insights I tried to gather.

Finding the number of members and casual riders (June 2020-May 2022).

About 57% users are member riders and 42% are casual riders.

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/1e65e7ed-ac22-4a33-bd44-7becb7a8e6d6)




More rentals by casual riders than members

We see a general reduced usage of the service during the summer periods in Chicago (July to September — where the least number of trips can be observed) and a steady increase from October with a peak in Feb for the Casual group and Members.


Summary of Bike rentals every day of the week

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/5bbca1ce-06a0-46c4-8394-2acc708c7bb8)



Docked bikes are popular in both casual and member riders. But casual riders use these rides more often on weekends and member riders use them weekly consistently.


![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/fcf35a3f-da68-4ce5-b191-6f6faec2f483)



Trip duration classified by type of riders

Duration of casual riders start falling during winter season in Chicago (October to February — where the least duration of trips can be observed). Trip duration of member riders also falls during winter season. Trip duration peaks during summer season in Chicago (July to September — where the most duration of trips can be observed).

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/78539a89-9034-4da7-a865-b38f7d7b047e)



Top Ten Start Stations

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/d52e3351-5a42-4d47-99af-23c96e207778)



Streeter Dr & Grand Avenue, Lake Shore Dr & Monroe St, and Theater on the Lake are the top three stations that are significantly more popular among casual riders than members.

Hourly Trip Trend

Here, we see that members’ bookings peak at about 8 AM and 6 PM which coincides with general work resumption and closure time. Casual bookings show a steady increase throughout the day until 6 PM too.

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/4bde8186-b1f2-4ac4-bd63-a626737e3358)


Trip Duration

· Trips by casual group (2,107,789) account for 42.9% of the total number of trips, which is slightly lesser than that of member groups (1,583,898), 57.1%

· However, the casual group spent more time on trips, up to twice that of members for the whole 12 months.

· The average trip of the casual group (35mins) is slightly more than double that of members (17mins)

· This proves that Casual users ride for leisure most

![image](https://github.com/PayalGarg1201/GOOGLE-DATA-ANALYTICS-CAPSTONE-PROJECT-CYCLISTIC-CASE-STUDY/assets/133757186/e7071b7e-0677-4460-baad-40f34a8ce024)


Click on below link to view the dashboard for this case study
https://public.tableau.com/authoring/Payal_Google_cyclistic_project/CyclisticRidePatterns#1

Phase 5: SHARE

1) 60–70% of rentals for members occur during morning and evening, with an average rental duration of 35 minutes for casual riders and 17 minutes for member riders, indicating that member riders are likely office workers who use the bikes for commuting to work.

2) Top 10 starting station for casual riders are around the city centers or tourist attractions with 65–75% of rentals happening during evening timings. Casual riders could constitute a mix of office workers, tourist and students.

3) Rental activity for casual riders start to pick up during winter months

4) Across the last 12 months, total number of hours rented by members showed that activity throughout weekdays and weekends tend to be relatively consistent. However, casual members rental activity favours a preference of weekends over weekdays.

Phase 6: ACT

Here are some insights that will be useful to the marketing campaign

The data illustrates that casual riders (average: 35mins) go on longer trips than members (average: 17mins). The longest trips for casual riders are done with docked bikes.

· The campaign should show how casual riders can save money being charged per trip rather than based on the duration of the trip

· An advert featuring the docked bike can be used since that is the most preferred bike for long trips by casual riders.

· Casual riders may prefer the ease of spending little by little for each trip taken, so the campaign should provide the option of upgrading by paying in installments

Casual members prefer weekend trips with peak usage in the month of February

· The campaign should feature a membership plan where weekend trips remain unchanged while weekday trips are discounted for casuals. This ought to encourage an upgrade to a membership plan and more weekday rides.

· The campaigns should be heavy in the Summer to gain good conversion before Winter

The heaviest market campaigns should be in these stations: Streeter Dr & Grand Avenue, Lake Shore Dr & Monroe St, and Theater on the Lake
