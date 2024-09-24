# Instagram User Analytics - SQL Fundamentals

__Difficulty Level:__ Intermediate

## Description

Imagine you're a data analyst working alongside the __Product Team__ at Instagram. Your primary responsibility is to analyze user interactions and engagement to provide actionable insights that can drive business growth. User analysis is crucial for understanding how people engage with Instagram, which can help various teams:

- __Marketing:__ Tailor campaigns and reward loyal users.
- __Product:__ Decide which features to build based on user behavior.
- __Development:__ Improve the user experience by analyzing activity and engagement trends.
  
This project focuses on answering key business questions using __SQL__ and __MySQL Workbench__. Your SQL expertise will uncover insights that can shape the future direction of one of the world's most influential social media platforms.

## Project Tasks:

### A) Marketing Analysis

1. #### Loyal User Reward:

- __Goal:__ The marketing team wants to reward the most loyal users—those who have been with the platform for the longest time.
- __Task:__ Identify the five oldest users on Instagram by registration date.
 ##### SQL Query:
 ``` sql
SELECT username, created_at
FROM users
ORDER BY username, created_at ASC
LIMIT 5;
```

2. #### Inactive User Engagement:

- __Goal:__ Encourage inactive users to start posting by sending them promotional emails.
- __Task:__ Identify users who have never posted a photo.
 ##### SQL Query:
 ``` sql
SELECT username
FROM users
LEFT JOIN photos ON users.id = photos.user_id
WHERE photos.user_id IS NULL;
```

3. #### Contest Winner Declaration:

- __Goal:__ Determine the winner of a contest where the user with the most likes on a single photo wins.
- __Task:__ Identify the user with the highest number of likes on a single post.
 ##### SQL Query:
```sql
SELECT username, photos.id, photos.image_url,
COUNT(likes.user_id) as like_count
FROM photos
INNER JOIN likes ON likes.photo_id=photos.id
INNER JOIN users ON users.id=photos.user_id
GROUP BY photo_id
ORDER BY like_count DESC
LIMIT 1;
```

4. #### Hashtag Research:
   
- __Goal:__ A partner brand wants to know which hashtags are most effective for engagement.
- __Task:__ Identify the top five most commonly used hashtags on the platform.
 ##### SQL Query:
```sql
SELECT tag_name ,count(*) as hashtag_count
FROM tags
JOIN photo_tags ON photo_tags.tag_id= tags.id
GROUP BY tag_name
ORDER BY hashtag_count DESC
LIMIT 5;
```

5. #### Ad Campaign Launch:

- __Goal:__ Find the best day of the week to launch a new ad campaign based on user registration activity.
- __Task:__ Identify the day of the week with the highest number of user registrations.
 ##### SQL Query:
```sql
SELECT DAYNAME(created_at) AS registration_day,
COUNT(*) AS registration_count
FROM users
GROUP BY registration_day
ORDER BY registration_count DESC
limit 2;
```

### B) Investor Metrics

1. #### User Engagement:

- __Goal:__ Provide insights into how engaged users are and how frequently they post.
- __Task:__ Calculate the average number of posts per user and provide the total number of posts divided by the total number of users.
 ##### SQL Query:
```sql
SELECT AVG(photo_count) AS average_posts_per_user
FROM (
SELECT user_id, COUNT(*) AS photo_count
FROM photos
GROUP BY user_id
)user_photos_count;

SELECT COUNT(*) AS total_photos, COUNT(DISTINCT user_id) AS
total_users,
COUNT(*) / COUNT(DISTINCT user_id) AS
average_photos_per_user
FROM photos;
```

2. #### Bots & Fake Accounts:

- __Goal:__ Identify users who may be bots or fake accounts by detecting unusual behavior.
- __Task:__ Identify users who have liked every single photo on Instagram.
 ##### SQL Query:
```sql
SELECT id, username
FROM users
JOIN (
SELECT user_id
FROM likes
GROUP BY user_id
HAVING COUNT(DISTINCT likes.photo_id) = (SELECT
COUNT(DISTINCT image_url) FROM photos)
) likes ON users.id = likes.user_id
ORDER BY username ASC;
```

## Tools Used:

- SQL
- MySQL Workbench

## Deliverable:

The deliverable is an [Instagram User Analytics Report](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/Instagram_User_Analytics/Instagram%20User%20Analytics.pdf) that includes:

- __Marketing insights__ (loyal users, effective hashtags).
- __Investor metrics__ (user engagement trends).
- __Bot detection analysis__ to ensure data integrity.

The report will provide visualizations and insights derived from SQL queries to help stakeholders make data-driven decisions.
