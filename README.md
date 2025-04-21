# Data-Analysis-Internship---Elevate-labs
# Netflix Movies and TV Shows – Data Cleaning Project

## Dataset Overview
This project involves cleaning and preprocessing the **Netflix Movies and TV Shows** dataset from Kaggle. The dataset contains metadata like title, director, cast, country, date added, release year, rating, and more.

## Tools Used
- Python
- Pandas
---

## Cleaning Steps Performed

### 1. Data Exploration
- Used `df.info()` to inspect column data types and non-null counts.
- Used `df.describe(include='all')` to view summary statistics of all columns.
- Used `df.isnull().sum()` to identify missing values.

### 2. Missing Value Treatment
- Dropped rows with missing `title`.
- Filled missing values in:
  - `director` and `cast` → `'Not Available'`
  - `country` and `rating` → Most frequent value (mode)

### 3. Duplicate Handling
- Removed all duplicate rows using `df.drop_duplicates()`.

### 4. Standardization of Text Data
- Converted all country names to title case using `str.title()` and removed extra spaces using `str.strip()`.
- Converted all entries in the `type` column to lowercase using `str.lower()`.

### 5. Date Format Correction
- Converted `date_added` column to datetime format using `pd.to_datetime()` with error handling.

### 6. Column Name Formatting
- Renamed all column headers to lowercase with underscores using `str.lower()` and `str.replace()`.

### 7. Data Type Fixes
- Ensured `release_year` is of integer type.

---

## Output Summary
The cleaned dataset:
- Has consistent and properly formatted columns.
- Contains no duplicates.
- Has all missing values handled appropriately.
- Is ready for analysis, visualization, or model building.

---

## Key Learning
This task improved understanding of:
- Detecting and handling missing values
- Removing duplicates
- Standardizing categorical data
- Converting and formatting date/time fields
- Data quality checks using Pandas

---

## Source
Dataset from [Kaggle – Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)

