# Task 3 : Customer Segmentation Using RFM Analysis

## 📌 Project Overview

* This project applies *RFM (Recency, Frequency, Monetary) analysis* to the **Online Retail dataset** in order to segment customers based on their purchase behavior.

* The main objective is to:
    1. Clean and preprocess the dataset.
    2. Calculate RFM scores for each customer.
    3. Segment customers into meaningful groups.
    4. Visualize the distribution of customers across segments.
    5. Suggest simple marketing idea for each segment.

* RFM analysis helps businesses identify their most valuable customers and design targeted marketing strategies (e.g., rewarding loyal customers, re-engaging inactive ones, or offering discounts to price-sensitive customers).


---

## 🔗 Data Source


The dataset is taken from the uc irvine machine learning repository 👉 [Online Retail - UCI Machine Learning repository](https://archive.ics.uci.edu/dataset/352/online+retail).

## 🛠 Data Preprocessing

Steps performed before analysis:

1. **Removed duplicates**
2. **Filtered invalid transactions** (Quantity > 0, UnitPrice > 0)
3. **Dropped missing values (NaN)**
4. **Created `TotalPrice` column** = `Quantity × UnitPrice`

---

## 📊 RFM Analysis

* **Recency (R)**: Days since last purchase &rarr; more recent = better
* **Frequency (F)**: Number of invoices &rarr; more frequent = better
* **Monetary (M)**: Total spent by customer &rarr; higher = better

### Scoring:

* Each metric (R, F, M) was divided into **10 quantiles (1–10)**.
* **R\_Score** was reversed (lower days &rarr; higher score).
* **RFM\_Score** was generated as a combination of the three scores.


###  Customer Segmentation & Possible Marketing Ideas  

| Segment            | Description                                | Suggested Marketing Idea |
|--------------------|--------------------------------------------|---------------------------|
| **Champions**      | Recent, frequent, and high spenders        | Exclusive rewards, early access to products |
| **Loyal Customers**| Frequent buyers with good recency          | Loyalty programs, personalized recommendations |
| **Potential Loyalist** | Recent and moderate spenders           | Targeted promotions to increase spending |
| **Recent Users**   | New but low spending                       | Welcome offers, onboarding campaigns |
| **Promising**      | Average on all metrics                     | Nurture with regular engagement emails |
| **Needs Attention**| High spenders but inactive                 | Re-engagement campaigns, special discounts |
| **About To Sleep** | Below average on all metrics               | Gentle reminders, win-back offers |
| **Price Sensitive**| Frequent but low spenders                  | Discounts, bundle deals |
| **Can’t Lose Them**| High spenders but inactive                 | Personalized offers, VIP treatment |
| **Hibernating**    | Rarely purchase and inactive               | Seasonal campaigns, awareness marketing |
| **Lost**           | Lowest scores in all metrics               | Low-priority segment, occasional reactivation attempts |

---

## 📈 Visualization

The final output are **bar chart** and **Heat map** showing the distribution of customers by segment.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** (data manipulation)
* **NumPy** (numeric operations)
* **Matplotlib**  (visualizations)
