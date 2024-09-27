# Analyzing the Impact of Car Features on Price and Profitability

### Final Project 3

__Difficulty Level:__ Advanced

## Introduction

In today’s rapidly evolving automotive industry, manufacturers face increasing pressure to innovate and adapt to changing consumer preferences. The shift towards fuel-efficient and eco-friendly vehicles, combined with the enduring dominance of traditional gasoline-powered cars, presents a complex market landscape.

As a __Data Analyst__, I was tasked with answering a critical question for an automotive client:

"__How can a car manufacturer optimize pricing and product development decisions to maximize profitability while meeting consumer demand?__"

In this project, I aim to provide data-driven insights into how various car features and market categories influence price and profitability. By understanding consumer preferences and the profitability of different features, manufacturers can make informed decisions that balance innovation, consumer demand, and revenue growth.

## Project Overview

The goal of this project is to use __data analysis__ to help the car manufacturer optimize their pricing strategy and make informed product development decisions. Through an in-depth analysis of the dataset, the aim is to identify which car features and market categories are:

- Most attractive to consumers.
- Most profitable for the manufacturer.
  
This analysis is based on a dataset that contains detailed information on over __11,000 car models__, including their make, model, year, engine specifications, fuel type, transmission type, and MSRP (Manufacturer’s Suggested Retail Price).

## Approach

This project analyzes a dataset containing various __car features__, their respective __market categories__, and associated __prices__. The following __data analysis techniques__ are used to provide insights:

1. __Exploratory Data Analysis (EDA):__

- Conducted to understand the distribution of features such as car type, fuel type, engine size, and transmission, and their relationships with price.

2. __Regression Analysis:__

- Used to assess how various car features (e.g., engine size, fuel efficiency, and technology integration) influence __pricing__.

3. __Market Segmentation:__

- Identified different market segments based on consumer preferences and feature sets to highlight the most __profitable categories__ for manufacturers.

4. __Profitability Analysis:__

- Analyzed which features and categories contribute the most to __profit margins__, helping the manufacturer make strategic decisions on pricing and future product development.

## Technical Skills and Tools:

This project demonstrates the application of advanced Excel and data analysis techniques, including:

- __Advanced Excel:__
  
  - Pivot Tables
  - Regression Analysis
  - Scatter Plots
  - Combo Charts
  - Stacked Column Charts
  - Bubble Charts
  - Trendlines
    
- __Data Analysis Techniques:__
  
  - Correlation Analysis
  - Trend Analysis
  - Regression Modeling
    
By leveraging these techniques, the project delivers a comprehensive analysis to aid in strategic decision-making for car manufacturers.

## Data Cleaning

- __NUMBER OF DOORS:__ Utilized online sources to gather information on missing values for the brands: Ford Model FF and Tesla Model.
- __TRANSMISSION TYPE:__ Performed mode imputation by replacing abnormal data point "__Unknown__" with the mode value "__Automatic__" .
- __ENGINE HP:__ Null values in the engine horsepower variable were filled using data gathered from reliable online sources and through pivot tables, ensuring data completeness and accuracy.
- __ENGINE FUEL TYPE:__ Removed three rows with null values in the engine fuel type variable, all belonging to one vehicle (Suzuki).
- __ENGINE CYLINDERS:__ Filled null values in the engine cylinders variable with 0, as the corresponding vehicles with missing cylinder values were electric or Mazda RX7 and RX8, which do not have traditional cylinder configurations.
- __Deleted 715 duplicated rows__ from the dataset to ensure data integrity and accuracy in the analysis.

## Key Insights & Tasks:

### 1. Popularity and Market Categories:

- __Insight Required:__ How does the popularity of car models vary across different market categories?

![Screenshot 2024-09-27 162048](https://github.com/user-attachments/assets/e17177ad-d515-4a91-b850-26172a4bbf5a)

### 2. Engine Power and Price Relationship:

- __Insight Required:__ What is the relationship between a car’s engine power (HP) and its price (MSRP)?

![Screenshot 2024-09-27 170355](https://github.com/user-attachments/assets/8acfa788-e7fc-4d9c-9bab-cfbf201cb4fb)

### 3. Price Determinants - Regression Analysis:

- __Insight Required:__ Which car features have the most significant impact on determining a car’s price?

![Screenshot 2024-09-27 170540](https://github.com/user-attachments/assets/97e927f5-515d-4393-abbd-e755be596f17)

### 4. Manufacturer and Price:

- __Insight Required:__ How does the average price of a car vary across different manufacturers?

![Screenshot 2024-09-27 170756](https://github.com/user-attachments/assets/c0923790-b2c8-48e2-a483-ea75ef782388)

### 5. Fuel Efficiency and Engine Cylinders:

- __Insight Required:__ What is the relationship between the number of engine cylinders and fuel efficiency (MPG)?

![Screenshot 2024-09-27 171718](https://github.com/user-attachments/assets/f5b9dc19-3e33-488d-a20d-cadfba58d157)

## Dashboard Design:

The next phase involves building an interactive Excel dashboard that presents the following insights using filters and slicers:

- __Car Price Distribution by Brand and Body Style__
- __Average MSRP by Brand and Body Style__
- __Impact of Transmission Type on MSRP__
- __Fuel Efficiency Trends by Model Year and Body Style__
- __Relationship Between Horsepower, MPG, and Price Across Brands__

Filters and slicers allow users to explore the data dynamically

![Screenshot 2024-09-27 160429](https://github.com/user-attachments/assets/0359492a-2122-4f04-8093-8ec471ea4fa6)

## Insights

1. Cars with __powerful engines__ typically command __higher prices__.
2. Cars with __higher MPGs and popularity__ are __inversely__ related with __car prices__.
3. A trend observed suggests that as the __number of doors in a car increases__, there is a tendency for the __price to decrease__.
4. __Higher engine horsepower__, __more engine cylinders__, and newer model years tend to __increase car prices__.
5. As the __number of cylinders in a car's engine increases, the highway MPG tends to decrease__.
6. __Luxury and exotic cars__ may have lower average popularity despite their premium status.

## Deliverables:

- [Raw Dataset](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/Analyzing%20the%20Impact%20of%20Car%20Features%20on%20Price%20and%20Profitability/Dataset.xlsx)
- [Data Visualization Files](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/Analyzing%20the%20Impact%20of%20Car%20Features%20on%20Price%20and%20Profitability/Data%20Analysis.xlsx)
- [Presentation Slides](https://github.com/Shivi2599/Trainity-Internship-Projects/blob/main/Analyzing%20the%20Impact%20of%20Car%20Features%20on%20Price%20and%20Profitability/Analyzing%20the%20Impact%20Of%20Car%20Features%20on%20Price.pptm)














