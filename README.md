# 🛒 Retail Giant Analytics Dashboard (2017-2018)

![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

## 📊 Project Overview
An end-to-end Power BI business intelligence solution designed to analyze retail operations. This project transforms raw data into a strategic tool for monitoring sales, customer demographics, and store efficiency.

---

## 🖼️ Dashboard Preview

### 1. Sales Performance Overview
Focuses on high-level KPIs and temporal trends to track growth.
![Sales Overview](sales.png)

### 2. Customer Segmentation
Deep dive into who the customers are, their income levels, and purchasing habits.
![Customer Insights](customers.png)

### 3. Product & Returns Analysis
Inventory-focused page to identify "Star" products and high-return risks.
![Product Analysis](products.png)

### 4. Store Operations & Efficiency
Mapping stores and measuring revenue density per square foot.
![Store Performance](stores.png)

---

## 🛠️ Technical Workflow

### 1. Data Engineering (Power Query)
* **Data Append:** Merged `Sales 2017` and `Sales 2018` into a unified Fact table.
* **ETL:** Standardized data types and cleaned nulls in customer records.
* **Calendar Table:** Created a custom DAX Calendar for advanced Time Intelligence.

### 2. Data Modeling
* **Schema:** Implemented a **Star Schema** for optimal performance.
* **Relationships:** 1:Many relationships between Dimensions (`Customers`, `Products`, `Stores`) and Fact tables (`Sales`, `Returns`).

### 3. Advanced DAX Measures
Selected calculations used in this report:
* **Total Revenue:** `SUMX(Sales, Sales[quantity] * RELATED(Products[price]))`
* **Profit Margin:** `DIVIDE([Total Profit], [Total Revenue], 0)`
* **Return Rate:** `DIVIDE(SUM(Returns[quantity]), [Total Quantity])`

---

## 🚀 Key Business Insights
* **Profitability:** Identified the top 10 products contributing to 40% of the total margin.
* **Customer Persona:** Discovered that middle-income customers with "Graduate" degrees are the highest frequent buyers.
* **Efficiency:** Smaller "Grocery" store types showed higher **Sales per Sqft** compared to large Supermarkets.

---

## 📬 Contact & Portfolio
**Created by:** [Mohamed Elkomy]  
**Tools:** Power BI Desktop, Power Query, DAX.
