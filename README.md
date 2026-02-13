# SQL Project: Global Company Layoffs Analysis
# Project Overview
This project involves a comprehensive two-stage process: Data Cleaning and Exploratory Data Analysis (EDA) using a dataset of global company layoffs from 2020 to 2023. The goal was to take a messy, raw dataset and transform it into a clean, queryable format to uncover high-level business insights regarding the economic landscape over a three-year period.

# Stage 1: Data Cleaning
Remove Duplicates: Utilized CTEs and the ROW_NUMBER() window function partitioned across all columns to identify and delete redundant records.

Standardize the Data: Cleaned inconsistent entries by trimming whitespace from company names, standardizing industry labels (e.g., merging various "Crypto" variations), and converting text-based date strings into functional DATE formats.

Null Values or Blank Values: Addressed missing data by populating null industry fields using a self-join on existing company data and identifying records with insufficient quantitative information for analysis.

Remove Any Columns: Streamlined the final dataset by dropping auxiliary columns used during the cleaning process (such as row_num) to optimize the table for the next phase.

# Stage 2: Exploratory Data Analysis (EDA)
With the cleaned data, I performed a deep dive to identify trends and patterns:

Aggregate Analysis: Calculated the total layoffs by company, industry, and country to identify the sectors most impacted by economic shifts.

Time-Series Insights: Analyzed layoff trends by year and month, uncovering peak periods of workforce reductions.

Advanced Calculations: Developed Rolling Totals and Ranking systems using complex window functions to visualize the progression of layoffs and identify the top 5 companies with the most layoffs for each year.

# Tools Used
SQL Dialect: MySQL

Environment: MySQL Workbench

Concepts: CTEs, Window Functions (PARTITION BY, DENSE_RANK), Joins, and Data Transformation

# Key Insights
The Consumer and Retail industries experienced the highest volume of layoffs within the dataset timeframe.

Layoffs peaked significantly in 2022, with a high volume of activity continuing into early 2023.

Major tech giants (e.g., Google, Amazon, Meta) dominated the largest single-day layoff events.
