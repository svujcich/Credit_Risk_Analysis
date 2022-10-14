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
  ![random_oversampling](https://user-images.githubusercontent.com/106559768/195912383-8a77dca2-3750-449e-9d8f-cc1de6057f84.jpg)
  
  ### (2) SMOTE algorithm
  <img width="741" alt="smote_oversampling" src="https://user-images.githubusercontent.com/106559768/195912431-a60fe1ff-7e47-42b8-8ee5-34aef3d2a975.png">
  
  ### (3) ClusterCentroids algorithm
  <img width="773" alt="undersampling" src="https://user-images.githubusercontent.com/106559768/195913170-3f22f9ec-2054-490b-b8b6-ee175f42ecb6.png">

  ### (4) SMOTEEN algorithm
  <img width="770" alt="combo_over_under_sampling" src="https://user-images.githubusercontent.com/106559768/195913212-d833b711-32ff-4bf2-bec9-9f16eeaf7043.png">

  
  
  ### (5) BalancedRandomForestClassifier algorithm
  <img width="749" alt="balanced_random_forest" src="https://user-images.githubusercontent.com/106559768/195913249-323fa4d0-4f7c-449e-8619-c2957a0bc725.png">

  
  
  ### (6) EasyEnsambleClassifier algorithm
<img width="739" alt="easy_ensemble_classifier" src="https://user-images.githubusercontent.com/106559768/195913264-c50eac58-d0c0-4747-8646-f14305fab33b.png">





## Summary
In the scenerio of credit loans, the goal is to detect every high risk loan in the data set. The best metric for summarizing these values is the sensativity scores because it considers every high risk loan in the data set (meaning it considers all the high risk loans that were correctly identified as well as all of the high risk loans which were incorrectly categorized as low risk loans). When looking at the recall scores, the ensamble learners,the BalancedRandomForestClassifier and the EasyEnsambleClassifier, preformed the best with the recall scores. One thing to note is that although the EasyEnsambleClassifier preformed the best, in every scenerio the model preforms exceptionally well. This result is suspicious of overfitting, which means the model might preform differently when presented with a different data set. In this case, the BalancedRandomForest algorithm would be the best model for identifying high risk loans. 




