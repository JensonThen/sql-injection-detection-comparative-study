# Comparative Analysis of SQL Injection Detection and Prevention Techniques in Database Management Systems
Comparison of SQL Injection detection using 12 ML/DL models (CNN-LSTM, BiLSTM, Random Forest, etc.) on 10k query SQLiV3 dataset. A combination of CNN-LSTM provided high accuracy, recall, with latency trade-offs. It includes the Jupyter notebook and results table with plots for security analysis of the DBMS.\

## Accessible By
Code can be run by Visual Studio Code & Google Colab\
Dataset from Kaggle (Access Link) : https://www.kaggle.com/datasets/syedsaqlainhussain/sql-injection-dataset
# requirements.txt Content
pandas\
numpy\
matplotlib\
seaborn\
scikit-learn\
tensorflow>=2.10.0\
xgboost\
kagglehub

# Comparative Study of SQL Injection Detection Models

**University Project – Database Management Systems (SEG2102)**  
**Group 29**  
**Members:** Then Ye Herng (22072466), Tan Kah Lok (24009441), Aw Jun Le (23126048)  

## Project Overview

This repository contains the implementation and results of a comparative analysis of SQL injection (SQLi) detection techniques using traditional machine learning, ensemble methods, and deep learning models.

The study evaluates **12 different models** on a dataset of 10,000 SQL queries (SQLiV3.csv from Kaggle) using the following metrics:
- Accuracy
- Recall
- F1-Score
- Inference Latency (ms per query)

**Key Finding:** The CNN-LSTM hybrid model achieved the highest performance with **99.72% accuracy**, **99.34% recall**, and **99.63% F1-score**, making it the most effective for detecting complex and obfuscated attacks while maintaining reasonable latency.

This work supports the use of hybrid deep learning approaches to enhance data integrity and access control in modern Database Management Systems (DBMS).

## Dataset
- Source: [SQL Injection Dataset (SQLiV3.csv)](https://www.kaggle.com/datasets/syedsaqlainhussain/sql-injection-dataset)
- The dataset is automatically downloaded in the notebook using `kagglehub`.
- Contains ~10,000 labeled SQL queries (benign vs malicious).

## Results Summary

| Model                  | Accuracy (%) | Recall (%) | F1-Score (%) | Latency (ms) |
|------------------------|--------------|------------|--------------|--------------|
| CNN-LSTM Hybrid        | 99.72        | 99.34      | 99.63        | 0.0726       |
| Bidirectional LSTM     | 99.51        | 98.95      | 99.34        | 0.5037       |
| Random Forest          | 99.46        | 98.77      | 99.27        | 0.0181       |
| GRU Network            | 99.41        | 98.46      | 99.20        | 0.2786       |
| Decision Tree          | 99.31        | 98.77      | 99.07        | 0.0002       |
| KNN                    | 99.31        | 98.51      | 99.07        | 0.3150       |
| XGBoost                | 99.25        | 98.24      | 98.98        | 0.0007       |
| SVM (Linear)           | 96.99        | 94.11      | 95.88        | 0.0406       |
| SGD Classifier         | 95.19        | 89.20      | 93.25        | <0.001       |
| Logistic Regression    | 95.00        | 88.67      | 92.96        | <0.001       |
| AdaBoost               | 93.87        | 85.51      | 91.22        | 0.0035       |
| Naive Bayes            | 92.53        | 80.90      | 88.96        | <0.001       |

### Visualizations
[Accuracy Comparison] <img width="1481" height="740" alt="image" src="https://github.com/user-attachments/assets/b107835e-75df-44d5-ad6b-407c9f76e7e9" />
[Recall Comparison]<img width="1480" height="740" alt="image" src="https://github.com/user-attachments/assets/db2fba67-583a-4f8e-8728-1c5bdd269de3" />
[F1-Score Comparison] <img width="1475" height="737" alt="image" src="https://github.com/user-attachments/assets/baa4fb2e-8f73-4b68-baff-c7d134547f52" />
[Latency Comparison] <img width="1473" height="729" alt="image" src="https://github.com/user-attachments/assets/ea7bf406-c40b-4a63-bc0c-824a99bbb1e1" />


