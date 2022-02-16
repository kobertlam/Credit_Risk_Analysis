# Credit_Risk_Analysis

## Overview of the analysis:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.  Therefore, you’ll need to use different techniques to train and evaluate models with unbalanced classes. You will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to predict credit risk.

You will **oversample** the data using the `RandomOverSampler` and `SMOTE` algorithms, and **undersample** the data using the `ClusterCentroids` alogirithm with logistic regression model.  Then, you will use a combinatorial approach of **over-and undersampling** using the `SMOTEENN` algorithm with logistic regression model.  Finally, you will compare two machine learning models `BalancedRandomForestClassifer` and `EasyEnsembleClassifier` hope to reduce bias for predicting credit risk.

## Data Source:
Credit card credit dataset from [LendingClub](https://www.lendingclub.com/), a peer-to-peer lending services company

## Deliverables:
[Deliverable 1](./credit_risk_resampling.ipynb): Use **Resampling Algorithm** to Predict Credit Risk

[Deliverable 2](./credit_risk_resampling.ipynb): Use the **SMOTEENN Algorithm** to Predict Credit Risk

[Deliverable 3](./credit_risk_ensemble.ipynb): Use **Ensemble Classifiers** to Predict Credit Risk

Deliverable 4: A Written Report on the Credit Risk Analysis (this file)

## Results:
We analyse the balanced accuracy score, the precision and recall scores on the **high_risk** class from each model, as our target is to find a model that can better predict the high credit risk.

1) Oversampling using RandomOverSampler:
    * balanced accuracy score: 65.73%
    * precision and recall scores: The precision for **high_risk** is 0.01, and the recall for **high_risk** is 0.71, and the F1 score is 0.02.
![image 1](./Resources/1_RandomOverSampler.jpg)

2) Oversampling using SMOTE:
    * balanced accuracy score: 66.22%
    * precision and recall scores: The precision for **high_risk** is 0.01, and the recall for **high_risk** is 0.63, and the F1 score is 0.02.
![image 2](./Resources/2_SMOTE.jpg)

3) Undersampling using Cluster Centroids algorithm:
    * balanced accuracy score: 54.43%
    * precision and recall scores: The precision for **high_risk** is 0.01, and the recall for **high_risk** is 0.69, and the F1 score is 0.01.
![image 3](./Resources/3_ClusterCentroids.jpg)

4) Over- and undersampling using SMOTEENN algorithm:
    * balanced accuracy score: 68.76%
    * precision and recall scores: The precision for **high_risk** is 0.01, and the recall for **high_risk** is 0.57, and the F1 score is 0.02.
![image 4](./Resources/4_SMOTEENN.jpg)

5) Balanced Random Forest Classifier:
    * balanced accuracy score: 95.54%
    * precision and recall scores: The precision for **high_risk** is 0.06, and the recall for **high_risk** is 1.00, and the F1 score is 0.12.
![image 5](./Resources/5_BalancedRandomForestClassifier.jpg)

6) Easy Ensemble Classifier:
    * balanced accuracy score: 93.17%
    * precision and recall scores: The precision for **high_risk** is 0.09, and the recall for **high_risk** is 0.92, and the F1 score is 0.16.
![image 6](./Resources/6_EasyEnsembleClassifier.jpg)


## Summary:
* The balanced accuracy score for the models using oversampling/undersampling/over-and-undersampling are between 54.43% and 68.76%:
    * The SMOTEENN algorithm has the highest balanced accuracy score (68.76%) among this 4 models.
    * The Cluster Centroids algorithm has the lowest balanced accuracy score (54.43%) among this 4 models.
    * All 4 models have very low precision for **high_risk** class (0.01), and the recall for **high_risk** class is between 0.57 and 0.71.
* The **Balance Random Forest Classifier** and **Easy Ensemble Classifier** have very high balanced accuracy score and recall for **high_risk** class:
    * Balanced accuracy score: (1) Balance Random Forest --> 95.54%,  (2) Easy Ensemble --> 93.17%
    * Recall for **high_risk** class: (1) Balance Random Forest --> 1.00, (2) Easy Ensemble --> 0.92
* The precision for **high_risk** class are still low: **Balance Random Forest** (0.06) and **Easy Ensemble** (0.09)
* In overall, **Balanced Random Forest Classifier** has the highest balanced accuracy score of 95.54%, and also has the highest recall for **high_risk** of 1.00.  On the other hand, **Easy Ensemble Classifier** has the highest precision for **high_risk** of 0.09, and the highest F1 score (0.16) on high_risk class
* Since the sensitivity on predicting high risk class is the most important factor when considering a model for credit risk prediction, the **Balanced Random Forest Classifier** has the amazing 1.00 on the recall for **high_risk** class (i.e. it can predict ALL cases as "high_risk" which are actually in "high_risk" class!), and this model also has very high balanced accuracy score (95.54%), I will recommend the **Balanced Random Forest Classifier** as the model to predict credit risk based on the existing dataset.

