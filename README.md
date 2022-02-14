# Credit_Risk_Analysis

## Overview 

In order to determine which credit card loan applications should be considered as high risk vs low risk, we are going to use supervised machine learning to detect it.  In order to see which model will be most effective, we will test 4 resampling models and 2 ensemble models.


## Results
## Resampling

For our resampling models, we resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and then generate the classification report.

Here are the results for reach model.

### Naive Random Oversampling

Accuracy Score :0.6456130066757718</br>
Precision High Risk: 0.01</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.61</br>
Sensitivity Low Risk: 0.68</br>
F1 Score High Risk: 0.02</br>
F1 Score Low Risk: 0.81


### SMOTE Oversampling

Accuracy Score : 0.6234433606890912 </br>
Precision High Risk: 0.01</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.61</br>
Sensitivity Low Risk: 0.64</br>
F1 Score High Risk: 0.02</br>
F1 Score Low Risk: 0.78

### Undersampling

Accuracy Score : 0.5134421923283014 </br>
Precision High Risk: 0.01</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.61</br>
Sensitivity Low Risk: 0.42</br>
F1 Score High Risk: 0.01</br>
F1 Score Low Risk: 0.59</br>

### Combination (Over and Under) Sampling


Accuracy Score : 0.6531287896185101</br>
Precision High Risk: 0.01</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.69</br>
Sensitivity Low Risk: 0.62</br>
F1 Score High Risk: 0.02</br>
F1 Score Low Risk: 0.76</br>


## Ensemble

### Balanced Random Forest Classifier

Accuracy Score : 0.7877672625306695</br>
Precision High Risk: 0.04</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.67</br>
Sensitivity Low Risk: 0.91</br>
F1 Score High Risk: 0.07</br>
F1 Score Low Risk: 0.95

### Easy Ensemble AdaBoost Classifier

Accuracy Score : 0.925427358175101</br>
Precision High Risk: 0.07</br>
Precision Low Risk: 1.00</br>
Sensitivity High Risk: 0.91</br>
Sensitivity Low Risk: 0.94</br>
F1 Score High Risk: 0.14</br>
F1 Score Low Risk: 0.97


## Summary

If we look at the numbers showing how each model performed, the model that performed the best seems to be the Easy Ensemble Adaboost Classifier.  It had the higest accuracy score and had the highest sensitivity when it came to picking up high risk applications.  In my opinion, none of these models would be good enough to use to detect high risk credit card lenders simply due to the fact that none of these models have shown to have enough precision.  With these models, it would fail to properly diagnose true positives (high risk applications)
