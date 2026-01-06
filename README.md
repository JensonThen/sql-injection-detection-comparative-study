# Comparative Analysis of SQL Injection Detection and Prevention Techniques in Database Management Systems
Comparison of SQL Injection detection using 12 ML/DL models (CNN-LSTM, BiLSTM, Random Forest, etc.) on 10k query SQLiV3 dataset. A combination of CNN-LSTM provided high accuracy, recall, with latency trade-offs. It includes the Jupyter notebook and results table with plots for security analysis of the DBMS.\
Code can be run by Visual Studio Code & Google Colab\
Dataset from Kaggle (Access Link) : https://www.kaggle.com/datasets/syedsaqlainhussain/sql-injection-dataset
# text
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
**Group G29**  
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
<img src="results/accuracy_plot.png" alt="Accuracy Comparison" width="800"/>
<img src="results/recall_plot.png" alt="Recall Comparison" width="800"/>
<img src="results/f1_plot.png" alt="F1-Score Comparison" width="800"/>
<img src="results/latency_plot.png" alt="Latency Comparison" width="800"/>
<img src="![Uploading Accuracy.png…]()"/>
