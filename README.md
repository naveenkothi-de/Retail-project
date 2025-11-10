This project demonstrates a Retail Data Engineering Pipeline built on Microsoft Azure, integrating multiple data sources, data lake zones, Databricks transformations and Power BI analytics.

It automates the entire data flow — from ingestion to insights — for a retail client using modern cloud data engineering practices.

Tools & Services Used:
	•	Azure Data Factory (ADF): Orchestrates data ingestion from multiple sources.
	•	Azure Data Lake Storage (ADLS): Central data repository organized into Bronze, Silver, and Gold zones.
	•	Azure Databricks: Performs transformation, cleansing, and data quality checks.
	•	Power BI: Visualizes curated Gold-layer data for analytics and business KPIs.

Architecture Flow:
	1.	Data ingested from:
	•	Azure SQL DB → Transaction, Store, and Product data
	•	REST API (JSON) → Customer data
	2.	Data loaded into ADLS (Data Lake).
	3.	Data processed through Databricks notebooks into three layers:
	• Bronze: Raw ingested data (no transformation)
	• Silver: Cleaned, joined, and validated data
	• Gold: Aggregated and business-ready data (e.g., sales summary)
	4.	Final data visualized in Power BI dashboards.

  Transformation Logic (Databricks)
	•	Mounted ADLS using dbutils.fs.mount()
	•	Read data from multiple zones using spark.read
	•	Performed data cleaning, joins, and enrichment
	•	Wrote outputs in Delta format for versioned data storage
  
Tech Stack
	•	Azure Data Factory (ETL orchestration)
	•	Azure Data Lake Storage (Gen2)
	•	Azure Databricks (Data transformation, Delta Lake)
	•	Power BI (Data visualization)
	•	Python | PySpark | SQL

 Key Outcomes

1. Automated ingestion from SQL DB and APIs
2. Structured data lake zones (Bronze → Silver → Gold)
3. Data quality and cleansing pipeline
4. Analytical dashboards for sales insights
5. Cloud-native, scalable architecture

Next Steps / Enhancements
	•	Add Data Quality Checks using Great Expectations
	•	Automate deployment via ADF triggers + CI/CD
	•	Integrate with Azure Synapse or Snowflake for advanced analytics
	•	Enable Real-time streaming with Azure Event Hub / Kafka



<img width="1280" height="800" alt="Screenshot 2025-11-09 at 10 59 30 pm" src="https://github.com/user-attachments/assets/79fe3892-f6a0-411b-8e29-344b6a69024c" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 00 10 pm" src="https://github.com/user-attachments/assets/3a2738eb-45c1-4baa-9587-14f389c935d0" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 00 21 pm" src="https://github.com/user-attachments/assets/901a6062-5d35-41c3-9e22-4bcc0e034443" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 00 45 pm" src="https://github.com/user-attachments/assets/09207153-33b0-4cc9-9fcd-01b38440eaaa" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 04 14 pm" src="https://github.com/user-attachments/assets/5c17032f-47a2-4f78-be85-e3b61be1cf70" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 04 29 pm" src="https://github.com/user-attachments/assets/a69d0e43-853f-4e63-aa41-a63f51217737" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 04 33 pm" src="https://github.com/user-attachments/assets/bb661ae3-528b-4902-bb1e-74be710154dc" />
<img width="1280" height="800" alt="Screenshot 2025-11-09 at 11 04 41 pm" src="https://github.com/user-attachments/assets/ca4093db-3355-40a3-ad43-db0177cd29e2" />

