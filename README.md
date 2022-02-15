# Credit_Risk_Analysis

## Overview of the analysis:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.  Therefore, you’ll need to use different techniques to train and evaluate models with unbalanced classes. You will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to predict credit risk.

You will **oversample** the data using the `RandomOverSampler` and `SMOTE` algorithms, and **undersample** the data using the `ClusterCentroids` alogirithm.  Then, you will use a combinatorial approach of **over-and undersampling** using the `SMOTEENN` algorithms.  Finally, you will compare two machine learning models `BalancedRandomForestClassifer` and `EasyEnsembleClassifier` hope to reduce bias for predicting credit risk.

## Data Source:
Credit card credit dataset from [LendingClub](https://www.lendingclub.com/), a peer-to-peer lending services company

## Deliverables:
Deliverable 1: Use Resampling Models to Predict Credit Risk
Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Deliverable 4: A Written Report on the Credit Risk Analysis

## Results:
* Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models.
* Use screenshots of your outputs to support your results.

## Summary:
* Summarize the results of the machine learning models,
* include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

