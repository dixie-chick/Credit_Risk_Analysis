# Credit_Risk_Analysis
imbalanced-learn and scikit-learn libraries to build machine learning and evaluate models

This analysis uses Python in a machine learning environment including imbalanced-learn and scikit-learn libraries to determine credit risk from loan data from LendingTree. 

## Process
In these models, loan risks are assigned:
- "o" equals high-risk
- "1" equals low-risk

- The first analysis oversamples the data using RanomOverSample and Smote to predict credit risk:
  - Balaned Accuracy Score: 65%
  - ![over](https://user-images.githubusercontent.com/79612565/126854076-19ea1df7-f57d-419c-b951-c54c0cdb7e47.png)


- The second analysis undersamples the data using SMOTEENN to see if this reduces bias from analysis 1
    - Balanced Accuracy Score: 64%
    - ![SMOTE](https://user-images.githubusercontent.com/79612565/126854068-a714ad1b-dde3-4a0a-8069-b8631ee10410.png)

- Finally, the two models are compared to evaluate the performance and determine which model is most accurate
    - Accuracy Score: 55%
    - ![d_2_cluster](https://user-images.githubusercontent.com/79612565/126854064-9595e786-16ea-4634-814e-37718c8dc1d8.png)


### Additional Models
In addition to the above models, ensemble learning is used to combine multiple models helping improve accuracy and robustness as well as decrease variance of the model thereby increasing overall performance.

- First RandomForest samples data to build several small decision trees
    - Accuracy Score: 87%
    - ![random_forest](https://user-images.githubusercontent.com/79612565/126854053-f244ec53-3b70-416b-a2a1-00654ddf9147.png)


- Next Boosting is used to combine weak learners to learn the mistakes of the previous model
    - Accuracy Score:
    - ![ADA_BOOST](https://user-images.githubusercontent.com/79612565/126854054-4bd03956-799f-4cc7-9662-80f69bc2bfb2.png)


## To Wrap It Up
Based on the above outcomes and scores, the AdaBoost Ensemble Model outperformed the others meaning it is the most accurate in prediction. For credit-risk evaluation, having false positives can be extremely dangerous in that what could be a high-risk loan is being incorrectly classified as low risk. LendingTree may use the AdaBoost Ensemble Model model for future assesements. 
