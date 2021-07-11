# Credit_Risk_Analysis

## Overview and Purpose:
Credit Risk is an inherently unbalanced data set as most credit applications meet a financial insitutions risk management requirements. Given the disparity in the data, we need to utilize different types of analysis to address the oversampling and undersampling problem. For this analysis, we used credit card credit data from LendingClub, a peer-to-peer lending services company. Using this data we created and trained different models using scikit-learn and imbalanced-learn. Below you will find the results for the six machine learning models used for this analysis:

# Machine Learning Results

## Naive Random Oversampling
The Naive Random Oversampling returned a 63.7% balanced accuracy score. The model has almost zero precision for identifying high-risk applications properly. The model had a recall score of 62% for high-risk application. This model is largely ineffective in identifying high_risk applications.

<img width="668" alt="Screen Shot 2021-07-11 at 8 36 22 AM" src="https://user-images.githubusercontent.com/80016496/125197792-ac28ff00-e224-11eb-8e14-ecc0f59692d9.png">


## SMOTE Results
The model returned a balanced accuracy score of 66%. Precision for high_risk applications was similarly low at 1%, and recall was 62% again.

<img width="672" alt="Screen Shot 2021-07-11 at 8 48 45 AM" src="https://user-images.githubusercontent.com/80016496/125197983-8ea86500-e225-11eb-83c0-b27e8354b1f6.png">

## Undersampling Results
The model had a balanced acuracy score of 63.7%, with a precision score of 1% and a recall of 69% for high risk applications.

<img width="660" alt="Screen Shot 2021-07-11 at 8 55 39 AM" src="https://user-images.githubusercontent.com/80016496/125198075-fe1e5480-e225-11eb-9c09-27764370b37e.png">

## Combination Sampling (Over & Under)
The model had a balanced accuracy score of 54%, with a precision score of 1% but ahigher recall at 72% for high risk applications

<img width="678" alt="Screen Shot 2021-07-11 at 8 59 47 AM" src="https://user-images.githubusercontent.com/80016496/125198196-87358b80-e226-11eb-98a4-8478d5d27f98.png">

## Balanced Random Forest Classifier
The model had an accuracy score of 78.6% (our highest so far) with a precision score of 4%, and a recall score of 67% for high risk applications.

<img width="654" alt="Screen Shot 2021-07-11 at 9 06 40 AM" src="https://user-images.githubusercontent.com/80016496/125198402-543fc780-e227-11eb-9e39-f85039f8d9f2.png">

## Easy Ensemble AdaBoost Classifier
The model had a balanced accuracy score of 91.7%, with a precision score of 9% and a a recall score of 89% for high risk applications. This model proved to be the most affective at accurately identifying the high_risk applicants correctly.

<img width="654" alt="Screen Shot 2021-07-11 at 9 08 10 AM" src="https://user-images.githubusercontent.com/80016496/125198514-cfa17900-e227-11eb-9d7d-53df17d13c7e.png">

# Summary

Given the inherent disparity in data, we employed a few different sampling techniques (oversampling, undersampling, and both) in order to understand which model was most efficient at predicting high risk applicants. In our Random Forest and Ensemble AdaBoost Models the data was resampled in order to prediect the relative risk level of applicants in our data set. The first four models all had low precision and recall scores indicating that they are all laregely ineffective means of managing credit risk for a finacial instituiton. Precision measures how many true "high risk" applicants were in our total high risk determination set. A Low precision indicated that there were many false positive in our model meaning a loss of revenue if these loans were rejected without a manual review. While the Recall scores of the first 4 models (all ~60% range) were better, it still implies the model only identified true high risk applications 60% of the time. Using any of these models would rely on a manual intervention to ensure a large part of the adressable market is not overlooked. When we resampled the data and used ensemble classifiers, we registered a higher precision and recall score for the moidels indicating they are more effective at correctly identifying true high risk applicants and they are more efficient at doing so. I would recommend the Ensemble AdaBoost Classifier for persistent credit risk analysis based on its high precision and recall score. 
