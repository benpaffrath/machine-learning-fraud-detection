# Machine Learning Fraud Detection

## Project Goal

The goal of this project is to develop and demonstrate machine learning techniques for detecting fraudulent credit card transactions. Fraud detection is a critical task in financial services to prevent monetary losses and protect customers.

This project focuses on applying classical machine learning methods to distinguish between legitimate and fraudulent transactions with high accuracy, while addressing challenges such as class imbalance and model interpretability.

## Dataset

This project uses the publicly available [Credit Card Fraud Detection dataset from Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

- The dataset contains transactions made by European cardholders in September 2013.
- It includes 284,807 transactions, out of which only 492 are fraudulent, making it a highly imbalanced classification problem.
- Features are numerical and result from a PCA transformation to protect sensitive information.
- The target variable indicates whether a transaction is fraudulent (`1`) or legitimate (`0`).

## Project Structure

```
machine-learning-fraud-detection/
├── data/                       # Directory for storing the creditcard dataset
├── notebooks/                  # Jupyter notebooks for analysis and experiments
├── final_model_training.py     # Production-ready model training code
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## Results

### Logistic Regression

| Metric | Class 0 (Non-Fraud) | Class 1 (Fraud) |
|--------|---------------------|---------------------|
| Precision | 1.0 | 0.87 |
| Recall | 1.0 | 0.80 |
| F1-Score | 1.0 | 0.84 |

### XGBoost

| Metric | Class 0 (Non-Fraud) | Class 1 (Fraud) |
|--------|---------------------|---------------------|
| Precision | 1.0 | 0.93 |
| Recall | 1.0 | 0.82 |
| F1-Score | 1.0 | 0.87 |

Overall ROC-AUC Score:
- Logistic Regression: 0.981
- XGBoost: 0.965

### Conclusion

Despite the marginally lower ROC AUC, XGBoost is the better model for this task due to its stronger precision–recall balance, fewer false positives, and better detection of actual fraud cases.