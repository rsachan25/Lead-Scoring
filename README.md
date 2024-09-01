# Lead-Scoring
## Problem Statement
Our objective is to build a classification machine learning model that assigns lead scores, reflecting the likelihood of conversion. The aim is to prioritize leads with higher scores, indicating a greater chance of conversion.
## Data Exploration
During exploratory data analysis, we identified features with varying numbers of missing values. To prevent data loss, we imputed 'missing' and "select" for features with a high number of missing values. For features with fewer missing values, imputation was done using median values or the most frequent value. Numerical features underwent scaling, and categorical features were one-hot encoded.
## Modeling
The chosen model is logistic regression, and its performance was assessed using k-fold cross-validation. Results indicated satisfactory generalization, ensuring the model's robustness.
## Evaluation
Evaluation metrics include the confusion matrix, precision, and recall scores. Given the company's emphasis on identifying the most potential leads, we increased the model's threshold to enhance precision and reduce false positives. The final evaluation on test data yielded an impressive accuracy of approximately 80%.
Feel free to explore the code and documentation for a detailed understanding of our lead scoring model.
