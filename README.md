# cloud-data-warehouse-etl-pipeline
End-to-end data engineering pipeline using Apache Hop, Oracle Autonomous Database, dimensional modeling, SQL, and Power BI for sales analytics and forecastingI.

# Project Overview

The goal of this project was to build a complete data pipeline for sales analytics.

The solution covers:

- Data ingestion
- Data transformation
- Dimension lookups
- Fact table loading
- Cloud data warehousing
- Star schema modeling
- Business intelligence
- Sales forecasting

## Architecture

The pipeline follows this flow:

Source Data  
↓  
Apache Hop ETL  
↓  
Data Cleaning & Transformation  
↓  
Dimension Lookups  
↓  
Oracle Autonomous Database  
↓  
Star Schema  
↓  
Power BI  
↓  
Analytics & Forecasting

![ETL Pipeline](architecture/apache-hop-etl-pipeline.jpg)

## ETL Pipeline

The Apache Hop pipeline was built to process and prepare sales data before loading it into the warehouse.

The pipeline performs:

1. Source data ingestion
2. Data transformation
3. Customer dimension lookup
4. Product dimension lookup
5. Dimension key mapping
6. Record filtering
7. Fact table loading
8. Pipeline execution validation

![Pipeline Execution](architecture/apache-hop-pipeline-execution.jpg)

## Data Warehouse Design

The warehouse follows a star-schema design.

The central fact table is:

- FACT_SALES

The supporting dimension tables include:

- DIM_PRODUCT
- DIM_CUSTOMER
- DIM_DATE

The fact table stores measures such as sales price and quantity, while the dimension tables support analysis across products, customers, and time.

![Star Schema Data Model](architecture/star-schema-data-model.png)

## Power BI Dashboard

The warehouse was integrated with Microsoft Power BI to create an interactive sales analytics dashboard.

The dashboard includes:

- Total sales
- Units sold
- Number of transactions
- Sales by category
- Quarterly sales
- Brand performance
- Yearly sales trends
- Sales forecasting

![Power BI Sales Dashboard](dashboard/powerbi-sales-dashboard.png)

## Key Results

- Total Sales: $15.76K
- Units Sold: 3.01K
- Sales Transactions: 1,000
- Wheat contributed approximately 40% of total sales
- Dairy contributed approximately 39%
- Candy contributed approximately 22%

The dashboard also uses historical sales data to generate forecasts for future performance.

## Tech Stack

- Apache Hop
- Oracle Autonomous Database
- SQL
- Microsoft Power BI
- ETL
- Data Warehousing
- Dimensional Modeling
- Star Schema
- Data Visualization
- Forecasting

## Repository Structure

```text
cloud-data-warehouse-etl-pipeline/
│
├── README.md
│
├── architecture/
│   ├── apache-hop-etl-pipeline.jpg
│   ├── apache-hop-pipeline-execution.jpg
│   └── star-schema-data-model.png
│
├── dashboard/
│   ├── powerbi-sales-dashboard.png
│   └── sales-dashboard.pbix
│
└── etl/
    └── Apache Hop pipeline files
