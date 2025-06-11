# 🚀 Azure Data Engineering Project – End-to-End ADF Pipeline

This project showcases a complete Azure Data Engineering solution using **Azure Data Factory (ADF)**. It automates data ingestion, transformation, and storage using Azure Data Lake and GitHub REST API integrations.

---

## 🎯 Project Objective

To build an automated Azure Data Engineering pipeline using **ADF** that can:
- Ingest structured data from Azure Data Lake and GitHub (via REST API)
- Transform and store data into target Data Lake containers
- Schedule, monitor, and manage data flows using Azure-native tools

---

## 🧱 Architecture Overview

### ✅ Components Used:
- **Azure Resource Group** – Logical container for all Azure assets
- **Azure Storage Account** – Enabled with hierarchical namespace to simulate a Data Lake
  - `source` container – holds raw files (CSV)
  - `destination` container – stores processed data
- **Azure Data Factory** – Main tool for orchestration

---

## 🔧 Step-by-Step Implementation

### 1️⃣ Resource Setup
- Created an Azure Resource Group
- Provisioned a Storage Account (with hierarchical namespace)
- Defined `source` and `destination` containers

### 2️⃣ Upload Initial Data
- Uploaded `fact_sales_1.csv` to `source/csv_files/`

### 3️⃣ Create ADF and Linked Services
- Created ADF instance linked to the same resource group
- Defined Linked Services:
  - Azure Data Lake Gen2
  - GitHub via HTTP

### 4️⃣ Dataset Creation
- Dataset for source: `source/csv_files/fact_sales_1.csv`
- Dataset for sink: `destination/csv_files/`

---

## 🔄 Pipelines Developed

### 📂 Pipeline 1: Source CSV Ingestion
- **Activity**: Copy Activity
- Transfers CSV from `source` to `destination`
- **Pipeline Name**: `Pipeline_Manager`

### 🌐 Pipeline 2: GitHub CSV Ingestion
- **Source**: GitHub HTTP REST endpoint (e.g., `fact_sales_2.csv`)
- Stores pulled data in `destination` container

### 🧩 Pipeline 3 & 4:
- Additional pipelines for:
  - Pipeline Management
  - Parameterized and dynamic data processing

---

## 📸 Screenshots

Diagrams and UI walkthroughs available in:
- `pipeline 1/` and `pipeline 2/` directories (Copy activities)
- `execution pipeline/` (monitor & trigger screens)
- `pipeline 3/4/` (manager pipeline & variable pipelines)

---

## 🧠 Key Learnings

- Hands-on implementation of Azure Data Factory pipelines
- Real-world API integration using ADF HTTP connector
- Scalable ingestion design using datasets and linked services
- Modular, reusable pipeline architecture for data engineering

---

## 📁 Folder Structure

```bash
AzureDataEngineeringProject/
├── pipeline 1/
├── pipeline 2/
├── pipeline 3/
├── pipeline 4/
├── execution pipeline/
├── ADF Ansh FLow.docx
```

---

## 🛡️ Prerequisites

- Active Azure Subscription
- Azure Storage Account
- GitHub repository with sample CSV data

---

## 👤 Author

**Tushar** – Azure Data Engineering Enthusiast  
📧 Reach out via LinkedIn or GitHub for collaborations

**Motivation and Credits**
Ansh Lamba
