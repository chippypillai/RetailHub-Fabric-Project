# 🛒 RetailHub – End-to-End Microsoft Fabric Data Engineering Project

> An enterprise-style Data Engineering project built using **Microsoft Fabric**, demonstrating modern data engineering practices through **Medallion Architecture**, **Delta Lake**, **PySpark**, **Microsoft Fabric Pipelines**, **Semantic Models**, and **Power BI**.

---

# 📌 Project Overview

RetailHub is an end-to-end Data Engineering solution built using Microsoft Fabric that transforms raw retail transaction data into business-ready analytical datasets.

The project demonstrates a modern Medallion Architecture (Bronze → Silver → Gold) while implementing production-inspired engineering concepts including:

- Incremental Data Loading
- Delta Lake Storage
- Data Quality Validation
- PySpark Transformations
- Fabric Pipeline Orchestration
- Direct Lake Semantic Model
- Power BI Reporting

---

# 🎯 Business Problem

Retail organisations generate thousands of sales transactions every day.

Raw transactional data often contains:

- Missing Customer IDs
- Cancelled Orders
- Duplicate Records
- Invalid Quantities
- Zero-Priced Products
- Inconsistent Data Types

Without proper data engineering processes, these issues lead to inaccurate reporting and poor business decisions.

RetailHub demonstrates how Microsoft Fabric transforms raw transactional data into trusted, business-ready datasets.

---

# 🏗️ Solution Architecture

```text
                    Online Retail Dataset (CSV)
                               │
                               ▼
                    🥉 Bronze Lakehouse Layer
               Raw Data + Incremental Loading
                               │
                               ▼
                    🥈 Silver Lakehouse Layer
         Data Cleaning • Validation • Business Rules
                               │
                               ▼
                     🥇 Gold Lakehouse Layer
              Business Ready Analytical Tables
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

> **Note:** A professional architecture diagram will replace this placeholder in a future update.

---

# 📷 Solution Screenshots

## Microsoft Fabric Workspace

![Microsoft Fabric Workspace](images/workspace.png)

---

## Lakehouse

![Lakehouse](images/lakehouse.png)

---

## Microsoft Fabric Pipeline

![Pipeline](images/pipeline.png)

---

## Power BI Executive Dashboard

![Dashboard](images/dashboard.png)

---

# 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| Microsoft Fabric | End-to-End Data Platform |
| OneLake | Unified Data Storage |
| Lakehouse | Central Data Repository |
| Delta Lake | ACID Storage Format |
| PySpark | Data Transformation |
| Spark SQL | Data Analysis |
| Fabric Pipelines | Workflow Orchestration |
| Semantic Model | Reporting Layer |
| Direct Lake | High Performance Analytics |
| Power BI | Dashboard & Visualisation |

---

# 📂 Dataset

**Dataset:** Online Retail Dataset (UCI Machine Learning Repository)

The dataset contains retail transactions with the following fields:

- Invoice Number
- Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

---

# 🥉 Bronze Layer

## Purpose

- Load raw retail transaction data
- Store source data as Delta Tables
- Implement Incremental Loading
- Preserve original records

**Output Table**

```
bronze_sales
```

---

# 🥈 Silver Layer

## Purpose

Transform raw data into trusted analytical datasets.

### Data Quality Rules

- Remove duplicate records
- Handle missing Customer IDs
- Detect cancelled invoices
- Flag zero-priced products
- Validate negative quantities
- Standardise data types
- Extract Year and Month
- Calculate TotalAmount

### Business Flags

- IsCancelled
- HasCustomerID
- IsZeroPrice
- IsNegativeQuantity

**Output Table**

```
silver_sales
```

---

# 🥇 Gold Layer

Business-ready analytical tables used for reporting.

| Table | Description |
|--------|-------------|
| gold_sales_summary | Executive KPIs |
| gold_monthly_sales | Monthly Revenue Trends |
| gold_country_sales | Country Performance |
| gold_product_performance | Product Analysis |
| gold_customer_summary | Customer Analysis |

---

# 🔄 Pipeline Orchestration

The Microsoft Fabric Pipeline orchestrates the complete data flow.

```text
Bronze Notebook
       │
       ▼
Silver Notebook
       │
       ▼
Gold Notebook
```

Future Enhancement

```text
Gold Notebook
       │
       ▼
Refresh Semantic Model
       │
       ▼
Email Notification
```

---

# ⚡ Incremental Loading

RetailHub implements an incremental loading strategy to process only new records.

```text
Incoming Records
        │
        ▼
Compare Business Key
        │
 ┌───────────────┐
 │Already Exists?│
 └──────┬────────┘
        │
   Yes      No
    │        │
 Skip    Insert
```

### Benefits

- Faster processing
- Reduced compute cost
- Improved scalability
- Prevents duplicate records

---

# ⭐ Key Features

- End-to-End Microsoft Fabric Solution
- Medallion Architecture
- Incremental Data Loading
- Delta Lake Storage
- PySpark Data Processing
- Spark SQL Analytics
- Fabric Pipeline Orchestration
- Direct Lake Semantic Model
- Interactive Power BI Dashboard

---

# 🚀 Skills Demonstrated

- Microsoft Fabric
- Data Engineering
- OneLake
- Lakehouse
- Delta Lake
- PySpark
- Spark SQL
- ETL / ELT
- Incremental Loading
- Data Validation
- Medallion Architecture
- Pipeline Orchestration
- Data Modelling
- Semantic Models
- Power BI

---

# 📁 Repository Structure

```text
RetailHub/

│── notebooks/
│     ├── 001_Bronze_Layer.ipynb
│     ├── 002_Silver_Layer.ipynb
│     └── 003_Gold_Layer.ipynb

│── SQL/
│     ├── silver_queries.sql
│     ├── gold_queries.sql
│     └── analytics_queries.sql

│── pipeline/

│── dashboard/

│── images/
│     ├── workspace.png
│     ├── lakehouse.png
│     ├── pipeline.png
│     └── dashboard.png

│── docs/
│     ├── EngineeringDesignDocument.pdf
│     ├── Architecture.pdf
│     └── ProjectJournal.pdf

│── README.md
```

---

# 🔮 Future Enhancements

- Automated Data Quality Monitoring
- Semantic Model Refresh from Pipeline
- Slowly Changing Dimensions (SCD Type 2)
- Parameterised Pipelines
- Azure DevOps CI/CD
- Real-Time Streaming
- Data Warehouse Integration
- Monitoring & Alerting

---

# 👨‍💻 Author

**Chippy Pillai**

MSc Data Analytics

Aspiring Microsoft Fabric Data Engineer

🔗 LinkedIn: *(Add your LinkedIn profile URL)*

💻 GitHub: *(Add your GitHub profile URL)*

---

⭐ If you found this project interesting, feel free to star the repository and connect with me on LinkedIn.
