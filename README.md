# credit-risk-classification

![credit](https://github.com/caitlin-hartley/credit-risk-classification/blob/main/images/risk_analysis.svg)

Training and evaluating a model to assess loan risk using a dataset of historical lending activity from a peer-to-peer lending services company. The goal is to build a model that can accurately determine the creditworthiness of borrowers, helping to identify high-risk and healthy loans.

---

[Model]

[Report]

---

## Creating and Analyzing the Model

- Created the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns
  * A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
- Split the data into training and testing datasets
- Fited a logistic regression model by using the training data
- Saved the predictions for the testing data labels by using the testing feature data and the fitted model

![model](https://github.com/caitlin-hartley/credit-risk-classification/blob/main/images/model.png)
  
- Evaluated the model’s performance:
  * Generated a confusion matrix
  * Printed the classification report
 
![analysis](https://github.com/caitlin-hartley/credit-risk-classification/blob/main/images/analysis.png)


---


## Credit Risk Analysis Report

### Overview
  The purpose of this analysis is to evaluate the performance of a machine learning model designed to predict credit risk by distinguishing between healthy loans and high-risk loans. The model’s ability to accurately classify loan types is essential for the company to make informed lending decisions, minimize financial risk, and maintain overall portfolio health.

### Model Performance
* Accuracy: 99% overall, indicating strong performance across both loan categories.
* Precision for Healthy Loans: 100%, with nearly no healthy loans being misclassified as high-risk.
* Precision for High-Risk Loans: 87%, showing that 13% of loans predicted as high-risk were actually healthy.
* Recall for High-Risk Loans: 95%, meaning that the model correctly identified 95% of high-risk loans, with only 32 misclassified as healthy.

### Summary of Results and Recommendation
  The model demonstrates excellent performance overall, achieving 99% accuracy and strong recall for high-risk loans. It performs best when predicting healthy loans, with perfect precision and recall, correctly classifying almost all of them. However, the model struggles slightly with precision when identifying high-risk loans, misclassifying 86 healthy loans as high-risk. Despite this, its high recall for high-risk loans ensures that most of them are correctly flagged, which is crucial for minimizing financial exposure.

For financial institutions, it is generally more important to minimize financial risk by accurately identifying high-risk loans (1s). Thus, improving precision is important to avoid unnecessary rejections of healthy loans. However, since correctly identifying high-risk loans is critical for managing credit risk, the model’s ability to capture the majority of these loans makes it a valuable tool for the company. Given this and its overall high accuracy and strong recall, I recommend the model for use by the company. 
