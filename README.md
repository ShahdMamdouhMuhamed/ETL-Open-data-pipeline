# Data Engineering Project – ETL Pipeline (CSV → Parquet → BigQuery)

##  Project Overview

This project demonstrates the design and implementation of a modern ETL (Extract, Transform, Load) pipeline. The pipeline ingests open CSV data, processes and transforms it, stores it in Parquet format, and loads it into Google BigQuery for efficient querying and analysis.

---

##  Objectives

* Build a scalable ETL pipeline
* Clean and transform raw data
* Optimize storage using Parquet format
* Load data into BigQuery
* Automate and monitor the workflow

---

##  Project Architecture

1. **Data Source:** Open CSV datasets (e.g., weather or transportation)
2. **Processing Layer:** Python (Pandas / Polars)
3. **Storage Format:** Parquet
4. **Data Warehouse:** Google BigQuery
5. **Orchestration:** Airflow / Cron Jobs

---

##  Team Members & Responsibilities

###  Menna – Data Engineer (Ingestion & Preprocessing)

* Collect raw CSV data
* Explore data schema
* Clean data (handle missing values, duplicates)
* Convert CSV to Parquet

**Tools:** Python, Pandas, Polars

---

###  Shahd – Data Transformation Engineer

* Build transformation pipeline
* Apply business logic
* Filter and structure data
* Create new features

**Tools:** Python, Pandas, Polars

---

###  Walaa – Data Validation & Quality Engineer

* Validate data accuracy and completeness
* Perform data quality checks
* Detect and handle inconsistencies

**Tools:** Python, Great Expectations

---

###  Soha – Deployment & Cloud Engineer

* Load data into BigQuery
* Schedule pipeline execution
* Manage deployment using Airflow or Cron

**Tools:** Google BigQuery, Airflow, GCP

---

###  Nada – Monitoring, Documentation & Presentation

* Monitor pipeline performance
* Implement logging and alerts
* Prepare documentation and presentation
* Demonstrate project execution

**Tools:** Python, Markdown, PowerPoint

---

##  Project Workflow

1. Data Ingestion (CSV)
2. Data Cleaning & Preprocessing
3. Data Transformation
4. Data Validation
5. Data Storage (Parquet)
6. Data Loading (BigQuery)
7. Scheduling & Automation
8. Monitoring & Reporting

---

##  Project Structure

```
project/
│── data/
│── ingestion/
│── transformation/
│── validation/
│── deployment/
│── monitoring/
│── docs/
│── README.md
```

---

##  How to Run the Project

1. Clone the repository:

```
git clone <repo-link>
```

2. Install dependencies:

```
pip install -r requirements.txt
```

3. Run the pipeline:

```
python main.py
```

4. (Optional) Run Airflow for scheduling

---

##  Expected Output

* Cleaned and transformed dataset
* Parquet files
* Data loaded into BigQuery
* Query-ready tables

---

##  Future Improvements

* Add real-time streaming (Kafka)
* Improve monitoring dashboards
* Optimize pipeline performance
* Add CI/CD integration

---

##  Deliverables

* Source Code (GitHub)
* Documentation
* Final Presentation (PPT/PDF)
* Demo of pipeline execution

---

##  Conclusion

This project provides hands-on experience in building end-to-end data pipelines, applying data engineering best practices, and working with modern data tools and cloud platforms.

------------------------------------------------------------------------------------

# Chicago Traffic Crashes ETL Pipeline

## Milestone 1: Data Collection & Preprocessing

**Dataset**: Chicago Traffic Crashes (1.067 million rows)

### Files
- `chicago_traffic_crashes_etl.ipynb` → Main notebook
- `data/chicago_traffic_crashes_cleaned.parquet` → Cleaned & optimized data (recommended to use)

### How to Use

```python
import polars as pl

# Load the cleaned data
df = pl.read_parquet("data/chicago_traffic_crashes_cleaned.parquet")
print(df.shape)
