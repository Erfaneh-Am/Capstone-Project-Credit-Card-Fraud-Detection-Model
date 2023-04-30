## Second-Capstone-Project
# Uncovering Fraud: A Machine Learning Model to Predict Credit Card Fraud Transactions

<img width="550" alt="image" src="https://user-images.githubusercontent.com/121911081/235372591-0eac6f88-c364-47f2-903a-0cf970361a65.png">

### Problem Statement
Credit card fraud is a significant concern in the financial industry. In order to prevent fraudulent transactions, a machine learning model can be trained on historical transaction data to identify fraudulent activity in real-time. It is important to detect and prevent fraud in credit card transactions for three main reasons including: protecting customers, preserving financial stability, and maintaining trust. 
In this report we have explored seven different machine learning models for credit card fraud detection and found that the Random Forest Classifier with max depth of 9 and gini criterion performed the best. This model was able to predict 90% of the fraud transactions with a relatively low false positive rate of 1.9%, meaning that only 1.9% of legitimate transactions were mistakenly classified as fraud.

### Data Wrangling
For this project the credit dars history data was obtained from Kaggle, which includes legitimate and fraud transactions from the duration 1st Jan 2019 - 31st Dec 2020. It covers credit cards of 1000 customers doing transactions with a pool of 800 merchants and includes information on the transaction amount, merchant, location, and time. The data included 1296675 transactions from which 7506 transactions were fraud. That equals to %0.58 of the total transactions.

### Exploratory Data Analysis
Exploratory data analysis (EDA) was performed to better understand the data and identify any patterns or relationships. The final shape of the data was 1296675 rows with 37 columns. After performing statistical tests, it is obvious that transaction amount (`amt`), transaction hour (`trans_hour`), customer age (`age`), and transaction month (`trans_month`) are the most significant features.

### Preprocessing and Training
Several machine learning models were evaluated including decision tree classifier, random forest, gradient boosting, hist gradient boosting, adaboost classifier, naive bayes, and K nearest neighbor on the training data. Various evaluation metrics such as precision, recall, and F1 score have been used to compare the performance of different models. Among all of the models, the random forest model was the best model, when predicting training data, with more than 99.9% accuracy, recall and f1 scores. Also, the precision score is 1 therefore, it can perfectly predict the legitimate transactions and almost all fraud transactions. 

### Final Modeling
Once the best-performing machine learning model was identified, we have fine-tuned it using techniques such as hyperparameter tuning and cross-validation.
Therefore, the Random Forest with max_depth of 9 and criterion gini was used as our best model. The results showed that the model could accurately classify 90% of the fraud transactions in the unseen data. Even though some false positives could be seen in the results, the false positive rate is only about 1.9% which can be negligible since in this case we care more about the false negatives and would like to minimize the number of fraud transactions that are mistakenly classified as legitimate transactions.
