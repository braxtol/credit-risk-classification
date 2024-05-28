# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to create a supervised machine learning model that will predict if a loan is healthy (class 0) or high-risk (class 1). We will use logistic regression as a binary classifier for our model here. The analysis was conducted on financial data, specifically focusing on loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The objective was to predict the loan status, either as a healthy loan (0) or a high-risk loan (1). The data used is a 77,500-line CSV file.

The stages of the machine learning process in this analysis included:

* Splitting data into labels and features, with the loan status (healthy or high-risk) being the label and the remaining seven columns as features.
* The data was then split into training and testing data sets.
* A Logistic Regression model from sklearn was created.
    * Logistic Regression as a binary classifier was chosen as we are classifying loans as healthy OR high-risk and only those two options.
* The model was then fit with the training data.
* Predictions were made with the test data.
* The model’s performance was evaluated using accuracy, precision, and recall scores.

## Results

Description of Logistic Regression Model Accuracy, Precision, and Recall scores.

* Accuracy: The overall accuracy of the model is 0.99, indicating that it correctly classifies 99% of the instances.
* Precision
    * Healthy Loan (class 0): 1.00
    * High-Risk Loan (class 1): 0.85
* Recall
    * Healthy Loan (class 0): 0.99
    * High-Risk Loan (class 1): 0.91

## Summary

The logistic regression model excels in predicting healthy loans (class 0) with precision of 1.00 and recall of 0.99. In the case of risky loans (class 1), the model maintains a strong prediction performance, with precision at 0.85 and recall at 0.91. The model is therefore a good fit for this data set.

The slightly lower precision and recall for predicting risky loans may be attributed to the imbalanced dataset, as the support test data for risky loans is significantly lower at 619 compared to 18,765 for class 0 (healthy loans.) There is potential for enhancement in predicting high-risk loans, which stems from the limited number of high-risk loans available for the model to learn from in comparison to the abundance of healthy loans in the dataset. Introducing more high-risk loan data for training could lead to improvements in the model. In the context of loan classification, prioritizing the prevention of high-risk loans holds greater significance than approving loans, as a single defaulted loan can result in more significant financial loss than the interest earned from multiple loans. The overall accuracy of the model is notably high at 99%.

Considering the overall performance and the significance of predicting high-risk loans accurately, the logistic regression model appears to be a suitable choice. Its high accuracy in predicting healthy loans, coupled with decent performance in predicting risky loans, makes it a valuable tool for loan classification tasks. However, continuous efforts to enhance the model's performance in predicting high-risk loans, such as introducing more data for training, could further improve its effectiveness in mitigating financial risks. 