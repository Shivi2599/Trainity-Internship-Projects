# Operation Analytics and Investigating Metric Spike - Advanced SQL

__Difficulty Level:__ Advanced

## Description:

__Operational Analytics__ is an integral process that analyzes a company's end-to-end operations, focusing on identifying areas for improvement and efficiency. This project involves working closely with various departments, such as operations, support, and marketing, to derive actionable insights from data. One of the key tasks in operational analytics is investigating metric spikes, such as sudden increases or decreases in user engagement or sales.

In this project, you'll take on the role of a __Lead Data Analyst__, responsible for analyzing datasets from different business operations and investigating spikes in key metrics. 
By utilizing __advanced SQL__ skills, you'll answer key questions posed by different teams, focusing on throughput analysis, language share, and user engagement.

## Case Study 1: Job Data Analysis

You will work with a table named `job_data`, which contains the following columns:

- __job_id:__ Unique identifier for each job.
- __actor_id:__ Unique identifier for each actor reviewing a job.
- __event:__ Type of event related to the job (decision/skip/transfer).
- __language:__ Language of the job content.
- __time_spent:__ Time spent reviewing the job (in seconds).
- __org:__ Organization to which the actor belongs.
- __ds:__ Date in the format `yyyy/mm/dd` (stored as text).

## Tasks:

1. #### Jobs Reviewed Over Time:

- __Objective:__ Calculate the number of jobs reviewed per hour for each day in November 2020.

##### SQL Query:
```sql
SELECT ROUND(SUM(jobs_review_per_hour) / COUNT(ds), 3) AS jobs_review_per_hour_per_day
FROM (
SELECT ROUND(COUNT(DISTINCT job_id) * 3600 / SUM(time_spent), 3)  AS jobs_review_per_hour,    ds  
FROM job_data    
WHERE MONTH(ds) = 11 AND YEAR(ds) = 2020  
GROUP BY ds
) AS A;
```

2. #### Throughput Analysis:

- __Objective:__ Calculate the 7-day rolling average of throughput (events per second).

##### SQL Query:
```sql
WITH daily AS
(
SELECT Round(COUNT(event)/sum(time_spent),2) AS daily_throughput,
ds AS date
FROM  job_data
GROUP BY date
 )
SELECT ROUND(AVG(daily_throughput),2)    
AS rolling_average, date
FROM daily
GROUP BY date;
```
- __Preference:__ The __7-day rolling average__ smooths out daily fluctuations, providing a more stable trend for long-term analysis, making it preferable for decision-making.

3. #### Language Share Analysis:

- __Objective:__ Calculate the percentage share of each language in the last 30 days.

##### SQL Query:
```sql
SELECT language, 
COUNT(job_id) AS Language_Count,
(COUNT(*) / ( SELECT COUNT(*)    
              FROM  Job_data)
             ) * 100 AS Percentage_Share
FROM    Job_data
GROUP BY language;
```
4. #### Duplicate Rows Detention:

- __Objective:__ 

##### SQL Query:
```sql
SELECT *
FROM  job_data
GROUP BY job_id, actor_id, event, language, time_spent, org, ds
HAVING COUNT(*) > 1;
```

## Case Study 2: Investigating Metric Spike

You will work with three tables:

- __users:__ Contains descriptive information about each user’s account.
- __events:__ Contains one row per user action (e.g., login, messaging).
- __email_events:__ Contains specific events related to email activity.

## Tasks:

1. #### Weekly User Engagement:

- __Objective:__ Measure weekly user engagement.

##### SQL Query:
```sql
SELECT WEEK(occured_at) AS week_number,
COUNT(DISTINCT user_id) AS weekly_engagement
FROM events
WHERE event_type='engagement’
GROUP BY week_number
ORDER BY week_number;
```
![Screenshot 2024-09-24 213708](https://github.com/user-attachments/assets/36638187-0b86-4509-a2a4-51e9e4d1d435)


2. #### User Growth Analysis:

- __Objective:__ Analyze user growth over time.

##### SQL Query:
```sql
SELECT DATE_FORMAT(created_at, '%Y-%m') AS month,
COUNT(DISTINCT user_id) AS  user_count,    
LAG(COUNT(DISTINCT user_id)) OVER (ORDER BY DATE_FORMAT(created_at, '%Y-%m')) AS previous_user_count,
(
COUNT(DISTINCT user_id) - LAG(COUNT(DISTINCT user_id)) OVER (ORDER BY DATE_FORMAT(created_at, '%Y-%m'))) / LAG(COUNT(DISTINCT user_id)) OVER (ORDER BY DATE_FORMAT(created_at, '%Y-%m')) * 100 AS growth_percentage
FROM users
GROUP BY month
ORDER BY month;
```
![Screenshot 2024-09-24 213807](https://github.com/user-attachments/assets/d87f38ff-5d0e-429c-a73f-4147d836ed53)

3. #### Weekly Retention Analysis:

- __Objective:__ Analyze weekly user retention after sign-

##### SQL Query:
```sql
WITH user_weekly_activity AS 
(   
SELECT user_id, WEEK(occured_at) AS week_number    
FROM  events  
GROUP BY user_id, week_number
) 
SELECT week_number AS current_week,
LAG(week_number)  OVER (ORDER BY week_number) AS previous_week,   
COUNT(DISTINCT   user_id) AS retained_users,
LAG(COUNT(DISTINCT user_id)) OVER (ORDER BY week_number) AS starting_users,  
COUNT(DISTINCT user_id) / LAG(COUNT(DISTINCT user_id)) OVER (ORDER BY week_number) * 100 AS retention_percentage
FROM user_weekly_activity
GROUP BY week_number
ORDER BY week_number; 
```
![image](https://github.com/user-attachments/assets/04bc207d-74f2-46c2-b8ef-163109b3698b)

4. #### Weekly Engagement Per Device:

- __Objective:__ Measure weekly engagement on different devices.

##### SQL Query:
```sql
SELECT WEEK(occured_at) AS week_number, device,   
COUNT(DISTINCT user_id) AS weekly_engagement
FROM events
GROUP BY week_number, device
ORDER BY week_number, device;
```
![Screenshot 2024-09-24 214230](https://github.com/user-attachments/assets/d9ec650e-9944-4a86-b327-bd073581fb81)

5. #### Email Engagement Analysis:

- __Objective:__ Analyze user engagement with the email service.

##### SQL Query:
```sql
SELECT    user_id,   
COUNT(DISTINCT    user_id)     AS     total_emails_received,    
COUNT(
CASE WHEN action='email_open' 
THEN user_id END
) AS total_emails_opened,    
COUNT(
CASE WHEN action='email_clickthrough' 
THEN user_id END
) AS total_emails_clicked,   
COUNT(
CASE WHEN action='sent_weekly_digest' 
THEN user_id END
) AS total_emails_delivered
FROM email_events
GROUP BY user_id
ORDER BY user_id;
```
![Screenshot 2024-09-24 214453](https://github.com/user-attachments/assets/2d9a6422-ad5f-4ee4-bce3-7f300f35d453)


## Insights:

- Jobs reviewed per hour for each day in November 2020 is __126.18__.
- Week 17 has high retention percentage.
- Week 34 has low retention percentage.
- __Macbook Pro__ device has high activenessof users on a weekly basis.

## Deliverable:

The deliverable is an [Operation Analytics and Investigating Metric Spike Report]().






