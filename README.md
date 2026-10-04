# Customer Churn Prediction

A machine learning project that predicts whether a customer is likely to churn based on customer behavior, demographics, subscription details, and spending.

## Models

* Logistic Regression
* Random Forest

## Dataset

Customer churn dataset containing customer information such as:

* Age & Gender
* Tenure
* Usage Frequency
* Support Calls
* Payment Delay
* Subscription Type
* Contract Length
* Total Spend
* Last Interaction

`CustomerID` was removed because it is an identifier rather than a predictive feature.

## Preprocessing

* Removed missing values
* Standardized numerical features
* One-hot encoded categorical features
* Used a stratified 80/20 train-test split for the main evaluation

## Results

| Model               |  Accuracy | Precision |    Recall |  F1-score |   ROC-AUC |
| ------------------- | --------: | --------: | --------: | --------: | --------: |
| Logistic Regression |     85.0% |     86.8% |     86.1% |     86.4% |         — |
| **Random Forest**   | **93.6%** | **89.8%** | **99.7%** | **94.5%** | **95.3%** |

### Best Model

**Random Forest** achieved the best overall performance and was selected as the final model.

## Key Finding

The original training and testing files had noticeably different data distributions, which resulted in much lower performance when they were used directly. A stratified random split provided a more consistent evaluation.

## Technologies

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Jupyter Notebook

## Project Structure

```text
customer-churn-prediction/
├── data/
│   └── raw/
├── notebooks/
│   └── customer_churn_prediction.ipynb
├── src/
└── README.md
```
