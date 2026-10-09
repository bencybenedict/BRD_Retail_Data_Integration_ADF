# 🛒 Retail Data Integration Platform (RDIP)

## 📌 Project Overview

The **Retail Data Integration Platform (RDIP)** is a data engineering project designed to integrate retail data from multiple sources, transform it into a consistent and structured format, and load the processed data into a centralized database for reporting and business analysis.

The project uses **Azure Data Factory (ADF)** to orchestrate data ingestion and transformation workflows. It follows a layered data processing approach to organize raw and processed data and prepare a consolidated sales summary for business intelligence and reporting.

## 🎯 Project Objectives

* Integrate retail data from multiple data sources.
* Automate data ingestion and processing workflows.
* Clean, standardize, and transform retail data.
* Join order, product, and store information.
* Aggregate sales data to generate meaningful business insights.
* Load curated sales data into Azure SQL Database for reporting.

## 🛠️ Technologies Used

* **Azure Data Factory (ADF)** – Data pipeline orchestration and ETL workflows.
* **Azure Data Lake Storage Gen2 (ADLS Gen2)** – Storage for raw and processed data.
* **Azure SQL Database** – Storage for curated sales summary data.
* **SQL Server** – Relational data source for retail orders.
* **REST API** – Product catalog data ingestion.
* **CSV** – Store master data source format.
* **Parquet** – Processed data storage format.
* **Git & GitHub** – Version control and project documentation.

## 📂 Data Sources

The project integrates data from three sources:

1. **Orders Data:** Retail order records retrieved from SQL Server.
2. **Product Catalog:** Product information retrieved from a REST API.
3. **Store Master:** Store details provided through a CSV file.

These datasets are combined to create a consolidated view of retail sales.

## ⚙️ Data Engineering Workflow

### 1. Data Ingestion

Azure Data Factory pipelines ingest data from the configured source systems and store the raw data in Azure Data Lake Storage Gen2.

### 2. Data Transformation

The transformation workflow processes the ingested data through activities such as:

* Data cleansing and validation.
* Standardization of relevant fields.
* Joining orders with product and store information.
* Aggregating sales quantities and amounts.
* Preparing the sales summary dataset.

### 3. Processed Data Storage

The transformed sales summary is stored in Parquet format in the data lake for efficient storage and downstream processing.

### 4. Data Loading

The curated sales summary data is loaded into Azure SQL Database, providing a structured dataset for reporting and business intelligence.

## 🏗️ Pipeline Architecture

The project organizes its Azure Data Factory workflows into the following pipelines:

* **master_pipeline:** Coordinates the overall workflow by executing the required pipelines.
* **raw_pipeline:** Ingests source data into the raw storage layer.
* **silver_pipeline:** Cleans, joins, and aggregates the ingested data.
* **gold_pipeline:** Loads the curated sales summary into the target database.

## 💡 Key Learning Outcomes

* Building and orchestrating data pipelines using Azure Data Factory.
* Integrating data from relational databases, REST APIs, and CSV files.
* Working with Azure Data Lake Storage Gen2.
* Performing data cleansing, joining, and aggregation.
* Using Parquet for processed data storage.
* Loading transformed data into Azure SQL Database.
* Organizing data engineering projects using GitHub.

## 👩‍💻 Author

**Bency Benedict**

Aspiring Data Engineer | Python | SQL | Azure Data Factory | Azure Data Lake Storage Gen2 | Azure SQL

GitHub: [bencybenedict](https://github.com/bencybenedict)

---

⭐ *This project demonstrates a practical approach to retail data integration, pipeline orchestration, data transformation, and preparing curated datasets for analytics.*
