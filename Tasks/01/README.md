
# 📊 Sales Forecasting Dashboard — Task Documentation

## 📁 Excel File Overview

- **Source**: [Kaggle - Sales Forecasting](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)  
- **File Format**: Excel Workbook (.xlsx)  
- **Sheets Included**:
  1. **Original Dataset** – Raw data as downloaded from Kaggle with initial preprocessing applied
  2. **Preprocessed Dataset** – Cleaned and transformed for analysis  
  3. **Key Metrics** – Pivot table visualizations and performance indicators  
  4. **Overall Performance** – Geographic and categorical breakdowns

---

## 🧹 Data Cleaning & Preprocessing

### 🔍 Original Dataset Structure:
- **Total Columns**: 18  
- **Types of Columns**:
  - **Categorical**: 8  
  - **Date**: 2  
  - **Primary ID**: 1  
  - **Additional IDs**: 3  
  - **Numerical**: 2 (including `Sales`, the core metric)  
  - **Text**: 2  

### 🚫 Duplicate & Missing Data:
- **Duplicates**: None (verified using Excel’s “Remove Duplicates” tool)  
- **Blank Cells**: 11 (all in the `Postal Code` column, verified with `=COUNTBLANK()` formula)

### 🧼 Cleaning Summary:
- The cleaned dataset contains **10 columns**, reduced from the original 18.
- Key transformations include:
  - Extracting **month** and **year** from `Order Date`
  - Removing redundant or overly detailed columns

### ✅ Retained Columns:
- **IDs**: `Row ID`, `Order ID`
- **Categorical**: `Segment`, `Ship Mode`, `Region`, `Category`, `State`
- **Numerical**: `Sales`, `Order Month`, `Order Year`

### 🗑️ Removed Columns:
| Column           | Reason for Removal |
|------------------|--------------------|
| `Country`        | Only US data is relevant |
| `City`           | State-level analysis suffices |
| `Sub-Category`   | Focused on high-level category only |
| `Product Name`   | Too detailed for this analysis |
| `Postal Code`    | Not relevant for trend analysis |
| `Product ID`     | Redundant with category info |
| `Order Date`, `Ship Date` | Replaced with `Order Month` & `Order Year` |
| `Customer Name`, `Customer ID` | Customer is traceable through `Order ID` |

---

## 📈 Key Metrics Sheet

This sheet provides core business performance insights using **Pivot Tables**, including:

- 🔢 **Total Units Sold**
- 💵 **Total Revenue**
- 📅 **Monthly Trends**
- 📊 **Year-over-Year (YoY) Change**
- 📉 **Month-over-Month (MoM) Change**

All metrics are enhanced with **Slicers**, allowing dynamic filtering by `Category` and `Region` fields.

---

## 🌍 Overall Performance Sheet

This section focuses on geographic and categorical distribution of sales:

- 🗺️ **US Sales Map**  
  - Visualizes total sales by **state**  
  - Built from a pivot table but placed in a static table to support map creation

- 🥧 **Pie Charts for Categorical Breakdown**  
  - One for `Segment`  
  - One for `Ship Mode`  
  - Both charts are interactive and controlled by **Slicers**, which also allowing dynamic filtering by `Category` and `Region` fields.

---

## 📌 Dataset Summary

| Metric            | Value |
|-------------------|-------|
| **Total Rows**     | 9,800 |
| **Total Columns**  | 18    |
| **Duplicates**     | None  |
| **Blank Cells**    | 11 (in `Postal Code`) |
| **Source**         | [Kaggle Dataset](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting) |
