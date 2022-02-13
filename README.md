# Credit_Risk_Analysis

Overview of the analysis: 

This code trains and evaluates models to predict credit risks using the credit card credit dataset from LendingClub, a peer to peer lending services company.

Credit risk is an unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, this analysis employs different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate the models using resampling.

The following techniques have been used:

 - Oversampling the data using the RandomOverSampler and SMOTE algorithms, 
 - Undersampling the data using the ClusterCentroids algorithm. 
 - A combinatorial approach of over- and undersampling using the SMOTEENN algorithm
 - BalancedRandomForestClassifier and EasyEnsembleClassifier

The analysis will give a recommendation on whether these models should be used to predict credit risk.

---

Results: accuracy scores and the precision and recall scores

 ## 1. Naive Random Oversampling
   
  - Balanced Accuracy score
  
  ![image](https://user-images.githubusercontent.com/91682586/153724383-356f9c32-4a82-4ab2-86ec-7d3ef1873b1e.png)

    - The balanced accuracy score for the naive oversample model is 0.6441747142552103. 
    - That means the classifier seem to predict correctly about 64,4% of the time.
    - This can be misleading for imbalanced models.
    
    - In our case a confusion matrix and an Imbalanced classification report can give better insights because they show which classes are being predicted correctly, 
       or incorrectly, and what type of errors are being made.
       
  - Confusion Matrix
  
  ![image](https://user-images.githubusercontent.com/91682586/153724436-f196bfcc-5f6e-44ee-a7a5-b5ccecb05b7c.png)

  - Imbalanced Classification report
  
  ![image](https://user-images.githubusercontent.com/91682586/153724454-29fa4bc5-7ea7-4464-82cb-50b9fe48b086.png)

   For our model the imbalanced classification report shows the following details:
    
    - Precision is the measure of how reliable a positive classification is. It shows how many of the positive class belong to the positive class.
      The precision for the good loan applications can be determined by the ratio TP/(TP + FP)
     
     - The precicion for high risk is 0.01
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
     
     - Recall shows how well the positive class was predicted.
     
      - The recall for high risk is 0.62
      - The recall for low risk is 0.67
      - the avg/total recall is 0.67
  
      
 ## 2. SMOTE Oversampling
 
  ![image](https://user-images.githubusercontent.com/91682586/153724516-6d8bf8a1-f75b-4a5b-922c-196981b50368.png)

  -  The balanced accuracy score for the Smote oversampled model is 0.6482720346801714. 
     
       
  ##### confusion matrix
  
  ![image](https://user-images.githubusercontent.com/91682586/153724536-c007d50b-eea0-43a7-9c5f-c0c48543fe13.png)

  ##### imbalanced classification report
  
  ![image](https://user-images.githubusercontent.com/91682586/153724548-ca55bb18-6e79-4d28-bee9-026a30e58f3e.png)

  ##### Precision: 
     
     - The precicion for high risk is 0.01
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   ##### Recall:
     
      - The recall for high risk is 0.66
      - The recall for low risk is 0.64
      - the avg/total recall is 0.64

---
   
   
 ## 3. Undersampling

#### balanced accuracy score

  - The balanced accuracy score for the Undersampled model is: 0.6482720346801714
  
-![image](https://user-images.githubusercontent.com/91682586/153724603-7a5df627-da32-4390-844e-07725e0d27b8.png)

##### confusion matrix

![image](https://user-images.githubusercontent.com/91682586/153724626-63260578-c608-41fe-8f63-f1a9c85148b5.png)
 

##### imbalanced classification report 

![image](https://user-images.githubusercontent.com/91682586/153724636-c79580f2-9830-4ff8-b93d-6356d4f7e9f7.png)


##### Precision: 
     
     - The precicion for high risk is 0.01
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   ##### Recall:
     
      - The recall for high risk is 0.57
      - The recall for low risk is 0.45
      - the avg/total recall is 0.45


---

 ## 4. Combination (Over and Under) Sampling (SMOTEENN)

#### balanced accuracy score

- The balanced accuracy score for the SMOTEENN model is: 0.5124410279963418
![image](https://user-images.githubusercontent.com/91682586/153724681-9cace363-123a-4d93-b765-3b024fbbac6c.png)

##### confusion matrix

![image](https://user-images.githubusercontent.com/91682586/153724701-94788919-3124-4412-8c79-8aa62c66ad7f.png)
 
##### imbalanced classification report 

![image](https://user-images.githubusercontent.com/91682586/153724712-dc2676fc-ba1d-4b3c-b0c8-ff1a06bc3b04.png)

 ##### Precision: 
     
     - The precicion for high risk is 0.01
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   ##### Recall:
     
      - The recall for high risk is 0.69
      - The recall for low risk is 0.58
      - the avg/total recall is 0.58
 
---

 ## 5. Balanced Random Forest Classifier
    
 #### balanced accuracy score

- The balanced accuracy score for the Balanced Random Forest Classifier model is: 0.7844011748069183

![image](https://user-images.githubusercontent.com/91682586/153730376-535f3d82-f216-4770-a40e-0a3603fdb223.png)

##### confusion matrix

![image](https://user-images.githubusercontent.com/91682586/153730395-993b62c8-415a-402c-a6bc-84e3c20c31f5.png)


##### imbalanced classification report 
![image](https://user-images.githubusercontent.com/91682586/153730420-82439e94-58ee-4e51-9de0-83a58310f9eb.png)

##### Precision

     - The precicion for high risk is 0.03
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   ##### Recall:
     
      - The recall for high risk is 0.68
      - The recall for low risk is 0.89
      - the avg/total recall is 0.89
 
---

    
## 6. Easy Ensemble AdaBoost classifier
    
   #### balanced accuracy score

- The balanced accuracy score using the Easy Ensemble AdaBoost classifier is: 0.9243174154247797

![image](https://user-images.githubusercontent.com/91682586/153730589-c7cc482f-9c1a-40d9-8381-929d885ef90c.png)


   ##### confusion matrix

![image](https://user-images.githubusercontent.com/91682586/153730617-035e2edd-9c7f-4ca9-beb6-bcabeab0622d.png)

   ##### imbalanced classification report 
   
![image](https://user-images.githubusercontent.com/91682586/153730623-e8653a72-8fc8-4938-bea7-d1c2d0b7483c.png)


   ##### Precision

     - The precicion for high risk is 0.07
     - The precision for low risk is 1.00
     - The avg/total precision is 0.99
     
   ##### Recall:
     
      - The recall for high risk is 0.91
      - The recall for low risk is 0.94
      - the avg/total recall is 0.94
 
---

## Summary: 

The balanced accuracy score is not the best measurement for an imbalanced model.
Therefore I would recommend to use the Easy Ensemble AdaBoost classifier as it seems to predict the credit risk best.
It has the highest recall. Recall is the ability of the classifier to find all the positive samples, which will be the the highest proirity in order find the high risks and in addition has the same high precision as the second ranking Balanced Random Forest Classifier.


