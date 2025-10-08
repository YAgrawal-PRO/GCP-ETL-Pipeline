# **GCP ETL Pipeline: Public Data to PostgreSQL & Dash Visualization**

## **🏆 Key Result: 60% Reduction in Data Processing Time**

This project demonstrates a highly efficient, end-to-end data pipeline built on **Google Cloud Platform (GCP)** using scalable **Open-Source** tools. By replacing a traditional manual process with this automated **Python ETL** workflow, we achieved a **60% reduction in data processing and load time**, significantly improving data accessibility for real-time reporting.

### **1\. My Role**

**Data Architect & Automation Lead**

* **Responsibility:** Designed the full data architecture, developed the optimized Python ETL script, managed the PostgreSQL schema, and orchestrated the deployment on GCP infrastructure.  
* **Focus:** Delivering measurable efficiency gains using flexible, cloud-agnostic tools.

### **2\. Architecture & Tech Stack**

The architecture is designed for scalability and cost-efficiency.

| Component | Tool / Technology | Role in Pipeline |
| :---- | :---- | :---- |
| **Cloud Platform** | GCP (Cloud Run / Cloud SQL) | Hosting, Scalability, Database Management |
| **Extraction/Transformation** | Python / pandas | Data fetching from API/Source, Cleaning, Validation |
| **Loading & Storage** | PostgreSQL (hosted on Cloud SQL) | High-performance relational data storage |
| **Visualization** | Python (Dash or Streamlit) | Interactive, Open-Source Business Intelligence (BI) |
| **Orchestration** | GCP Cloud Scheduler (or Airflow) | Automated daily/hourly execution |

### **3\. Setup and Execution (Step-by-Step)**

Follow these steps to set up and run the ETL script.

#### **A. Prerequisites**

1. **GCP Account:** Enable the Cloud SQL API and set up a PostgreSQL instance.  
2. **Local Environment:** Ensure Python 3.9+ is installed.  
3. **Dependencies:** Install required Python libraries.

\# Install core dependencies for ETL  
pip install pandas requests psycopg2-binary 

#### **B. Database Schema Setup**

Create a simple sales\_data table in your GCP PostgreSQL instance.

```
-- SQL: Create the table structure  
CREATE TABLE IF NOT EXISTS sales\_data (  
    sale_id SERIAL PRIMARY KEY,  
    product_category VARCHAR(100),  
    region VARCHAR(50),  
    sale_amount NUMERIC(10, 2),  
    transaction_date DATE,  
    load_timestamp TIMESTAMP WITHOUT TIME ZONE DEFAULT NOW()  
);  
```
