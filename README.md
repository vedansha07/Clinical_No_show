# Clinical Appointment No-Show Prediction System

## 📌 Overview
This project predicts the probability that a patient will miss a scheduled clinical appointment (No-Show) using traditional machine learning techniques.

The system includes:
- Data preprocessing & feature engineering
- Model training & evaluation
- Risk categorization
- Interactive Streamlit-based deployment

---

## 🎯 Problem Statement
Missed medical appointments lead to:
- Revenue loss
- Inefficient scheduling
- Wasted medical resources

This system helps clinics proactively identify high-risk appointments and take preventive action.

---

## 📊 Dataset
Source: Kaggle – Medical Appointment No Shows

Link: https://www.kaggle.com/datasets/joniarroba/noshowappointments

Key Features Used:
- Lead time (days between booking and appointment)
- Lead time bucket (engineered feature)
- Age & age group
- SMS received
- Day of week
- Medical history indicators (Diabetes, Hypertension, Alcoholism, Handicap)
- Interaction features (e.g., SMS × lead time)

Target Variable:
- `No-show` (1 = No-show, 0 = Show)

---

## 🛠 Feature Engineering
The following engineered features were added:
- Lead time calculation
- Lead time bucketization
- Age grouping
- Weekend indicator
- SMS–Lead Time interaction feature

---

## 🤖 Model Used
Random Forest Classifier

Hyperparameters:
- n_estimators = 500
- max_depth = 12
- min_samples_split = 10
- class_weight = "balanced"

---

## 📈 Model Performance

| Metric        | Value |
|---------------|-------|
| ROC-AUC       | ~0.73 |
| Accuracy      | ~0.61 |
| Recall (No-Show Class) | ~0.77 |

The model prioritizes recall for the No-Show class to minimize missed high-risk cases.

---

## 🖥 System Features

✔ Upload appointment CSV  
✔ Predict no-show probability  
✔ Risk classification (Low / Medium / High)  
✔ Risk distribution summary  
✔ Model feature importance visualization  

---

## 🚀 How to Run Locally

```bash
pip install -r requirements.txt
streamlit run app.py
