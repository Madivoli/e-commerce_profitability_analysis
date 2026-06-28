


# BrightCart Profitability Analysis: A Deep Dive into D2C Margins and Marketing ROI

## 📌 Project Overview
This repository contains an end-to-end data analytics project evaluating e-commerce transactional data. The objective is to engineer a clean data pipeline from raw, unstandardized data (order, marketing, and product logs) into an interactive executive dashboards and visualizations that surfaces insights on net profit margin, return & discount rates, return on advertisement spend (ROAS), cost per acquisition (CPA), cost per click (CPC), revenue & cost leakages, marketing attribution patterns, and so on.

---

## 📂 Project Structure and Code Artifacts
To explore the technical implementation of this pipeline and visualization layers, access the files directly via the links below:

*   **Data Engineering and Pipelines:**
    *    [Python Data Cleaning Notebook](https://github.com/Madivoli/e-commerce_profitability_analysis/blob/main/orders.py) — *The complete automated data pipeline used for handling missing values, standardizing datetime objects, downcasting integer columns to memory-efficient types, and creating & saving database*:

*   **Data Layers:**
    *   [Raw Transaction Dataset](./data/raw_ecommerce_transactions.csv) — *The uncleaned, raw transactional ledger containing initial format discrepancies and missing customer identifiers.*
    *   [Processed and Cleaned Dataset](./data/cleaned_ecommerce_transactions.csv) — *The optimized, structurally sound dataset engineered for direct ingestion into Tableau Desktop.*
      
*   **Business Intelligence and Dashboards:**
    *   [Tableau Workbook (Packaged)](./dashboards/ecommerce_executive_analytics.twbx) — *The interactive workbook containing executive-ready visual stories, dashboards, calculated fields, and parameters.*

*   **Executive Report and Summary:**
    *   [Executive Summary](./dashboards/ecommerce_executive_analytics.twbx) — *Summary of numerous reports containing main findings and numbers, recommendations, conclusion, and call-to-action sections for management
---

## 🛠️ Data Pipeline Architecture (Python Implementation)
The data cleaning process achieved the following data-quality benchmarks:
1. **Install and Import Pandas:** Installed the Pandas modules first since it is not pre-installed in the Jupyter Notebook IDE.
2. **Loading the Data:** Loaded and read the CSV files into DataFrames. Since I was working with 3 files, I called the dataframes with readable names (orders, marketing, products).
3. **Understanding the Data:** Used the `df.info()` command to check the column, what type it is, and how many non-null values it has. 
4. **Handling Missing Values:** Checked for missing values. There were no NaN or missing values.
5. **Converting Data Types:** Converted columns (e.g., `channel`, `payment_method`, `region`) from objects/strings to categorical data types to save memory and improve speed.
6. **Saving the Clean Data:** Saved the cleaned data into a CSV file.
7. **Creating a Database:** Installed the sqlite3 module. Created and saved the cleaned dataframe into databases (orders, marketing spend, and product) for further analysis using DBeaver's (Database Management Software) SQL and Tableau.
