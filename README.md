# ✈️ Airline Passenger Satisfaction Forecast

This project applies **deep learning and machine learning algorithms** to predict airline passenger satisfaction using demographic, flight, and service-related data. It was completed as a final project for the Deep Learning for Business Outcomes course.

## 📌 Project Overview

Modern airlines can improve operational efficiency and customer retention by accurately predicting passenger satisfaction. In this project, we:

- Collected and preprocessed real-world airline survey data
- Implemented three predictive models:  
  - **Fully Connected Neural Network (FCNN)**  
  - **1D Convolutional Neural Network (CNN)**  
  - **XGBoost**
- Evaluated each model based on accuracy, recall, F1-score, and ROC-AUC

---

## 📂 Dataset

- **Source**: Airline Passenger Satisfaction Dataset (129,880 records, 25 features)
- **Target Variable**: `Satisfaction` (Satisfied vs Neutral/Dissatisfied)
- **Data Types**: Both categorical and numerical features

### 🧼 Preprocessing Steps

- Removed irrelevant columns: `id`, `Unnamed: 0`
- Handled missing values: 393 nulls in `Arrival Delay` → filled with **median**
- Applied:
  - **Label encoding** for binary features: `Gender`, `Satisfaction`
  - **One-hot encoding** for categorical features: `Customer Type`, `Type of Travel`, `Class`
- Standardized `Flight Distance`

---

## 🧠 Models & Results

### 🔷 1. Fully Connected Neural Network (FCNN)

- Architecture: 3-layer network (64-32-1) + ReLU + Dropout
- Final Accuracy: **95.57%**
- F1 Score: **0.9540**
- ROC-AUC: Very high
- ✅ Best overall generalization

### 🔶 2. Convolutional Neural Network (Conv1D)

- Used local feature extraction with global pooling
- Final Accuracy: **85.62%**
- F1 Score: **0.8749**
- ROC-AUC: **0.9603**
- ⚠️ Weaker on non-sequential tabular data

### 🟢 3. XGBoost

- Gradient boosting classifier with `binary:logistic` objective
- Final Accuracy: **97.48%**
- F1 Score: **0.9568**
- ROC-AUC: **0.9603**
- ✅ Best performance with fastest training and lowest overfitting

---

## 📊 Model Comparison

| Model | Accuracy | F1 Score | ROC-AUC |
|-------|----------|----------|---------|
| FCNN  | 95.57%   | 0.9540   | High    |
| CNN   | 85.62%   | 0.8749   | 0.9603  |
| XGBoost | **97.48%** | **0.9568** | **0.9603** |

---

## 📈 Key Insights

- Both **FCNN** and **XGBoost** performed very well for this binary classification task.
- **XGBoost** had a slight edge in performance and training efficiency.
- **CNN** was less effective due to the non-sequential nature of the data.

---

## 📦 Tools Used

- Python
- TensorFlow / Keras (Deep Learning)
- Scikit-learn
- XGBoost
- Pandas / NumPy / Matplotlib

---

## 📁 Project Structure


---

## 👥 Group Members

- **Daniel Du (MSBA)** – Parts 1-6, 8, 9  
- **Keven Xia (MSQF)** – Parts 2, 4, 6-7

📅 Date: October 18, 2024  
🎓 Course: Deep Learning for Prediction of Business Outcomes

---

## 📚 References

Key references include:
- Ian Goodfellow et al. (2016), *Deep Learning*
- Chen & Guestrin (2016), *XGBoost: A Scalable Tree Boosting System*
- Chu et al. (2016), *Data Cleaning Overview and Challenges*
- McKinsey (2017), *Digital Opportunity in Airlines*

> See full bibliography in the final report.
