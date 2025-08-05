# 🏗️ Modern Data Engineering Pipeline with Medallion Architecture  
**Built using DBT, Databricks, Apache Spark, Azure Data Lake Gen2, and Azure Data Factory**

This project showcases a modern data engineering pipeline leveraging the **Medallion Architecture** on Azure. It demonstrates how to ingest, transform, and curate data using tools like **Apache Spark**, **Databricks**, **DBT**, and **Azure Data Factory**, storing it efficiently in **Azure Data Lake Gen2**. The layered approach ensures high data quality, scalability, and reusability across business analytics and machine learning use cases.

---

## 🔧 Tech Stack

| Tool | Purpose |
|------|---------|
| **Apache Spark** | Distributed data transformation and processing |
| **Databricks** | Collaborative notebooks and scalable Spark compute |
| **DBT** | SQL-based data modeling and transformation in Silver/Gold layers |
| **Azure Data Factory (ADF)** | Orchestration and ingestion into the Bronze layer |
| **Azure Data Lake Gen2** | Cloud storage for raw, processed, and curated data |
| **Apache Kafka** *(optional)* | Real-time streaming ingestion (retail/event use cases) |

---

## 🧱 Architecture: Medallion Layers

### 🥉 Bronze Layer  
- Raw ingestion from various sources (Kafka, Kinesis, CSV, JSON)  
- Data stored in ADLS Gen2 for long-term retention  
- Minimal transformation applied

### 🥈 Silver Layer  
- Data is cleansed, joined, enriched, and standardized  
- Spark performs heavy transformations  
- DBT models applied for structured transformation pipelines

### 🥇 Gold Layer  
- Business-level aggregates ready for downstream consumption  
- Final models are analytics-ready for BI and ML use cases  
- Data quality checks and documentation powered by DBT

---

## 📈 Key Features

- ✅ End-to-end orchestration from ingestion to analytics-ready data  
- ✅ Scalable PySpark transformations in Databricks  
- ✅ Modular and maintainable SQL-based transformations via DBT  
- ✅ Data versioning, logging, and reproducibility  
- ✅ Cloud-native storage and compute using Azure stack  
- ✅ Support for both batch and streaming (Kafka) ingestion

---

## 📁 Project Structure

```bash
project/
│
├── bronze/              # Ingestion logic (ADF pipelines or Kafka producers)
├── silver/              # PySpark jobs for cleansing/enrichment
├── gold/                # DBT models and SQL-based transformations
├── data_lake/           # Simulated directory structure for ADLS Gen2
├── orchestration/       # Azure Data Factory JSON pipeline templates
├── notebooks/           # Databricks notebooks for exploration & testing
├── dbt_project/         # DBT models, seeds, tests, and documentation
├── img/                 # Architecture diagram and project assets
└── README.md
