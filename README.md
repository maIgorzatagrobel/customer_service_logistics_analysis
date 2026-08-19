# Customer Service Logistics Analysis

Comparative Analysis of Customer Logistics Service Based on Selected Companies in the Fashion Industry

## Introduction

This dataset was created based on an online survey that I designed and conducted independently as part of my engineering project. The survey was targeted at respondents who had made at least one online purchase from the stores included in the study.

The original company names were anonymized for portfolio purposes.

For portfolio development and improvement, I decided to rebuild the project using a full ETL process in Power Query and present the results in a Power BI dashboard instead of Excel, as it was originally done during my studies.

**Project Goal**

The objective of the project was to compare the logistics customer service performance of two stores, identify the most important criteria for respondents, and determine areas requiring improvement.

## 🎥 Dashboard Demonstration

![Dashboard Demonstration](/Assets/dasboard_overview_gif.mp4.gif "Dashboard Demonstration")

**🔧 Tools used:** Microsoft Excel, Power BI (DAX), Power Query (M)

**⚙️ Power BI Features & Techniques:**

- Visualizations: bar charts, column charts, donut charts, scatter plot, KPI card, line chart
- Interactive Elements: slicers, filters, buttons (home, back etc.), page navigation
- Data Analysis: DAX measures, calculated columns
- Dashboard Design: layers, grouping, selection pane, bookmarks
- Formatting: conditional formatting, customized tooltips and visual interactions

**⚙️ Power QUERY Features & Techniques:**

- Append & Merge Queries
- Data Cleaning & Transformation (Clean & Trim Text, Replace Values)
- Unpivot Columns
- Extract Values from Columns
- Custom Columns
- Conditional Columns
- Data Formatting & Type Conversion
- M Language Editing

# Project Overview

## 1. Data Preparation

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

**Data Cleaning Issue**

During the development of the KPI representing the most important customer satisfaction measure, an inconsistency was identified in the data. The total number of points did not match the expected value, resulting in a difference of 16 points and \*an error of 0.065%.
To identify the incorrect records,a new column calculating the total number of points for each response was created. The data was then filtered to identify records where the total score differed from the expected 100 points. As a result, four incorrect records were identified: indexes 40, 74, 268, and 287, with two records corresponding to each store.

The identified responses were excluded from further analysis and were therefore not taken into account when calculating the final results.

**Data Transformation Examples**

_Text Cleaning (Power Query M)_

![Text Cleaning Using Power Query M](/Images/text_cleaning_m_code.png "Text Cleaning Using Power Query M")

_Standardizing Text Values (Power Query M)_

![Standardizing Text Values Using Power Query M](/Images/standarized_text_values_m_code.png "Standardizing Text Values (Power Query M)")

_Data Type Transformation (Power Query M)_

![Data Type Transformation Using Power Query M](/Images/change_data_type_m_code.png "Data Type Transformation Using Power Query M")

## 2. Dashboard

The dashboard includes five pages:

### 📄 Page 2.1. Home Page

    The first page serves as the main navigation page. It contains four interactive buttons with assigned actions that direct users to the corresponding dashboard pages. When hovering over each button, a preview image of the selected dashboard page is displayed. The page also includes a brief description of the project and its main purpose.

![Home Page](/Images/home_page.png "Home Page")

### 📄 Page 2.2 Executive Summary

    This page presents an overall overview of customer satisfaction, including the performance and importance of individual logistics customer service criteria.

- Three main KPIs present the Customer Satisfaction Index (CSI), overall satisfaction score, and the total number of respondents, providing a concise overview of the survey results.
- Average Satisfaction by Criteria – a bar chart presenting the average customer satisfaction score for each logistics customer service criterion.
- Importance of Criteria – a bar chart showing the importance assigned by respondents to each criterion.

![Executive Summary](/Images/executive_summary_image.png "Executive Summary")

### 📄 Page 2.3. Customer Profile

    The page presents an overview of the respondent profile and demographic characteristics.

- Age Distribution – a column chart presenting the age distribution of the survey respondents.
- Gender Distribution – a donut chart showing the gender breakdown of the respondents.
- Employment Distribution – a donut chart presenting the employment status of the respondents.
- Shopping Method Distribution – a donut chart showing respondents’ preferred shopping method.
- City Size Distribution – a bar chart illustrating the distribution of respondents according to the size of their place of residence.
- Shopping Frequency – a bar chart presenting how frequently respondents shop.

