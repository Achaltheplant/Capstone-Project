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

The solution proposed is to utilise an interactive test which is cost-effective screening compared to imaging tests and if a positive is found, the patient can be forwarded to specialists which in turn, is a scalable solution for hospitals and telemedicine platforms
---

### 2️⃣ Data Understanding and Preparation
The dataset consists of structured clinical and demographic information collected from patient records. It was sourced from Kaggle using the link "https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset"

**Key Features:**
- Demographic: `Age`, `Gender`, `EducationLevel`
- Cognitive & Clinical: `MMSE`, `CDR`, `FunctionalAssessment`, `ADL`
- Behavioral: `MemoryComplaints`, `BehavioralProblems`
- Target variable: `Diagnosis` (Alzheimer’s / Non-Alzheimer’s)

**Data Preparation**
- Removed irrelevant identifier columns
- Handled missing values
- Encoded categorical variables
- Ensured correct target formatting


---

### 3️⃣ Explaratory Data Analysis

Heatmap reveals that the features do not have any strong correlations among themselves. However, there are five columns that show a correlation with the target variable

**Correlation Insights (Pearson’s Correlation):**
- `MMSE`, `FunctionalAssessment`, and `ADL` are negatively correlated with `Diagnosis`
- `MemoryComplaints` and `BehavioralProblems` are positively correlated with `Diagnosis`

---

### 4️⃣ Modeling
**Models Evaluated:**
- Logistic Regression:This model was chosen for its simpleness and interpretability and is also used in medical datasets
- SVM: This model was chosen because its good for small datasets and effective with scaled features
- Random Forest: This model was chosen due to its stability and because it handles non linear data well
- XGBoost: This model was chosen because it is what is commonly used in smaller medical datasets since it handles mixed numerical and categorical data well

**Final Model:**
- **XGBoost** selected since XG BOOST offers the best predictive capabilities with an accuracy of 95% predicting 271 true negatives 6 false positives which is a false alarm but medically less dangerous than getting a false negative, 14 false negatives and 139 true posistives.¶

---

### 5️⃣ Evaluation
- Accuracy
- Recall
- Confusion Matrix
- Classification Report
  
  MODEL             ACCURACY     RECALL(0)     RECALL(1)     CONFUSION MATRIX
 RANDOM FOREST        94.42%        0.97          0.89          [270,  8]
                                                                [16 ,136]
 XG BOOST             95.35%        0.98          0.91          [271,  6]
                                                                [14 ,139]
 LOGISTIC REGRESSION  83.02%        0.89          0.73          [246, 31]
                                                                [42 ,111]
 SVM                  83.26%        0.90          0.71          [250, 27]
                                                                [45 ,108]
---

### 6️⃣ Challenges & Limitations
- Data quality and missing values
- Class imbalance
- Limited explainability
- Need for real-world clinical validation
- Need for clinical validation on real-world hospital data
- Potential demographic bias across age and gender groups
- Improved model explainability for clinicians
- Regular retraining with new patient data
  
---

### Conclusion

This project demonstrates how machine learning, guided by the CRISP-DM framework, can support early Alzheimer’s disease screening. The selected XGBoost model shows strong predictive performance while emphasizing clinically important metrics such as recall. Future improvements will focus on explainability, fairness, and real-world deployment readiness.

---

### ⚠️ Disclaimer
This project is for educational purposes only and is not a medical diagnostic tool.
