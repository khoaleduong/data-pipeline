# 📊 Data Pipeline

## 📌 Project Overview

This project is an end-to-end **data pipeline** integrating social media platforms (TikTok, Facebook, YouTube, Twitter) and business sales systems into a centralized **Google BigQuery** data warehouse.

The objective is to transform raw, unstructured data into clean, analytics-ready tables for real-time dashboards and insights using **Power BI** or **Tableau**.

---

## ✨ Features

- ✅ Extracts data from multiple social and transactional sources  
- ✅ Cleans and stages raw data in a unified format  
- ✅ Transforms data into dimensional models with dbt  
- ✅ Builds aggregated data marts for reporting  
- ✅ Supports dashboarding with BI tools like Power BI and Tableau  

---

## 🧱 Architecture

![Pipeline Architecture](https://raw.githubusercontent.com/khoaleduong/data-pipeline/main/Architecture.png)

```plaintext
                     +-----------------------+
                     |     Data Sources      |
                     |-----------------------|
                     | TikTok, Facebook, etc |
                     | Sales DB              |
                     +-----------+-----------+
                                 |
                                 ▼
                         +--------------+
                         |   Staging    |  ← Raw data cleaned & normalized
                         +--------------+
                                 |
                                 ▼
                    +------------------------+
                    |  Business Transform    |  ← Fact & Dimension models (dbt)
                    +------------------------+
                                 |
                                 ▼
                          +-----------+
                          |  Marts    |  ← Analytics-ready tables
                          +-----------+
                                 |
                                 ▼
              +----------------------------+
              | Power BI / Tableau Reports |
              +----------------------------+
