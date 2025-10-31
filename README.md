# PowerCo Customer Churn Analysis

## 📘 Project Overview

**Client:** PowerCo — a major gas and electricity utility supplying small and medium-sized enterprises (SMEs).

In recent years, the energy market has become increasingly competitive, offering customers more choices than ever before. PowerCo has observed a rise in customer **churn** — when customers switch to other service providers — and has partnered with **Boston Consulting Group (BCG)** to identify the key drivers behind this behavior.

The primary hypothesis is that **price sensitivity** may be the most influential factor driving churn. This project aims to validate or refute that hypothesis using **data analysis** and **machine learning** techniques.

---

## 🎯 Objective

To determine whether **price sensitivity** is the main factor influencing customer churn, and if not, to quantify its relative influence compared to other business and customer-related features.

---

## 🧠 Business Understanding

* **Churn**: When a PowerCo customer switches to another provider.
* **Price Sensitivity**: The degree to which customer behavior changes in response to a price change, typically measured using **price elasticity of demand**:

  **Price Elasticity of Demand** = (% Change in Quantity Demanded) / (% Change in Price)

  * If |Elasticity| > 1 → The product/service is **elastic** (highly sensitive to price).
  * If |Elasticity| < 1 → The product/service is **inelastic** (less sensitive to price).

The goal is to analyze how changes in price and related factors influence whether customers remain with or leave PowerCo.

---

## 🧩 Data and Methodology

### 1. **Exploratory Data Analysis (EDA)**

* Assessed data completeness, customer demographics, and behavioral patterns.
* Identified correlations between churn and features such as **tenure**, **net margin**, **consumption**, and **contract renewal timing**.

### 2. **Feature Engineering**

* Derived new variables capturing **price sensitivity**, **tenure milestones**, and **time since last contract update**.
* Encoded categorical variables and normalized numerical data for model readiness.

### 3. **Modeling Approach**

* **Model Used:** Random Forest Classifier
* **Rationale:** Handles non-linear relationships, identifies feature importance, and performs well on structured business data.

---

## 📊 Key Insights

1. **Tenure is highly predictive of churn.**
   Customers with **4 months or less** tenure are far more likely to churn.

   * The jump between 4 and 5 months represents a **4% reduction in churn likelihood**, marking this as a critical retention milestone.

2. **Net Margin and 12-Month Consumption** are strong churn predictors.

   * Lower margins and consumption levels are associated with higher churn.

3. **Margin on Power Subscription** also plays a significant role.

   * Indicates profitability and engagement levels for each customer.

4. **Time-Related Factors** (e.g., tenure, months active, time since last contract update) are consistently influential.

5. **Price Sensitivity** is **not the primary driver** of churn.

   * While price-related features contribute to the model, they rank **lower in importance** compared to tenure, margin, and consumption.

---

## 💡 Conclusion

> **Is churn driven by customers’ price sensitivity?**

Based on the Random Forest feature importance analysis, **price sensitivity is not the main driver of customer churn**. Instead, factors related to **customer tenure, net margin, and energy consumption** dominate churn behavior.

However, **price sensitivity still plays a secondary role**, and further experimentation with advanced modeling and segmentation may help clarify its impact on specific customer groups.

---

## ⚙️ Tools and Technologies

* **Python**, **Pandas**, **NumPy**, **Scikit-learn**, **Matplotlib**, **Seaborn**
* **Random Forest Classifier**
* **EDA and Feature Engineering** for insight generation
* **Jupyter Notebook** for development and analysis

---

## 🏁 Next Steps

* Perform **segmented churn analysis** to explore whether price sensitivity varies across customer types.
* Incorporate **contract type** and **pricing plan** details for deeper price-behavior relationships.
* Test alternative models such as **XGBoost** or **Logistic Regression** for interpretability and validation.
* Develop an **early churn prediction dashboard** for PowerCo to proactively retain at-risk customers.
