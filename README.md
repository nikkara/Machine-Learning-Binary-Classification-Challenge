# Machine-Learning-Binary-Classification-Challenge
This repository contains a solution for a binary classification challenge. The task involves developing models to predict a binary outcome based on a provided dataset. Three distinct models were trained and evaluated to assess their performance in predicting the outcomes.
## Dataset
The project utilizes a dataset where the target variable is "transaction". This dataset consists of various numerical and categorical features, from which 20% was reserved for testing, 75% of the remaining for training, and 25% for validation. The dataset required preprocessing which included encoding categorical variables, applying normalization techniques like z-score to manage outliers, and employing oversampling to address class imbalance.
## Models Used
We trained three models for this classification task:
1. **Decision Trees (Baseline Model)**: Chosen for its simplicity, interpretability, and fewer requirements for hyperparameter tuning.
2. **Logistic Regression**: Selected for its ability to provide probabilistic outputs and suitability for binary classification tasks involving both numerical and categorical data.
3. **XGBoost**: Utilized for its strength in handling complex datasets with an ensemble of weak prediction models to improve accuracy.
## Model Training and Hyperparameters
- **Decision Trees**: Minimal tuning required; focused on basic parameters to maintain simplicity.
- **Logistic Regression**: Hyperparameters tuned included regularization strength (C), penalty type (l1, l2), solver (liblinear, saga), and max iterations using GridSearch to find the optimal settings.
- **XGBoost**: Tuned using the Optuna framework with hyperparameters like n_estimators, max depth, learning rate, subsample rates, and regularization parameters (reg_alpha & reg_lambda).
## Results and Discussion
The models were evaluated using F1-score, precision, and recall:
- **XGBoost** showed the best performance with an F1 score of 0.84, demonstrating its robustness in handling the dataset complexities.
- **Decision Trees** provided a solid baseline with an F1 score of 0.78.
- **Logistic Regression** showed an F1 score of 0.77, indicating a slight struggle with class imbalance despite tuning.

Confusion matrices for each model indicated higher true positives and true negatives compared to false positives and false negatives, validating the effectiveness of the models in classifying the transaction outcomes accurately.
