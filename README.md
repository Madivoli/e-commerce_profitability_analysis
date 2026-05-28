𝗕𝗿𝗶𝗴𝗵𝘁𝗖𝗮𝗿𝘁 𝗣𝗿𝗼𝗳𝗶𝘁𝗮𝗯𝗶𝗹𝗶𝘁𝘆 𝗔𝗻𝗮𝗹𝘆𝘀𝗶𝘀


# E-Commerce Customer Behavior & Transaction Analytics

## 📌 Project Overview
This repository contains an end-to-end data analytics project evaluating e-commerce transactional data. The objective is to engineer a clean data pipeline from raw, unstandardized purchase logs into an interactive executive dashboard that surfaces insights on customer lifetime value (CLV), cohort retention, and seasonal purchasing patterns.

---

## 📂 Project Structure & Code Artifacts
To explore the technical implementation of this pipeline and visualization layers, access the files directly via the links below:

*   **Data Engineering & Pipelines:**
    *   [Python Data Cleaning Notebook](./scripts/ecommerce_cleaning_pipeline.ipynb) — *The complete automated data pipeline used for handling missing values, standardizing datetime objects, and extracting feature variables (e.g., Cohort Month, Total Order Value).*
*   **Data Layers:**
    *   [Raw Transaction Dataset](./data/raw_ecommerce_transactions.csv) — *The uncleaned, raw transactional ledger containing initial format discrepancies and missing customer identifiers.*
    *   [Processed & Cleaned Dataset](./data/cleaned_ecommerce_transactions.csv) — *The optimized, structurally sound dataset engineered for direct ingestion into Tableau Desktop.*
*   **Business Intelligence & Dashboards:**
    *   [Tableau Workbook (Packaged)](./dashboards/ecommerce_executive_analytics.twbx) — *The interactive workbook containing executive-ready visual stories, cohort matrices, and sales distribution models.*

---

## 🛠️ Data Pipeline Architecture (Python Implementation)
The data cleaning process achieved the following data-quality benchmarks:
1. **Handling Missing Values:** Imputed missing values or dropped incomplete transaction strings where critical identifiers (e.g., `Customer ID`) were missing.
2. **Feature Engineering:** Extracted `Order Month`, calculated `Total Spend per Invoice` ($Quantity \times UnitPrice$), and parsed geographic location markers.
3. **Outlier Mitigation:** Filtered out negative quantities (returns/cancellations) into a dedicated returns dataframe to keep the core sales metrics pristine.
