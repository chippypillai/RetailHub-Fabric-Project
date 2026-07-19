# 🛒 RetailHub – End-to-End Data Engineering Project using Microsoft Fabric

## Project Overview

RetailHub is an end-to-end data engineering project built using **Microsoft Fabric** following the **Medallion Architecture (Bronze, Silver and Gold)**.

The project demonstrates how raw retail transaction data can be transformed into business-ready analytical datasets using **PySpark**, **Delta Lake**, **Microsoft Fabric Pipelines**, **Semantic Models**, and **Power BI**.

The solution simulates a real-world enterprise data platform with incremental loading, data validation, business transformations and interactive reporting.

---

## Solution Architecture

```
Online Retail Dataset
        │
        ▼
Bronze Layer
(Raw Data + Incremental Loading)
        │
        ▼
Silver Layer
(Data Cleaning & Transformations)
        │
        ▼
Gold Layer
(Business Ready Tables)
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

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Microsoft Fabric | End-to-End Data Platform |
| OneLake | Data Storage |
| Lakehouse | Central Data Repository |
| PySpark | Data Transformation |
| Delta Lake | ACID Storage |
| Spark SQL | Data Analysis |
| Fabric Pipeline | Workflow Orchestration |
| Semantic Model | Reporting Layer |
| Power BI | Dashboard & Visualisation |

---

## Medallion Architecture

### 🥉 Bronze Layer

Purpose

- Load raw retail data into the Lakehouse
- Perform incremental loading
- Prevent duplicate records using Business Key
- Store raw data as Delta Tables

Output Table

```
bronze_sales
```

---

### 🥈 Silver Layer

Purpose

- Clean and validate data
- Standardise data types
- Handle missing values
- Generate business flags
- Create derived columns

Key Transformations

- Data Cleaning
- Duplicate Removal
- Year / Month Extraction
- Total Amount Calculation
- Cancelled Order Flag
- Missing Customer Flag
- Zero Price Flag

Output Table

```
silver_sales
```

---

### 🥇 Gold Layer

Business-ready tables created for reporting.

| Gold Table | Purpose |
|------------|---------|
| gold_sales_summary | Executive KPIs |
| gold_monthly_sales | Monthly Sales Trends |
| gold_country_sales | Country Performance |
| gold_product_performance | Product Analysis |
| gold_customer_summary | Customer Analysis |

---

## Pipeline

Current Pipeline

```
Bronze
   │
   ▼
If Success
   │
   ▼
Silver
   │
   ▼
Gold
```

Future Enhancement

```
Bronze
   │
Silver
   │
Gold
   │
Refresh Semantic Model
```

---

## Dashboard

The Power BI Executive Dashboard includes:

- Executive KPI Cards
- Monthly Revenue Trend
- Top Countries by Revenue
- Top Products by Revenue
- Top Customers by Spend

### Dashboard Preview

> ![alt text](<WhatsApp Image 2026-07-19 at 13.55.00.jpeg>)

---

## Key Features

- End-to-End Microsoft Fabric Project
- Medallion Architecture
- Incremental Data Loading
- Delta Lake Tables
- PySpark Transformations
- Fabric Pipelines
- Direct Lake Semantic Model
- Executive Power BI Dashboard

---

## Skills Demonstrated

- Microsoft Fabric
- Lakehouse
- OneLake
- PySpark
- Spark SQL
- Delta Lake
- ETL Development
- Incremental Loading
- Data Validation
- Data Modelling
- Pipeline Orchestration
- Power BI
- Business Intelligence

---

## Project Structure

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

## Future Improvements

- Refresh Semantic Model from Pipeline
- Data Quality Monitoring
- Logging Framework
- Azure Data Factory Integration
- CI/CD Deployment
- Git Integration

---

## Author

**Chippy Pillai**

MSc Data Analytics

Aspiring Microsoft Fabric & Data Engineer

LinkedIn: *(Add Link)*

GitHub: *(Add Link)*
