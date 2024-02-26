# Bellabeat-casestudy
A case study on smart device usage for the company Bellabeat, as part of the Google Data Analytics Specialization's capstone project. I have used SQL in Bigquery and created my visualizations by utilizing Tableau.

This case study follows the six step data analysis process:
 * Ask
 * Prepare
 * Process
 * Analyze
 * Share
 * Act

## Introduction
Bellabeat is a high-tech manufacturer of health-focused products for women. Bellabeat is a successful smaller company, but they have the potential to become a larger player in the global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company.

![image](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/8ab93fe6-42c1-4d42-a609-7e394282c1eb)

# Step 1: Ask

## Business Task
To Identify potential opportunities for growth and provide recommendations for the Bellabeat marketing strategy improvement based on trends in smart device usage

Key Stakeholders:
- Urška Sršen: Bellabeat’s cofounder and Chief Creative Officer
- Sando Mur: Mathematician and Bellabeat’s co-founder

Questions to explore for the analysis:
1. What are some trends in the usage of smart devices?
2. How could these trends apply to Bellabeat customers?
3. How could these trends help influence Bellabeat Marketing strategy?

# Step 2: Prepare
In order to complete Bellabeat's Business Tasks, I will be using Fitbit Fitness Tracker Data. The data set used for this case study can be found here: FitBit Fitness Tracker Data [https://www.kaggle.com/datasets/arashnic/fitbit]  (CC0: Public Domain, dataset made available through Mobius[https://www.kaggle.com/arashnic] ): This Kaggle data set contains personal fitness tracker from thirty FitBit users. Thirty Eligible FitBit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. It includes information about daily activity, steps, and heart rate that can explore users’ habits.

The Data set contains 18 CSV files organized in long format. I will be using 8 of these files for my analysis.  

## Dataset Considerations
The dataset comprises information from 33 Fitbit users who authorized the sharing of their personal tracker data consisting of physical activity, heart rate, and sleep monitoring. However, teh dataset has limitations. It is dated, spanning from April 12, 2016 to May 12, 2016, covering a 31-day duration. There are also demographic details such as gender, location, and age that are absent, introducing certain constraints. Additionally, the dataset includes 30 users, with the selection criteria for this sample remaining unknown. Despite these limitations, the insights derived from this dataset hold significance and serve as the foundation of my analysis.

For this analysis, I cleaned and analyzed the data using BigQuery for SQL and created visualizations using Tableau.

# Step 3: Process
To process this data, I have cleaned and formatted the data to be clear and concise. The cleaning process included standardizing data types, checking for and removing duplicates, and creating new tables to merge data for a more efficient analysis.
![1SQL cleaning](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/bb060a54-677c-4a31-ad42-281529130898)
![2SQL cleaning](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/75f0380b-72f7-4e59-9e65-cba84227772a)

There are 33 users in the daily_activity, daily_calories, daily_intensities, hourly_activity, hourly_intensities, hourly_calories, and hourly_steps tables. There is 24 users in the sleep_day table. In the heartrate_seconds table there are only 7 users and in the weight_log table there are 8 users. Due to this small sample size in both of these tables, I have decided to not include them in my analysis.

![3SQL cleaning](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/5d4809b1-0fb9-418e-b516-931a278163b8)
![4SQL cleaning](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/b30146a0-551c-4f34-aaf9-ba869036d2c7)

# Step 4: Analyze
![1SQL analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/0722460b-5c3c-4d33-a292-03b74001ff2b)
![SQL1 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/15cb7b54-5ef8-4079-a6f6-e47285a273aa)


This query shows the average steps, distance, and calories burned per day of the week. If we look at the amount of average steps and calories burned, we can conclude that users are most active on Saturdays and least active on Sundays. Also, the most desirable times of the day to be active is seen to be from 5:00 AM to 7:00 PM. We can use this information to allow for notifications on Bellabeat smart devices to cater specifically to these days and times throughout the week.

![2SQL analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/06a7a22a-c25d-4d23-853a-d60859dd8772)

