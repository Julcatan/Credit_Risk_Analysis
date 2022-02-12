# Credit_Risk_Analysis

Overview of the analysis: 

This code trains and evaluates models to predict credit risks using the credit card credit dataset from LendingClub, a peer to peer lending services company..

Credit risk is an unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, this analysis employs different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate the models using resampling.

The following techniques have been used:
 - Oversampling the data using the RandomOverSampler and SMOTE algorithms, 
 - Undersampling the data using the ClusterCentroids algorithm. 
 - A combinatorial approach of over- and undersampling using the SMOTEENN algorithm
 - BalancedRandomForestClassifier and EasyEnsembleClassifier

The analysis will give a recommendation on whether these models should be used to predict credit risk.

Results: 

 1. Naive Random Oversampling
   
   
   count before oversampling - imbalanced
   ![image](https://user-images.githubusercontent.com/91682586/153724318-c0577952-a473-4ea9-90a5-d89053c637f5.png)
count after oversampling - balanced
![image](https://user-images.githubusercontent.com/91682586/153724343-2805d91b-33dc-474b-aa59-777540eb37d1.png)

   Balanced Accuracy score
   ![image](https://user-images.githubusercontent.com/91682586/153724383-356f9c32-4a82-4ab2-86ec-7d3ef1873b1e.png)

   Confusion Matrix
   ![image](https://user-images.githubusercontent.com/91682586/153724436-f196bfcc-5f6e-44ee-a7a5-b5ccecb05b7c.png)

   Imbalanced Classification report
   ![image](https://user-images.githubusercontent.com/91682586/153724454-29fa4bc5-7ea7-4464-82cb-50b9fe48b086.png)

   -
 2.
    -
    -
 3.
    -
    -
 4.
    -
    -
 5.
    -
    -
 6.
    -
    -

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
