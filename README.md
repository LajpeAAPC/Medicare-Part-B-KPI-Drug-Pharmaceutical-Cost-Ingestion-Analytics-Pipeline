# Medicare KPI Drug Cost & Pharmaceutical Analytics Pipeline
<img width="996" height="470" alt="Image" src="https://github.com/user-attachments/assets/0ddd997e-aa2e-4d2b-b11d-e0f39cb462c6" />

## 📌 Project Overview
This **KPI Dashboard** project reveals **Drug Code J0178** drives a staggering **$1.76 Billion** in direct federal Medicare payouts, commanding the **highest financial footprint in the entire dataset!** It uses an end-to-end data engineering and analytics pipeline using CMS Medicare Part B 2024 National Summary data and focuses specifically on **Non-Chemotherapy Drugs (J-Codes J0000 - J8499)**. 

## 💡 Key Analytical Insight:
Out of hundreds of specialized medications, a single formulation—**Drug Code J0178**—drives **$1.76 Billion** in direct federal Medicare payouts, the **highest in the entire dataset. Drug Code J0178 refers to “aflibercept (brand name Eylea).** A drug that treats diabetic eye conditions.

## 🛠️ Tech Stack & Analytical Skills
**Link for SQL File & SQL Queries:**
https://github.com/LajpeAAPC/Medicare-Part-B-KPI-Drug-Pharmaceutical-Cost-Ingestion-Analytics-Pipeline/blob/main/SQL%20queries.sql

**Link for PYTHON EDA & Data Cleaning:** https://github.com/LajpeAAPC/Medicare-Part-B-KPI-Drug-Pharmaceutical-Cost-Ingestion-Analytics-Pipeline/blob/main/EDA%20Cleaning%20KPI%20Drug%202026

- **Data Pipeline & Engineering:** Python (`pandas`, `numpy`, `openpyxl`, `sqlite3`)
- **Database Architecture & Querying:** SQL / SQLite (Advanced Aggregations, Conditional Logic, Type Casting)
- **Business Intelligence & Reporting:** Tableau Public (Executive BAN KPI Dashboards, Custom Dynamic Ratios)
- **Core Competencies Showcase:** Data Quality Auditing, Schema Normalization, Financial Data Analysis

## 🛢️ Data Engineering Pipeline & Integrity Auditing
Raw healthcare administration files frequently have complex layout barriers that break downstream analytical models. This pipeline implements strict institutional validity controls to clean and reduce **1,420 raw records down to 535 highly audited data rows**. The data pipeline takes unstructured enterprise spreadsheets, fixes severe data quality anomalies, handles a local relational database migration, and reveals operational expenditure drivers via an interactive executive dashboard.:

1. **Dynamic Schema Alignment:** Bypassed unstructured text disclaimer cells and layout noise by mapping multi-row text metadata headers to expose true table arrays on row index 3.
2. **De-duplication & Inflation Controls:** Detected and eliminated hidden nested duplicate summary rows (`modifier != 'TOTAL'`). This crucial data quality audit **prevented a 100% inflation error** across aggregate financial metrics.
3. **Type Enforcement & Casting:** Restructured unformatted object strings into clean numeric primitives (`FLOAT`) to enable reliable mathematical calculation.
4. **Outlier Mitigation:** Audited and purged zero-value transaction streams and negative service anomalies to safeguard dataset validity.

## 🔍 Production SQL Business Insights
To model enterprise-scale operations, a local relational database layer was constructed to run analytical audits across millions of implied transaction units:

- **Financial Volatility Mapping:** Structured aggregation scripts to identify systemic market spending outliers, exposing the massive micro-level scale of top tier medications.
- **System Scale Optimization:** Engineered `CAST(allowed_services AS BIGINT)` routines into the script architecture to protect calculation strings from memory truncation errors over multi-billion-dollar columns.
- **Sub-Category Segmentation:** Deployed string manipulation filters (`LIKE 'J01%'`) to instantly segment early-stage injection profiles from bulk datasets.

## 📊 Business Intelligence & Executive Deliverables
The audited dataset was exported as an optimized flat file and piped directly into an interactive executive interface built on Tableau Public.

- **Interactive Executive Dashboard:**
  https://public.tableau.com/authoring/MedicarePartBKPIDrugSpendLiability/Dashboard1#1
  
<img width="996" height="470" alt="Image" src="https://github.com/user-attachments/assets/0ddd997e-aa2e-4d2b-b11d-e0f39cb462c6" />
  
- **Core Business Metrics Tracked (3 BAN Layout):**
  - **Total Approved Charges:** Captures the macro-level economic footprint approved for specialized drug distribution.
  - **Total Medicare Payouts:** Isolates actual paid-out government capital liability to map public insurance dependencies.
  - **Medicare Coverage Ratio:** An advanced, engineered custom business ratio (`SUM([Payment]) / SUM([Allowed Charges])`) designed to show exactly what percentage of costs the government covers versus what financial cost is covered by the patient.

