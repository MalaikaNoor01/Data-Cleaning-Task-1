# Data Cleaning and Preprocessing Project

## Project Overview
This repository contains the complete implementation for Task 1: Data Cleaning and Preprocessing. The objective of this project is to clean, standardize, and prepare a raw dataset for downstream data analysis.

## Dataset Details
- Dataset Name: Customer Personality Analysis (marketing_campaign.csv)
- Primary Tool Used: Python (Pandas framework)

---

## Data Cleaning Steps Executed

1. Handling Duplicate Records
   -checked for duplicate rows
   - Dropped duplicate records removed duplicate rows to clean data to maintain data integrity.

2. Standardizing Column Headers
   - Stripped leading and trailing whitespaces from header names.
   - Converted all column names to lowercase format, replacing spaces with underscores (_).

3. Handling Missing Values
   - Identified missing entries in the income column found missing values in income column
   - Imputed missing numerical values using the median statistic to avoid bias from outliers.

4. Data Type and Date Formatting
   - Standardized inconsistent date string formats in dt_customer column using pd.to_datetime().
   - Formatted all dates to YYYY-MM-DD.

5. Data Quality Verification
   - Verified that no missing values or duplicate rows remain in the final cleaned dataset.

---

## Technical Q&A / Conceptual Questions

1. What are missing values and how do you handle them?
Missing values represent unobserved or unrecorded data points in a dataset. They are handled either by deletion (dropna()) when missingness is low, or by imputation (fillna()) using mean, median, or mode.

2. How do you treat duplicate records?
Duplicate records are identified using duplicated() and removed using drop_duplicates() to prevent skewed analysis and data inflation.

3. What is the difference between dropna() and fillna()?
dropna() removes rows or columns containing missing values, whereas fillna() replaces missing values with a specified default value or statistic.

4. What is outlier treatment and why is it important?
Outlier treatment involves identifying and managing extreme values that deviate significantly from the rest of the data. It is important because outliers can distort statistical analysis and machine learning model metrics.

5. Explain the process of standardizing data.
Data standardization involves bringing data into a common format or scale, such as converting text strings to uniform lowercase, formatting dates consistently, or scaling numerical features.

6. How do you handle inconsistent data formats?
Inconsistent formats are handled by applying transformation functions, such as converting varying date strings into standardized datetime objects using pandas to_datetime().

7. What are common data cleaning challenges?
Common challenges include handling high percentages of missing data, dealing with hidden missing values (like empty strings or '?'), mixed data types in a single column, and resolving formatting inconsistencies.

8. How can you check data quality?
Data quality is verified by checking summary statistics (describe()), counting missing values (isnull().sum()), checking for duplicates (duplicated().sum()), and verifying column data types (info()).
