# World Layoffs SQL Project (SQL Server)

## Overview

This project demonstrates a complete data analyst workflow using SQL Server: importing raw data, cleaning the dataset, and performing exploratory data analysis (EDA).

The original layoffs dataset contains duplicate records, inconsistent text values, and missing information. The data was cleaned and standardized before analysis to ensure reliable insights.

---

## Project Structure

```
data/
  layoffs.csv                # Raw dataset

sql/
  data_cleaning.sql          # Data cleaning and preparation
  eda.sql                    # Exploratory data analysis queries

README.md
```

---

## Data Cleaning (data_cleaning.sql)

The dataset was transformed into an analysis‑ready table using the following steps:

### Create Staging Table

* Preserved the raw dataset
* Prevented accidental data loss

### Remove Duplicates

* Used `ROW_NUMBER()` window function
* Kept only the first occurrence of each record

### Standardize Data

* Unified country naming (e.g., `United States.` → `United States`)
* Merged industry variations into `Crypto`
* Fixed inconsistent text formatting

### Handle Missing Values

* Filled missing industry values using matching company records
* Preserved meaningful NULL values for accuracy

### Remove Unusable Data

* Dropped rows and columns without analytical value

**Output:** Cleaned dataset stored in `layoffs_staging2`

---

## Exploratory Data Analysis (eda.sql)

After cleaning, SQL queries were used to analyze layoff patterns.

### Analysis Performed

* Largest layoff events
* Companies with highest total layoffs
* Layoffs by country and location
* Layoffs by industry and company stage
* Yearly and monthly layoff trends
* Company shutdown cases (100% layoffs)
* Top companies per year using ranking functions
* Rolling cumulative layoffs over time

### Techniques Used

* Aggregations (`SUM`, `MAX`, `MIN`)
* `GROUP BY` analysis
* Window functions (`DENSE_RANK`, running totals)
* Time‑series analysis

---

## Workflow

1. Import CSV into SQL Server
2. Clean and standardize data (`data_cleaning.sql`)
3. Analyze trends (`eda.sql`)

---

## Skills Demonstrated

* SQL Data Cleaning
* Data Preparation
* Handling Missing Data
* Data Standardization
* Window Functions
* Exploratory Data Analysis
* Analytical Thinking

---

## Result

The dataset was transformed from raw, inconsistent data into a structured analytical dataset ready for business insight and reporting.
