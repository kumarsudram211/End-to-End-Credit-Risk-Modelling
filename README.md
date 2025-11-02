# 💳 Credit Risk Modeling

## 🧭 Project Overview

Credit risk modeling is essential for financial institutions to estimate the probability of borrower default and make informed lending decisions.
This project focuses on developing a **machine learning–based credit risk prediction system** using real-world loan data. The primary goal is to identify key factors influencing credit risk, build robust predictive models, and optimize them through hyperparameter tuning to achieve high accuracy and interpretability.

---

## 📂 Data Preprocessing

The dataset consists of borrower demographics, financial details, and loan information with approximately 10% default cases, creating an **imbalanced classification problem**.

**Key preprocessing steps include:**

* Handling **missing values** and outliers
* Encoding **categorical variables** using label or one-hot encoding
* **Feature scaling** using StandardScaler for numerical variables
* Splitting the dataset into **train-test sets (80–20 ratio)**
* Applying **SMOTE (Synthetic Minority Oversampling Technique)** to handle class imbalance

---

## 🧩 Feature Engineering

Feature engineering was performed to enhance model performance and interpretability by:

* Deriving new financial ratios such as **Debt-to-Income** and **Credit Utilization Rate**
* Performing **correlation analysis** to remove redundant features
* Applying **domain knowledge** to create meaningful variables influencing creditworthiness
* Conducting **feature importance analysis** using tree-based models

---

## 🤖 Model Building

Multiple machine learning algorithms were implemented and compared to identify the best-performing model.

**Models evaluated:**

* Logistic Regression
* Random Forest
* XGBoost

After experimentation, **XGBoost** emerged as the most effective model, balancing accuracy and interpretability.

---

## ⚙️ Hyperparameter Tuning

To further optimize model performance, **Optuna** was used for automated hyperparameter tuning.
Key tuned parameters included:

* `n_estimators`
* `max_depth`
* `learning_rate`
* `subsample`
* `colsample_bytree`

This approach ensured optimal bias-variance tradeoff and improved model robustness.

---

## 📈 Model Evaluation

The final model was evaluated using standard classification metrics:

| Metric               |      Score     |
| :------------------- | :------------: |
| **AUC**              |      0.98      |
| **Gini Coefficient** |      0.97      |
| **KS Statistic**     |     86.87%     |
| **Accuracy**         |      High      |
| **Precision/Recall** | Strong balance |

**Model interpretability tools:**

* **SHAP** – Global feature importance visualization
* **LIME** – Local explanation for individual predictions

The evaluation confirmed that the model effectively distinguishes high-risk borrowers with excellent discriminative power.

---

## 🧾 Summary

This project successfully demonstrates a complete end-to-end **credit risk modeling pipeline**, covering:

* Data cleaning and preprocessing
* Feature selection and engineering
* Model training and optimization
* Comprehensive performance evaluation

The resulting model provides a reliable, explainable, and data-driven framework for assessing borrower default risk.
