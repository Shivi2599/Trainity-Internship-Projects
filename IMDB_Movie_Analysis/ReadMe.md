# IMDB Movie Analysis

### Final Project 1

## Project Overview

What makes a movie successful on IMDB? This analysis dives deep into a dataset of IMDB movies to answer this critical question. Success is defined by a movie's IMDB rating, a key metric for movie producers, directors, and investors. By identifying the factors that influence higher ratings, we can offer data-driven insights that guide future decisions in the film industry.

Through careful __data cleaning, exploration, and analysis__, this project seeks to uncover relationships between various factors—such as __genre, duration, language, director, and budget—and a movie’s success__.
The results of this analysis are designed to provide actionable insights that will support informed decision-making in movie production and distribution.

## The Problem We Set Out to Solve:

Our journey began with one key question: __What makes a movie successful on IMDB?__ 

By answering this question, we can offer insights to help studios, producers, and directors craft movies that are more likely to resonate with audiences.

## Our Approach to Unveiling the Truth:

Like all good stories, ours starts with preparation. 

The first step in any analysis is ensuring the dataset is reliable. Here, we processed the IMDB dataset by:

- Handling missing values
- Removing duplicates
- Ensuring data types were appropriate for analysis
  
By cleaning the data, we created a solid foundation for accurate and meaningful insights.

## Data Analysis - Exploring the Story Behind the Numbers

### Task A: Genre Analysis - The Power of Genre

#### Key Questions Explored:

- Which genres dominate the dataset?
- How do different genres compare in terms of average IMDB ratings?

Using __descriptive statistics__, we analyzed the most common movie genres and their respective IMDB ratings. With functions like `AVERAGE`, `MEDIAN`, and `STDEV`, we explored which genres consistently performed better than others.

 ![Screenshot 2024-09-25 180508](https://github.com/user-attachments/assets/f32da40d-dd1f-48e7-a233-878ec4fe82fb)
Through this analysis, we aim to provide insights for movie producers on which genres are most likely to succeed.

### Task B: Movie Duration Analysis - Does Length Matter?

#### Key Question Explored:
- Does the length of a movie have any bearing on its ratings?

 ![Screenshot 2024-09-25 183416](https://github.com/user-attachments/assets/c76df0db-ec3f-4db7-bb4a-b0c57bdc0c18)

For directors and producers, understanding the relationship between movie duration and audience reception can influence critical decisions in film editing.

### Task C: Language Analysis - Global Reach

#### Key Questions Explored:

- Do movies in specific languages tend to perform better on IMDB?
- Which languages are most common in the dataset?

     ![image](https://github.com/user-attachments/assets/e757ff29-5cfd-4a0e-a9b9-2fe9acb9a074)  
![Screenshot 2024-09-25 185149](https://github.com/user-attachments/assets/033c3e59-06fe-4242-99dc-51928b217fbb)

### Task D: Director Analysis - The Signature of Success

In this task, we calculated the __average IMDB score__ for each director and identified the top-performing directors using __percentile analysis__.

#### Key Questions Explored:

- Who are the top directors based on average IMDB scores?
- How much influence does a director’s reputation have on the success of a movie?

  ![Screenshot 2024-09-25 185623](https://github.com/user-attachments/assets/6556171a-4800-48e5-bfa0-634414929743)

### Task E: Budget Analysis - Does Money Buy Success?

In the film industry, money matters. But does a larger budget guarantee a successful movie?
To explore this, we analyzed the relationship between __movie budgets__ and __gross earnings__, calculating __correlation coefficients__ to assess the strength of this relationship. We also calculated __profit margins__ to identify movies with the highest return on investment.

#### Key Questions Explored:

- Is there a strong correlation between budget size and gross earnings?
- Which movies achieved the highest profit margins?

  ![image](https://github.com/user-attachments/assets/5efb037e-5287-4053-a63e-e2f46a859b34)

 Correlation Coefficient between movie budgets and gross earnings using Excel's CORREL function is __0.0964902__.

## The Five Whys - Digging Deeper into Success

The __Five Whys__ technique helps us explore the root causes of trends in the data. For example, when we discovered that movies with higher budgets tend to have higher ratings, we asked __why__ repeatedly until we reached a deeper understanding:

- __Why do higher-budget movies have higher ratings?__
  Because they can afford better production quality.
- __Why does better production quality matter?__
  It enhances the viewer's experience.
- __Why does this lead to higher ratings?__
  Positive viewer experiences result in more favorable reviews and ratings.

  Through this process, we uncover the deeper reasons behind movie success, offering richer insights for decision-makers.

## Tools and Technologies Used:

- __Excel:__ Used for data cleaning, descriptive statistics, and visualization.
- __IMDB Dataset:__ Provides information on movie genres, durations, languages, directors, budgets, and gross earnings.
- __PowerPoint:__ Used for creating report.

## Deliverables:

1. [IMDB Movie Analysis Report](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/IMDB_Movie_Analysis/imdb%20movies%20analysis.pptx)
2. [Excel Workbook](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/IMDB_Movie_Analysis/IMDB%20movies_analysis.xlsx)









