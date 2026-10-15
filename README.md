# 📊 Business Intelligence & ERP Data Analytics Portfolio

## 📌 Overview
This repository serves as a portfolio of my work as a **Data Analyst / BI Developer**. It showcases my ability to extract raw data from enterprise systems (ERPNext, MES), transform it using complex SQL queries, and build highly actionable Business Intelligence dashboards using **Apache Superset** and **Power BI**.

The dashboards below were designed to solve real-world business challenges in Finance, Supply Chain, and Inventory Management, adhering to the Single Source of Truth principle.

---

## 💼 1. Financial Analytics: Accounts Receivable & Payable (AR/AP)
**Objective:** Provide the CFO and Executive team with a real-time overview of cash flow health, outstanding debts, and risk of bad debts.

**Technical Implementation:**
- Modeled data from ERPNext's General Ledger and Sales/Purchase Invoices.
- Built SQL Views to calculate aging buckets dynamically (31-60 days, 61-90 days, >90 days).
- Utilized **Big Number with Trendline** for overall outstanding amounts, **Gauge Charts** for overdue percentages, and **Stacked Bar Charts** for customer/supplier breakdowns.

### 📈 AR/AP Aging Dashboard
> <img width="1629" height="737" alt="image" src="https://github.com/user-attachments/assets/5aea6be2-9aad-45cb-b554-c04fc63e6692" />

![AR AP Dashboard](link_chi_toi_image_bc2f9c.png_cua_ban)

**Key Insights Delivered:**
- Instantly highlights high-risk customers with long-overdue payments (e.g., >90 days).
- Balances the view between cash inflow (AR) and cash outflow (AP) obligations.

---

## 📦 2. Supply Chain & Inventory Analytics
**Objective:** Optimize inventory levels by identifying dead stock, slow-moving items, and capital tied up in warehouses.

**Technical Implementation:**
- Queried ERPNext's Stock Ledger and Bin tables to track material movements.
- Calculated inventory aging based on the last transaction date versus the current date.
- Visualized risk using **Gauge Charts** (Slow-moving ratio) and detailed **Horizontal Stacked Bar Charts** to pinpoint which exact warehouse or item group holds the oldest stock.

### 📉 Inventory Aging & Slow-Moving Stock Dashboard
> <img width="1649" height="748" alt="image" src="https://github.com/user-attachments/assets/129e71e7-b5f7-484c-9e96-cb89f4107514" />

![Inventory Dashboard](link_chi_toi_image_bc33bb.png_cua_ban)

**Key Insights Delivered:**
- Identified that a specific portion of capital (over 13 Billion VND) is tied up in slow-moving stock (>90 days).
- Enabled warehouse managers to drill down into specific item groups (e.g., "Nhóm Nguyên Vật Liệu") that require immediate liquidation or usage strategies.

---

## 🛠️ Data Architecture & SQL Engineering
Behind these visualizations lies a robust data architecture:
- **Data Source:** PostgreSQL / MariaDB (ERPNext & MES).
- **Medallion Architecture:** Transformed raw transactional data (Bronze) into curated, business-ready SQL Views (Gold) directly on the Production environment.
- **SQL Techniques:** Extensively used `CTEs`, `Window Functions`, and `Multi-table JOINs` to ensure data accuracy and optimal query performance for live Superset dashboards.

## 📖 Superset Knowledge Base
As part of my workflow, I also compiled a comprehensive internal guide on **Apache Superset Data Visualization**, detailing chart selection strategies, deck.gl 3D geospatial mapping, and Handlebars custom UI extensions. 
*(You can view the full documentation in the files attached to this repository).*
