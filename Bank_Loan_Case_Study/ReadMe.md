# Bank Loan Case Stdy

### Final Project 2

__Difficulty Level:__ Advanced

## Project Overview:
In today’s fast-paced financial services industry, __risk assessment__ and __loan default prediction__ are critical elements in maintaining the financial health of lending institutions. This case study takes us into the role of a data analyst at a finance company that specializes in lending various types of loans to urban customers. The primary objective of this project is to analyze patterns in loan applications and identify factors that contribute to __loan default__, enabling the company to make more informed decisions during the loan approval process.

This study aims to ensure that:

- __Capable applicants are not rejected__, safeguarding potential business opportunities.
- __Risky applicants are identified early__, reducing potential financial losses.
  
Using __Exploratory Data Analysis (EDA)__, we dive into a dataset of loan applications to extract valuable insights and inform the company's lending strategies.

## Business Objectives:
The company faces two key risks during loan processing:

1. __Lost business:__ When a capable applicant who can repay the loan is denied.
2. __Financial loss:__ When a risky applicant who cannot repay the loan is approved.

The goal of this project is to:

- Understand customer and loan attributes that influence __loan default__.
- Identify patterns that signal __difficulty in repayment__ to make better decisions about loan approval, such as denying risky applicants, reducing the loan amount, or increasing interest rates for higher-risk customers.

## Key Data Analytics Tasks:

### A. Identify Missing Data and Deal with It Appropriately:

Handling missing data is crucial for ensuring the accuracy and integrity of our analysis. We begin by identifying missing values in the dataset and employing suitable strategies to handle them.

#### Task:

- Identify missing data using __Excel functions__ (e.g., `COUNT`, `ISBLANK`, `IF`).
- Apply appropriate methods like __imputation__ (e.g., using `AVERAGE` or `MEDIAN`) to fill in missing values.

#### Graph Suggestion:

- Create a __bar chart or column chart__ to visualize the proportion of missing values for each variable.

### B. Identify Outliers in the Dataset:

Outliers can skew the analysis and affect decision-making. Our objective is to detect and handle outliers in key numerical variables.

#### Task:

- Detect outliers using __Excel statistical functions__ like __QUARTILE__ and __Interquartile Range (IQR)__.
- Use __conditional formatting__ and thresholds to highlight and investigate outliers.

#### Graph Suggestion:

- Create __scatter plots__ to visualize the distribution of numerical variables and highlight potential outliers.
  
### C. Analyze Data Imbalance:

Understanding the distribution of classes (e.g., loan default vs. non-default) is essential, especially for binary classification problems. Data imbalance can lead to biased models and incorrect insights.

#### Task:

- Calculate the proportion of each class (e.g., default vs. non-default) using __Excel functions__ (`COUNTIF`, `SUM`).
- Assess the data imbalance and understand its implications.

#### Graph Suggestion:

- Create a __pie chart__ to visualize the distribution of the target variable and highlight data imbalance.

### D. Perform Univariate, Segmented Univariate, and Bivariate Analysis:

To gain deep insights into the driving factors behind loan default, we perform:

- __Univariate analysis__ to explore the distribution of individual variables.
- __Segmented univariate__ analysis to compare variable distributions across different scenarios.
- __Bivariate analysis__ to examine relationships between variables and the target variable (loan default).

#### Task:

- Use Excel functions like `COUNT`, `AVERAGE`, `MEDIAN` for descriptive analysis.
- Apply __filters, sorting, and pivot tables__ for segmented and bivariate analysis.

### E. Identify Top Correlations for Different Scenarios:

Understanding the correlation between customer/loan attributes and the likelihood of loan default helps in identifying key indicators for risk assessment.

#### Task:

- Segment the dataset into different scenarios (e.g., customers with payment difficulties and all other cases).
- Use Excel functions like CORREL to compute correlation coefficients between variables and the target variable for each segment.
- Rank correlations to determine the top indicators of loan default for each scenario.

#### Graph Suggestion:

Create __correlation matrices or heatmaps__ to visualize correlations.

## Tools Used:
- __Microsoft Excel:__ for data cleaning, analysis, and visualization.
- __Excel functions__ such as `COUNTIF`, `AVERAGE`, `CORREL`, `IF`, `QUARTILE`, and others for handling missing data, outliers, correlations, and performing EDA.

## Deliverables:
The final deliverable is a comprehensive [Bank Loan Case Study Report] that provides the following:

- __Insights into missing data__, outliers, and data imbalance.
- __Univariate, segmented univariate, and bivariate analysis__ of key variables.
- __Top correlations__ for different customer and loan scenarios.
- __Actionable recommendations__ based on EDA findings to improve loan approval processes.
  
## Conclusion:

This project provides a structured approach to performing __Exploratory Data Analysis (EDA)__ on loan application data. By identifying patterns in customer and loan attributes, we aim to help the company minimize risk and optimize its loan approval decisions. The insights derived from this analysis can be used to:

- Refine loan approval criteria.
- Design targeted loan products for different customer segments.
- Implement better risk management practices to prevent financial losses.

## How to Run the Project:

- Load the dataset into __Microsoft Excel__.
- Follow the steps outlined for identifying missing data, handling outliers, and performing analysis using Excel functions.
- Visualize the findings using the suggested charts and graphs.
- Interpret the insights to make informed decisions about loan approval.
