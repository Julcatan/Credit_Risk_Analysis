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

Results: accuracy scores and the precision and recall scores

 1. Naive Random Oversampling
   
      count before oversampling - imbalanced
   ![image](https://user-images.githubusercontent.com/91682586/153724318-c0577952-a473-4ea9-90a5-d89053c637f5.png)
count after oversampling - balanced
![image](https://user-images.githubusercontent.com/91682586/153724343-2805d91b-33dc-474b-aa59-777540eb37d1.png)



   - Balanced Accuracy score
   - ![image](https://user-images.githubusercontent.com/91682586/153724383-356f9c32-4a82-4ab2-86ec-7d3ef1873b1e.png)

     The balanced accuracy score for the naive oversample model is 0.6441747142552103. That means the classifier predicts correctly about 64% of the time.
     
     



   Confusion Matrix
   ![image](https://user-images.githubusercontent.com/91682586/153724436-f196bfcc-5f6e-44ee-a7a5-b5ccecb05b7c.png)

   Imbalanced Classification report
   ![image](https://user-images.githubusercontent.com/91682586/153724454-29fa4bc5-7ea7-4464-82cb-50b9fe48b086.png)

  Precision is the measure of how reliable a positive classification is. It shows how many of the positive class belong to the positive class,
  The precision for the good loan applications can be determined by the ratio TP/(TP + FP)
     
     - The precicion for high risk is 0.01
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   Recall shows how well the positive class was predicted.
     
      - The recall for high risk is 0.62
      - The recall for low risk is 0.67
      - the avg/total recall is 0.67
  
   
  
   
   
   
   
 2. SMOTE Oversampling
    -![image](https://user-images.githubusercontent.com/91682586/153724493-b7e40769-3017-4087-a6ed-2ef31db03549.png)

balanced accuracy score
![image](https://user-images.githubusercontent.com/91682586/153724516-6d8bf8a1-f75b-4a5b-922c-196981b50368.png)


confusion matrix
![image](https://user-images.githubusercontent.com/91682586/153724536-c007d50b-eea0-43a7-9c5f-c0c48543fe13.png)


imbalanced classification report 
![image](https://user-images.githubusercontent.com/91682586/153724548-ca55bb18-6e79-4d28-bee9-026a30e58f3e.png)

   -
 3. Undersampling
    -![image](https://user-images.githubusercontent.com/91682586/153724594-01c98ec6-1e29-4546-b889-2ff2e6621e43.png)
Balanced accuracy score
    -![image](https://user-images.githubusercontent.com/91682586/153724603-7a5df627-da32-4390-844e-07725e0d27b8.png)
confusion matrix
![image](https://user-images.githubusercontent.com/91682586/153724626-63260578-c608-41fe-8f63-f1a9c85148b5.png)
imbalanced classification report 
![image](https://user-images.githubusercontent.com/91682586/153724636-c79580f2-9830-4ff8-b93d-6356d4f7e9f7.png)

 4. Combination (Over and Under) Sampling\

![image](https://user-images.githubusercontent.com/91682586/153724666-fd98b3d2-36bf-42b1-89fe-48b43b580fb3.png)

balanced accuracy score
![image](https://user-images.githubusercontent.com/91682586/153724681-9cace363-123a-4d93-b765-3b024fbbac6c.png)

confusion matrix
![image](https://user-images.githubusercontent.com/91682586/153724701-94788919-3124-4412-8c79-8aa62c66ad7f.png)
 
imbalanced classification report 
![image](https://user-images.githubusercontent.com/91682586/153724712-dc2676fc-ba1d-4b3c-b0c8-ff1a06bc3b04.png)

 
 -
    -
 5. Balanced Random Forest Classifier¶
    -

    -
 6. Easy Ensemble AdaBoost classifier
    -
    -

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
