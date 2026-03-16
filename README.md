# 🚀 Azure Data Engineering Pipeline — Medallion Architecture

![Azure](https://img.shields.io/badge/Azure-Data%20Engineering-blue)
![Databricks](https://img.shields.io/badge/Databricks-PySpark-orange)
![ADF](https://img.shields.io/badge/Azure-Data%20Factory-purple)
![Delta](https://img.shields.io/badge/Delta-Lake-red)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📌 Project Overview

This project demonstrates an **end-to-end Azure Data Engineering pipeline** built using:

- **Azure Data Lake Storage Gen2**
- **Azure Databricks**
- **PySpark**
- **Delta Lake**
- **Azure Data Factory**

The pipeline processes a retail dataset using the **Medallion Architecture** to transform raw data into **analytics-ready datasets**.

Azure Data Factory orchestrates the Databricks notebooks to create a **fully automated data workflow**.

---

# 🏗 Architecture

```
Online Retail Dataset (Excel)
        ↓
Azure Data Lake Storage Gen2
        ↓
Databricks Bronze Notebook
        ↓
Databricks Silver Notebook
        ↓
Databricks Gold Notebook
        ↓
Azure Data Factory Pipeline
        ↓
Monitoring
```

---

# ⚙️ Technologies Used

| Technology | Purpose |
|------------|--------|
| **Azure Data Lake Storage Gen2** | Cloud data storage |
| **Azure Databricks** | Distributed data processing |
| **PySpark** | Data transformation |
| **Delta Lake** | Reliable lakehouse storage |
| **Azure Data Factory** | Pipeline orchestration |
| **Pandas** | Excel ingestion |

---

# 📊 Dataset

**Online Retail Dataset**

Source:  
https://archive.ics.uci.edu/ml/datasets/Online+Retail

The dataset contains transactional data for a UK-based online retail store including:

- Invoice number
- Product description
- Quantity
- Unit price
- Customer ID
- Country

---

# 🔄 Data Pipeline Layers

---

## 🥉 Bronze Layer — Raw Ingestion

The Bronze notebook ingests the raw Excel dataset into Azure Data Lake Storage and stores it in **Delta format**.

### Key Tasks

- Read Excel dataset using Pandas
- Convert data into Spark DataFrame
- Store raw data in the Bronze container

📸 **Bronze Notebook**

![Bronze Notebook](<img width="1330" height="483" alt="Screenshot 2026-03-16 192239" src="https://github.com/user-attachments/assets/8b931bd2-4f56-4993-a9d6-8e2c0dbf985e" />
)

---

## 🥈 Silver Layer — Data Cleaning & Transformation

The Silver notebook cleans and standardizes the dataset.

### Transformations

- Remove duplicate records  
- Trim whitespace from string columns  
- Fix `CustomerID` values  
- Filter invalid transactions  
- Create **Revenue column**  
- Add ingestion timestamp  

📸 **Silver Notebook**

![Silver Notebook](<img width="1338" height="745" alt="Screenshot 2026-03-16 192537" src="https://github.com/user-attachments/assets/94d6ffac-2c28-4ca6-819a-7f987ed3bc05" />
)

---

## 🥇 Gold Layer — Business Analytics

The Gold notebook generates **analytics-ready datasets**.

### Generated Datasets

| Dataset | Description |
|--------|-------------|
| **Daily Revenue** | Revenue aggregated by day |
| **Top Products** | Products generating highest revenue |
| **Country Sales** | Revenue by country |
| **Customer Revenue** | Customer purchase analytics |

📸 **Gold Notebook**

![Gold Notebook](<img width="1326" height="517" alt="Screenshot 2026-03-16 192806" src="https://github.com/user-attachments/assets/725afc8e-3174-45df-a2f6-d295af8aff4e" />
)

---

# 🔁 Pipeline Orchestration

Azure Data Factory orchestrates the Databricks notebooks.

Pipeline execution flow:

```
Bronze Notebook
      ↓
Silver Notebook
      ↓
Gold Notebook
```

📸 **ADF Pipeline Canvas**

![ADF Pipeline](<img width="1920" height="859" alt="Screenshot 2026-03-16 185656" src="https://github.com/user-attachments/assets/15078085-de86-41e7-a1f2-18e467d26ff8" />
)

---

# 📈 Monitoring

Pipeline runs are monitored in **Azure Data Factory Monitor**, providing visibility into:

- Pipeline status
- Activity execution
- Duration
- Logs and debugging

📸 **ADF Monitoring**

![ADF Monitor](images/adf_monitor.png)

---

# 🗂 Data Lake Structure

The project follows **Medallion Architecture storage layers**.

```
raw
bronze
silver
gold
```

📸 **ADLS Containers**

![ADLS Containers](<img width="1918" height="860" alt="Screenshot 2026-03-16 185715" src="https://github.com/user-attachments/assets/388f3d0f-9835-4fe0-9ee7-762f9ffa3a0f" />
)

---

# ✨ Key Features

✔ End-to-end Azure data engineering workflow  
✔ Medallion architecture implementation  
✔ Delta Lake storage format  
✔ PySpark transformations  
✔ Automated orchestration using Azure Data Factory  
✔ Cloud-based scalable data processing

---

# 👨‍💻 Author

**Sachait Likhi**

📍 Dubai, UAE  

🔗 LinkedIn  
https://linkedin.com/in/sachait-likhi-377b55220  

🌐 Portfolio  
https://sachaitlikhi.github.io/Sachait-s-Portfolio/

---

