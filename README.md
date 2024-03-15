# Fraud Detection Of Financial Transactions

Download the data using link: https://drive.google.com/file/d/18i9lAHzkwxb0hZwYY-b8XxxIpjflSLAR/view?usp=drive_link and name it as creditcard.csv in the root directory.

Sanitized data, removing Null values rows:

![Screenshot 2024-03-15 at 7 08 41 PM](https://github.com/rapolunagarjuna/Fraud-detection-of-financial-transactions/assets/112997527/146dd67e-5f29-46f4-80d8-b3679177c79a)


![Screenshot 2024-03-15 at 7 09 47 PM](https://github.com/rapolunagarjuna/Fraud-detection-of-financial-transactions/assets/112997527/5e00e90d-2e0a-4c78-9c21-ea10428d621d)
![Screenshot 2024-03-15 at 7 10 01 PM](https://github.com/rapolunagarjuna/Fraud-detection-of-financial-transactions/assets/112997527/f5890dff-e12d-42a4-9c52-acdbed3f8327)


## Overview
This project focuses on the detection of fraudulent transactions using credit card data. The primary goal is to identify and flag fraudulent transactions accurately while minimizing the impact on legitimate transactions. In the context of credit card fraud detection:
- **True Positive (TP)**: A fraudulent transaction correctly identified as fraud.
- **True Negative (TN)**: A legitimate transaction correctly identified as non-fraud.
- **False Positive (FP)**: A legitimate transaction incorrectly identified as fraud, leading to potential customer dissatisfaction.
- **False Negative (FN)**: A fraudulent transaction incorrectly identified as non-fraud, posing a risk to the account holder.

## Key Metrics
The performance of fraud detection models is evaluated based on several key metrics:
- **Accuracy**: The proportion of correctly identified transactions (both fraud and non-fraud). `(TP + TN) / Total Instances`
- **Precision**: The proportion of true positive results in all positive predictions. `TP / (TP + FP)` This is critical as high precision reduces false positives, minimizing legitimate transaction disruptions.
- **Recall (Sensitivity)**: The ability of the model to detect all fraudulent transactions. `TP / (TP + FN)` High recall reduces false negatives, ensuring fraudulent transactions are captured.
- **F1 Score**: The harmonic mean of precision and recall, providing a balance between the two. `2 * (Precision * Recall) / (Precision + Recall)`

Given the critical nature of fraud detection, a model must achieve high precision and recall, ensuring both minimal disruption to legitimate transactions and effective identification of fraudulent activities.

## Model Selection
Upon evaluating various machine learning models, it became apparent that not all models suit the nuanced requirements of fraud detection. Decision trees and gradient boosting exhibited lower precision and recall scores, indicating a higher rate of false positives and negatives, which is undesirable.

Comparatively, **Random Forest** and **XGBoost** models demonstrated superior performance across accuracy, precision, and recall metrics. Both models are well-suited for our objectives, but when considering the Area Under the Precision-Recall Curve (AUPRC) and training time, XGBoost stands out. A higher AUPRC indicates a better balance of precision and recall, crucial for fraud detection.

### Why XGBoost?
- **Efficiency and Speed**: XGBoost provides a faster training time compared to Random Forest, making it more efficient for large datasets.
- **Performance**: It offers a comparable, if not superior, balance of precision and recall, essential for minimizing false positives and negatives.
- **Scalability**: XGBoost scales well with data and feature dimensionality, maintaining high performance.

## Conclusion
Considering the criticality of high precision and recall in fraud detection to minimize customer disruption and financial loss, XGBoost emerges as the optimal choice for our credit card fraud detection model. Its efficiency, coupled with outstanding performance metrics, positions it as the best tool for tackling the challenges of fraud detection in financial transactions.
