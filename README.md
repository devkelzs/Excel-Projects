# Automated Sales Reporting and Business Intelligence Dashboard Using Microsoft Excel

## Project Overview

This project demonstrates how Microsoft Excel can transform raw retail sales data into a structured, refreshable business intelligence reporting solution.

The solution combines multiple CSV files, cleans and validates sales records using Power Query, calculates key performance indicators (KPIs), and presents sales performance through an interactive-style dashboard built with Excel charts and summary tables.

The dashboard helps business stakeholders evaluate revenue performance, identify top-performing products, compare regional sales, review sales representative performance, and monitor data quality.

## Business Objectives

- Automate the consolidation of sales data from multiple CSV files.
- Improve data quality through validation, standardization, and duplicate removal.
- Calculate key sales performance indicators.
- Identify top-performing products and sales representatives.
- Compare revenue across geographical regions.
- Analyze monthly revenue trends.
- Build a refreshable reporting workflow that reduces repetitive manual work.

## Tools and Technologies

- **Microsoft Excel:** Dashboard development, reporting, and data presentation.
- **Power Query:** Data import, transformation, cleaning, validation, and consolidation.
- **Excel Tables:** Structured storage of cleaned records and analytical outputs.
- **Excel Charts:** Monthly trends, product comparisons, regional performance, representative performance, and data quality reporting.
- **CSV:** Source data format.

## Dataset Overview

The project uses three sample retail sales CSV files containing a combined total of 3,018 rows, including headers.

After combining the files, the dataset contained 3,000 distinct sales records following the removal of 18 exact duplicate records.

### Data Fields

The source data contains ten fields:

| Field | Description |
|---|---|
| Order ID | Sales transaction identifier |
| Order Date | Date of the transaction |
| Product | Product sold |
| Product Category | Product classification |
| Quantity | Number of units sold |
| Unit Price | Price per unit |
| Region | Sales region |
| Sales Representative | Representative responsible for the sale |
| Customer ID | Customer identifier |
| Payment Method | Payment method used |

The CSV filenames reference Q1, Q2, and Q3, but the records span January through December 2025.

## Data Cleaning and Transformation

Power Query was used to build a repeatable data preparation workflow.

### 1. Data Consolidation
- Imported multiple CSV files from a folder.
- Combined the files into one dataset.
- Standardized column headers and data types.

### 2. Duplicate Detection and Removal
- Investigated duplicate records using the original source columns.
- Identified 18 additional copies of existing records.
- Removed exact duplicates while retaining 3,000 distinct records.

### 3. Data Quality Validation
Created quality indicators to identify missing, invalid, and incomplete information.

The validation rules covered:

- Missing and invalid order dates.
- Missing and non-positive quantities.
- Missing and non-positive unit prices.
- Missing customer identifiers.
- Incomplete records.
- Sales records requiring further review.

### 4. Standardization
- Trimmed unnecessary spaces from product and region values.
- Standardized capitalization for product and region names.
- Preserved records requiring review instead of silently deleting them.

### 5. Valid Revenue Calculation
Revenue was calculated as quantity multiplied by unit price for records that passed the sales validity checks.

Records failing the required checks were excluded from valid sales revenue calculations but retained for data quality reporting.

## Key Performance Indicators

The completed dashboard reports the following metrics:

| KPI | Result |
|---|---:|
| Total valid sales revenue | 463,682.94 |
| Valid sales records | 2,943 |
| Average revenue per valid sales record | 157.55 |
| Valid sales rate | 98.1% |
| Total distinct sales records | 3,000 |
| Records requiring review | 57 |

*Note: The average revenue metric represents revenue per valid sales record, not necessarily average order value. Currency was not explicitly specified in the source dataset.*

## Key Business Insights

### 1. Monthly Revenue Performance

December recorded the highest monthly valid revenue at **59,293.67**, while January recorded the lowest at **26,545.16**.

This pattern provides a starting point for investigating seasonal demand, holiday purchasing, and potential year-end sales opportunities.

### 2. Product Performance

The 27-Inch Monitor was the highest-revenue product, generating **106,938.87**. Office Chair followed with **92,299.35**.

Together, these two products contributed approximately **43.0%** of total valid sales revenue, highlighting their importance to overall performance.

### 3. Regional Performance

Central was the highest-revenue named region at **94,736.21**, while West was the lowest at **89,290.73**.

Revenue across the five named regions was relatively close, suggesting that sales were distributed fairly evenly geographically.

An additional **661.99** in valid revenue was associated with records without a region value. These records were retained as unassigned rather than being attributed to an unsupported region.

### 4. Sales Representative Performance

Amara N. generated the highest valid revenue at **73,162.12**, followed by David M. at **71,804.28**.

The results provide a basis for comparing performance and investigating differences in customer portfolios, product mix, and sales opportunities.

### 5. Data Quality

The consolidated dataset contained 3,000 distinct records. Of these, 2,943 passed the sales validity checks, while 57 required review.

The data quality assessment identified missing dates, invalid dates, missing and invalid quantities, missing and invalid prices, missing customer identifiers, and incomplete records.

These findings demonstrate why data validation is essential before reporting business performance.

## Dashboard Features

The Excel dashboard includes:

- KPI cards for revenue, valid sales records, average revenue per valid record, and valid sales rate.
- Monthly sales revenue trend for 2025.
- Top 10 products by revenue.
- Sales revenue by region.
- Sales revenue by representative.
- Sales data quality overview.

The dashboard combines summary metrics with visual analysis to support faster interpretation of sales performance.

## How to Refresh the Report

The workbook uses Power Query to consolidate and transform source files.

1. Open `Sales_Reporting_Dashboard.xlsx` in Excel.
2. Ensure the source CSV files remain in the configured input folder.
3. To include additional files, place compatible CSV files in the exact folder referenced by the Power Query folder source.
4. Open the workbook and select **Data → Refresh All**.
5. Wait for the queries to finish refreshing.
6. Verify that the cleaned data, KPI summaries, analytical tables, and charts reflect the refreshed results.

New CSV files should follow the expected column structure and data types. Test the workflow with a new sample file before relying on it for recurring business reporting.

## Project Structure

```text
Automated-Excel-Sales-Reporting/
├── data/
├── sample_input_files/
│   ├── Retail_Sales_Q1_2025.csv
│   ├── Retail_Sales_Q2_2025.csv
│   └── Retail_Sales_Q3_2025.csv
├── screenshots/
├── Sales_Reporting_Dashboard.xlsx
└── README.md
```

The folders support source data management, report delivery, screenshots, and project documentation. Keep the original input files separate from generated outputs.

## Skills Demonstrated

- Excel data analysis and reporting.
- Power Query ETL workflows.
- Data cleaning and standardization.
- Duplicate detection and removal.
- Data quality assessment.
- KPI development.
- Business performance analysis.
- Dashboard and chart design.
- Repeatable data refresh workflows.
- Translating analytical results into business insights.

## Limitations and Future Improvements

Potential improvements include:

- Adding interactive slicers connected to PivotTables and PivotCharts.
- Introducing category-level sales analysis.
- Comparing actual performance against sales targets.
- Adding profit and margin analysis if cost data becomes available.
- Improving automatic handling of newly added source files.
- Adding automated checks for unexpected columns and data types.
- Expanding the dashboard with year-over-year comparisons when additional years are available.


