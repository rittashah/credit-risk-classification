# credit-risk-classification
## Overview of the Analysis

This model tests and validates credit risk for potential future loans using Supervised Learning techniques to ensure the highest accuracy and build a model that can identify the creditworthiness of borrowers.
- the main Purpose of the analysis is to predict the probablity of high-risk applicants in order to reduce total number of defaults on bank loans.
  
## Data Resource:
lending_data.csv

## Factors considered in the analysis included data on:

   - the  loan size.
  -  its interest rate
  -  the borrower's income
   - the debt to income ratio
   - the number of accounts the borrower have.
   - derogatory marks against the borrower
   - the total debt

- The dataset contain (77,536 data points) and  was split into training and testing sets.
- The training set was used to build an initial logistic regression model(Model 1), using the LogisticRegression module from scikit-learn.
- Logistic Regression Model was then applied to the testing dataset.
- The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk.
the intial model had 75,036 low-risk loan data points and 2,500 high-risk data points.

To resample the training data and ensure that the logistic regression model had an equal number of data points, the training set data was resampled with the RandomOverSampler module (Model 2) from imbalanced-learn. This generated 56,277 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.

The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results are summarized below.

## Results

Logistic Regression Model 1:

  -  Accuracy: the model displays 18679 true positive results and 558 true negative results.with blanced accuracy of 0.9442676901753825
  -  Precision:the model performs better predicting healthy loans (precision 1) than high-risk loans (precision 0.87).
  -  Recall (the ratio of actual positives identified correctly): the model performs better predicting healthy loans (recall 1) than high-risk loans (recall 0.89).
  -   Support (the number of actual occurrences of the class in the specified dataset): according to the support column, the model is imbalanced in the training data (healthy loans 18759 vs high-risk loans 625), indicating structural weaknesses in the reported scores, in the evaluation process.

Logistic Regression Model 2:

- Accuracy: the model displays 55945 true positive results and 55954 true negative results, with    blanced accuracy of 0.994180571103648
- Precision: the model performs equally well for predicting healthy loans (precision 0.99) and high-risk loans (precision 0.99).
-Recall (the ratio of actual positives identified correctly): the model performs equally well for predicting healthy loans (recall 0.99) and high-risk loans (recall 0.99).
- Support (the number of actual occurrences of the class in the specified dataset): according to the support column, the model is balanced in the training data (healthy loans 56277 vs high-risk loans 56277), indicating structural strength in the reported scores, in the evaluation process

## Summary

keeping in mind that identifying potential high-risk loan holders is of most importance, since those accounts are responsible for the majority of the bank's lost.

'Machine Learning Model 2'  reported high balanced score and shows high levels of Accuracy, Precision and Recall for both healthy loans and high-risk loans. With more data points after the resampling, the model.
We would recommend utilizing the second model because of its heightened ability to detect 'high risk loans' accurately. This is especially important given how much it can cost a loan provider to misidentify and lend money to a 'high risk loan' applicant, and the minimal cost of misidentifying a 'healthy loan' applicant. 
we can see thatthe  first model is slightly better at identifying 'healthy loan' applicants. However, this is less important than correctly identifying 'high risk loan' applicants, which is accomplished better with the second model.




