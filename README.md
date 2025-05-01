Project Title: Bank Marketing Effectiveness Prediction
Project Type: Classification
Contribution: Individual
Team Member: Abhimanyu Kumar

Problem Statement
This project aims to predict whether a customer will subscribe to a term deposit product based on data from a Portuguese bank's direct marketing campaigns, which were conducted over phone calls. Often, customers were contacted multiple times. The goal is to build a classification model to predict if a customer will subscribe (output variable: y, with values 'yes' or 'no').

Project Summary
This project used machine learning to analyze and predict the success of bank marketing campaigns. The dataset included 45,211 records with 17 features, including both categorical variables (like job, marital status, education) and numerical variables (like age and balance).

Data Preparation
Missing values in columns like job, education, and contact were filled with the most frequent values.

Features with more than 50% missing values were removed.

Outliers were handled using the Interquartile Range (IQR) method.

Key Insights
Most subscriptions came from clients aged 30–36.

Blue-collar workers were less likely to subscribe, while those in managerial positions subscribed more.

Married clients were the most common subscribers, while divorced ones subscribed less.

Higher education was associated with higher subscription rates.

Clients with no credit default, no housing loans, and no personal loans were more likely to subscribe.

Cellular contacts were more effective than other methods.

Most subscriptions occurred between April and August, especially in May.

Clients who were contacted fewer than three times had higher chances of subscribing.

Longer call durations (average ~400 seconds) were linked to higher subscription rates.

Data Processing
Categorical features were encoded using label encoding; one-hot encoding was used for variables like job and month that had many categories.

The class imbalance (only 11.7% subscribed) was addressed using SMOTE (Synthetic Minority Oversampling Technique).

Features were scaled using MinMaxScaler to standardize the data.

Modeling and Results
Several models were tested, including Logistic Regression, K-Nearest Neighbors (KNN), Random Forest, and XGBoost.

Cross-validation was used to improve model reliability.

XGBoost outperformed the other models, achieving around 93% accuracy, along with high precision, recall, F1-score, and ROC AUC.

Conclusion
The XGBoost model effectively predicted which customers would subscribe to a term deposit. These insights can help the bank better target potential customers and improve marketing campaign efficiency.
