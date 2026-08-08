# Retail Sales Analytics

An end-to-end retail sales analytics project built using **Python, Snowflake, SQL, and Power BI**.

The project demonstrates the complete data analytics workflow, from data cleaning and cloud data warehousing to 
incremental data processing and interactive business intelligence dashboards.

---

## 📌 Project Overview

The objective of this project is to build a scalable retail sales analytics solution that transforms raw retail data into meaningful business insights.

The project covers:

- Data cleaning and preprocessing using Python
- Cloud data warehousing using Snowflake
- Raw, staging, and analytics layers
- Star schema data modeling
- Fact and dimension tables
- Sales and profit calculations
- Incremental data processing using Snowflake Streams
- Automated processing using Snowflake Tasks
- MERGE-based upsert logic
- DAX measures and interactive Power BI dashboards
- Business analysis across sales, customers, and products

---

## 🏗️ Project Architecture

```text
Raw Retail Data
       │
       ▼
   Python / Colab
       │
       │ Data Cleaning & Validation
       ▼
   Snowflake Stage
       │
       ▼
   RAW Layer
       │
       ▼
  STAGING Layer
       │
       ├───────────────┐
       │               │
       ▼               ▼
 Dimension Tables    FACT_SALES
       │               │
       └───────┬───────┘
               ▼
        Analytics Layer
               │
       Streams + Tasks
               │
          MERGE / Upsert
               │
               ▼
           Power BI
               │
               ▼
      Interactive Dashboard

