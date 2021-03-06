# Credit Risk Analysis using Supervised Machine Learning Models

## Overview 

LendingClub, a peer-to-peer lending service, wants to compare different machine learning models to identify which best and most accurately represents the results of credit card risk within the dataset. 

We used imbalanced-learn and scikit-learn modules to test a naive oversampling model using RandomOverSampler, an oversampling model using SMOTE, an undersampling model using ClusterCentroids, a combination sampling model using SMOTEENN, and two ensemble learners using BalancedRandomForestClassifier and EasyEnsembleClassifier. 

Each model was used to produce an accuracy score, confusion matrix, and classification report in order to compare the efficacy of each model in predicting credit card risk. 


## Results 

### Naive Random Oversampling Model: 
* Balanced accuracy score: .6456 
* Confusion matrix 

  ![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/de8b704a78368ec244dda7d5684e6abb69b320b3/Screen%20Shot%202022-01-01%20at%201.21.52%20PM.png)
* imbalanced classification report 

  ![classification report](https://github.com/msprech/Credit_Risk_Analysis/blob/2ed5a8d4e413ea2d90bdcd0f87f38abb477d01f3/Screen%20Shot%202022-01-01%20at%201.23.07%20PM.png)
  
### SMOTE Oversampling 
* Balanced accuracy score: .6234
* Confusion matrix 

![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/5d02f2774907c11d14eec34eeae241d1bd30c3e0/Screen%20Shot%202022-01-01%20at%201.26.11%20PM.png)

* Imbalanced classification report 

![report](https://github.com/msprech/Credit_Risk_Analysis/blob/56cf6294042b72205d28b84448b32bb3b83cb62d/Screen%20Shot%202022-01-01%20at%201.27.13%20PM.png)

### Undersampling Model 
* Balanced accuracy score: .5293
* Confusion matrix 

![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/03207808f575f2b1dc216d7351b275b93b6be48a/Screen%20Shot%202022-01-01%20at%201.28.33%20PM.png)

* Imbalanced classification report 

![report](https://github.com/msprech/Credit_Risk_Analysis/blob/122b2e3981b5579fba8e68d3ee5a43590fbf586c/Screen%20Shot%202022-01-01%20at%201.43.02%20PM.png)

### Combination Sampling Model 
* Balanced accuracy score: .6156
* Confusion matrix 

![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/3c03b11e947e9f81f1072a732ccb8c48c3ea362e/Screen%20Shot%202022-01-01%20at%201.44.52%20PM.png)

* Imbalanced classification report

![report](https://github.com/msprech/Credit_Risk_Analysis/blob/308cddd3cefc9404aa7307c31d03cf0cf2e6f432/Screen%20Shot%202022-01-01%20at%201.45.43%20PM.png)

### Balanced Random Forest Classifier 
* Balanced accuracy score: .7877
* Confusion matrix: 

![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/d27d79829b696ea0a1d181fe64099a0aeb6fe79c/Screen%20Shot%202022-01-01%20at%201.47.03%20PM.png)

* Imbalanced classification report 

![report](https://github.com/msprech/Credit_Risk_Analysis/blob/c44e0081c944ea0248b48e3f904ac81fc5511640/Screen%20Shot%202022-01-01%20at%201.47.53%20PM.png)

### Easy Ensemble AdaBoost Classifier 
* Balanced accuracy score: .9254
* Confusion matrix 

![cm](https://github.com/msprech/Credit_Risk_Analysis/blob/fa95f40a27bbdba0c923c6ecae0e3e6592807127/Screen%20Shot%202022-01-01%20at%201.49.26%20PM.png)

* Imbalanced classification report

![report](https://github.com/msprech/Credit_Risk_Analysis/blob/48e5dedbe5500e93316dd13387fadd5714bbbbfe/Screen%20Shot%202022-01-01%20at%201.50.25%20PM.png)

## Summary 

The most consistently high-performing model came in the form of the Easy Ensemble classifier. The accuracy score was very high at .93, as well as were the recall rates for both high risks (.91) and low risks (.94). This is a good indicator that most of the positives were correctly identified, however, the precision rate of high risks were low at .07. This is concerning in a credit risk model because it is a low indicator of reliability in positive classification of high risk credit. 

The F1 score was also relatively low for high-risk cases at .14, while the low-risk score was .97. 

Even though this model outperformed the other five, it still doesn't reliably catch the high-risk cases. Seeing as this is one of the greatest concerns in credit risk and prediction, other models should continue to be evaluated for better precision scores in the high risk cases. 
