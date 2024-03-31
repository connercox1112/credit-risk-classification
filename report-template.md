# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

1. The purpose of this analysis was to determine the credit risk associated with each loan application, identify loans that have a high risk of defaulting, and aid financial institutions in mitigating potential losses by accurately predicting credit risk.

2. The dataset for this analysis was comprised of loan application data. The critical variable used to predict was loan_status, which indicates whether a loan is likely to be paid off or at a high risk of defaulting. The binary outcome (0 for healthy loans and 1 for high-risk loans) serves as the foundation for the classification model.

3. The dataset included several variables related to the borrowers' financial health and loan characteristics. Key variables included borrower income, debt-to-income ratio, loan amounts, and others. Before building the model, analysis of the loan_status distribution using value_counts() was used to understand the balance between healthy and high-risk loans within the dataset. This step is vital to gauge the dataset's balance and inform the need for any sampling techniques to address imbalances.

4. The machine learning process for this analysis comprised of these stages:
- Data Preprocessing: Clean the data, handle missing values, encode categorical variables, and split the data into features (X) and labels (y).
- Splitting the Data: Divide the dataset into training and testing sets to evaluate the model's performance on unseen data.
- Model Selection and Training: It as determined the LogisticRegression model was the best fit due to its suitability for binary classification tasks. The model was trained using the training dataset.
- Model Evaluation: The model's performance was assessed using the testing set. A confusion matrix and a classification report were generated to evaluate the model's accuracy, precision, recall, and f1-score.

5. 
- Logistic Regression: This algorithm was the primary method used for classification. It's particularly suited for binary classification problems. Logistic regression estimates probabilities using a logistic function, making it effective for predicting binary outcomes.
- Evaluation Techniques: Used confusion matrices and classification reports as part of our model evaluation. These tools helped us understand the model's performance in classifying both healthy and high-risk loans.

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Linear Regression Report:
- Accuracy: 0.99
- Precision (0): 1.00
- Recall (0): .99
- Precision (1): .85
- Recall (1): .91

Random Forest Classifier
- Accuracy: .99
- Precision (0): 1.00
- Recall (0): 0.99
- Precision (1): 0.85
- Recall (1): 0.89

Gradient Boosting Classifier
- Accuracy: 0.99
- Precision (0): 1.00
- Recall (0): 0.99
- Precision (1): 0.85
- Recall (1): 0.99

Summary:
The Gradient Boosting Classifier appears to be the best classfier. All three classifiers perform the same except high risk loan recall. The Gradient Boosting Classifier has the best recall score at .99, giving it the clear edge.

When choosing a classifier the problem absolutley matters. In this case, the financial institution would experience considerable more loss if they approved high risk loans in comparision to denying healthy loans. So, choosing a classifier that is proven to be accurate in identifying high risk candidates in imperative.
