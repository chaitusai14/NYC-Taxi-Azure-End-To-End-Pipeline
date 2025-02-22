# 🚀 Azure End-to-End Data Engineering Project

## 📌 Overview
This project is an end-to-end **Azure Data Pipeline** that ingests, processes, and analyzes **NYC Taxi Trip Data** to generate meaningful insights using a **Power BI** dashboard. The pipeline follows the **Medallion Architecture** (Bronze, Silver, Gold) and leverages **Azure services** for efficient data processing.

## 📖 Table of Contents
- [Overview](#-overview)
- [Architecture](#-architecture)
- [Technologies Used](#-technologies-used)
- [Setup Instructions](#-setup-instructions)
  - [Prerequisites](#prerequisites)
  - [Clone the Repository](#1%EF%B8%8F⃣-clone-the-repository)
  - [Configure Azure Services](#2%EF%B8%8F⃣-configure-azure-services)
  - [Set Up Databricks Notebooks](#3%EF%B8%8F⃣-set-up-databricks-notebooks)
  - [Connect Power BI to Gold Layer](#4%EF%B8%8F⃣-connect-power-bi-to-gold-layer)
- [Dataset API URL](#-dataset-api-url)
- [Key Insights & Future Enhancements](#-key-insights--future-enhancements)
- [License](#-license)
- [Contributing](#-contributing)
- [Contact](#-contact)

## 🏗️ Architecture

![Architecture Diagram] /Users/saichaitanya/Desktop/architecture.png

The project follows a structured data pipeline:

1. **Data Ingestion (Bronze Layer)**: Extracts Green Taxi trip data from an **API** and stores it in **Azure Data Lake Storage (ADLS Gen2)** in **Parquet format** using **Azure Data Factory**.
2. **Data Processing (Silver Layer)**: Uses **Azure Databricks** to clean, transform, and standardize the raw data before saving it back to ADLS in **Parquet format**.
3. **Data Analytics (Gold Layer)**: Converts the Silver layer Parquet files into **Delta tables** for optimized querying.
4. **Visualization & Reporting**: Connects Power BI to the Gold layer to create **interactive dashboards** for data-driven decision-making.

## 🛠️ Technologies Used
- **Azure Data Factory (ADF)** - Orchestrates the data pipeline
- **Azure Data Lake Storage (ADLS Gen2)** - Stores ingested and processed data
- **Azure Databricks** - Processes and transforms data using **PySpark**
- **Delta Lake** - Ensures ACID transactions and scalable data storage
- **Power BI** - Creates visual dashboards for business intelligence

## 🔧 Setup Instructions

### Prerequisites
Before setting up the project, install the required dependencies:
```bash
pip install -r requirements.txt
```

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/chaitusai14/NYC-Taxi-Azure-End-To-End-Pipeline.git
cd azure-data-pipeline
```

### **2️⃣ Configure Azure Services**
- **Create an ADLS Gen2 Storage Account** and set up containers for **bronze, silver, and gold** layers.
- **Deploy Azure Data Factory (ADF)** and configure linked services for API ingestion and ADLS.
- **Create a Databricks Workspace** and generate a personal access token for authentication.

### **3️⃣ Set Up Databricks Notebooks**
Upload the provided Databricks notebooks:
- `bronze_to_silver_dump.ipynb`
- `silver_to_gold_dump.ipynb`

Run them in Databricks with appropriate configurations.

### **4️⃣ Connect Power BI to Gold Layer**
- Open **Power BI Desktop**.
- Connect to **Databricks SQL Endpoint**.
- Load Gold layer Delta tables and design dashboards.

## 🌐 Dataset API URL
**Placeholder for Dataset API URL:** `https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page`

## 📊 Key Insights & Future Enhancements
- **Current Focus**: Creating interactive **Power BI dashboard** for real-time analysis.
- **Planned Enhancements**:
  - Implementing **Synapse Analytics** for faster queries.
  - Enhancing security with **RBAC and Managed Identities**.
  - Automating monitoring and alerts for data pipeline failures.

## 🤝 Contributing
Contributions are welcome! Feel free to open issues and submit pull requests.

## 📬 Contact
For questions or collaborations, connect on **LinkedIn**: [Your Profile](https://www.linkedin.com/in/chaitusai14031998).
