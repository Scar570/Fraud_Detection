# Fraud_Detection
## Context
This case requires to development of a model for predicting fraudulent transactions for a financial company and using insights from the model to develop an actionable plan.

## Dataset Source
Data can be found on this link :
https://drive.google.com/file/d/1kv0rXS0kQopla-w_V9giSIaS7tb8_nLE/view?usp=drive_link
From here anyone can access the data.

## Columns
step - maps a unit of time in the real world. In this case, 1 step is 1 hour of time. Total steps 744 (30 days simulation).

type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.

amount - the amount of the transaction in local currency.

nameOrig - customer who started the transaction

oldbalanceOrg - initial balance before the transaction

newbalanceOrig - new balance after the transaction

nameDest - customer who is the recipient of the transaction

oldbalanceDest - initial balance recipient before the transaction. Note that there is no information for customers that start with M (Merchants).

newbalanceDest - new balance recipient after the transaction. Note that there is no information for customers that start with M (Merchants).

isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset, the fraudulent behavior of the agents aims to profit by taking control of customer's accounts and trying to empty the funds by transferring them to another account and then cashing out of the system.

isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200,000 in a single transaction.

## Fraud Detection Model
The fraud detection model used in this case is an XGBoost classifier. XGBoost is an ensemble learning technique based on decision trees, known for its high predictive power and ability to handle imbalanced datasets. Here's an elaboration on the model:

* Algorithm Choice: XGBoost was chosen because it is a robust algorithm capable of handling imbalanced datasets and capturing complex relationships in the data.

* Ensemble Approach: XGBoost is an ensemble method that combines multiple decision trees to make predictions. This ensemble approach helps improve model accuracy and generalization.

* Model Interpretability: XGBoost provides feature importance, allowing us to understand which features are most important for making predictions.

## Conclusions
The data is extremely unbalanced. However, it was possible to make all the data analysis and create good scores.
