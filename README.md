# credit-risk-classification
## Overview of the Analysis

The goal of this analysis is to develop a supervised machine learning model that can classify loans as either healthy (0) or high-risk (1). For this purpose, we will employ logistic regression as a binary classifier. The dataset used for this analysis is a financial record containing 77,500 entries, with features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The primary objective is to predict the loan's status, determining whether it is a healthy loan (0) or a high-risk loan (1).

### Key steps:
1. Data Preparation: The dataset was first separated into labels and features. The loan status (healthy or high-risk) was assigned as the label, while the other seven columns served as features.

2. Data Splitting: The data was divided into training and testing sets to train the model and evaluate its performance.

3. Model Creation: A Logistic Regression model from scikit-learn was used for classification.

4. Model Selection: Logistic Regression was chosen as the binary classifier since the task involves classifying loans into one of two categories: healthy or high-risk.

5. Model Training: The model was trained using the training dataset.

6. Prediction: Predictions were made on the test data to assess the model’s ability to generalize.

7. Model Evaluation: The model’s performance was evaluated using key metrics such as accuracy, precision, and recall scores.

## The results

```
Classification Report:
               precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619
           
    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384
```

Class 0 ("healthy"):

Precision: 1.00
The model is 100% accurate when predicting class 0, meaning there are no false positives for this class.

Recall: 0.99
The model correctly identifies 99% of the actual class 0 samples.

F1-Score: 1.00
The F1-score, which balances precision and recall, is 1.00, indicating perfect performance for class 0.

Class 1 ("high-risk"):

Precision: 0.84
The model predicts class 1 correctly 84% of the time when it predicts class 1, but there are some false positives.

Recall: 0.94
The model identifies 94% of the actual class 1 samples, which is relatively high.

F1-Score: 0.89
The F1-score of 0.89 reflects a good balance between precision and recall, but it is lower than that of class 0 due to the lower precision.

Overall:

Accuracy: 0.99
The model has an overall accuracy of 99%, which is very high, meaning it correctly classifies 99% of all samples.

Macro Average:
Precision: 0.92
Recall: 0.97
F1-Score: 0.94
The macro average takes the mean of the individual class metrics (without considering class imbalance). It shows the model is performing well across both classes.

Weighted Average:
Precision: 0.99
Recall: 0.99
F1-Score: 0.99
The weighted average accounts for the imbalance in the class distribution and reflects the overall model performance, indicating excellent results.

## Summary

The logistic regression model performs excellently in predicting healthy loans (class 0), achieving a precision of 1.00 and a recall of 0.99. For high-risk loans (class 1), the model still delivers strong results, with a precision of 0.85 and a recall of 0.91.For high-risk loans, the model achieves a precision of 0.84 and a recall of 0.94, leading to a strong F1-score of 0.89, though not as high as for healthy loans. Overall, the model’s accuracy is 99%, with a macro F1-score of 0.94, showing balanced performance, and a weighted F1-score of 0.99, reflecting its robustness in an imbalanced dataset. This suggests the model is highly reliable for both classes, with a slight advantage in predicting the healthy loans.