![Customer Profile](/Images/customer_profile_img.png "Customer Profile")

### 📄 Page 2.4. Analysis

    This page presents an in-depth analysis of the survey results, enabling a more detailed assessment of individual criteria and helping to identify key findings and draw specific conclusions.

- Presents and compares the satisfaction scores for the four criteria considered most important by respondents.
- Overall Satisfaction by Store – shows the overall satisfaction level for each of the analyzed stores.
- Overall Satisfaction by Gender – presents differences in overall satisfaction between male and female respondents.
- Overall Satisfaction by City Size – illustrates how customer satisfaction varies depending on the size of the respondent’s place of residence.

![Analysis](/Images/analysis_imge.png "Analysis")

- Satisfaction vs. Importance Analysis – a scatter plot was used to examine the relationship between customers’ satisfaction levels and the importance assigned to individual logistics customer service criteria.

To create a scatter plot, the following steps were applied:

      ⚙️1. Data preparation – the Satisfaction Analysis and Importance Analysis tables were combined to create a dataset containing both satisfaction and importance scores for each respondent and criterion.

      ⚙️2. Unpivoting the data – the Unpivot Columns function in Power Query was used to transform the satisfaction data into a format where each record represents a respondent–criterion combination, making it possible to compare satisfaction scores across individual criteria.

      ⚙️3. Data merging – the tables were merged using Index as the respondent identifier and Criterion as the criterion identifier.

      ⚙️4. Criterion standardization – a helper column, Criterion Merge, was created in the Importance Analysis table to standardize criterion names solely for the purpose of merging the datasets. The original criterion names were preserved.

Final dataset – the resulting Satisfaction Importance Analysis table contained the following fields:

- Index – respondent identifier
- Criterion – logistics customer service criterion
- Satisfaction – satisfaction rating on a 1–5 scale
- Importance – importance rating on a 0–100 scale

The final dataset was then used to calculate and compare the average satisfaction and importance levels for each criterion, allowing areas with high customer importance but relatively low satisfaction to be identified.

![Satisfaction vs. Importance Analysis](/Images/scatter_dashboard.png "Satisfaction vs. Importance Analysis")

### 📄 Page 2.5. Key Insights

The summary of the main survey insights

![Home Page](/Images/key_insights_image.png "Home Page")

## 3. Key Insights

The results of the online survey showed an average Customer Satisfaction Index (CSI) of 83%, with an average rating of 4.12 points across the analyzed logistics customer service criteria.

Store B achieved, on average, 0.09 points higher scores across the four main KPIs than Store A. However, the differences in ratings are relatively small, indicating that both fast fashion companies operate at a similar level and face challenges in the same areas. A relationship between city size and customer satisfaction can nevertheless be observed, namely that customer satisfaction decreases as city size decreases. In the case of both stores, it can also be observed that men are more critical in their assessments, assigning lower average scores than women.

Among the logistics customer service criteria, order completeness received the highest rating and was also identified as one of the most important criteria by the respondents, ranking second in terms of importance. Only delivery time received an importance rating that was 4 percentage points higher, making it the most important criterion for the respondents. Unfortunately, the high importance attributed to delivery time is not reflected in the level of satisfaction, as respondents gave this criterion one of the lower ratings. This indicates that delivery time is an area requiring significant improvement.

Product availability received the lowest rating, while its importance was ranked in the middle of the overall ranking. The analysis of this criterion does not indicate a clear relationship between the low rating and the respondents’ age, gender, or place of residence. However, a considerable proportion of respondents indicated in-store shopping as their preferred shopping method. This may suggest that the issue of product availability is particularly related to e-commerce distribution, which may require further improvement.

Product availability should therefore be subject to a more in-depth analysis in order to determine the underlying causes of such low ratings and identify the source of the problem.

A key element in improving customer service could be the introduction of clearly defined target scores for individual criteria, which would enable their systematic monitoring. For this purpose, benchmarking methods could be used, involving comparisons with competitors or relevant market standards. The SMART method could also be applied to define objectives in a measurable, achievable, relevant, and time-bound manner.

## 4. Repository Structure

![Home Page](/Images/Structure.png "Home Page")
