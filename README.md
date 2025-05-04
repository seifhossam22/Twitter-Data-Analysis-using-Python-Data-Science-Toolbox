# Twitter Data Analysis using Python

## Overview
This project performs comprehensive analysis and cleaning of Twitter data using Python and Pandas. The analysis covers data import, cleaning, function writing, iterators, list comprehensions, lambda functions, variable scoping, and exploratory data analysis. The goal is to extract insights about trending keywords and engagement metrics.

## Project Files

- twitter_analysis.py - Main Python script containing all data processing, analysis, and plotting code.
- README.txt - Project overview and instructions (this file).
- report.pdf or report.md - Summary report of findings and insights (to be generated after running the analysis).

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib

Install dependencies via:
pip install pandas numpy matplotlib

## Dataset

Assumed columns:
- Tweet_Date: Date (and time) of the tweet
- Tweet_Text: Content of the tweet
- Retweet_Count: Number of retweets
- Like_Count: Number of likes
- Hashtags: Hashtags used in the tweet

## Workflow Summary

1. Data Importing & Cleaning

- Import dataset using pandas.
- Convert Tweet_Date to datetime.
- Remove nulls from Retweet_Count and Like_Count.
- Strip whitespace from Tweet_Text.
- Convert Hashtags to lowercase.
- Cap outliers in Retweet_Count and Like_Count using quantile-based clipping.
- Convert counts to integer type.
- Sort tweets by date.

2. Function Writing

- filter_tweets(df, keyword):  
  Filters tweets containing a specific keyword (case-insensitive). Raises an error if the DataFrame is empty.

- avg_retweets_and_likes_count_by_range(df, start_date, end_date):  
  Calculates and returns average retweet and like counts for a given date range. Handles errors and returns multiple values.

- avg_retweets_or_likes_count_by_range(df, column, start_date, end_date):  
  Calculates average for a specified column within a date range. Handles missing columns and date errors.

3. Iterators and List Comprehensions

- count_keyword(df, keyword):  
  Iterates over tweet texts and counts keyword occurrences.

- List comprehension:  
  Creates a list of hashtags from tweet texts.

4. Lambda Functions and Scoping

- extract_year:  
  Lambda function to extract year from Tweet_Date.

- add_keyword_column(df):  
  Adds a new column extracting part of the tweet text as a keyword.

5. Exploratory Data Analysis

- Plots histograms of keyword occurrences for the whole year and for specific months.
- Uses custom functions to filter and analyze tweets by date range.

## How to Run

1. Place your Twitter dataset (CSV) in the project directory.
2. Update the file path in the script if necessary.
3. Run the script:
   python twitter_analysis.py
4. Review the output and generated plots.
5. Check the report for a summary of findings.

## Key Features

- Robust data cleaning and outlier handling.
- Modular, reusable functions with error handling.
- Efficient keyword analysis using iterators and list comprehensions.
- Exploratory visualizations for trend analysis.

## Author

Seif Hossam Eldeen
