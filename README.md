# Google Analytics Capstone Project
## Bellabeat's "Time" product analysis

### Introduction
Welcome to the case study developed as part of the Google Data Analytics Capstone activities of the Google Data Analytics Professional Certificate course. This course
promoted knowledge and skills development about the analysis processes (ask, prepare, process, analyze, share and act) that were useful in this case study. This study
made it possible to put this knowledge into practice to answer key business questions from real scenarios, such as the high-tech manufacturer of health-focused
products for women, Bellabeat. To develop this project I chose to use tools such as Excel, SQL, RStudio and Tableau.

### Scenario
Bellabeat is a successful company that operates in the global market of smart devices. Urška Sršen, co-founder and creative director of Bellabeat, believes in data
analytics to help unlock new growth opportunities for the company. My role in this case study will be to analyze data from smart devices to gain insights into how
consumers use them. The insights I discover will help guide the company's marketing strategy.

### Ask
#### A clear statement of the business task
The purpose of the business task is to analyze data from non-Bellabeat smart device users to gain insights that can be applied to Bellabeat smart devices, such as the
smart watch, "Time". In addition, trends applicable to users and influencing marketing strategies are welcome.

### Prepare
This dataset is located on Kaggle and is in the public domain - FitBit Fitness Tracker Data (https://www.kaggle.com/datasets/arashnic/fitbit). They are presented in
spreadsheets, with the data organized into 18 files and titled by category. The archives include information such as: Id numbers, date, daily activity, heart rate, calories,
steps, and Intensities por horas, as well METs (metabolic equivalent of task) by minute, sleep day and information about weight. Data were obtained between April 12 to
May 12, 2016. In addition, the survey was developed by Amazon Mechanical Turk, that is, a reputable company that contributes to the integrity of the data but needs to
be confirmed.

### Process
#### Documentation of any cleaning or manipulation of data
I downloaded the data to my computer and took a look at it, I figured i don't need all the tables since some of them were considered in another tables in the same dataset or were irrelevant for the analysis task.
The tables ive used are: 
- dailyActivity_merged
- hourlyCalories_merged
- hourlyIntensities_merged
- hourlySteps_merged
- minuteMETsNarrow_merged
- sleepDay_merged_corrected
- weightLogInfo_merged_corrected

I used the DISTINCT function to identify the number of unique Ids. This way it will be possible to know how many users were evaluated for each table. As a result I came to a concolusion that most tables had 33 users,
however, some tables had less than 30 meaning the answers will not provide enough insights to make an effective business decision,  as they do not adequately represent a population. Based on that, I excluded those tables from the analysis.
I used another query to check for any null values, example for the query:

SELECT

(asterisk)

FROM `date-learning.fitbit.fitbit_daily_activity` 

WHERE

ActivityDate IS NULL


Then, I used another SELECT DISTINCT function to check for potential errors in the values of each column. Example:

SELECT

DISTINCT ActivityDate

FROM `date-learning.fitbit.fitbit_daily_activity`

### Analyze
 At this stage i performed calculations for further analysis:
* mean (average)
* std (standard deviation)
* min and max
* percentiles 25%, 50%, 75%

Interpreting statistical findings:
1. On average, users logged 7,637 steps which covered 5.4km, According to the CDC (Centers for Disease Control and Prevention) an adult female has to aim to atleast 10,000 steps per day.
2. The afternoon is the part of the day when users are mostly active at and burn most calories because of that.
![Screenshot_2](https://user-images.githubusercontent.com/123517106/214452647-1f869e24-1389-45b2-a401-0ce42b1a07c4.png)
3. Most users are in a sedentary state 81% of the day.
4. Users spend slightly less than 7 hours per day in bed, they are asleep for 91% of that time.




### Share

![Dashboard 1](https://user-images.githubusercontent.com/123517106/214453165-8b1d70e8-ac55-48df-ba20-769cb8ba881f.png)

![Screenshot_7](https://user-images.githubusercontent.com/123517106/214453064-7df2fa68-cd0f-4508-a5e6-8a04c5288b5d.png)

![Screenshot_3](https://user-images.githubusercontent.com/123517106/214456512-2e2acee0-e518-4ed8-a726-f06dd6380f9a.png)
### Act
#### Recommendations
Upon the insights I gained through the analysis proccess I would recommend to:
1. Bellabeat should offer incentives for consistent tracking like in-app competitions among friends or users in the same area, winner will get discount for next subscriptions or future products.
2. Adding a RMR calculator to calculate daily average calorie burn dynamically for each user and upon that the user will be able to set a goal for weight gain / weight loss.
3. Bella can encourage users to be more active by educating them about fitness benefits and suggest different types of exercies in order to create a diverse of activites and each user will be able to choose what suits best for him.






