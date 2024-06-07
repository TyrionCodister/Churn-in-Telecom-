SYRIATEL CUSTOMER CHURN PREDICTION


BUSINESS UNDERSTANDING


Project Overview


Syriatel, a telecommunications company, is experiencing a significant rate of customer churn. Customer churn, or the rate at which customers stop doing business with a company, is a critical issue in the telecom industry. Retaining customers is not only more cost-effective than acquiring new ones but also crucial for sustaining profitability and market position. This project aims to build a predictive model to identify customers who are likely to churn, enabling Syriatel to implement proactive retention strategies to mitigate revenue loss.


STAKEHOLDERS

Primary Stakeholder:

Syriatel Mobile Telecom: The telecom company that will use the model to reduce customer churn and improve profitability.


Other Stakeholders:

Shareholders: Will benefit from increased profitability and market stability.

Employees: Will benefit from a more stable business environment and potentially better compensation.

Customers: Will benefit from improved services and customer support.

BUSINESS PROBLEM

The main business problem is the high rate of customer churn at Syriatel, leading to substantial revenue loss and increased costs associated with acquiring new customers. The goal is to develop a predictive model that can identify customers who are likely to churn, allowing Syriatel to take targeted actions to retain these customers and reduce overall churn rates.

Project Scope

In-Scope:


Identifying key features that predict customer churn.

Developing a robust classification model to predict churn.

Providing actionable insights and recommendations for retention of more customers


Out-of-Scope:

Directly implementing the retention strategies.

Long-term monitoring and adjustments of the model post-deployment.


DATA UNDERSTANDING


To better serve the identified consumers and clearly project the problem(s) stated in the background, I will use the Churn in Telecom's dataset from Kaggle (https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset).



The dataset contains 3333 ROWS and 21 columns, including information about the state, account length, area code, phone number, international plan, voice mail plan, number of voice mail messages, total day minutes, total day calls, total day charge, total evening minutes, total evening calls, total evening charge, total night minutes, total night calls, total night charge, total international minutes, total international calls, total international charge, customer service calls and churn.

MODELLING

We begin by constructing multiple models, evaluating their performance, and subsequently engaging in hyper-parameter tuning to enhance their effectiveness. Our primary objective is to identify the model and parameter configurations that yield the most favorable outcomes.

We proceed with the training and evaluation of the following models:

1. Logistic Regression Model,

2. K-Nearest Neighbors,

3. Decision Trees,

4. Random Forest

5. XG BOOST


MODEL EVALUATION

Model Comparisons:
Logistic Regression (AUC = 0.75): This model performs reasonably well, with an AUC (Area Under Curve) of 0.75. It balances TPR and FPR effectively.

Decision Tree (AUC = 0.76): Slightly better than logistic regression, but still not the best performer.

Random Forest (AUC = 0.83): Shows significant improvement. Its AUC indicates strong discrimination ability.

KNN (AUC=0.65):performed poorest

Gradient Boosting (AUC = 0.83): The winner! Highest AUC, indicating excellent performance.



Both gradient boosting model and the randomforest performed well.

let's compare their accuracy scores as well because they are also equally important in evaluating the best model for deployment

 Model  Accuracy  Precision  Recall  F1 Score  Sample Size
 
0  Logistic Regression      0.84       0.64    0.56      0.58         1000

1  KNN                      0.84       0.65    0.60      0.62         1000

2 Decision Tree             0.88       0.77    0.67      0.71         1000

3 Random Forest             0.89       0.85    0.66      0.71         1000

4 XGBOOST                   0.89       0.84    0.68      0.72         1000



CONCLUSIONS:

1. Subscription Plans: The features 'international plan' and 'voice mail plan' have the highest importance scores, indicating that customers' subscriptions to these additional services are strong predictors of churn behavior.

2. Geographical Location: The feature 'area_code' has a relatively low importance score, indicating that a customer's geographical location may not be as influential in predicting churn compared to other features.

3. The feature 'account_length' has a moderate importance score, implying that the length of time a customer has been with SyriaTel plays a role in their likelihood of churning.



