<h1 align="center">🛒 E-Commerce Analytics Lakehouse</h1>

<p align="center">
End-to-End Data Lakehouse Solution using Databricks, PySpark, Delta Lake & Medallion Architecture
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Databricks-FF3621?logo=databricks&logoColor=white"/>
  <img src="https://img.shields.io/badge/PySpark-E25A1C?logo=apachespark&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-336791?logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Delta%20Lake-00ADD8?logo=databricks&logoColor=white"/>
  <img src="https://img.shields.io/badge/Data%20Lakehouse-4285F4"/>
  <img src="https://img.shields.io/badge/Medallion%20Architecture-Gold"/>
</p>

---

## 🚀 Project Overview

This project demonstrates the design and implementation of an end-to-end **Data Lakehouse** solution on **Databricks** using **PySpark**, **SQL**, and **Delta Lake**.

The solution ingests raw e-commerce datasets into a centralized Data Lake, processes them through the **Medallion Architecture (Bronze → Silver → Gold)**, and creates business-ready analytical datasets for reporting, dashboarding, and AI-powered insights.

The final Gold layer was leveraged to generate business insights using **Databricks Genie AI** and build interactive dashboards for sales, customer, and product analytics.

> [!NOTE]
> This project follows a modern ELT (Extract, Load, Transform) approach commonly used in enterprise Data Lakehouse implementations.

---

## 🏗️ Architecture

```text
Raw CSV Files
      │
      ▼
Data Lake Storage
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
      ├──────────────► Databricks Genie AI
      │
      └──────────────► Interactive Dashboards
```

---

## 🛠️ Tech Stack

| Category | Technologies |
|-----------|-------------|
| Platform | Databricks |
| Processing | PySpark |
| Query Language | SQL |
| Storage Format | Delta Lake |
| Architecture | Data Lakehouse |
| Data Modeling | Fact & Dimension Tables |
| Governance | Unity Catalog |
| Analytics | Databricks Genie AI |
| Visualization | Databricks Dashboards |

---

## 📂 Data Pipeline

### 🥉 Bronze Layer

The Bronze layer stores raw source data exactly as received from the source systems.

#### Activities Performed

- Imported raw CSV datasets
- Created Bronze Delta Tables
- Preserved source-level data
- Maintained schema consistency
- Enabled scalable storage using Delta Lake

#### Bronze Tables

```text
brz_customers
brz_products
brz_brands
brz_category
brz_calendar
brz_order_items
```

---

### 🥈 Silver Layer

The Silver layer focuses on cleansing, standardizing, and validating the data.

#### Activities Performed

- Data cleansing
- Null value handling
- Schema validation
- Data standardization
- Data quality checks
- Business rule implementation
- PySpark transformations

#### Silver Tables

```text
slv_customers
slv_products
slv_brands
slv_category
slv_calendar
```

---

### 🥇 Gold Layer

The Gold layer contains business-ready analytical datasets optimized for reporting and decision-making.

#### Activities Performed

- Dimensional modeling
- Fact table creation
- Dimension table creation
- KPI generation
- Analytical dataset preparation

#### Gold Tables

```text
gld_dim_customers
gld_dim_products
gld_dim_date
gld_fact_order_items
```

---

## 📊 Data Modeling

The project follows a dimensional modeling approach.

### Dimension Tables

- Customer Dimension
- Product Dimension
- Date Dimension

### Fact Tables

- Order Items Fact

This structure enables efficient analytical queries and dashboard reporting.

---

## ⚡ Delta Lake Features

The project utilizes **Delta Lake** to provide:

- ACID Transactions
- Reliable Data Processing
- Schema Enforcement
- Data Consistency
- Scalable Storage
- Optimized Query Performance

> [!TIP]
> Delta Lake enables Data Lake storage to behave like a Data Warehouse while maintaining scalability and flexibility.

---

## 🔄 ETL / ELT Workflow

### Extract

Raw e-commerce CSV datasets were collected from source systems.

### Load

Data was loaded into Bronze Delta Tables within the Data Lakehouse.

### Transform

Data was cleaned, validated, and modeled across Silver and Gold layers using PySpark and SQL.

```text
Extract
   ↓
Load (Bronze)
   ↓
Transform (Silver)
   ↓
Business Modeling (Gold)
   ↓
Analytics & Dashboards
```

---

## 🤖 Databricks Genie AI

Databricks Genie AI was used to perform natural language analytics on curated Gold-layer datasets.

### Example Business Questions

- What are the top 10 products by revenue?
- Which categories generate the highest sales?
- What is the average revenue per customer?
- Which sales channels perform best?
- What are the monthly sales trends?

### Benefits

- Faster insight generation
- Natural language querying
- Reduced dependency on manual SQL analysis



---

## 📈 Dashboard & Analytics

Built interactive dashboards to monitor business performance across multiple dimensions.

### Sales Analytics

- Monthly Revenue Trends
- Revenue Distribution
- Category Performance

### Customer Analytics

- Average Revenue per Customer
- Customer Contribution Analysis
- Channel Performance

### Product Analytics

- Top Products by Revenue
- Brand Performance
- Category Contribution


---

## 💡 Key Business Insights

Some examples of insights generated:

- Top-performing products by revenue
- Best-selling categories
- Customer revenue trends
- Channel-wise performance analysis
- Brand contribution analysis
- Revenue distribution across products

---


## 📁 Repository Structure

```text
ecommerce-lakehouse-project
│
├── notebooks
│   ├── setup_catalog.ipynb
│   ├── 1_dim_bronze.ipynb
│   ├── 2_dim_silver.ipynb
│   ├── 3_dim_gold.ipynb
│   ├── 1_fact_bronze.ipynb
│   ├── 2_fact_silver.ipynb
│   └── 3_fact_gold.ipynb
│
├── screenshots
│   ├── dashboard.png
│   ├── genie_ai.png
│   ├── architecture.png
│   └── catalog_structure.png
│
└── README.md
```

---

## 🎯 Skills Demonstrated

### Data Engineering

- Data Lakehouse Architecture
- Medallion Architecture
- ETL / ELT Pipelines
- Delta Lake
- Data Modeling

### Data Processing

- PySpark
- SQL
- Data Cleansing
- Data Transformation
- Data Validation

### Analytics

- Business Intelligence
- Dashboard Development
- KPI Reporting
- Databricks Genie AI
- Data Visualization

---
