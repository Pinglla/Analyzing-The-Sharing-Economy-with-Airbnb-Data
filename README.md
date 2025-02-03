# Analyzing The Sharing Economy with Airbnb Data

[Project PowerPoint](Analyzing_The_Sharing_Economy_with_Airbnb_Data.pdf)

## Project Overvies

This project examines the impact of COVID-19 on the Airbnb market by analyzing key trends before and after the pandemic (2018–2019 vs. 2020–2021). While price increases are a well-documented effect, our goal was to identify other significant shifts driven by market uncertainty, changing traveler behavior, and the strategies adopted by both hosts and Airbnb to sustain their business. Specifically, we focused on changes in minimum night stay requirements across different locations and host types to understand how they adapted to the evolving landscape. Through data analysis, we explored how these adjustments varied and what they reveal about the transformation of the sharing economy in response to the pandemic.

## Data Source

The dataset for this project was provided by Professor Milan Miric, an Associate Professor of Data Science at USC. It consists of monthly Airbnb listing data for Los Angeles, covering the period from March 2018 to January 2021. The dataset includes 1,603,477 records across 109 fields, offering detailed information on each listing, such as the property name, space, number of reviews, descriptions, minimum night stay, and more. 

## Tools

- Python – Used for data cleaning, analysis, and visualization.
- PowerPoint – Used for creating reports and presenting findings.

## Data cleaning

During the initial data preparation phase, we performed the following tasks:
1. Handling Missing Values – Some records contained missing values, which could impact the accuracy of our analysis. We addressed these gaps to ensure data integrity.
2. Filtering Data – Since our focus was on locations within Los Angeles, we filtered out listings from other areas to achieve a more accurate and relevant analysis.

## Exploratory Data Analysis

Our analysis focuses on three key questions related to the increase in minimum night stay requirements set by Airbnb hosts:

- Trend Analysis - Does the trend of rising minimum night stays really persist over time?
- Geographical Influence – Does geographical location influence this trend?
- Host Size Impact - How does host size impact the changes in this trend?

## Data Analysis

We used Python for data analysis in this project, with the most interesting aspect being the use of Plotly’s geographic scatter plot to visualize changes over time across different locations. This analysis required extracting latitude and longitude data from the dataset, allowing us to effectively examine spatial trends and variations in minimum night stay requirements.

```
import plotly.express as px
import pandas as pd

fig = px.scatter_geo(data_merge_2018, lat='latitude', lon='longitude', color='minimum_nights',
                     hover_name='neighbourhood', size='minimum_nights',
                     title='2018 Mean minimum nights in LA', width=800, height=500)
fig.show()
```

## Findings

1. The minimum night stay requirements increased after the pandemic.
2. We initially hypothesized that listings near airports would experience a greater increase in minimum night stays. We speculated that government regulations may have encouraged hosts to implement longer minimum stay requirements to reduce potential exposure by restricting travelers who may have been affected from interacting with the general population. Additionally, COVID-19 detection typically required at least seven days, and travelers might prefer accommodations near airports upon arrival. However, our geographic scatter plot analysis did not support this assumption.
3. Hosts managing multiple listings on Airbnb were more likely to increase minimum night stay requirements. This is likely a strategic decision to reduce operational costs, such as cleaning and maintenance, in response to decreased guest turnover.

## Limitations

Since our team members were not fully familiar with the geography of Los Angeles, there may be additional factors related to location that could influence minimum night stay requirements. This presents an opportunity for further exploration in future studies, where a deeper understanding of the area's specific characteristics could provide more insights into how geography impacts the trend.
