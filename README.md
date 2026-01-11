# ICU Mortality Prediction & Biostatistical Analysis

This repository contains a comprehensive data science pipeline for analyzing ICU patient data. The project emphasizes **clinical interpretability** and **model validation**, using biostatistical methods to identify key risk factors and predict mortality with high precision.

## 📋 Project Scope

The analysis is designed to transform complex physiological data into actionable medical insights through the following stages:

### **1. Data Acquisition & Cleaning**

* **Dataset:** PhysioNet ICU Mortality dataset (sourced via Kaggle).
* **Preprocessing:** Handles high-dimensional medical data, manages missing values, and performs feature engineering on clinical scores like **SOFA** (Sequential Organ Failure Assessment) and **SAPS-I**.

### **2. Exploratory Data Analysis (EDA)**

* **Feature Correlation:** Identifies relationships between vital signs, laboratory results, and patient outcomes.
* **Risk Indicators:** Statistically validates which predictors (e.g., survival time, age, physiological scores) have the highest impact on mortality.

### **3. Modeling & Optimization**

* **Primary Model:** Decision Tree Classifier.
* **Hyperparameter Tuning:** Compares a "Basic" vs. "Optimized" Decision Tree to improve discriminative ability while minimizing overfitting.
* **Validation:** Rigorous checking of the Training-Test gap to ensure the model generalizes well to new patient data.

---

## 📈 Performance Results

The optimized model achieved significant discriminative power, as evidenced by the Area Under the Curve (AUC):

| Metric | Basic Decision Tree | Optimized Decision Tree |
| --- | --- | --- |
| **Test AUC** | 0.9807 | **0.9890** |
| **Training-Test Gap** | 0.0193 | **0.0075** (Better Generalization) |
| **Improvement** | - | +0.9% |

---

## 🏥 Clinical Insights

The analysis yielded several key findings relevant to intensive care:

* **Primary Predictors:** Survival time and severity scores (SOFA/SAPS-I) emerged as the most critical indicators of patient outcome.
* **Interpretability:** Unlike "black-box" models, the **Decision Tree** provides clear, rule-based logic that clinicians can use to understand *why* a certain risk level was assigned.

---

## 🛠️ Tech Stack

* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** `pandas`, `numpy`, `scikit-learn` (Modeling), `matplotlib` & `seaborn` (Visualization).
* **Data Source:** Kaggle / PhysioNet API.

## 🚀 How to Use

1. **Installation:** Ensure you have your Kaggle API credentials configured to download the dataset.
2. **Execution:** Run the notebook.
3. **Review:** The notebook concludes with a detailed **"Validation Status"** and **"Recommendations"** section for clinical implementation.

---

## 🎯 Final Recommendations

1. Implement the optimized Decision Tree rules into clinical decision support systems.
2. Prioritize monitoring of SOFA and SAPS-I scores for early risk detection.
3. Validate performance on external ICU datasets to ensure multi-center reliability.
