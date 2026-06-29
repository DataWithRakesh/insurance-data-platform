# 🚀 Azure Insurance Data Platform | End-to-End Data Engineering Project

## 📌 Project Overview

This project demonstrates a **production-style Azure Data Engineering pipeline** built using the **Medallion Architecture (Landing → Bronze → Silver → Gold)**.

The project processes insurance claim data from raw CSV files, performs data quality validation, implements **Slowly Changing Dimension (SCD Type 2)** for dimensions, builds a **Fact Table**, and creates a **Gold Reporting Layer** using Delta Lake.

---

# 🏗️ Architecture

```text
Landing
   │
   ▼
Bronze (Raw Parquet)
   │
   ▼
Silver
   ├── Dim Policy (SCD2)
   ├── Dim Customer (SCD2)
   ├── Dim Vehicle (SCD2)
   └── Fact Claim
   │
   ▼
Gold
   └── Gold Claim Summary
```

---

# 🛠️ Technology Stack

* ☁️ Azure Synapse Analytics
* 🐍 PySpark
* 📂 Azure Data Lake Storage Gen2
* 🔷 Delta Lake
* 🔄 Azure Data Factory / Synapse Pipelines
* 💻 Python
* 🗄️ SQL

---

# 📂 Project Structure

```text
Insurance-Data-Platform
│
├── Landing
├── Bronze
│
├── Silver
│   ├── Policy Dimension (SCD2)
│   ├── Customer Dimension (SCD2)
│   ├── Vehicle Dimension (SCD2)
│   └── Claim Fact
│
├── Gold
│   └── Claim Summary
│
├── Pipelines
├── Notebooks
└── README.md
```

---

# 📊 Implemented Features

## ✅ Bronze Layer

* Raw CSV ingestion
* CSV → Parquet conversion
* Azure Synapse Pipeline
* ADLS Gen2 storage

---

## ✅ Silver Layer

### Policy Dimension

* SCD Type 2
* SHA256 Change Detection
* Surrogate Key Generation
* Effective Start Date
* Effective End Date
* Current Record Flag

---

### Customer Dimension

* SCD Type 2
* SHA256 Change Detection
* Data Validation
* Historical Tracking

---

### Vehicle Dimension

* SCD Type 2
* SHA256 Change Detection
* Historical Tracking

---

### Claim Fact

* Fact Table Creation
* Lookup Surrogate Keys
* Policy Dimension Join
* Customer Dimension Join
* Vehicle Dimension Join

---

# 📈 Gold Layer

### Gold Claim Summary

Business-ready reporting table created by joining:

* Policy Dimension
* Customer Dimension
* Vehicle Dimension
* Claim Fact

This table can directly power BI dashboards and analytical reports.

---

# 🔍 Data Quality Checks

Implemented validations include:

* ✅ Record Count Validation
* ✅ Null Business Key Check
* ✅ Duplicate Business Key Check
* ✅ Business Rule Validation
* ✅ Exception Handling

---

# 🔄 SCD Type 2 Implementation

Implemented complete SCD Type 2 logic including:

* Business Key Comparison
* SHA256 Hash Comparison
* INSERT Detection
* UPDATE Detection
* NO_CHANGE Detection
* Expire Existing Records
* Insert New Version
* Historical Data Maintenance

---

# ⚡ Delta Lake Features

* Delta Tables
* Transaction Log
* ACID Transactions
* Version History
* Delta Overwrite
* Delta File Management

---

# 📊 Data Flow

```text
CSV
 │
 ▼
Landing
 │
 ▼
Bronze (Parquet)
 │
 ▼
Silver Dimensions
 │
 ▼
Fact Table
 │
 ▼
Gold Reporting
```

---

# 📚 Key Concepts Demonstrated

* Medallion Architecture
* Delta Lake
* Slowly Changing Dimension (SCD2)
* Star Schema
* Fact & Dimension Modeling
* Surrogate Keys
* SHA256 Hashing
* Data Quality Validation
* Azure Synapse Pipelines
* PySpark Transformations

---

# 🎯 Learning Outcomes

This project demonstrates practical implementation of:

* End-to-End Data Engineering
* Production-style ETL Pipeline
* Data Warehouse Design
* Dimensional Modeling
* Historical Data Tracking
* Delta Lake Best Practices
* Azure Synapse Analytics

---

# 🚀 Future Enhancements

* Delta MERGE based SCD2
* Metadata Driven Framework
* Audit Framework
* Logging Framework
* Incremental Fact Loading
* Gold Analytical Data Marts


---

# 👨‍💻 Author

**Rakesh Nayak**

Azure Data Engineer | PySpark | Azure Synapse | Delta Lake | Data Engineering
