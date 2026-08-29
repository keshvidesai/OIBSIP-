# L2-Task 3 – Fraud Detection

## 📌 Project Overview

This project focuses on building a **Machine Learning pipeline for detecting fraudulent financial transactions** from a highly imbalanced dataset.

Fraud detection is a challenging classification problem because fraudulent transactions usually represent only a small percentage of total transactions. Therefore, this project focuses on handling **class imbalance** and evaluating the models using metrics such as **Precision, Recall, F1-Score, and AUC-ROC** rather than relying only on accuracy.

---

## 🎯 Objective

The main objectives of this project are:

* Analyze the class imbalance in the transaction dataset.
* Determine the percentage of fraudulent transactions.
* Perform Exploratory Data Analysis (EDA).
* Analyze transaction amounts for fraud and non-fraud transactions.
* Analyze fraud patterns based on transaction time.
* Explain why accuracy can be misleading for imbalanced datasets.
* Handle class imbalance using **SMOTE oversampling**.
* Perform a stratified train-test split.
* Train and compare two machine learning models.
* Evaluate models using Precision, Recall, F1-Score, and AUC-ROC.
* Analyze feature importance and model coefficients.
* Discuss how the fraud detection system can scale to large transaction volumes.



## 🔍 Exploratory Data Analysis

The following analyses were performed:

### Class Imbalance

The number and percentage of fraudulent transactions were calculated to understand the imbalance between fraudulent and legitimate transactions.

### Transaction Amount Analysis

The distribution of transaction amounts was compared between fraudulent and non-fraudulent transactions using histograms and boxplots.

### Time-of-Day Analysis

The `transaction_hour` feature was analyzed to identify patterns in fraudulent transactions across different hours of the day.

---

## ⚠️ Why Accuracy Can Be Misleading

Fraud detection datasets are generally highly imbalanced.

For example, if 99% of transactions are legitimate and only 1% are fraudulent, a model that predicts every transaction as legitimate can achieve 99% accuracy while detecting **zero fraudulent transactions**.

Therefore, accuracy alone is not a suitable metric for this problem.

This project focuses on:

* **Precision**
* **Recall**
* **F1-Score**
* **AUC-ROC**

---

## ⚖️ Handling Class Imbalance

### SMOTE

The project uses **SMOTE (Synthetic Minority Over-sampling Technique)** to address class imbalance.

SMOTE generates synthetic examples of the minority class instead of simply duplicating existing fraud transactions.

SMOTE is applied **only to the training data after the train-test split** to prevent data leakage.

### Workflow

Original Dataset
       ↓
Train/Test Split
       ↓
Preprocessing
       ↓
SMOTE on Training Data
       ↓
Balanced Training Data
       ↓
Model Training
       ↓
Evaluation on Original Test Data


---

## 🧪 Train/Test Split

A **stratified train-test split** was used.

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

Stratification ensures that both the training and testing datasets contain representative proportions of fraudulent and non-fraudulent transactions.

---

## 🤖 Machine Learning Models

Two classification models were trained:

### 1. Logistic Regression

Logistic Regression provides a simple and interpretable baseline model for binary classification.

It also allows coefficient analysis to understand the influence of individual features.

### 2. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees.

It can capture nonlinear relationships between transaction features and fraud and also provides feature importance scores.

---

## 📈 Model Evaluation

The models were evaluated using:

### Precision

Measures how many transactions predicted as fraudulent were actually fraudulent.

### Recall

Measures how many actual fraudulent transactions were successfully detected.

Recall is particularly important in fraud detection because missing a fraudulent transaction can result in financial loss.

### F1-Score

The F1-Score provides a balance between Precision and Recall.

### AUC-ROC

AUC-ROC measures how well the model distinguishes fraudulent transactions from legitimate transactions across different classification thresholds.


🔄 Precision vs Recall Trade-off

Recall is generally given higher importance in fraud detection because the main objective is to identify as many fraudulent transactions as possible.

However, Precision must also be considered. Very low Precision can result in many legitimate transactions being incorrectly flagged as fraudulent.

Therefore, the objective is to achieve **high Recall while maintaining an acceptable level of Precision**.


🔎 Feature Importance

Feature analysis was performed using:

Random Forest Feature Importance
Logistic Regression Coefficients

Random Forest feature importance identifies the features that contribute most to the model's predictions.

Logistic Regression coefficients indicate the direction and strength of the relationship between features and fraud predictions.


📈 Scalability

The system is designed with scalability in mind.

If the system receives **1 million transactions per hour**, it would need to process approximately:


1,000,000 / 3,600 ≈ 277.78 transactions per second


For such a workload, the system could use:

 Real-time model serving
 Apache Kafka for transaction streaming
 Parallel model-serving instances
 Apache Spark for large-scale processing
 Efficient feature preprocessing
 Model monitoring and periodic retraining

The trained preprocessing pipeline and model should be deployed together to ensure that new transactions are processed consistently.


🛠️ Technologies Used

Python
Pandas
NumPy
Scikit-learn
Imbalanced-learn
SMOTE
Matplotlib
Seaborn
Jupyter Notebook


Conclusion

This project demonstrates a complete machine learning pipeline for fraud detection using an imbalanced transaction dataset.

SMOTE was used to address class imbalance, while Logistic Regression and Random Forest were trained for fraud classification. The models were evaluated using Precision, Recall, F1-Score, and AUC-ROC to provide a more meaningful assessment than accuracy alone.

The project also demonstrates feature analysis and discusses how the system could be scaled to handle approximately **1 million transactions per hour** in a real-world environment.


**OIBSIP – Task 3: Fraud Detection**

