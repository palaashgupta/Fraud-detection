# Decription: Fraud-detection with imbalanced dataset
Credit Card Fraud Detection using various Linear and Non Linear machine learning model.

# Source of The Data: 

1. Using API commands: kaggle datasets download -d mlg-ulb/creditcardfraud
2. Dowloading the CSV file from the kaggle webpage with the link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data

# Target Variable:
'Class': 0 or 1 (Binary classification)

# Project Summary
The project addresses the challenge of fraud detection using a highly imbalanced dataset. In this dataset, there are 284,315 non-fraudulent transactions and only 492 fraudulent transactions, making the detection of fraud particularly challenging due to the class imbalance.

To improve model performance in the face of this imbalance, we applied advanced data preprocessing techniques. Specifically, we utilized SMOTE (Synthetic Minority Over-sampling Technique) combined with Tomek Links. SMOTE generates synthetic samples for the minority class (fraudulent transactions) to balance the dataset, while Tomek Links helps clean up the majority class (non-fraudulent transactions) by removing overlapping examples. This combination helps create a more balanced dataset that can lead to more effective model training.

We evaluated five different machine learning models to determine the best approach for fraud detection:

1. Decision Tree: A simple yet interpretable model that makes decisions based on splitting the data along feature values.
2. XGBoost: An ensemble method known for its high performance and efficiency, which builds multiple decision trees and combines their results.
3. Gaussian Naive Bayes: A probabilistic model that assumes features are normally distributed and calculates the likelihood of fraud based on these distributions.
4. Logistic Regression: A linear model that estimates the probability of fraud by fitting a logistic function to the input features.
5. Neural Network: A deep learning model that captures complex patterns and relationships in the data through multiple layers of interconnected neurons.

Since the dataset is imbalanced, we used the F1 score as our primary evaluation metric. The F1 score balances precision and recall, providing a more comprehensive measure of model performance than accuracy alone.

In addition to the F1 score, we also analyzed the ROC (Receiver Operating Characteristic) curves and AUC (Area Under the Curve) values for each model. The AUC scores, which measure the model's ability to discriminate between fraudulent and non-fraudulent transactions, are as follows:

1. Decision Tree: 0.87
2. XGBoost (Ensemble Method): 0.98
3. Gaussian Naive Bayes: 0.96
4. Logistic Regression: 0.97
5. Neural Network: 0.97
   
The results indicate that XGBoost achieved the highest AUC score, demonstrating superior performance in detecting fraudulent transactions compared to the other models. As such, XGBoost is identified as the most effective model for deployment in this fraud detection system.
