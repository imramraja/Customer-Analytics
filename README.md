# Customer Analytics — End-to-End Analysis

**Author:** Ramraja Yadav  
Delhi NCR, India  
GitHub: https://github.com/imramraja  

This project performs an end-to-end analysis of an e-commerce transaction dataset to understand customer behavior, revenue patterns, and customer value. The analysis includes data cleaning, exploratory data analysis (EDA), cohort retention analysis, RFM segmentation, clustering, and a simple machine learning model to identify high-value customers.

---

# Project Objective

The main goal of this project is to explore retail transaction data and answer important business questions such as:

- Which countries and products generate the most revenue?
- How does revenue change over time?
- How concentrated is revenue among customers?
- How well does the business retain customers over time?
- Which customers are the most valuable?
- Can we predict high-value customers using machine learning?

---

# Dataset

The dataset contains retail transaction records where each row represents a purchased product within an invoice.

Main columns:

| Column | Description |
|------|-------------|
| Invoice | Unique invoice number |
| StockCode | Product identifier |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date and time of transaction |
| Price | Price per unit |
| Customer_ID | Customer identifier |
| Country | Customer location |

---

# Workflow

## 1. Data Loading
Load the dataset and inspect its structure, data types, and basic statistics.

## 2. Data Cleaning
Several cleaning steps are applied:

- Remove missing customer IDs
- Remove duplicate rows
- Remove cancelled transactions
- Remove negative quantities and invalid prices
- Handle extreme values using percentile capping

A cleaned revenue feature is created to reduce the effect of extreme outliers.

---

## 3. Feature Engineering

Additional features are created from the transaction timestamp:

- Invoice month
- Invoice week
- Day of week
- Hour of purchase

These features help analyze purchasing patterns and seasonality.

---

## 4. Exploratory Data Analysis

EDA is performed to answer key business questions:

- Monthly revenue trend
- Top countries by revenue
- Top products by revenue
- Distribution of invoice values

Charts are used to visualize trends and patterns.

---

## 5. Revenue Concentration (Pareto Analysis)

Customer revenue distribution is analyzed using Pareto principles.

Metrics calculated include:

- cumulative revenue share
- top customer contribution
- approximate Gini coefficient

This helps understand how much revenue is driven by a small group of customers.

---

## 6. Cohort Retention Analysis

Customers are grouped based on their **first purchase month**.

A cohort retention heatmap shows:

- how many customers return in later months
- how retention decreases over time

This analysis helps identify opportunities to improve repeat purchases.

---

## 7. Customer Lifetime Features

Customer-level features are created such as:

- total orders
- total revenue
- average order value
- customer lifetime duration

These features help measure customer value.

---

## 8. RFM Customer Segmentation

Customers are segmented using the **RFM framework**:

- **Recency** — how recently the customer purchased  
- **Frequency** — how often the customer purchases  
- **Monetary** — how much the customer spends  

Customers are categorized into segments like:

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Hibernating
- Lost

This helps prioritize retention and marketing strategies.

---

## 9. Customer Clustering

K-Means clustering is applied to RFM features to create data-driven customer segments.

This provides an alternative segmentation approach compared to rule-based RFM segmentation.

---

## 10. Machine Learning

A simple machine learning model is built to identify high-value customers.

Steps include:

- defining a high-value customer target
- training a Random Forest classifier
- evaluating model performance
- basic hyperparameter tuning

---

# Key Insights

Some important observations from the analysis include:

- Revenue is highly concentrated among a small number of customers.
- A few products generate a large portion of total sales.
- Customer retention drops significantly after the first purchase month.
- RFM segmentation clearly identifies high-value and at-risk customers.

These insights can help guide marketing strategies and customer retention efforts.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---
