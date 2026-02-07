# SMART-FORECAST: Retail Demand & Inventory Optimisation

## Project Overview
SMART-FORECAST is an advanced business analytics project that demonstrates how retail demand forecasting can be converted into actionable inventory and revenue decisions.

The project uses real-world transactional sales data to identify true customer demand, forecast future sales, and optimise inventory planning. Unlike basic forecasting projects, this work focuses on decision-making and measurable business value rather than model output alone.

---

## Business Problem
Retail organisations often rely on historical average sales to plan inventory. This traditional approach leads to:

- Stockouts during high-demand periods  
- Excess inventory during low-demand periods  
- Revenue loss due to unmet demand  
- Reactive and inefficient decision-making  

The business requires a forecast-driven and proactive inventory planning approach.

---

## Project Objectives
- Clean transactional data using business rules  
- Analyse monthly demand trends  
- Forecast future demand using an industry-accepted model  
- Convert forecasts into inventory recommendations  
- Measure business impact using percentage-based KPIs  
- Build a reusable analytical framework  

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
The Online Retail dataset contains transactional data from a UK-based online retail company covering the period from December 2010 to December 2011.

Each row represents a transaction and includes details such as invoice number, product information, quantity sold, unit price, transaction date, and customer identifier. The dataset also includes cancelled orders and returns, making it suitable for realistic business analytics and demand forecasting.

---

### Why This Dataset Was Chosen
This dataset was selected because:

- It represents real-world retail transactions  
- It includes business complexities such as cancellations and returns  
- It allows business-rule-based data cleaning  
- It supports time-series demand analysis  
- It is widely used in academic and industry case studies  

These characteristics make it ideal for building a practical and decision-focused forecasting framework.

---

### Dataset Attributes Used in This Project

| Attribute     | Description                   | Usage in Project                    |
|--------------|-------------------------------|-------------------------------------|
| InvoiceNo    | Unique invoice identifier      | Used to identify cancelled orders   |
| Quantity     | Number of units sold           | Used to calculate demand            |
| InvoiceDate  | Transaction date and time      | Used for monthly aggregation        |
| UnitPrice    | Price per unit                 | Used to calculate revenue           |
| StockCode    | Product identifier             | Not used directly                   |
| Description  | Product description            | Not used directly                   |
| CustomerID   | Customer identifier            | Not used directly                   |
| Country      | Customer country               | Not used directly                   |

---

### Data Preprocessing Rules Applied
The following business rules were applied before analysis:

- Cancelled invoices (InvoiceNo starting with "C") were excluded  
- Transactions with zero or negative quantities were removed  
- Transactions with zero or negative unit prices were removed  

This ensured that only valid customer demand was used for forecasting and inventory planning.

---

### Dataset Limitations and Handling
The dataset contains approximately one year of historical data, which limits full seasonal decomposition.

To address this limitation:
- Trend analysis using rolling averages was applied  
- Holt’s Exponential Smoothing was selected as a trend-aware forecasting model  

This ensured statistical validity while maintaining realistic business interpretation.

---

## Methodology
1. Data quality assessment and business-rule-based cleaning  
2. Feature engineering through revenue calculation  
3. Monthly demand aggregation  
4. Trend analysis using rolling averages  
5. Demand forecasting using Holt’s Exponential Smoothing  
6. Inventory optimisation with safety buffer  
7. Before versus After impact analysis  
8. Dashboard-style visualisation for decision support  

---

## Key Results
- Inventory aligned dynamically with forecasted demand  
- Approximately 12 percent revenue protection achieved  
- Significant reduction in stockout risk  
- Shift from reactive to proactive inventory planning  

---

## Reusability
The framework is reusable with minimal effort:

1. Replace the input dataset with updated sales data  
2. Rerun the notebook or script  
3. Forecasts, KPIs, and inventory decisions update automatically  

No redesign is required.

---

## Tools and Technologies
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Statsmodels  

---

## Business Value
This project demonstrates how analytics can directly support management decisions by linking data, forecasting, inventory planning, and financial impact into a single decision-support framework.

---

## Repository Structure
