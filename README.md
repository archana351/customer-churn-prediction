# customer-churn-prediction
Customer Churn Prediction System

🚀 A Day-by-Day End-to-End Machine Learning Project targeting Telecom Customer Retention.

📌 Project Overview

Customer churn occurs when customers stop doing business with a company. For telecom providers, acquiring new customers costs significantly more than retaining existing ones. This project builds an end-to-end predictive pipeline that identifies at-risk customers, isolates key churn drivers, and provides actionable business recommendations using optimized machine learning classifiers.

By deploying techniques like SMOTE (Synthetic Minority Over-sampling Technique), this model shifts focus to high Recall to catch maximum churn instances before they happen.

📈 Key Business Insights & EDA

During our Exploratory Data Analysis (EDA) and Feature Importance extraction, several critical patterns emerged:

The First-Year Volatility: Customer churn is heavily concentrated within the first $12$ months of tenure. If a customer stays past year one, their likelihood of leaving drops drastically.

Contract Type is King: Customers on month-to-month contracts exhibit an incredibly high correlation with churn, whereas long-term ($1$-year and $2$-year) contracts act as strong retention anchors.

The Fiber Optic Paradox: While Fiber Optic internet offers the fastest speeds, it correlates positively with churn—indicating potential issues with pricing, service reliability, or competitor promotions in that segment.

🛠️ Tech Stack & Libraries

Environment: Google Colab / Jupyter Notebook

Data Manipulation: pandas, numpy

Visualization: matplotlib, seaborn

Machine Learning Framework: scikit-learn

Imbalanced Data Handling: imbalanced-learn (SMOTE)

📊 Model Performance & SMOTE Impact

Our initial baseline models struggled to predict churned customers accurately due to class imbalance (only $\approx 26.5\%$ of the historical dataset represented churned customers). Applying SMOTE on our training partition successfully resolved this issue and significantly boosted model Recall (our primary target metric for retention).

Classifier Model

Test Accuracy

Precision

Recall (Catching Churn)

Logistic Regression

$80.12\%$

$63.85\%$

$55.45\%$

Decision Tree (Depth = 5)

$78.49\%$

$60.10\%$

$53.64\%$

Random Forest (Baseline)

$79.11\%$

$63.15\%$

$49.32\%$

Random Forest (Optimized + SMOTE)

$77.56\%$

$57.14\%$

$78.61\%$ 🚀

Why this is a Massive Success:

While overall accuracy dropped slightly, our Recall jumped by nearly $30\%$ (from $49.32\%$ to $78.61\%$). In a customer retention scenario, catching $78\%$ of customers planning to leave is infinitely more valuable to business stakeholders than maintaining high overall accuracy while letting half of the departing customers slip through the cracks unnoticed.

🧬 Feature Importance (Top Drivers)

The Random Forest model identified the following top 5 features influencing customer churn:

Total Charges / Monthly Charges: Cost pressures directly accelerate churn.

Tenure: Shorter customer relationship length increases volatility.

Contract Type (Month-to-Month): Flexible terms allow low-barrier departures.

Internet Service (Fiber Optic): Highlights potential service-to-price dissatisfaction.

Payment Method (Electronic Check): High correlation compared to automated autopay systems.

🚀 How to Run this Project

Clone the Repository:
(Verify your GitHub username is spelled correctly in the URL below)

git clone [https://github.com/archana351/customer-churn-prediction.git](https://github.com/archana351/customer-churn-prediction.git)
cd customer-churn-prediction


Open in Google Colab or Jupyter:
Upload the Customer_Churn_Prediction.ipynb notebook directly to Google Colab or run it locally using Jupyter.

Install Dependencies:

pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn


Execute all cells to see the raw data pull, automated cleaning pipeline, SMOTE balancing, comparative model metrics, and feature visualizations.

💼 Resume Highlight

Customer Churn Prediction System (Machine Learning)

Developed an end-to-end predictive pipeline using Logistic Regression and Random Forest algorithms on a $7{,}000+$ customer telecom dataset to identify at-risk accounts.

Implemented SMOTE oversampling on the training partition to resolve extreme class imbalance, successfully scaling minority-class Recall from $49.32\%$ to $78.61\%$.

Extracted Random Forest feature importances to deliver key business insights, identifying contract structures and tenure as primary churn drivers to support retention campaign design.
