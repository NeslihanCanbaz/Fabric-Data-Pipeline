# End-to-End Data Engineering Pipeline | Microsoft Fabric

This project demonstrates a fully functional data pipeline designed in **Microsoft Fabric**. It automates the ingestion, staging, and transformation of sales data.

## 🚀 Pipeline Architecture

The pipeline consists of three automated stages:
1. **Staging Cleanup**: Ensures the environment is ready by removing old files.
2. **Data Ingestion**: Extracts raw CSV data from a GitHub source via HTTP and loads it into the Lakehouse.
3. **ETL Transformation**: A PySpark Notebook processes the raw data, applies schema logic, and persists it into a Delta Table.

## 📊 Pipeline Execution Status
Below is the confirmation of a successful end-to-end run. All activities completed successfully within the orchestration.

<img src="pipeline_run.jpg" width="800">

## 💻 Transformation Logic (PySpark)
The notebook uses Spark SQL functions to transform `CustomerName` into separate `FirstName` and `LastName` columns and derives date hierarchies.

<img src="spark_code.png" width="800">

## 🗄️ Final Data Schema
The processed data is stored as a managed Delta table (`sales`) in the Lakehouse, optimized for analytical queries.

<img src="schema.png" width="800">

## ⚙️ Source Configuration
The ingestion layer is configured with a dynamic HTTP connection to fetch real-time data updates from the source repository.

<img src="source_config.png" width="800">

## 🛠️ Tech Stack
- **Orchestration:** Microsoft Fabric Pipelines
- **Compute:** Apache Spark (PySpark)
- **Storage:** OneLake (Delta Lake format)
- **Source:** GitHub Raw Data (HTTP)
