# SCT_DS_04

## Project Title

Road Accident Data Analysis using Python

## Objective

The main objective of this project is to analyze road accident data and identify accident patterns based on:

Weather conditions
Road surface conditions
Time of the day
Accident severity
This analysis helps to understand the major factors influencing road accidents.

## Dataset Used

Dataset Name: RTA Dataset
File Format: CSV
Description:
The dataset contains information about road accidents including date, time, weather conditions, road surface conditions, and accident severity.

## Tools & Libraries Used

Google Colab – for running Python code
Python Libraries:
Pandas – data loading, cleaning, and analysis
Matplotlib – data visualization

 ## Steps Followed in the Project
 
Step 1: Data Loading
The dataset was uploaded to Google Colab and loaded using Pandas.

Python
import pandas as pd
df = pd.read_csv("RTA Dataset.csv")

Step 2: Data Understanding
Checked dataset structure
Viewed column names
Identified missing values

Python
df.info()
df.columns

Step 3: Data Cleaning
Removed duplicate records
Handled missing values
Cleaned column names
Converted time into hourly format
 
Python 
df = df.dropna()
df['Hour'] = pd.to_datetime(df['Time'], errors='coerce').dt.hour

Step 4: Data Analysis
Accident patterns were analyzed based on:
Weather conditions
Road surface conditions
Time of the day
Accident severity

Python
df['Weather_Conditions'].value_counts()
df['Road_surface_conditions'].value_counts()
df['Hour'].value_counts()

Step 5: Data Visualization
Bar charts were used to visualize accident patterns clearly.
Accidents by Weather
Accidents by Road Surface
Accidents by Time of Day
Accidents by Severity

Example:
Python
df['Weather_Conditions'].value_counts().plot(kind='bar')

## Results & Findings

Most accidents occur during peak traffic hours.
Dry and wet road conditions show higher accident counts.
Normal weather conditions have more accidents compared to extreme weather.
Accident severity analysis helps understand the impact level.

## Conclusion
This project successfully analyzed road accident data and identified key factors affecting accidents. The use of bar charts made it easier to compare accident patterns. This analysis can help authorities and researchers improve road safety measures.
