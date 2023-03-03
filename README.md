# Credit_Risk_Analysis

## Overview
This analysis uses machine learning to predict credit risk for LendingClub, a peer-to-peer lending services company. Credit risk is an unbalanced classification problem because most good loans outnumber risky loans. This imbalance means that the data needs to be resampled to increase the proportion of bad debt to good debt within the data. Once the data has been resampled, it is subjected to two machine learning algorithms: the balanced random forest and the easy ensemble classifier model to see which model best predicts credit risk.

## Results
### Naive Random Oversampling
The balanced accuracy score for this method of oversampling is 64%. The precision for high risk debt has a positivity of 1% which means out of all the loans that the model predicted to be bad debt, only 1% actually qualify as such. The recall percentage shows that the model is able to predict the correct outcome for 60% of the loans that are classified as high risk.

###  Synthetic Minority Oversampling Technique (SMOTE)
This method of oversampling works by creating extra datapoints from the minority class that replicate data included in the original dataset. The results using this method are similar to naive random oversampling. Once again, the balanced accuracy score is mediocre at just 66%. The precision for selecting bad debt is once again 1% with a recall of 69%.  The resulting F1 score is 0.02 which shows that this model rarely predicts the correct credit risk for loans.

### Undersampling
Undersampling takes the opposite approach to balancing out the dataset. Instead of increasing the minority data, undersampling decreases the majority data to align with the minority data. The results using the cluster centroids method show a balanced accuracy score of 54%, precision of 1%, and recall of 40%. 

### Combination (Over/Undersampling)
The SMOTEEN model mixes over and undersampling to optimize the accuracy of the resulting data. In this instance, the SMOTEEN model did not result in an improved balanced accuracy or F1 score.

### Balanced Random Forest Classifier
The balanced random forest classifier model resulted in a balanced accuracy score of 79%, precision of 3%, and recall of 70%. Thusfar in the analysis, this model is the best predictor of credit risk. 

### Easy Ensemble Classifer
The easy ensemble classifier had similar results to the balanced random forest classifier model.

## Summary
The balanced random forest classifier and the easy ensemble classifier are the two best models for predicting credit risk for LendingClub customers.