![2SQL analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/168b45df-f0c4-47d7-935d-331a76e71bfc)

Users are sleeping on average approximately 7 hours each night, and are in bed awake for approximately 39 minutes on average.  

![3SQL analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/6f6dd074-4572-4f43-ab7d-f0e09e0aa642)

![3SQL analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/77d63ad4-eb92-4ce8-9418-026c04e0f287)

Based on these averages calculated from the sums of minutes spent on each activity per user, it shows that the majority of active minutes spent are sedentary minutes at an average of 81.3%. The least amount of minutes spent is in the Fairly Active activity level, with 1.1% of time spent in a day.

![4SQL analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/d9ae7ae8-3b7c-4662-9380-9ca2cc92d5c1)

![4SQL analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/71c4683c-f36c-47d2-9bd2-d4d02e5af9d3)

![SQL5 analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/7cc7f445-700a-4d6b-bbd6-705e5af65b1d)

![SQL5 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/d9b9ab40-8567-4434-9a48-85f0cb9fe0ef)

Towards the end of the study, we can see that the amount of users per day decreases. Bellabeat should aim to focus on user retention.

![SQL6 analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/66367d55-503e-45ff-9a1b-c4ac452d5b4a)

![SQL6 analysisvisual2](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/da3794df-6dbc-4b24-8fff-bdbdd8084518)

 These findings indicate a relationship between activity intensity and calorie expenditure. "Very Active" minutes burn the most calories, whereas "Lightly Active" minutes burn fewer. To enhance awareness of activity levels, a device feature should notify users of their current activity level, with daily summaries provided at the end of each day.

![SQL9 analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/6a5be68a-c2c9-42f9-921d-ea44d491b640)

![SQL9 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/9330cef8-0863-4177-87e3-bd32f0453c41)

![SQL10 analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/87a8fb60-2698-4bcd-abb7-cb04ef8999e0)

![SQL7 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/c92047eb-6314-409e-b557-926322b324a6)

There is a positive correlation shown between the amount of steps acquired and the amount of calories burned each day, per user. This tell us that the more steps taken per day, the more calories that are burned. Users should strive to reach 10,000 steps per day as recommended by the CDC[^1]. A feature on Bellabeats' smart devices should incorporate this as a goal for users to meet. 

![SQL8 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/a7ebdb73-f653-4ab6-9211-41cdf0d60527)

![SQL11 analysis](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/a465af52-1406-4cf4-ae54-62e05fc77e8c)

![SQL11 analysisvisual](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/73382f16-d7e4-46e1-819b-d8f0005d2070)

According to the charity Just Stand[^2], the following thresholds determine a person's risk of developing health problems due to sitting:
 * Low Risk: Sitting for less than 4 hours per day.
 * Medium Risk: Sitting for 4-8 hours per day.
 * High Risk: Sitting for 8-11 hours per day.

As shown by this query, all users average sedentary minutes were well above 4 hours (240 minutes) per day. This increases their risk level of developing future health problems and should be made aware of while using a smart device. 

# Step 5: Share

## User Activity Dashboard

![Bellabeat dashboard1](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/053b274c-f03a-464d-ac2f-9e3a9ff210b3)

## User Caloric Expenditure Dashboard

![Bellabeat dashboard2](https://github.com/laneydsmith/Bellabeat-casestudy/assets/153331633/6a3feaef-0cec-476f-8698-45d344a52364)


# Step 6: Act



Citations
[^1]:Centers for Disease Control and Prevention. (n.d.). Physical Activity Basics. Retrieved from https://www.cdc.gov/physicalactivity/basics/pa-health/index.htm

[^2]:Sitting Time Calculator. https://www.juststand.org/the-tools/sitting-time-calculator/. This calculator determines "Risk for Sitting Disease" using thresholds defined by research published in Arch Intern Med. 2012;172(6). Dr. David Dunston summarizes the findings in this video from the 2012 JustStand Wellness Summit.

































