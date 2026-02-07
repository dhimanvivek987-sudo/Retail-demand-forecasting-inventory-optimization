# SMART-FORECAST: Retail Demand & Inventory Optimisation

## Project Overview
SMART-FORECAST is an advanced business analytics project that demonstrates how retail demand forecasting can be converted into actionable inventory and revenue decisions.

The project analyses real-world transactional sales data consisting of more than **500,000 retail transactions** and transforms it into a **forecast-driven inventory planning framework**.  
The focus is not only on predicting demand, but on **quantifying business impact** in terms of revenue protection, inventory alignment, and stockout risk reduction.

---

## Business Problem
Retail organisations commonly plan inventory using historical average sales. In this dataset, monthly demand varies by more than **100,000 units** between low and peak periods.

This traditional approach results in:
- Understocking during high-demand months  
- Overstocking during low-demand months  
- Revenue loss due to unmet demand  
- Reactive operational decisions  

The business requires a **proactive, data-driven planning approach** that adapts inventory levels to expected demand.

---

## Project Objectives
The key objectives of this project are to:

- Clean and validate over **500,000 transactional records** using business rules  
- Identify true customer demand patterns at a **monthly planning level**  
- Forecast demand for the **next 6 months**  
- Translate forecasts into inventory recommendations with a safety buffer  
- Quantify improvement using **percentage-based KPIs**  
- Deliver a reusable decision-support framework  

---

## Dataset Information

### Dataset Name
Online Retail Dataset

### Dataset Source
UCI Machine Learning Repository  

Dataset link:  
https://archive.ics.uci.edu/ml/datasets/online+retail

---

### Dataset Description
The Online Retail dataset contains transactional data from a UK-based online retail company covering the period from **December 2010 to December 2011**.

Key characteristics of the dataset:
- Over **500,000 transaction records**
- More than **4,000 unique products**
- Transactions across **multiple countries**
- Includes cancelled invoices and product returns

Each row represents a single transaction, including invoice number, quantity sold, unit price, and transaction date.

---

### Why This Dataset Was Chosen
This dataset was selected because it reflects **real operational complexity**, including:

- Cancelled transactions (approximately **9,000 records**)  
- Product returns and corrections (over **10,000 records**)  
- Price anomalies requiring business validation  

These characteristics make it ideal for demonstrating **business-rule-based preprocessing** rather than simple data cleaning.

---

### Dataset Attributes Used in This Project

| Attribute     | Description                  | Usage in Project                    |
|--------------|------------------------------|-------------------------------------|
| InvoiceNo    | Unique invoice identifier     | Identifies cancelled transactions   |
| Quantity     | Units sold per transaction    | Measures demand volume              |
| InvoiceDate  | Transaction timestamp         | Monthly aggregation and trend       |
| UnitPrice   | Price per unit                | Revenue calculation                 |
| StockCode   | Product identifier            | Not used directly                   |
| Description | Product description           | Not used directly                   |
| CustomerID  | Customer identifier           | Not used directly                   |
| Country     | Customer country              | Not used directly                   |

---

## Data Preprocessing and Validation
Business rules were applied to ensure the dataset reflects **true customer demand**:

- Cancelled invoices (InvoiceNo starting with "C") were excluded  
- Transactions with zero or negative quantities were removed  
- Transactions with zero or negative unit prices were removed  

After preprocessing, the dataset was reduced to **valid sales transactions only**, improving demand accuracy and forecasting reliability.

---

## Demand Analysis and Growth Insights
Monthly demand analysis revealed:

- Monthly sales volumes ranging from approximately **280,000 units** to over **350,000 units**  
- A clear upward trend in demand over the analysis period  
- A peak demand increase of more than **25%** during high-sales months  

Rolling average analysis confirmed **consistent demand growth**, validating the need for forward-looking inventory planning.

---

## Forecasting Methodology
Due to the availability of approximately **13 months of historical data**, full seasonal decomposition was statistically unsuitable.

Instead:
- Trend analysis was applied using rolling averages  
- Holt’s Exponential Smoothing was selected to capture demand growth  
- Demand was forecasted for the **next 6 months**

The model predicts continued month-on-month growth in demand.

---

## Inventory Optimisation Logic
Forecasted demand was converted into inventory recommendations using a **10% safety buffer**.

This resulted in:
- Average inventory levels increasing from approximately **398,000 units** (historical average)  
- To approximately **640,000 units** (forecast-based planning)  

This increase is **strategic and demand-aligned**, not arbitrary.

---

## Before vs After Impact Analysis

### Inventory Planning
- Before: Fixed inventory based on historical average  
- After: Dynamic inventory based on monthly forecast  

### Revenue Protection
- Forecast-based planning protects approximately **12% of revenue** that would otherwise be lost due to stockouts  
- More than **1.8 million units of potential lost sales** were identified in the traditional approach  

### Risk Reduction
- Significant reduction in stockout risk during high-demand periods  
- Improved service levels and customer satisfaction  

---

## Key Results
- Inventory aligned dynamically with forecasted demand  
- Approximately **12% revenue protection achieved**  
- Clear reduction in stockout risk  
- Shift from reactive to proactive inventory planning  

---

## Reusability
The framework is designed to be reusable:

1. Replace the input sales dataset with updated data  
2. Rerun the notebook or script  
3. Automatically regenerate forecasts, inventory plans, KPIs, and dashboards  

This makes the solution suitable for continuous monthly or quarterly planning.

---

## Tools and Technologies
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Statsmodels  

---

## Business Value
This project demonstrates how analytics can be used not only to predict demand, but to **quantify decision impact** by directly linking:

Data → Forecast → Inventory → Revenue → Risk

---

## Repository Structure
