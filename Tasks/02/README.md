# Task 2: Exploratory Data Analysis (EDA) on the Titanic Dataset

## 📌 Overview

This task explores the **Titanic dataset** using Python to uncover survival patterns and relationships between passenger demographics and survival rates. The analysis involves data cleaning, preprocessing, descriptive statistics, group-based insights, and visualizations.

---

## 🔗 Data Source

The dataset is taken from the Kaggle competition:
👉 [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/data)

---

## 🔧 Steps Performed

### 1. Data Import & Initial Inspection

* Loaded the dataset (`train.csv`) using **pandas**.
* Removed duplicate records.
* Moved the `Survived` column to the end for better readability.

### 2. Data Cleaning & Preprocessing

* Checked for missing values (both count and percentage).
* Dropped irrelevant or incomplete columns (`PassengerId`, `Cabin`).
* Removed rows with missing values.
* Encoded categorical variables:

  * `Sex`: Male → 0, Female → 1
  * `Embarked`: C → 0, Q → 1, S → 2

### 3. Exploratory Analysis

* Summary statistics (`describe`, `nunique`, `mode`).
* Grouped survival rates by:

  * Sex
  * Passenger Class (Pclass)
  * Port of Embarkation (Embarked)
  * Family relations (SibSp, Parch)
* Built survival tables with row & column totals for deeper insights.

### 4. Visualizations

* **Pie Chart**: Overall survival distribution.
* **Bar Plots**:

  * Survival rate by Sex
  * Survival rate by Class
  * Survival rate by Port of Embarkation
* **Heatmap**: Correlation matrix of numerical variables.

---

## 📊 Key Insights

1. **Gender**: Women had significantly higher survival rates (correlation ≈ **0.54**).
2. **Class**: First-class passengers were more likely to survive (correlation with Pclass ≈ **-0.36**).
3. **Embarkation**: Most survivors boarded at **Southampton**.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** (data manipulation)
* **Matplotlib** & **Seaborn** (visualizations)
