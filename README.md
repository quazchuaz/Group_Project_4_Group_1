# Group_Project_4_Group_1
Build a predictive model to predict customer churn for an e-commerce platform

# Customer Churn Prediction and Analysis

## Introduction
This project aims to predict customer churn for an e-commerce business using machine learning strategies. Customer churn, or attrition, refers to the phenomenon of customers leaving a business or discontinuing their services. It is a critical metric for businesses as it directly impacts revenue and profitability. By identifying potential churners in advance, businesses can take proactive measures to retain these customers.

In this project, we utilize logistic regression and a neural network model to predict customer churn based on various customer attributes and behaviors. The dataset used for this analysis is from an e-commerce business and contains information about customers, including their preferences, satisfaction scores, and historical transaction data. Dataset was downloaded from: https://www.kaggle.com/code/amrabdelatyfathalla/e-commerce-customer-churn-end-to-end-ml-project

## Dataset
The dataset used for this project is named "E Commerce Dataset" and is provided in an Excel format. It includes the following columns:

CustomerID: Unique identifier for each customer.
Churn: Target variable indicating whether a customer has churned (1) or not (0).
Tenure: The length of time a customer has been with the e-commerce platform.
PreferredLoginDevice: The device preferred by the customer for logging in.
CityTier: The tier of the customer's city.
WarehouseToHome: The distance from the customer's warehouse to their home.
PreferredPaymentMode: The preferred payment method chosen by the customer.
Gender: The gender of the customer.
HourSpendOnApp: The average number of hours a customer spends on the e-commerce app.
NumberOfDeviceRegistered: The number of devices registered by the customer.
PreferedOrderCat: The preferred order category chosen by the customer.
SatisfactionScore: The satisfaction score provided by the customer.
MaritalStatus: The marital status of the customer.
NumberOfAddress: The number of addresses associated with the customer.
Complain: Indicates whether the customer has ever complained (1) or not (0).
OrderAmountHikeFromlastYear: The percentage increase in order amount from the previous year.
CouponUsed: The number of coupons used by the customer.
OrderCount: The total number of orders placed by the customer.
DaySinceLastOrder: The number of days since the customer's last order.
CashbackAmount: The amount of cashback received by the customer.

## Data Preprocessing
Before building and training the predictive models, several preprocessing steps were performed on the dataset:

Handling Missing Values: Missing values in columns such as Tenure, WarehouseToHome, HourSpendOnApp, and others were imputed using iterative imputation techniques.
One-Hot Encoding: Categorical variables such as PreferredLoginDevice, PreferredPaymentMode, Gender, PreferedOrderCat, and MaritalStatus were one-hot encoded to convert them into numerical format for model training.
Splitting the Data: The dataset was split into training and testing sets, with 75% of the data used for training and 25% for testing.
Addressing Class Imbalance: To address class imbalance in the target variable (Churn), oversampling was performed on the training data.
Models and Evaluation
Three machine learning models were implemented and evaluated:

## Logistic Regression:

A logistic regression model was trained on the preprocessed data.
Key Metrics:
Accuracy: 88.78%

• The classification report indicates that the model achieved an accuracy of 88.78% on the test dataset.
• Precision measures the accuracy of positive predictions, and the model achieved a precision of 0.91 for class 0 (not churned) and 0.74 for class 1 (churned).
• Recall measures the proportion of actual positive cases correctly predicted by the model. The model achieved a recall of 0.97 for class 0 and 0.49 for class 1.
• The F1-score, which balances precision and recall, is 0.93 for class 0 and 0.59 for class 1.
• The support indicates the number of instances for each class in the test dataset (1176 for class 0 and 232 for class 1).
The confusion matrix further breaks down the model's performance:

There are 1136 true negatives (customers correctly predicted as not churned).
There are 40 false positives (customers incorrectly predicted as churned when they are not).
There are 118 false negatives (customers incorrectly predicted as not churned when they have churned).
There are 114 true positives (customers correctly predicted as churned).
The model excels in correctly classifying customers who did not churn (high true negatives), but there is room for improvement in identifying customers at risk of churning (low true positives and high false negatives).

while the Logistic Regression model demonstrates good overall accuracy, a deeper analysis of the classification report and confusion matrix highlights areas where the model may benefit from optimization, especially in correctly identifying customers who have churned. Hence our group decided to explore other machine learning Models

## Neural Network:

A neural network model with hyperparameter optimization was trained on the preprocessed data.
Hyperparameter Tuning: Hyperband optimization was used to find the best hyperparameters.
Key Metrics:
Accuracy: 98.30%

## Conclusion
The machine learning models developed in this project provide valuable insights into customer churn prediction for the e-commerce business. The logistic regression model achieved an accuracy of 88.78%, while the neural network model with hyperparameter optimization achieved an accuracy of 98.30%. The high accuracy of the neural network model suggests that it is a promising approach for customer churn prediction.

Understanding and predicting customer churn can help businesses take proactive measures to retain valuable customers and improve overall customer satisfaction. This project demonstrates the potential of machine learning in identifying and addressing customer churn in e-commerce businesses. Further analysis and fine-tuning of models can lead to even more accurate predictions and actionable insights.
