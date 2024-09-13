# Lead Scoring Case Study
## Introduction
This project aims to develop a lead scoring model for X Education, an online course provider. The company's sales conversion rate was around 30%, and the goal was to prioritize leads more effectively, thereby improving the conversion rate to 80%. This lead scoring model assigns a score to each lead, reflecting their likelihood of converting into paying customers, empowering the sales team to prioritize high-potential leads.

## Problem Statement
X Education faced challenges converting website visitors to paying customers. With an initial conversion rate of approximately 30%, the company wanted a tool to identify leads with a higher probability of conversion. The CEO set a goal of achieving an 80% conversion rate, necessitating a predictive model that could score leads based on conversion potential.

## Approach
**1. Data Exploration:**

- The dataset contained **9240 unique customer entries**.
- During exploratory data analysis, features with missing values were imputed. For features with many missing values, placeholders such as "missing" or "select" were used, while for others, the median or most frequent value was applied.
- Categorical features were one-hot encoded, and numerical features underwent scaling to ensure uniformity during modeling.
  
**2. Feature Engineering:**

- Dummy variables were created for categorical features.
- Recursive Feature Elimination (RFE) was employed to select the top **15 most influential features**, including Total Time Spent on Website, Do Not Email, and Lead Source.
- Scaling was applied to numerical features to normalize the dataset.
  
**3. Modeling:**

- The model was built using **Logistic Regression** due to its effectiveness in classification problems.
- The dataset was split into **70% training** and **30% test** sets.
- **Min-Max Scaling** was applied to numerical variables.
  
**4. Threshold Optimization:**

- The model's threshold was adjusted to **improve precision** and reduce false positives. The optimal cutoff was determined to be **0.33**, improving **accuracy to 80%**.
  
**5. Model Evaluation:**

- The model achieved an **accuracy of 80.8%** on the test set with a **sensitivity of 82%** and **specificity of 79%**. This performance aligns well with the business goal of identifying high-potential leads for prioritization.
- The **ROC** curve showed an **AUC of 0.88**, indicating strong discrimination ability between positive (converted leads) and negative (non-converted leads) cases.
- **Precision and recall** metrics were also analyzed, with precision at **81%** and recall at **80%**.
## Observations
**Top Features:**

- **Total Time Spent on Website:** The more time a lead spends on the website, the higher the likelihood of conversion.
- **Lead Origin:** Leads from sources such as API submissions and landing pages have a higher conversion potential.
- **Occupation and Email Preferences:** "Do Not Email" flags and occupation data significantly affect conversion probabilities.
  
**Train Data:**

- Accuracy: 80%
- Sensitivity: 83%
- Specificity: 78%
  
**Test Data:**

- Accuracy: 80.8%
- Sensitivity: 82%
- Specificity: 79%
## Conclusion
The logistic regression model provides reliable predictions, achieving an **accuracy of over 80%** on both the training and test datasets. The model successfully identifies potential leads by ranking them based on conversion likelihood, thus aiding in optimizing marketing efforts. Furthermore, the selected features provide valuable insights into customer behavior and lead sources, enabling targeted lead nurturing strategies.

The model shows robustness and adaptability, and with regular updates, it can serve as an effective tool for X Education to increase their conversion rate and meet business goals.
