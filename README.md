
# 🫀 Heart Failure Mortality Prediction & Analysis

## 📌 Overview

This project aims to **analyze and predict the mortality of heart failure patients** using **Machine Learning** and visualize key health factors through **Power BI dashboards**.

It combines:

1. **Predictive Modeling** – Using Python, Scikit-learn, and TensorFlow to train models that predict the likelihood of patient death (`DEATH_EVENT`) based on clinical data.
2. **Interactive Analytics** – A Power BI dashboard that highlights death event trends across different health attributes like age, blood pressure, anaemia, diabetes, and smoking habits.

---

## 📊 Power BI Dashboard

The Power BI report provides a **visual summary** of mortality patterns in heart failure patients.

**Key Insights Displayed:**

* **Total Death Events** – Overall count of deaths in the dataset.
* **Mortality by Age** – A breakdown showing which age groups are most affected.
* **Mortality by Risk Factors** – Includes high blood pressure, diabetes, anaemia, and smoking.
* **Correlations** – Displays how clinical features (creatinine, ejection fraction, serum sodium, etc.) relate to death events.



## 🤖 Machine Learning Model

**Dataset:**

* Source: `heart_failure_clinical_records_dataset.csv`
* Features: Age, Anaemia, High Blood Pressure, Creatinine Phosphokinase, Ejection Fraction, Platelets, Serum Creatinine, Serum Sodium, Time, etc.
* Target: `DEATH_EVENT` (1 = death occurred, 0 = survived)

**ML Pipeline:**

1. **Data Preprocessing**

   * Missing value check
   * Feature scaling with `StandardScaler`
2. **Exploratory Data Analysis (EDA)**

   * Heatmaps & correlation analysis
   * Distribution plots for each feature
3. **Modeling**

   * **Support Vector Machine (SVM)** for baseline classification
   * **Neural Network** with TensorFlow for improved accuracy
4. **Evaluation Metrics**

   * Accuracy
   * Precision, Recall, F1-Score
   * Classification Report

---

## 🧮 DAX Formula Example (Power BI)

Example measure to calculate deaths for patients aged **60**:

```DAX
TotalDeath_Age60 =
CALCULATE(
    SUM('Table'[DEATH_EVENT]),
    'Table'[age] = 60
)
```

---

## 📂 Project Structure

```
├── heart_failure_prediction.py   # Machine learning model training & evaluation
├── Screenshot 2025-08-12 182322.png  # Power BI dashboard
├── README.md                     # Project documentation
└── dataset.csv                   # Clinical records dataset (not included in repo for privacy)
```

---

## 🚀 How to Run

### **1️⃣ Power BI Dashboard**

* Open `Screenshot 2025-08-12 182322.png` to view the example dashboard.
* Load your dataset into Power BI.
* Add visualizations for `DEATH_EVENT` segmented by clinical features.

### **2️⃣ Python Model**

```bash
# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow

# Run the script
python heart_failure_prediction.py
```

---

## 📈 Results

* **Power BI**: Clear trends show that mortality is higher among patients with **high blood pressure**, **low ejection fraction**, and **older age groups**.
* **Machine Learning**:

  * SVM model achieved moderate accuracy.
  * Neural Network model improved prediction stability and reduced overfitting with dropout layers and early stopping.


If you want, I can **add a "Motivation & Future Work" section** so it reads like a complete professional portfolio project.
Do you want me to add that?
