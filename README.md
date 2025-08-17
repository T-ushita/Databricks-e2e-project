# Databricks E2E Project 🚀  
End-to-end data pipeline built on Databricks using the Medallion architecture (Bronze → Silver → Gold) with Spark and Azure.

## 📌 Project Objectives  
- Build an **end-to-end data pipeline** on **Azure Databricks** using the **Medallion Architecture** (Bronze → Silver → Gold).  
- Automate ingestion, transformation, and curation of raw data into **business-ready datasets**.  
- Implement **governance and access control** with Unity Catalog for metadata, permissions, and reusable functions.  
- Enable **real-time and batch processing** with Autoloader, Delta Lake, and Delta Live Tables (DLT).  
- Deliver **analytics-ready data in a Star Schema** for reporting in Power BI and downstream warehouses.  

---

## 📚 What the Project Covers  

### 🔹 Azure Setup  
- Resource Group, Data Lake (ADLS Gen2), Storage Containers (**bronze, silver, gold**).  
- Access control with **Access Connector** and IAM roles.  

### 🔹 Databricks Setup  
- Workspaces, clusters, compute (**serverless, job, all-purpose**).  
- **Unity Catalog** for metastore, external locations, schemas, functions.  

### 🔹 Bronze Layer – Raw Ingestion  
- Ingest raw parquet data from data sources using **Autoloader** (incremental + idempotent).  
- Store raw data in Bronze containers with **schema evolution** + checkpoints.  
- Automated ingestion pipelines via **Workflows** and parameterized notebooks.  

### 🔹 Silver Layer – Clean & Conform  
- Apply transformations with **PySpark** (schema cleaning, deduplication, window functions).  
- Use **OOP classes** for reusable functions.  
- Store curated data in **Delta tables** for ACID compliance.  
- Register reusable **SQL/Python functions** in Unity Catalog.  

### 🔹 Gold Layer – Business Ready  
- Build **Star Schema** with Fact and Dimension tables.  
- Implement **Slowly Changing Dimensions (SCD1, SCD2)**.  
- Use **Delta Live Tables (DLT)** for declarative, streaming pipelines with expectations/constraints.  
- Create surrogate keys and manage **upserts** for incremental data.  

### 🔹 Analytics & Reporting  
- **FactOrders** table created by joining dimensions with fact data.  
- Ready for visualization in **Power BI** or querying with **SQL Warehouses**.  

---

## 🔄 Flow of the Project  

🔽 **Data Sources** (GitHub / Azure Parquet)  
➡️ **Bronze Layer**: Raw ingestion with Autoloader → Delta format (schema evolution).  
➡️ **Silver Layer**: Transformations, deduplication, enrichment → Delta tables.  
➡️ **Gold Layer**: Business-ready **Star Schema** (Fact + Dimensions, SCD handling).  
➡️ **Governance**: Unity Catalog (schemas, permissions, metadata, reusable functions).  
➡️ **Analytics Layer**: Fact tables consumed in **Power BI / SQL Warehouses** for dashboards.  

---

## ✅ Project Outcomes  
- Automated and **scalable data pipeline** on Azure Databricks.  
- Data stored in **Delta format** ensuring ACID transactions and time travel.  
- **Real-time + batch ingestion** with schema evolution and checkpointing.  
- Reusable code via **PySpark classes + Unity Catalog functions**.  
- Strong **data governance & security** with Unity Catalog and IAM.  
- **Star Schema** model built for efficient querying and BI reporting.  
- End-to-end orchestration using **Databricks Workflows** (Bronze → Silver → Gold → Reporting).  
- Final output: **Analytics-ready datasets** powering Power BI dashboards and supporting advanced analytics.  

---
