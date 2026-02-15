# Layoffs Data Cleaning (SQL Server)

## Overview
This project demonstrates a real-world SQL data cleaning workflow.
The raw layoffs dataset contains duplicate rows, inconsistent text values, and missing data that must be cleaned before reliable analysis.

## Dataset Issues Found
- Duplicate records
- Inconsistent country naming (e.g., `United States` vs `United States.`)
- Multiple variations of industry names (Crypto variations)
- Missing industry values
- Unusable rows and columns

## Cleaning Process

### Create Staging Table
A staging table was created to preserve the original dataset.

### Remove Duplicates
Used `ROW_NUMBER()` to keep only the first occurrence of each record.

### Standardize Data
- Unified country names
- Standardized industry categories to `Crypto`
- Fixed inconsistent text formatting

### Handle Missing Values
- Filled missing industry values using matching company names
- Kept meaningful NULL values for analysis accuracy

### Remove Unusable Data
Dropped rows and columns with no analytical value.

## Skills Demonstrated
- SQL Data Cleaning
- Window Functions
- Data Standardization
- Handling Missing Data
- Data Preparation

## Result
The dataset is now clean, consistent, and ready for analysis.
