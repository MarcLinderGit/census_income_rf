# Random Forest Model for Income Classification

**Objective:** This project aimed to build and fine-tune a Random Forest model for income classification based on census data from the 1994 Census database. The primary goal was to predict whether an individual earns more than $50,000 annually using this dataset.

Data source: [UCI Machine Learning Repository - Census Income](https://archive.ics.uci.edu/dataset/20/census+income)

**Project Highlights:**

1. **Exploratory Data Analysis (EDA):** The project began with data exploration to understand the income distribution. It was found that about 77% of the sample had incomes less than $50,000, while 24% had incomes greater than $50,000.

2. **Feature Selection:** Key features were selected for building the Random Forest model, including 'age,' 'capital-gain,' 'capital-loss,' 'hours-per-week,' 'sex,' and 'race.' Categorical variables were converted into binary features using one-hot encoding.

3. **Baseline Model:** A baseline Random Forest model was created with default parameters, resulting in an initial accuracy score on the test set. The accuracy score for the default model was approximately 85.196%.

4. **Hyperparameter Tuning:** The Random Forest model was fine-tuned by testing its performance over a range of `max_depth` values from 1 to 25. The accuracy scores for both the training and test sets were recorded for each `max_depth` value.

5. **Optimal Max_Depth Selection:** The `max_depth` value that yielded the highest accuracy on the test set was identified as the optimal value. In this case, the highest test accuracy was achieved when `max_depth` was set to 12, resulting in an accuracy score of approximately 86.276% on the test set.

6. **Feature Importance Analysis:** The importance of each feature in predicting income status was analyzed using the Random Forest model. The top five features by importance were identified as 'capital-gain,' 'age,' 'hours-per-week,' 'capital-loss,' and 'sex_Male.'

7. **Additional Feature Engineering:** The 'education' feature was further analyzed, and new features, 'education_bin,' were created by binning education levels into three groups: 'HS or less,' 'College to Bachelors,' and 'Masters or more.' The model was then re-tuned with these additional features.

8. **Re-Tuning and Model Improvement:** The Random Forest model was re-tuned with the new features and tested with different `max_depth` values from 1 to 9. The optimal `max_depth` was identified as 9, resulting in an improved test accuracy of approximately 86.446%.

9. **Final Model and Feature Importance:** The final Random Forest model with the optimal `max_depth` of 9 was saved. Feature importances were analyzed again, revealing that having a 'Masters degree or more' was among the top predictors for income classification.

**Conclusion:** This project demonstrated the process of building and optimizing a Random Forest model for income classification. It showcased the importance of hyperparameter tuning and feature engineering in improving model accuracy. Ultimately, the model successfully identified key features that influence income classification, providing valuable insights for future income prediction tasks.