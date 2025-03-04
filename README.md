Purpose of the Analysis: The goal of this analysis was to develop a machine learning model to predict the risk level of loans, specifically classifying loans into two categories: 0 (healthy loan) and 1 (high-risk loan). 
By doing so, the analysis aims to identify high-risk loans, potentially to prevent defaults or make data-driven financial decisions.

The Financial info that we analyzed contained:
1- Loan Size
2- Interest Rate
3- Borrower Income
4- Debt to Income Ratio
5- Number of Accounts
6- Derogatory Marks
7- Total Debt

Stages of the Machine Learning Process
Data Preparation:

We began by loading and cleaning the dataset, ensuring that any missing or inconsistent values were handled appropriately.
We separated the data into features (X) and the target variable (y).
Splitting the Data:

We used train_test_split to divide the data into training and testing sets, ensuring a good mix of data for training and evaluation.
Model Selection:

We selected Logistic Regression as our model for this analysis, given that it is a common choice for binary classification tasks.
Model Training:

We trained the Logistic Regression model using the training data, setting a fixed random_state for reproducibility.
Model Prediction:

We used the trained model to predict loan risk on the testing data.
Evaluation:

We evaluated the model using metrics like accuracy, precision, recall, and F1-score, focusing on the performance for both classes (healthy and high-risk loans).

Machine Learning Model 1: Logistic Regression
Accuracy: The model achieved an accuracy score of approximately 82%, indicating that it correctly predicted loan statuses 82% of the time.

Precision (for high-risk loans 1): 0.86 — This means that 86% of the predicted high-risk loans were actually high-risk loans.

Recall (for high-risk loans 1): 0.94 — This indicates that 94% of the actual high-risk loans were correctly identified by the model.

F1-Score (for high-risk loans 1): 0.90 — Balances precision and recall for high-risk loans.

Precision (for healthy loans 0): 1.00 — This means that 100% of the predicted healthy loans were actually healthy.

Recall (for healthy loans 0): 0.99 — This means 99% of the actual healthy loans were correctly identified.

F1-Score (for healthy loans 0): 1.00 — Balances precision and recall for healthy loans.

Which Model Performs Best?
The Logistic Regression model appears to be the best model based on the results from accuracy, precision, recall, and F1-scores.
While precision and recall for healthy loans (0) are high, the model's performance for high-risk loans (1) shows a reasonable trade-off between precision and recall.

Does Performance Depend on the Problem?
Performance can indeed depend on the problem we are trying to solve. For example, if detecting high-risk loans is more important (e.g., for preventing defaults), we would prioritize recall for 1, even if it slightly lowers precision.
On the other hand, if minimizing false positives (predicting healthy loans as high-risk) is critical, precision for 1 becomes more important.

