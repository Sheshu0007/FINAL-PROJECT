# 🛍️ E-commerce Return Rate Prediction Dashboard

## 📄 Abstract

This project focuses on analyzing and predicting customer return
behavior in an e-commerce environment. Using Python for preprocessing
and predictive modeling and Power BI for visualization, it identifies
major factors influencing product returns such as: - Product Category\
- Payment Method\
- Shipping Type\
- Customer Demographics

A **Logistic Regression** model predicts the probability of a return for
each order, supporting proactive decision-making and operational
efficiency. The final **Power BI Dashboard** offers actionable insights
into customer behavior, return trends, and category performance.

## 📚 Introduction

Product returns are a critical concern for e-commerce businesses,
leading to increased logistics costs, supply chain disruptions, and
reduced profit margins.\
This project integrates **data analysis**, **machine learning**, and
**business intelligence** to identify return patterns and predict future
return probabilities.\
The goal is to help companies: - Understand key drivers of product
returns.\
- Reduce return rates through data-driven strategies.\
- Optimize operations and improve customer satisfaction.

## 🧰 Tools Used

  -----------------------------------------------------------------------
  Tool                       Purpose
  -------------------------- --------------------------------------------
  **Python (Pandas, NumPy,   Data cleaning, feature engineering, and
  Scikit-learn)**            predictive modeling

  **Matplotlib & Seaborn**   Exploratory data analysis and visualizations

  **Power BI**               Interactive dashboard design and KPI
                             visualization

  **Excel / CSV**            Dataset storage and format for Power BI
                             import

  **Jupyter Notebook**       Data preprocessing and model execution
  -----------------------------------------------------------------------

## ⚙️ Steps Involved in Building the Project

### **1. Data Collection**

-   Source: CSV file (`ecommerce_returns.csv`)
-   Includes details about orders, products, customers, and
    transactions:
    -   Order details: ID, date, and return status.\
    -   Product details: Category, price, and quantity.\
    -   Customer details: Age, gender, and location.\
    -   Transaction details: Payment method, shipping type, and
        discount.

### **2. Data Preprocessing (Python)**

-   **Handling Missing Values:**
    -   Filled missing `Return_Reason` with *"No Return"*.
    -   Replaced missing `Return_Date` with *NaT* and `Days_to_Return`
        with 0.
-   **Feature Engineering:**
    -   Created `Days_to_Return_Calc = Return_Date - Order_Date`.
    -   Encoded categorical columns using `LabelEncoder`.
    -   Added binary `Returned` column (1 = Returned, 0 = Not Returned).
-   **Validation:**
    -   Removed duplicates and invalid rows (returns before order date).

### **3. Predictive Modeling**

-   **Algorithm Used:** Logistic Regression\
-   **Target Variable:** `Returned`\
-   **Feature Set:** Includes price, quantity, discount, category,
    demographics, and shipping/payment details.\
-   **Class Imbalance Handling:** Applied **SMOTE** for balanced
    training.\
-   **Model Evaluation:** Measured using Accuracy, Precision, Recall,
    F1-Score, and AUC-ROC.\
-   **Output:** Generated a `return_probability` score for each order.

### **4. Data Export & Integration**

-   Saved cleaned and processed data to `data_with_predictions.csv`.
