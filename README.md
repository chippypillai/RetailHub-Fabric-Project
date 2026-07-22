# 🛒 RetailHub – End-to-End Microsoft Fabric Data Engineering Project

> An enterprise-style Data Engineering solution built using Microsoft Fabric, implementing Medallion Architecture, Delta Lake, PySpark, Fabric Pipelines, Semantic Models and Power BI.

---

# Project Overview

RetailHub is an end-to-end Data Engineering project built using **Microsoft Fabric** to simulate a real-world retail analytics platform.

The project demonstrates how raw retail transaction data can be ingested, transformed, validated and modelled into business-ready datasets using a modern **Medallion Architecture (Bronze → Silver → Gold)**.

The solution incorporates production-inspired engineering practices including incremental loading, Delta Lake storage, data quality validation, pipeline orchestration and interactive business reporting.

---

# Business Problem

Retail organisations process thousands of sales transactions every day.

Raw transactional data frequently contains:

- Missing customer information
- Cancelled invoices
- Duplicate transactions
- Invalid quantities
- Zero-priced products
- Inconsistent data formats

Without proper cleansing and transformation, these issues result in inaccurate reporting and poor business decisions.

RetailHub demonstrates how Microsoft Fabric can transform raw retail data into trusted, analytics-ready datasets.

---

# Solution Architecture

```
                      Online Retail Dataset
                               │
                               ▼
                    Bronze Layer (Raw Delta)
             Incremental Loading + Raw Storage
                               │
                               ▼
               Silver Layer (Validated Delta)
      Data Cleaning • Business Rules • Data Quality
                               │
                               ▼
              Gold Layer (Business Data Model)
         KPIs • Customer Analytics • Sales Analytics
                               │
                               ▼
                  Microsoft Fabric Pipeline
                               │
                               ▼
                 Direct Lake Semantic Model
                               │
                               ▼
                 Power BI Executive Dashboard
```

---

# Technology Stack

| Technology | Purpose |
|------------|---------|
| Microsoft Fabric | End-to-End Data Platform |
| OneLake | Unified Storage |
| Lakehouse | Central Data Repository |
| Delta Lake | ACID Data Storage |
| PySpark | Data Transformation |
| Spark SQL | Analytics & Validation |
| Fabric Pipelines | Workflow Orchestration |
| Semantic Model | Reporting Layer |
| Power BI | Executive Dashboard |

---

# Dataset

**Dataset:** Online Retail Dataset (UCI Machine Learning Repository)

The dataset contains transactional sales records including:

- Invoice Number
- Product Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

---

# Medallion Architecture

## 🥉 Bronze Layer

### Purpose

- Load raw retail transactions
- Store source data as Delta Tables
- Perform incremental loading
- Preserve historical raw records

### Output

```
bronze_sales
```

---

## 🥈 Silver Layer

### Purpose

Transform raw data into trusted analytical datasets.

### Data Quality Rules

Implemented validations include:

- Remove duplicate records
- Handle missing Customer IDs
- Detect cancelled invoices
- Flag zero-priced products
- Validate negative quantities
- Standardise data types
- Extract Year and Month
- Calculate Total Amount

### Business Flags

- IsCancelled
- HasCustomerID
- IsZeroPrice
- IsNegativeQuantity

### Output

```
silver_sales
```

---

## 🥇 Gold Layer

Business-ready analytical tables created for reporting.

| Table | Description |
|---------|------------|
| gold_sales_summary | Executive KPIs |
| gold_monthly_sales | Monthly Revenue Trends |
| gold_country_sales | Country Performance |
| gold_product_performance | Best Selling Products |
| gold_customer_summary | Customer Insights |

---

# Pipeline Orchestration

The Microsoft Fabric Pipeline orchestrates the complete data flow.

```
Bronze Notebook
        │
        ▼
Silver Notebook
        │
        ▼
Gold Notebook
```

Future enhancement:

```
Gold
   │
Refresh Semantic Model
   │
Notify Users
```

---

# Incremental Loading

RetailHub implements an incremental loading strategy to improve efficiency.

```
Incoming Data
        │
        ▼
Compare Business Key
        │
 ┌───────────────┐
 │ Already Exists│
 └──────┬────────┘
        │
  Yes         No
   │           │
 Skip      Insert
```

Benefits:

- Faster processing
- Reduced compute cost
- Scalable architecture
- Avoid duplicate records

---

# Sample SQL Analytics

```sql
SELECT Country,
       SUM(TotalAmount) AS Revenue
FROM gold_country_sales
GROUP BY Country
ORDER BY Revenue DESC;
```

---

# Power BI Dashboard

Executive dashboard includes:

- Executive KPI Cards
- Monthly Revenue Trend
- Country Performance
- Product Performance
- Customer Spend Analysis

---

# Project Features

- End-to-End Microsoft Fabric Project
- Medallion Architecture
- Incremental Loading
- Delta Lake Tables
- PySpark Data Engineering
- Spark SQL Analytics
- Microsoft Fabric Pipelines
- Semantic Models
- Direct Lake
- Power BI Dashboard

---

# Skills Demonstrated

- Microsoft Fabric
- Data Engineering
- OneLake
- Lakehouse
- Delta Lake
- PySpark
- Spark SQL
- ETL / ELT
- Incremental Loading
- Data Quality Validation
- Medallion Architecture
- Pipeline Orchestration
- Data Modelling
- Semantic Models
- Business Intelligence
- Power BI

---

# Repository Structure

```
RetailHub/

│── notebooks/
│     ├── Bronze
│     ├── Silver
│     └── Gold

│── pipeline/

│── dashboard/

│── images/

│── docs/
│     ├── EngineeringDesignDocument.pdf
│     ├── Architecture.pdf
│     └── ProjectJournal.pdf

│── README.md
```

---

# Future Enhancements

- Automated Data Quality Monitoring
- Semantic Model Refresh from Pipeline
- Slowly Changing Dimensions (SCD Type 2)
- CI/CD using Azure DevOps
- Parameterised Pipelines
- Real-Time Streaming
- Data Warehouse Implementation
- Monitoring & Alerting

---

# Author

**Chippy Pillai**

MSc Data Analytics

Aspiring Microsoft Fabric Data Engineer

🔗 LinkedIn: *(Add your profile)*

💻 GitHub: *(Add your GitHub profile)*

---
