# 🩺 Predicting Diabetes Risk: Leveraging Machine Learning for Early Detection and Intervention

**Course:** DATA 110: Introduction to Data Science  
**Instructor:** Professor Richard Marks  
**Team:** Agustin Orozco, Prateek Mishra, David Yeboah, Yannick Apedo  
**Project Name:** Glucose Gurus

---

## 📌 Project Overview

Diabetes is a growing global health crisis that requires early detection to mitigate complications. This project explores how machine learning can classify individuals as non-diabetic, prediabetic, or diabetic using lifestyle and health indicators. By analyzing Behavioral Risk Factor Surveillance System (BRFSS) data, we aimed to create a predictive model that can support early intervention strategies and public health planning.

---

## 📊 Data Source

- **Dataset:** 2015 BRFSS (Behavioral Risk Factor Surveillance System)
- **Samples:** 253,680 individuals
- **Target Variable:** `Diabetes_012`  
  - 0 = Non-diabetic  
  - 1 = Prediabetic  
  - 2 = Diabetic
- **Features Included:**  
  - Demographics: Age, Sex, Income, Education  
  - Behavioral: Physical activity, Smoking, Alcohol use, Diet  
  - Health Indicators: BMI, Mental/Physical health, Hypertension, Cholesterol

> ⚠️ *Note: Dataset is self-reported and may include response bias.*

---

## 🛠️ Methods

### 🔬 Data Preparation
- Removed missing values
- Scaled continuous features (e.g., BMI, MentHlth)
- Addressed class imbalance with reweighting and resampling

### 📈 Exploratory Data Analysis
- Correlation heatmaps
- Box plots for BMI vs diabetes class
- Bar plots for prediabetic vs diabetic proportions

### 🤖 Model Building
We tested and evaluated:
- K-Nearest Neighbors (KNN)
- Logistic Regression
- Decision Tree (Final Model)

**Final Model: Decision Tree**
- Handled multiclass classification
- Allowed class weighting for imbalanced data
- Captured nonlinear relationships

### 🧪 Key Predictors
- **Age:** Risk increases with age
- **Glucose Level:** Key diagnostic metric
- **BMI:** Strong predictor of both diabetes and prediabetes

---

## ✅ Results

| Metric       | Class 0 (No Diabetes) | Class 1 (Pre-Diabetes) | Class 2 (Diabetes) |
|--------------|------------------------|-------------------------|--------------------|
| Precision    | High                   | Moderate                | Moderate           |
| Recall       | High                   | Low                     | Low                |
| F1-Score     | Strong                 | Needs Improvement       | Fair               |

- **KNN** underperformed due to class imbalance  
- **Decision Tree** offered better interpretability and handling of minority classes

---

## 🚀 Deployment & Ethics

This model could be embedded in Electronic Health Records (EHR) systems to:
- Flag high-risk individuals
- Support screening prioritization
- Inform personalized interventions

### ⚠️ Limitations & Risks
- Model bias due to class imbalance
- Risk of false negatives in diabetic classification
- Model drift over time
- Limited generalizability across regions/populations

---