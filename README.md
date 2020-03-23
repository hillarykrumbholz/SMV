# Supervised Machine Learning and Credit Risk

## Project Overview
To create worksheets. dashboards, and stories from New York City bike-sharing data using Tableau.

## Resources
Data Sources: LoanStats_2019Q1.csv <br>
Software: Jupyter Notebook, Python 3.7.6 <br>
Python dependencies: Numpy, Scipy, Scikit-learn

### Project Objective
Use Python to build and evaluate several machine learning models to predict credit risk. Being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.

### Project Summary
Credit risk is an inherently unbalanced classification problem, as the number of good loans easily outnumber the number of risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Your final task is to evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Analysis

### Naive Random Oversampling
The balanced accuracy score of Naive Random Oversampling was 65% (0.65), which means that it predicts 65% of risks accurately - it is only 65% accurate when determining true positives and true negatives. 

To determine the precision and recall scores for both high and low risk (0 and 1), it is best to look at the classification report. 

High-Risk
- Precision: There is a low precision of 1% (0.01), which indicates there is a large number of false positives. In this case, out of all predicted high-risk situations, only 1% are truly high-risk, the remaining 99% are actually low-risk.

- Recall: The recall score is 69% (0.69), which means the ability to to find all the true high-risk situations is only 69%. Therefore the remaining 31% are actually high-risk but were predicted to be low-risk.

Low-Risk
- Precision: There is a high precision score of 100% (1.0), which indicates that all predicted low-risk situations are actually low-risk.

- Recall: The recall score is 61% (0.61), which means the ability to to find all the true low-risk situations is only 61%. Therefore the remaining 39% are actually low-risk but were predicted to be high-risk.

### SMOTEE Oversampling
The balanced accuracy score of SMOTEE Oversampling was 66% (0.66), which means that it predicts 66% of risks accurately - it is only 66% accurate when determining true positives and true negatives. 

To determine the precision and recall scores for both high and low risk (0 and 1), it is best to look at the classification report. 

High-Risk
- Precision: There is a low precision of 1% (0.01), which indicates there is a large number of false positives. In this case, out of all predicted high-risk situations, only 1% are truly high-risk, the remaining 99% are actually low-risk.

- Recall: The recall score is 63% (0.63), which means the ability to to find all the true high-risk situations is only 63%. Therefore the remaining 37% are actually high-risk but were predicted to be low-risk.

Low-Risk
- Precision: There is a high precision score of 100% (1.0), which indicates that all predicted low-risk situations are actually low-risk.

- Recall: The recall score is 69% (0.69), which means the ability to to find all the true low-risk situations is only 69%. Therefore the remaining 31% are actually low-risk but were predicted to be high-risk.

### Undersampling
The balanced accuracy score of Undersampling was 66% (0.66), which means that it predicts 66% of risks accurately - it is only 66% accurate when determining true positives and true negatives. 

To determine the precision and recall scores for both high and low risk (0 and 1), it is best to look at the classification report. 

High-Risk
- Precision: There is a low precision of 1% (0.01), which indicates there is a large number of false positives. In this case, out of all predicted high-risk situations, only 1% are truly high-risk, the remaining 99% are actually low-risk.

- Recall: The recall score is 66% (0.66), which means the ability to to find all the true high-risk situations is only 66%. Therefore the remaining 34% are actually high-risk but were predicted to be low-risk.

Low-Risk
- Precision: There is a high precision score of 100% (1.0), which indicates that all predicted low-risk situations are actually low-risk.

- Recall: The recall score is 40% (0.40), which means the ability to to find all the true low-risk situations is only 40%. Therefore the remaining 60% are actually low-risk but were predicted to be high-risk.

### Combination (Over and Under) Sampling
The balanced accuracy score of a combination of Under and Oversampling was 53% (0.53), which means that it predicts 53% of risks accurately - it is only 53% accurate when determining true positives and true negatives. 

To determine the precision and recall scores for both high and low risk (0 and 1), it is best to look at the classification report. 

High-Risk
- Precision: There is a low precision of 1% (0.01), which indicates there is a large number of false positives. In this case, out of all predicted high-risk situations, only 1% are truly high-risk, the remaining 99% are actually low-risk.

- Recall: The recall score is 72% (0.72), which means the ability to to find all the true high-risk situations is only 72%. Therefore the remaining 28% are actually high-risk but were predicted to be low-risk.

Low-Risk
- Precision: There is a high precision score of 100% (1.0), which indicates that all predicted low-risk situations are actually low-risk.

- Recall: The recall score is 57% (0.57), which means the ability to to find all the true low-risk situations is only 57%. Therefore the remaining 43% are actually low-risk but were predicted to be high-risk.

## Recommendation
For this task of assessing credit risk, it is more importnat to be on the conservative side by potentially deeming some individuals as a high-risk when in fact they would be at low-risk for a loan. With that in mind, I would recommend using the Combination (Over and Under) Sampling technique. While it does have a low balanced accuracy sscore of 53%, meaning that it predicts only 53% of risks accurately; it has the greatest high-risk recall score of 72%. Meaning that this model is able to predict 72% of high-risk situations correctly. On the other hand, it does have a weak low-risk score of 57%. However, it is in a bank's best interest to deem a loan as high-risk when it is truly not, as it would overall keep the bank's financial security top priority. 



