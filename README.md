Customer Churn Prediction System

A machine learning pipeline designed to predict customer churn in the telecommunications sector and identify key risk drivers to support data-driven retention strategies.

Project Overview

Retaining existing customers is significantly more cost-effective for telecom providers than acquiring new ones. This project establishes an end-to-end predictive pipeline that flags at-risk accounts and isolates primary churn indicators.

By applying SMOTE (Synthetic Minority Over-sampling Technique), the model is optimized for high recall, ensuring that the business can identify the maximum number of potential churn cases before they occur.

Key Insights

The exploratory data analysis and feature importance evaluation revealed several critical operational insights:

First-Year Vulnerability: Customer churn is heavily concentrated within the first 12 months of tenure. Once a customer remains past the first year, their likelihood of leaving drops significantly.

Contract Structure: Customers on month-to-month terms exhibit a high correlation with churn, while long-term (1-year and 2-year) agreements act as strong retention anchors.

Fiber Optic Anomaly: Despite offering superior speeds, Fiber Optic internet service correlates positively with churn, pointing to potential issues with localized pricing, service reliability, or promotional competitor targeting.

Tech Stack

Environment: Google Colab / Jupyter Notebook

Libraries: pandas, numpy, matplotlib, seaborn

Modeling: scikit-learn

Class Imbalance: imbalanced-learn (SMOTE)

Model Performance & Evaluation

The original training data suffered from class imbalance, with only 26.5% of historical records representing churned cases. To address this, SMOTE was applied to the training partition to balance class representation and improve target recall.

Model Performance Metrics:

Logistic Regression

Test Accuracy: 80.12%

Precision: 63.85%

Recall (Catching Churn): 55.45%

Decision Tree (Depth = 5)

Test Accuracy: 78.49%

Precision: 60.10%

Recall (Catching Churn): 53.64%

Random Forest (Baseline)

Test Accuracy: 79.11%

Precision: 63.15%

Recall (Catching Churn): 49.32%

Random Forest (Optimized + SMOTE)

Test Accuracy: 77.56%

Precision: 57.14%

Recall (Catching Churn): 78.61%

Evaluation Analysis

Adjusting the training pipeline with SMOTE improved model recall by nearly 30% (from 49.32% to 78.61%).

In a proactive customer retention campaign, maximizing recall is highly prioritized. Catching 78% of churn-prone accounts allows marketing teams to deploy targeted retention offers, which yields a much higher business return than keeping overall accuracy high while missing half of the departing customer base.

Core Churn Drivers

The optimized Random Forest model identified the following top 5 features as the most influential indicators of customer churn:

Financial Pressure: Total charges and monthly charges.

Relationship Length: Shorter customer tenure.

Contract Type: Month-to-month agreement structures.

Service Type: Fiber Optic subscription issues.

Billing Preference: Electronic check payment methods (relative to automated autopay systems).

Installation and Execution

Clone the repository:

git clone https://github.com/archana351/customer-churn-prediction.git
cd customer-churn-prediction


Install dependencies:

pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn


Run the pipeline:
Open your Jupyter notebook environment, load the pipeline notebook file, and execute the cells sequentially to run the data cleaning, modeling, and visualization steps.
