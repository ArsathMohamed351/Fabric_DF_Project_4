Microsoft Fabric Data Pipeline – Automated File Ingestion

<img width="1917" height="998" alt="Success Pipeline" src="https://github.com/user-attachments/assets/141759d2-2b0a-41db-b5a1-f6a79fe970c9" />
<img width="1919" height="988" alt="Failed Pipeline" src="https://github.com/user-attachments/assets/5a898def-fd89-448a-bc92-ceaaea7dfaa0" />


## 📌 Overview
This project demonstrates an end-to-end **data ingestion and monitoring pipeline** built in **Microsoft Fabric**. It dynamically processes files from Azure storage, tracks successes and failures, and outputs analytics-ready datasets in **Parquet format**.

## ⚙️ Features
- Metadata-driven file ingestion using **Get Metadata**
- Dynamic **ForEach loop** with success/failure handling
- **Copy Data** activity with recursive ingestion
- Append variable logic for tracking copied and failed files
- Parent–child pipeline orchestration for modular workflows
- Output stored in **Azure Storage** with **Parquet format**

## 🔄 Pipeline Flow
1. **Get Metadata** – Retrieve Azure folder metadata  
2. **ForEach Loop** – Iterate over files  
   - Copy Data  
   - Append Copied Files / Append Failed Files  
3. **Set Variables** – Track counts and names of copied/failed files  
4. **Store Results** – Save outputs in Azure storage for downstream analytics  

## 📊 Example Outputs
- **Copied files count**: `8`  
- **Failed files count**: `3`  
- **Copied file names**:  
  ["features.csv","Fact_Sales_1.csv","stores.csv","ecommerce_orders_large.csv","ecommerce_sales_34500.csv","test.csv"]  
- **Failed file names**:  
  ["netflix_directors.csv","netflix_titles.csv","netflix_cast.csv"]

## 🛠️ Tech Stack
- Microsoft Fabric  
- Azure Storage  
- Parquet format  
- Pipeline Expressions (`@item().name`, `@length()`, `@string()`)

## 📂 Repository Structure
├── /pipeline_diagrams     # Screenshots of pipeline workflow  
├── /configs               # JSON/YAML configs if exported  
├── /docs                  # Documentation and notes  
└── README.md              # Project overview  

## 🌟 Why This Project Matters
- **Automation**: Eliminates manual file handling  
- **Resilience**: Tracks failures for debugging and retry logic  
- **Scalability**: Modular design with parent-child pipelines  
- **Analytics-ready**: Outputs in Parquet format for Power BI or downstream consumption  

## 👨‍💻 Author
**Arsath**  
*Data Engineer | Cloud & Streaming ETL Specialist*
