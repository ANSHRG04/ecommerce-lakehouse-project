🛒 E-Commerce Analytics Lakehouse Project
📌 Project Overview

This project demonstrates the design and implementation of an end-to-end Data Lakehouse solution using Databricks, PySpark, SQL, and Delta Lake.

The objective was to ingest raw e-commerce data, transform it through a Medallion Architecture (Bronze → Silver → Gold) pipeline, build business-ready analytical datasets, generate insights using Databricks Genie AI, and create interactive dashboards for business reporting.

🚀 Tech Stack
Databricks
PySpark
SQL
Delta Lake
Unity Catalog
Data Lakehouse Architecture
Medallion Architecture
Databricks Genie AI
Databricks Dashboards
ETL / ELT Pipelines
🏗️ Architecture
Raw CSV Files
       │
       ▼
Data Lake (Volume Storage)
       │
       ▼
Bronze Layer
(Raw Delta Tables)
       │
       ▼
Silver Layer
(Cleaned & Validated Data)
       │
       ▼
Gold Layer
(Business-Ready Analytics Tables)
       │
       ▼
Genie AI + Dashboards
📂 Data Sources

The project ingests raw CSV datasets including:

Customers
Products
Brands
Categories
Calendar/Date
Order Items

These files are stored in the Data Lake and processed through multiple transformation layers.

🥉 Bronze Layer
Objective

Store raw source data in Delta tables without applying business transformations.

Activities
Ingested CSV files into Databricks
Created Bronze Delta Tables
Preserved raw source data
Maintained schema consistency
Bronze Tables
brz_customers
brz_products
brz_brands
brz_category
brz_calendar
brz_order_items
🥈 Silver Layer
Objective

Clean, standardize, and validate the data.

Activities
Data cleansing
Null handling
Schema validation
Data standardization
Data quality checks
Transformation using PySpark and SQL
Silver Tables
slv_customers
slv_products
slv_brands
slv_category
slv_calendar
🥇 Gold Layer
Objective

Create business-ready analytical datasets using dimensional modeling.

Activities
Built dimension tables
Built fact tables
Implemented business logic
Optimized data for reporting and analytics
Gold Tables
gld_dim_customers
gld_dim_products
gld_dim_date
gld_fact_order_items
📊 Data Modeling

The project follows a dimensional model consisting of:

Dimension Tables
Customer Dimension
Product Dimension
Date Dimension
Fact Table
Order Items Fact

This structure enables efficient analytical queries and dashboard reporting.

⚡ Delta Lake Features Used
ACID Transactions
Schema Enforcement
Delta Tables
Optimized Data Storage
Reliable ETL Processing
🔄 ETL / ELT Pipeline
Extract
Imported raw CSV files into the Data Lake.
Load
Loaded raw datasets into Bronze Delta Tables.
Transform
Processed and cleaned data in Silver.
Created analytical datasets in Gold.

This project follows a modern ELT approach commonly used in Lakehouse architectures.

🤖 Databricks Genie AI

Leveraged Databricks Genie AI to perform natural language analytics on curated Gold-layer datasets.

Example Questions
Top 10 Products by Revenue
Revenue Analysis by Category
Customer Revenue Trends
Monthly Sales Performance
Channel-wise Revenue Analysis

Genie AI enabled rapid business insight generation without manually writing SQL queries.

📈 Dashboard & Business Insights

Built interactive dashboards to analyze:

Sales Performance
Monthly Sales Trends
Revenue Distribution
Category-wise Performance
Customer Analytics
Revenue per Customer
Customer Segmentation
Channel Performance
Product Analytics
Top Products by Revenue
Brand-wise Performance
Category Contribution Analysis
