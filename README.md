Project Overview
Goal of this project is to build a machine learning model to detect fraudulent credit card transactions. This ensures that customers are not charged for items they did not purchase.

Dataset Description
• Source: Data is from Kaggle. Link  : "https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download"
• Nature of Data: Dataset as highly imbalanced. It contains transactions made by European cardholders, where the vast majority of transactions are "Normal" (labeled as 0) and a very small fraction are "Fraudulent" (labeled as 1).
• Features: The features (V1-V28) are transformed using Principal Component Analysis (PCA) to protect user identity and confidentiality.

Workflow & Methodology
Steps:
1. Data Pre-processing: Data is imbalanced, used under-sampling technique.
2. Balancing the Data: Created a new dataset with a uniform distribution, combining the 492 fraudulent transactions with a random sample of 492 normal transactions.
3. Model Selection: Used Logistic Regression, as it is well-suited for binary classification problems.
Results and Performance
Accuracy metrics achieved by the model:
• Training Data Accuracy: Approximately 94%.
• Test Data Accuracy: Approximately 92.9% (nearly 93%).
• The similarity between training and test accuracy suggests the model is not overfitted.
Required Libraries
The Python libraries used in the project:
• numpy
• pandas
• scikit-learn
