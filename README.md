# Supply Chain Analysis Using Spark

This repository contains the code and analysis for a supply chain optimization project conducted as part of the final project for IST 718: Big Data Analytics. The project aims to analyze DataCo Global's supply chain data to predict and mitigate late deliveries, as well as to provide actionable insights for improving operational efficiency and customer satisfaction.

## Project Overview

In this project, we use PySpark to analyze a dataset sourced from Kaggle that contains 180,000 rows and 53 columns of supply chain-related information, including transaction, financial, customer, order, product, and shipping data. Our main objective is to assess the risk of late deliveries and suggest optimizations in the supply chain.

**Group Members:**
- Elizabeth Jones
- Tia Jones
- Kishan Polekar
- Prabin Raj Shrestha

## Key Features of the Project

- **Data Cleaning**: Handled missing values, standardized column names, and created new columns like `late_days` and `Late_Delivery` to facilitate our analysis.
  
- **Exploratory Data Analysis**: We explored various factors such as delivery time discrepancies, order statuses, payment types, and shipping modes to understand patterns in the supply chain.

- **Modeling**: We used logistic regression and random forest models to predict the likelihood of late deliveries. Our logistic regression model performed significantly better, with an accuracy of 81%, a precision of 80%, and a recall of 76%.

## Data Description

The dataset contains the following key information:
- **Transaction Details**: Type of transaction, real and scheduled shipping days.
- **Financial Information**: Benefit per order, sales per customer.
- **Customer Information**: City, country, and other demographics.
- **Order Information**: Product category, discount rates, sales, and profit margins.
- **Shipping Information**: Shipping date, mode, and delivery time details.

### Key Findings

- **Delivery Time Discrepancies**: We found that predicted delivery times (0-4 days) were often optimistic compared to actual delivery times (0-6 days), with an average discrepancy of 1 day.
- **Order Status**: Most orders were marked as "Complete" or "Pending Payment," with over 50% of the orders completed successfully.
- **Shipping Mode**: Courier services showed more significant delays, especially for late deliveries.

### Model Performance

The logistic regression model was the top-performing model in predicting late deliveries:
- **Accuracy**: 0.81
- **Precision**: 0.80
- **Recall**: 0.76
- **F1 Score**: 0.78
- **AUC**: 0.81

Top predictive features included scheduled shipping days, order item discount rate, and shipping mode.

### Interesting Results

We found that despite orders being canceled, the company was still making an average of $20 in revenue per canceled order. Additionally, first-class shipping often led to unexpected delays, primarily for orders placed on Sundays.

## Technologies Used

- **PySpark** for large-scale data processing and analysis.
- **Logistic Regression and Random Forest** for predictive modeling.
- **Kaggle Supply Chain Dataset** as the data source.

## How to Run

1. Install PySpark and other dependencies:
   ```bash
   pip install pyspark
   ```
2.	Clone this repository:
   ```bash
   git clone https://github.com/Prbn/Supply-Chain-Analysis.git
   ```
   
3.	Run the analysis notbooks

## Conclusion

Through comprehensive data analysis and predictive modeling, this project provides valuable insights into DataCo Global’s supply chain operations. These findings can help the company make informed decisions to reduce late deliveries, optimize shipping methods, and enhance customer satisfaction.

   

   
