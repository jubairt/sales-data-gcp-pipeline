# 🛒 Sales Data Pipeline using Google Cloud

This project implements a complete sales data pipeline using **Google Cloud Platform (GCP)**. It allows users to upload sales data via a **Flask web app**, stores the files in **Google Cloud Storage**, and automatically loads them into **BigQuery** via **Cloud Functions**. The final insights are visualized in an interactive **Looker Studio dashboard**.

---

## 📌 Project Overview

**Objective:** Automate the process of uploading, storing, transforming, and analyzing sales data using GCP’s cloud-native tools.

**Technologies Used:**
- 🐍 Python (Flask App & ETL Logic)
- ☁️ Google Cloud Functions (Serverless Compute)
- 🗃 Google Cloud Storage (Object Storage)
- 📊 BigQuery (Data Warehouse)
- 📈 Looker Studio (Visualization)

---

## 🧱 Architecture

![Web App Overview](https://github.com/jubairt/sales-data-gcp-pipeline/blob/main/WepPage.png)
*Flask Web App for Uploading Sales Files*

![Sales Summary Dashboard](https://github.com/jubairt/sales-data-gcp-pipeline/blob/main/Dashboard/SalesSummary.png)
*Looker Studio - Sales Summary View*

![Sales Detailed Dashboard](https://github.com/jubairt/sales-data-gcp-pipeline/blob/main/Dashboard/SalesDetailed.png)
*Looker Studio - Sales Detailed View*

---

## 🔄 Pipeline Steps

### 1. **File Upload via Flask Web App**
- Users upload `.csv` sales files from their local system.
- The app provides an easy interface and organizes the uploads for each country.

### 2. **Storage in Google Cloud Storage**
- Uploaded files are sent directly to a designated GCS bucket.
- Files include:
  - `data.csv`, `ISR_data.csv`, `Japan_data.csv`, `Spain_data.csv`, `UK_data.csv`, `USA_data.csv`

### 3. **ETL Trigger with Google Cloud Function**
- A Cloud Function is triggered automatically on file upload.
- It reads the CSV from GCS and loads it into BigQuery tables.
- Table: `sales_data.sales_summary` or respective country-specific datasets.

### 4. **Data Analytics with BigQuery**
- BigQuery enables fast, SQL-based queries over large volumes of structured sales data.
- Supports both global and country-wise analysis.

### 5. **Visualization with Looker Studio**
- Looker Studio dashboards connect to BigQuery datasets.
- Users can filter by country and Invoice NO.
  
---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| `app.py` | Flask web app to upload sales files |
| `index.html` | Frontend form for file uploads |
| `function.py` | Google Cloud Function to load CSVs into BigQuery |
| `requirements.txt` | Python package dependencies |
| `data.csv`, `ISR_data.csv`, etc. | Example data files |
| `WebPage.png` | Flask app interface screenshot |
| `SalesSummary.png` | Sales summary dashboard image |
| `SalesDetailed.png` | Sales detailed dashboard image |

---

## ✅ Conclusion

This project showcases the end-to-end automation of a real-world **sales data pipeline** using GCP services. From a user-friendly Flask web app to automated ingestion and BigQuery analysis, the system is designed to be scalable, efficient, and insightful.

Whether you're building an internal analytics tool, a business intelligence dashboard, or exploring GCP’s ETL capabilities, this project offers a hands-on foundation for cloud-native data engineering. 

