# Amazon-End-to-End-Analysis-Pipeline

This project implements an end-to-end ETL (Extract, Transform, Load) data flow for Amazon's mobile sales order data from three regions (India, USA, and France) using Snowpark and Snowflake. The pipeline efficiently handles data loading, curation, and dimensional modeling to facilitate analytical querying and reporting.

# Technical Stack: 
SQL, Snowflake, Snowpark Python API, AWS S3 bucket & IAM.

# Project Overview:

The ETL pipeline consists of the following key steps:
Data Loading: Mobile sales data from three regions is loaded into Snowflake's internal stage.
Data Curation: Using Snowpark Data Frame API, the data is transformed and cleansed.
Dimensional Modeling: The curated data is organized into a star schema for efficient analysis.

# Data Flow Diagram:

![sales_analysis drawio](https://github.com/user-attachments/assets/1607c291-aaec-40a6-bb9f-d1c279dbdc89)


# Key Components:

1. Snowflake Setup
Creation of virtual warehouse and user account
Database and schema object creation

2. Data Loading
Internal stage creation in the source schema
Loading data to internal stage using Snowpark File API

3. Data Curation
Creation of file format objects
Loading data from internal stage to source tables
Transformation of source data to curated layer

5. Dimensional Modeling
Creation of dimension tables (Region, Product, Promo Code, Customer, Payment, Date)
Creation of fact table (Sales)

6. Snowpark Python Scripts
Scripts for loading data from source to curated layer
Scripts for populating dimension and fact tables

# Key Features:

Handling of multiple data formats (CSV, Parquet, JSON)
Currency conversion for global sales analysis
De-duplication of data
Dimensional modeling for efficient querying

# Future Enhancements:

Implement incremental loading for efficiency
Add data quality checks and error handling
Develop visualization layer for sales analytics

