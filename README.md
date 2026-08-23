# Tokyo Olympics End-to-End Data Engineering Project

This project demonstrates an end-to-end data engineering and analytics pipeline using the **Tokyo 2020 Olympics dataset**.

The objective is to build a modern data pipeline that takes raw Olympic data through ingestion, storage, transformation, data quality, modeling, and analytics before delivering insights through Power BI.

## Project Architecture

The project follows the **Medallion Architecture**:

**Raw Data → Bronze → Silver → Gold → Power BI**

### Bronze Layer
Raw Tokyo Olympics datasets are ingested into Databricks and stored as **Delta tables** with minimal transformation.

### Silver Layer
The Bronze data is cleaned, validated, standardized, and transformed using **Apache Spark / PySpark**.

### Gold Layer
Business-ready datasets are created for analytical use cases, including medal performance, athletes, countries, and other Olympic metrics.

### Analytics & Visualization
The curated Gold data is connected to **Power BI** to create interactive dashboards and provide insights into Olympic performance.

## Technologies

- **Databricks**
- **Apache Spark / PySpark**
- **Delta Lake**
- **Unity Catalog**
- **SQL**
- **Power BI**
- **Python**
- **GitHub**

## Dataset

The project uses the Tokyo 2020 Olympic Games dataset, containing information about athletes, medals, coaches, and technical officials.

## Key Learning Objectives

This project is designed to demonstrate practical data engineering concepts including:

- Data ingestion
- Lakehouse architecture
- Medallion architecture
- Bronze, Silver and Gold data layers
- Delta Lake tables
- PySpark transformations
- Data cleaning and validation
- Data modeling
- SQL analytics
- Data quality checks
- Business intelligence
- Power BI visualization

##  Pipeline

```text
Tokyo Olympics Dataset
          │
          ▼
     Raw Data
          │
          ▼
   ┌──────────────┐
   │ Bronze Layer │
   │  Raw Delta   │
   └──────┬───────┘
          │
          ▼
   ┌──────────────┐
   │ Silver Layer │
   │ Cleaned Data │
   └──────┬───────┘
          │
          ▼
   ┌──────────────┐
   │  Gold Layer  │
   │  Analytics   │
   └──────┬───────┘
          │
          ▼
       Power BI
          │
          ▼
   Olympic Insights
