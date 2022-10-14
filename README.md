### Overview
Supervised machine learning is a process that uses a dataset to train a model to predict an outcome with known answers. In the circumstance of credit risk, the number of good loans disproportionately outnumber the risky loans, which creates a challenge in accurately training a model to identify risky loans. To address this lack of balance, this analysis uses the following supervised machine learning techniques to train and evaluate models to identify which models best predict credit risk in this scenerio. 
  - Oversampling
    - (1) RandomOversampler algorithm
    - (2) SMOTE algorithm
  - Under sampling
    - (3) ClusterCentroids algorithm
  - Combination of over and under sampling
    - (4) SMOTEEN algorithm
  - Ensemble Classifiers 
    - (5) BalancedRandomForestClassifier algorithm
    - (6) EasyEnsambleClassifier algorithm

## Results
- Balanced accuracy scores
  - (1) RandomOversampler algorithm: 0.66
  - (2) SMOTE algorithm: 0.66
  - (3) ClusterCentroids algorithm: 0.54
  - (4) SMOTEEN algorithm: 0.67
  - (5) BalancedRandomForestClassifier algorithm: 0.78
  - (6) EasyEnsambleClassifier algorithm: 0.93


- Precision scores
  - (1) RandomOversampler algorithm: 0.99
  - (2) SMOTE algorithm: 0.99
  - (3) ClusterCentroids algorithm:0.99
  - (4) SMOTEEN algorithm: 0.99
  - (5) BalancedRandomForestClassifier algorithm: 0.99
  - (6) EasyEnsambleClassifier algorithm: 0.99


- Recall (sensativity) Scores
  - (1) RandomOversampler algorithm: 0.60
  - (2) SMOTE algorithm: 0.69
  - (3) ClusterCentroids algorithm:0.40
  - (4) SMOTEEN algorithm: 0.57
  - (5) BalancedRandomForestClassifier algorithm: 0.87
  - (6) EasyEnsambleClassifier algorithm: 0.94
  
  ### RandomOversampler Algorithm
  <img width="770" alt="random_oversampling" src="https://user-images.githubusercontent.com/106559768/195916792-9cc8479b-0263-4a2b-b240-227b9c57f507.png">
 
  ### (2) SMOTE algorithm
  <img width="770" alt="smote_oversampling" src="https://user-images.githubusercontent.com/106559768/195916806-6751b6ff-04e4-4af7-a808-72c7f25136cf.png">

  ### (3) ClusterCentroids algorithm
  <img width="770" alt="undersampling" src="https://user-images.githubusercontent.com/106559768/195916837-d5c8f1cc-f038-49bf-80a4-ee3ff050bf91.png">

  ### (4) SMOTEEN algorithm
  <img width="768" alt="smoteenn_over_under_sampling" src="https://user-images.githubusercontent.com/106559768/195916856-7ee3f551-e84a-4a6a-bf79-6e0a3901c883.png">
  
  ### (5) BalancedRandomForestClassifier algorithm
  <img width="768" alt="bal_random_forest" src="https://user-images.githubusercontent.com/106559768/195916869-03a5bf40-21cc-4fca-ad89-9b91be8597f2.png">
  
  ### (6) EasyEnsambleClassifier algorithm
  <img width="769" alt="easy_ensamble" src="https://user-images.githubusercontent.com/106559768/195916895-8c09f57c-df2d-451c-a2f4-4471e9ae5726.png">





## Summary
In the scenerio of credit loans, the goal is to detect every high risk loan in the data set. The best metric for summarizing these values is the sensativity scores because it considers every high risk loan in the data set (meaning it considers all the high risk loans that were correctly identified as well as all of the high risk loans which were incorrectly categorized as low risk loans). When looking at the recall scores, the ensamble learners,the BalancedRandomForestClassifier and the EasyEnsambleClassifier, preformed the best with the recall scores. One thing to note is that although the EasyEnsambleClassifier preformed the best, in every scenerio the model preforms exceptionally well. This result is suspicious of overfitting, which means the model might preform differently when presented with a different data set. In this case, the BalancedRandomForest algorithm would be the best model for identifying high risk loans. 




