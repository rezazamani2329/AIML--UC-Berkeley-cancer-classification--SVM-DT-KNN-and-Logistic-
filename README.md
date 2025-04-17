# cancer-classification--SVM-DT-KNN-and-Logistic-
## Breast Cancer Prediction
## Python coder: Reza Zamani

# This project has two sections:
## 1- Analysing the cancer cell with SVM
## 2- Comparison of SVM performance with decision trees, logistic regression and KNN


## In section one:
### 1-	First define dummy classifier as baseline classifier. Its score is 0.62
### 2-	I use default SVC: score is 0.98 and check classification report
### 3-	Define grid search
### 4-	I check the optimal kernel, here is the result: 
#### {'gamma': 0.1, 'kernel': 'linear'}
#### 5-	Apply the best model, here is the result of Classification Report: 

  ###                           precision               recall                            f1-score                     support
  ###  0                            0.93                    0.95                                  0.94                         43
 1                             0.97                    0.96                                  0.96                         71

 accuracy                                                                                     0.96                          114
macro avg                0.95                     0.96                                 0.95                         114
weighted avg            0.96                     0.96                                0.96                         114

#### 6-	Use PCA to choose only two feature, here is the results 
#### 7-	Plot the classifiers 

# In Section two- comparison of Algorithms: 
## 1-	I define categorical and numerical columns
## 2-	Apply preprocessor
## 3-	Define models in pipeline , where hyperparameters for each classification is as following 
### 'KNN'n_neighbors': [3, 5, 7],
### 'Logistic Regression': (max_iter=1000), C: [0.1, 1, 10],
### 'SVC' : C': [0.1, 1, 10], kernel': ['linear', 'rbf'],
### 'Decision Trees': max_depth': [5, 10, 15]
## 4-	Here is the comparison of classifiers :

### 	                   Train Score 	            Test Score 	                 Average Fit Time
### KNN 	             0.980220     	       0.947368 	              0.050971
### Logistic Regression      0.986813 	               0.973684 	              0.044642
### SVC 	             0.982418 	               0.982456 	              0.038311
### Decision Trees           0.995604 	               0.947368 	              0.040977
