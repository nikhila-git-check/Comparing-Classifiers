# Comparing-Classifiers

This project compares 4 classification algorithms on the UCI Bank Marketing dataset:

- k-Nearest Neighbors (k-NN)
- Logistic Regression
- Decision Tree
- Support Vector Machine (SVM)

## Business Problem

A Portuguese bank wants to predict which customers are likely to subscribe to a term deposit after a telemarketing call.  
The bank can prioritize calls, cut expenses, and boost campaign efficacy with the help of accurate forecasts.

## Files

- notebook: bank_marketing_classifiers.ipynb  (Main analysis and modeling notebook) 
- data/bank-additional.csv (10% sample of the original UCI dataset)
- data/bank-additional-names.txt (Feature descriptions) 

## Summary of Findings

- The dataset shows a significant class imbalance, with the ‘yes’ category representing only approximately 11% of the samples.
- Focusing on F1-score or Recall works better for the business goal than using accuracy.
- Logistic Regression and SVM give a good mix of easy-to-understand results and solid performance.
- Features about past contact attempts (pdays, previous, poutcome) and economic factors (euribor3m, emp.var.rate) are the most useful predictors.

See the notebook for full details.

## How to Run
1. Create a virtual environment and install the requirements (scikit-learn, pandas, seaborn, matplotlib, etc.).
2. Place the data files under data/.
3. Open bank_marketing_classifiers.ipynb in Jupyter and run all cells.
