# Comparing-Classifiers

This project compares 4 classification algorithms on the UCI Bank Marketing dataset:

- Exploratory Data Analysis (EDA)  
- Feature engineering  
- One-Hot Encoding + Scaling  
- Train/Test Split  
- Baseline modeling  
- Model comparison across:
  - Logistic Regression  
  - k-Nearest Neighbors (KNN)  
  - Decision Tree Classifier  
  - Support Vector Machine (SVM)
    
## Business Problem

A Portuguese bank wants to predict which customers are likely to subscribe to a term deposit after a telemarketing call.  
The bank can prioritize calls, cut expenses, and boost campaign efficacy with the help of accurate forecasts.

## Files

- notebook: bank_marketing_classifiers.ipynb  (Main analysis and modeling notebook) 
- data/bank-additional-full.csv (10% sample of the original UCI dataset)
- data/bank-additional-names.txt (Feature descriptions) 

## Summary of Findings

- The dataset shows a significant class imbalance, with the ‘yes’ category representing only approximately 11% of the samples.
- Focusing on F1-score or Recall works better for the business goal than using accuracy.
- Logistic Regression and SVM give a good mix of easy-to-understand results and solid performance.
- Features about past contact attempts (pdays, previous, poutcome) and economic factors (euribor3m, emp.var.rate) are the most useful predictors.

See the notebook for full details.

## Conclusions

- The baseline model is not useful because it predicts only the majority class (“no”) with no ability to identify likely subscribers.
- Logistic Regression and SVM both outperform KNN and Decision Trees on this dataset.
- Logistic Regression offers:
      * Strong predictive performance
      * Good stability across train/test
      * Fast computation
      * Clear interpretability for business users
- Decision Trees provide interpretability but tend to overfit.
- KNN struggles due to high dimensionality after one-hot encoding.

##  Recommendations
- Deploy Logistic Regression as the first production-ready model.
- Use probability thresholds like target top 20% highest scores to prioritize calls.
