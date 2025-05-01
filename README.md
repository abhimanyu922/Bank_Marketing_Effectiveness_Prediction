
Project Title: Bank Marketing Effectiveness Prediction
Project Type: Classification
Contribution: Individual
Team Member: Abhimanyu Kumar

Problem Statement
The main goal of this project was to predict whether a customer would subscribe to a term deposit based on past marketing data collected by a Portuguese bank. These campaigns were carried out over phone calls, and some customers were contacted multiple times. The target variable in the dataset is 'y', which indicates whether the client subscribed (‘yes’) or not (‘no’). The idea was to build a classification model that could help the bank identify potential customers more effectively and improve the success rate of future campaigns.

Project Overview
This was a machine learning classification project where I worked with a real-world dataset consisting of 45,211 customer records and 17 features. The dataset included a mix of categorical and numerical features such as age, job, marital status, education level, account balance, type of communication, day, duration of call, and whether the customer had a housing or personal loan.

The project involved multiple steps such as data cleaning, exploration, preprocessing, model building, and evaluation.

1. Data Cleaning & Preprocessing
- Missing Values:
  Some columns like job, education, and contact had missing values. I handled this by filling in the most frequent values (mode) for those columns, as they had relatively fewer missing entries.
- Removing Columns:
  Any columns with more than 50% missing values were dropped, as they could have negatively impacted model performance and added noise to the data.
- Outlier Treatment:
  Outliers in numerical columns such as balance, duration, and campaign were treated using the Interquartile Range (IQR) method to reduce their influence on the model.

2. Exploratory Data Analysis (EDA)
I performed visualizations and statistical analysis to better understand patterns in the data:
- Age Distribution:
  Most customers who subscribed were aged between 30 to 36 years.
- Job Role:
  Customers with managerial jobs subscribed more often, while blue-collar workers were less likely to subscribe.
- Marital Status:
  Married clients were the most common and showed a higher likelihood of subscribing compared to single or divorced individuals.
- Education:
  Clients with tertiary education (college/university) had the highest subscription rates. Secondary education followed next.
- Loan Impact:
  Customers with no loans (housing or personal) were more likely to subscribe.
  Having both types of loans significantly decreased subscription likelihood.
- Communication Type:
  Cellular communication was much more effective than telephone.
- Campaign Performance by Month:
  Most subscriptions occurred in May, followed by June, July, August, and April.
- Call Duration:
  Calls longer than 400 seconds were more likely to result in a subscription. Also, most successful subscriptions came from customers contacted fewer than 3 times.
- Overall Conversion Rate:
  Only 11.7% of the clients subscribed to a term deposit, showing significant class imbalance.

3. Feature Engineering
- Encoding:
  - Used Label Encoding for categorical variables with fewer categories.
  - Used One-Hot Encoding for columns like job and month, which had many unique categories.
- Handling Class Imbalance:
  To deal with the skewed target variable (only 11.7% positive cases), I used SMOTE (Synthetic Minority Oversampling Technique) to balance the data and help the model learn both classes better.
- Scaling:
  Applied MinMaxScaler to scale the numerical features so that they fall between 0 and 1. This helps certain models (like KNN and Logistic Regression) perform better.

4. Model Building and Evaluation
I trained and tested multiple classification models:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest Classifier
- XGBoost Classifier

Each model was evaluated using metrics like Accuracy, Precision, Recall, F1 Score, and ROC AUC Score.
- I also used k-fold Cross-Validation to make sure the results were reliable and not dependent on a single train-test split.
- XGBoost outperformed all other models, achieving:
  - Accuracy: ~93%
  - Precision: High
  - Recall: High
  - F1 Score: High
  - ROC AUC: Close to 0.93

5. Conclusion
This project helped me understand how machine learning can be used to improve real-world marketing strategies. The final model, based on XGBoost, was able to predict with high accuracy whether a client would subscribe to a term deposit or not.

Key takeaways:
- Data preprocessing and handling class imbalance is crucial in real-world data.
- EDA provided valuable business insights like which age groups, job roles, or months are more likely to yield positive responses.
- The model can be a useful tool for banks to target the right customers, saving time, effort, and improving conversion rates in future campaigns.
