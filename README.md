Project Overview
Goal of this project is to build a machine learning model to detect fraudulent credit card transactions. This ensures that customers are not charged for items they did not purchase.

Dataset Description

• Source: Data is from Kaggle. Link  : "https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download"

• Nature of Data: Dataset as highly imbalanced. It contains transactions made by European cardholders, where the vast majority of transactions are "Normal" (labeled as 0) and a very small fraction are "Fraudulent" (labeled as 1).

• Features: The features (V1-V28) are transformed using Principal Component Analysis (PCA) to protect user identity and confidentiality.

In Project 10: 

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


In Anamoly Detection :

Exploratory Data Analysis (EDA):

• Transaction Amount: Fraudulent transactions tend to involve smaller amounts compared to normal transactions.
• Sampling: To manage execution time during development, a fraction of the data (0.1%) was used for initial processing.
• Correlation: A correlation matrix was used to understand how features relate to the 'Class' variable.

Algorithms Implemented

The project explores three main algorithms to detect outliers:
1. Isolation Forest: This algorithm isolates observations by randomly selecting a feature and a split value. Outliers are easier to isolate and require fewer splits, resulting in a lower depth/score in the decision tree.
2. Local Outlier Factor (LOF): This technique computes the local density deviation of a data point relative to its neighbors. Points with a substantially lower density than their neighbors are considered outliers.
3. Support Vector Machine (SVM): Used to establish a decision boundary to separate outliers, though it may not perform as well on highly imbalanced data compared to the other two methods.

Project Results

The models were evaluated based on the number of errors (misclassified transactions) and overall accuracy scores:
• Isolation Forest: Detected 73 errors with an accuracy of 99.74%.
• Local Outlier Factor: Detected 97 errors with an accuracy of 99.65%.
• SVM: Performed the worst, detecting 8,516 errors with an accuracy of approximately 70%.

Conclusion
Isolation Forest outperformed both LOF and SVM in correctly determining fraudulent transactions. It proved to be highly effective at handling the imbalanced nature of the credit card transaction data.


Required Libraries
The Python libraries used in the project:
• numpy
• pandas
• scikit-learn
