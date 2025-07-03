# Cybersecurity-Anomaly-Detectrion

This project implements a Network Intrusion Detection System (NIDS) using a deep learning approach. The system utilizes a Multi-Input Attention-based LSTM model to analyze network traffic data from the UNSW-NB15 dataset and classify it as either benign or malicious.

--- 

# Project Overview
The goal of this project is to demonstrate the effectiveness of deep learning, specifically an attention mechanism combined with an LSTM network, for identifying network intrusions. The UNSW-NB15 dataset, which contains a mix of normal network traffic and various types of attacks, is used for training and evaluating the model.

---

# Features
- Data preprocessing including handling categorical features, feature scaling, and outlier analysis.
- Feature selection using Random Forest importance.
- Implementation of a custom Multi-Input Attention-based LSTM model in PyTorch.
- Training and evaluation of the model on the UNSW-NB15 dataset.
- Visualization of training progress and model performance metrics (Loss, Accuracy, Precision, Recall, F1-score, Specificity, ROC AUC, PR AUC).

---

# Dataset
The UNSW-NB15 dataset is used in this project. It can be obtained from [www.kaggle.com/datasets/mrwellsdavid/unsw-nb15]. The dataset contains 49 features with the class label included.

---

# Model Architecture
 The core of the NIDS is a Multi-Input Attention-based LSTM model.

- It takes two inputs: a set of numerical features and a categorical feature ('proto').
- The 'proto' feature is processed through an embedding layer.
- The numerical features are processed through an LSTM layer.
- An attention mechanism is applied to the LSTM output to focus on the most relevant temporal aspects of the features.
- The output of the attention layer and the 'proto' embedding are concatenated and passed through fully connected layers for final classification.

---

# Benchmarks
The model was evaluated on the test set, achieving the following key performance metrics:

- Accuracy: 0.8266
- Precision: 0.7681
- Recall: 0.9813
- F1-score: 0.8617
- AUC-ROC: 0.9552
- AUC-PR: 0.9651
- Specificity (True Negative Rate): 0.6370

---
