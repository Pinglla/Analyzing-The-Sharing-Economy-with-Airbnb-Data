# Analyzing The Sharing Economy with Airbnb Data

## Project Overvies

This project examines the impact of COVID-19 on the Airbnb market by analyzing key trends before and after the pandemic (2018–2019 vs. 2020–2021). While price increases are a well-documented effect, our goal was to identify other significant shifts driven by market uncertainty, changing traveler behavior, and the strategies adopted by both hosts and Airbnb to sustain their business. Specifically, we focused on changes in minimum night stay requirements across different locations and host types to understand how they adapted to the evolving landscape. Through data analysis, we explored how these adjustments varied and what they reveal about the transformation of the sharing economy in response to the pandemic.

## Data Source

The dataset was provided by Professor Milan Miric, an Associate Professor of Data Science at USC. It comprises monthly Airbnb listing data for Los Angeles, spanning from March 2018 to January 2021.


## Data cleaning

To ensure the credibility of our analysis, we used Python to clean the dataset by removing columns with missing values. Additionally, since our focus was on locations within Los Angeles, we filtered out listings from other areas to achieve a more accurate and relevant analysis.

## Exploratory Data Analysis

Our analysis aims to address three key questions regarding the increase in minimum night stay requirements set by hosts:

- Does the trend of rising minimum night stays really persist over time?
- Does geographical location influence this trend?
- How does host size impact the changes in this trend?

## Data Analysis

We used Python for data analysis in this project, with the most interesting aspect being the use of Plotly’s geographic scatter plot to visualize changes over time across different locations. This analysis required extracting latitude and longitude data from the dataset, allowing us to effectively examine spatial trends and variations in minimum night stay requirements.

## Findings

1. The minimum night stay requirements increased after the pandemic.
2. We initially hypothesized that listings near airports would experience a greater increase in minimum night stays. We speculated that government regulations may have encouraged hosts to implement longer minimum stay requirements to reduce potential exposure by restricting travelers who may have been affected from interacting with the general population. Additionally, COVID-19 detection typically required at least seven days, and travelers might prefer accommodations near airports upon arrival. However, our geographic scatter plot analysis did not support this assumption.
3. Hosts managing multiple listings on Airbnb were more likely to increase minimum night stay requirements. This is likely a strategic decision to reduce operational costs, such as cleaning and maintenance, in response to decreased guest turnover.

## Limitations

Since our team members were not fully familiar with the geography of Los Angeles, there may be additional factors related to location that could influence minimum night stay requirements. This presents an opportunity for further exploration in future studies, where a deeper understanding of the area's specific characteristics could provide more insights into how geography impacts the trend.
