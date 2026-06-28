


# E-Commerce Customer Behavior & Transaction Analytics

## 📌 Project Overview
This repository contains an end-to-end data analytics project evaluating e-commerce transactional data. The objective is to engineer a clean data pipeline from raw, unstandardized data (order, marketing, and product logs) into an interactive executive dashboards and visualizations that surfaces insights on net profit margin, return & discount rates, return on advertisement spend (ROAS), cost per acquisition (CPA), cost per click (CPC), revenue & cost leakages, marketing attribution patterns, and so on.

---

## 📂 Project Structure and Code Artifacts
To explore the technical implementation of this pipeline and visualization layers, access the files directly via the links below:

*   **Data Engineering and Pipelines:**
    *   *The complete automated data pipeline used for handling missing values, standardizing datetime objects, downcasting integer columns to memory-efficient types, and creating & saving database*:
    *    [Python Data Cleaning Notebook](./scripts/orders.ipynb)
    *    [Python Data Cleaning Notebook](./scripts/ecommerce_cleaning_pipeline.ipynb)
    *    [Python Data Cleaning Notebook](./scripts/ecommerce_cleaning_pipeline.ipynb) 
*   **Data Layers:**
    *   [Raw Transaction Dataset](./data/raw_ecommerce_transactions.csv) — *The uncleaned, raw transactional ledger containing initial format discrepancies and missing customer identifiers.*
    *   [Processed & Cleaned Dataset](./data/cleaned_ecommerce_transactions.csv) — *The optimized, structurally sound dataset engineered for direct ingestion into Tableau Desktop.*
*   **Business Intelligence and Dashboards:**
    *   [Tableau Workbook (Packaged)](./dashboards/ecommerce_executive_analytics.twbx) — *The interactive workbook containing executive-ready visual stories, cohort matrices, and sales distribution models.*

---

## 🛠️ Data Pipeline Architecture (Python Implementation)
The data cleaning process achieved the following data-quality benchmarks:
1. **Handling Missing Values:** Imputed missing values or dropped incomplete transaction strings where critical identifiers (e.g., `Customer ID`) were missing.
2. **Feature Engineering:** Extracted `Order Month`, calculated `Total Spend per Invoice` ($Quantity \times UnitPrice$), and parsed geographic location markers.
3. **Outlier Mitigation:** Filtered out negative quantities (returns/cancellations) into a dedicated returns dataframe to keep the core sales metrics pristine.
