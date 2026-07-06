# Customer Service Logistics Analysis

Comparative Analysis of Customer Logistics Service Based on Selected Companies in the Fashion Industry

## Introduction

This dataset was created based on an online survey that I designed and conducted independently as part of my engineering project.

The original company names were anonymized for portfolio purposes.

For portfolio development and improvement, I decided to rebuild the project using a full ETL process in Power Query and present the results in a Power BI dashboard instead of Excel, as it was originally done during my studies.

The project is currently in progress. At this stage, the ETL process has been completed.

## Data Preparation

**Tools used:** Microsoft Excel, Power BI, Power Query (M)

- Imported raw data from XLSX files into Power BI
- Promoted the first row to column headers
- Added a custom column to identify data source (store/source)
- Appended queries to combine multiple datasets into a single table
- Added an index column for data tracking and structure
- Removed blank values and invalid records
- Renamed columns for better readability and consistency
- Performed text cleaning using Power Query (M language)
- Standardized text values using Power Query (M language)
- Changed data types to ensure data consistency and accuracy

## Data Transformation Examples

### Text Cleaning (Power Query M)

![Text Cleaning Using Power Query M](/Images/text_cleaning_m_code.png "Text Cleaning Using Power Query M")

### Standardizing Text Values (Power Query M)

![Standardizing Text Values Using Power Query M](/Images/standarized_text_values_m_code.png "Standardizing Text Values (Power Query M)")

### Data Type Transformation (Power Query M)

![Data Type Transformation Using Power Query M](/Images/change_data_type_m_code.png "Data Type Transformation Using Power Query M")
