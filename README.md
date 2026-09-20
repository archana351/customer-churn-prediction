# Customer Churn Prediction

A machine learning project that predicts whether a telecom customer is likely to **churn (leave the service)**.

## Features

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Churn prediction using Machine Learning
* SMOTE for handling imbalanced data
* Feature importance analysis
* Model performance comparison

## Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn (SMOTE)
* Google Colab / Jupyter Notebook

## Models Used

* Logistic Regression
* Decision Tree
* Random Forest
* Random Forest + SMOTE

## Best Result

Random Forest + SMOTE achieved:

* Accuracy: **77.56%**
* Precision: **57.14%**
* Recall: **78.61%**

The model focuses on **recall**, helping identify more customers who are likely to churn.

## Main Churn Factors

* Monthly Charges
* Total Charges
* Customer Tenure
* Contract Type
* Internet Service
* Payment Method

## Run the Project

```bash
git clone https://github.com/archana351/customer-churn-prediction.git
cd customer-churn-prediction
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
```

Open the notebook in **Google Colab or Jupyter Notebook** and run the cells.

## Author

**Archana**
B.E. Computer Science & Engineering
