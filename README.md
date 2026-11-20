# SQL Data Warehouse and Analytics Project

## Project Overview
This project demonstrates the development of an end-to-end data warehouse using Microsoft SQL Server. It integrates CRM and ERP data provided in CSV files, transforms and cleans the data, and organizes it into a structured data warehouse using the Medallion Architecture.

The project also includes exploratory data analysis (EDA) and advanced SQL analytics to generate business insights.

## Architecture
The data warehouse follows the Medallion Architecture:

- **Bronze Layer:** Stores raw data loaded from CRM and ERP CSV files.
- **Silver Layer:** Cleans, standardizes, and transforms the raw data.
- **Gold Layer:** Provides business-ready views organized into a Star Schema.

## Repository Structure

```text
sql-data-warehouse-and-analytics/
│
├── datasets/
│   ├── source_crm/
│   └── source_erp/
│
├── warehouse/
│   ├── documents/
│   ├── scripts/
│   │   ├── bronze/
│   │   ├── silver/
│   │   └── gold/
│   └── tests/
│
├── analytics/
│   ├── eda/
│   └── advanced_analytics/
│
└── README.md
```

## Data Warehouse Components

### 1. Bronze Layer
- Loads raw CRM and ERP data from CSV files.
- Stores source data in tables without major transformations.

### 2. Silver Layer
- Performs data cleansing and standardization.
- Handles duplicates, unwanted spaces, NULL values, and invalid dates.
- Applies transformations to improve data consistency.

### 3. Gold Layer
- Creates business-ready SQL views.
- Implements a Star Schema consisting of:
  - `gold.dim_customers`
  - `gold.dim_products`
  - `gold.fact_sales`

## Data Quality Checks
SQL scripts are included to validate the Silver and Gold layers, covering:
- Duplicate and NULL key checks.
- Data standardization and consistency.
- Date validation.
- Sales calculation consistency.
- Referential integrity between fact and dimension tables.

## Analytics

### Exploratory Data Analysis (EDA)
The EDA scripts cover:
- Database exploration
- Dimensional exploration
- Date range exploration
- Measure exploration
- Magnitude analysis
- Ranking analysis

### Advanced Analytics
The advanced analytics scripts cover:
- Change-over-time analysis
- Cumulative analysis
- Performance analysis
- Part-to-whole analysis
- Customer segmentation
- Product reporting

## Tools and Technologies
- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- T-SQL
- CSV datasets
- GitHub
