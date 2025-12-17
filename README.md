# 🧠 Alzheimer’s Disease Prediction Using Machine Learning  
**CRISP-DM Based Approach**

---

## 📌 Project Overview
Alzheimer’s disease is a progressive neurological disorder that leads to memory loss, cognitive decline, and loss of independence. Early detection plays a crucial role in slowing disease progression and improving patient care.

This project applies the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology to develop a **machine learning–based Alzheimer’s prediction model** using clinical and cognitive data. The final model is designed as a **decision-support tool** to assist healthcare professionals in early screening.

---

## 🧩 CRISP-DM Methodology

### 1️⃣ Business Understanding
Traditional Alzheimer’s diagnosis methods are expensive, time-consuming, and require specialist expertise. Delayed diagnosis reduces the effectiveness of interventions.

**Business Objective:**
- Develop a predictive model to identify individuals at high risk of Alzheimer’s disease
- Enable early screening using structured patient data
- Reduce diagnostic delays and healthcare costs
- Support clinicians with data-driven insights

---

### 2️⃣ Data Understanding
The dataset consists of structured clinical and demographic information collected from patient records.

**Key Features:**
- Demographic: `Age`, `Gender`, `EducationLevel`
- Cognitive & Clinical: `MMSE`, `CDR`, `FunctionalAssessment`, `ADL`
- Behavioral: `MemoryComplaints`, `BehavioralProblems`
- Target variable: `Diagnosis` (Alzheimer’s / Non-Alzheimer’s)

**Correlation Insights (Pearson’s Correlation):**
- `MMSE`, `FunctionalAssessment`, and `ADL` are negatively correlated with `Diagnosis`
- `MemoryComplaints` and `BehavioralProblems` are positively correlated with `Diagnosis`

---

### 3️⃣ Data Preparation
- Removed irrelevant identifier columns
- Handled missing values
- Encoded categorical variables
- Ensured correct target formatting

---

### 4️⃣ Modeling
**Models Evaluated:**
- Logistic Regression
- SVM
- Random Forest
- XGBoost

**Final Model:**
- **XGBoost** selected due to higher recall, better confusion matrix performance, and strong accuracy

---

### 5️⃣ Evaluation
- Accuracy
- Recall
- Confusion Matrix
- Classification Report

---

### 6️⃣ Challenges & Limitations
- Data quality and missing values
- Class imbalance
- Limited explainability
- Need for real-world clinical validation

---

## ⚠️ Disclaimer
This project is for educational purposes only and is not a medical diagnostic tool.
