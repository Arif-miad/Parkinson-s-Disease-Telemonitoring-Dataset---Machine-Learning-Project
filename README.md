# Parkinson's Disease Telemonitoring Dataset - Machine Learning Project

## Overview

The Parkinson's Disease Telemonitoring Dataset is a comprehensive collection of biomedical voice measurements from 42 patients with early-stage Parkinson's disease. The primary goal of this project is to leverage machine learning techniques to predict Parkinson's disease symptom severity, as measured by motor and total Unified Parkinson's Disease Rating Scale (UPDRS) scores, using the voice features available in the dataset.

---

## Dataset Description

### Source:

- Created by Athanasios Tsanas and Max Little, University of Oxford.
- Collaboration with 10 US medical centers and Intel Corporation.
- Original paper: "Accurate telemonitoring of Parkinson's disease progression by non-invasive speech tests" (Tsanas et al., IEEE Transactions on Biomedical Engineering, 2009).

### Structure:

- **Format**: CSV (Comma-Separated Values).
- **Records**: 5,875 voice recordings.
- **Subjects**: 42 patients with approximately 200 recordings per patient.

### Attributes:

1. **subject#**: Unique identifier for each patient.
2. **age**: Patient’s age.
3. **sex**: Gender of the patient (0 = male, 1 = female).
4. **test\_time**: Days since recruitment into the study.
5. **motor\_UPDRS**: Motor UPDRS score (target variable).
6. **total\_UPDRS**: Total UPDRS score (target variable).
7. **Voice Features**:
   - Jitter-related measures: `Jitter(%)`, `Jitter(Abs)`, `Jitter:RAP`, `Jitter:PPQ5`, `Jitter:DDP`
   - Shimmer-related measures: `Shimmer`, `Shimmer(dB)`, `Shimmer:APQ3`, `Shimmer:APQ5`, `Shimmer:APQ11`, `Shimmer:DDA`
   - Noise-to-tonal ratio: `NHR`, `HNR`
   - Nonlinear dynamics: `RPDE`, `DFA`, `PPE`

---

## Objectives

The project aims to:

1. Develop machine learning models to predict `motor_UPDRS` and `total_UPDRS` using the voice features.
2. Analyze the relationships between biomedical voice measurements and disease severity.
3. Identify the most important features contributing to Parkinson's disease symptom progression.
4. Evaluate the potential of voice-based telemonitoring for early detection and monitoring of Parkinson’s disease.

---

## Key Steps

### 1. Data Understanding and Exploration

- Load and inspect the dataset for missing values, outliers, and data distribution.
- Perform Exploratory Data Analysis (EDA) to visualize trends and relationships.

### 2. Data Preprocessing

- Handle missing or inconsistent values.
- Normalize or standardize features for optimal model performance.
- Encode categorical variables (e.g., `sex`).

### 3. Feature Engineering

- Analyze feature importance using correlation and statistical tests.
- Create new features if beneficial (e.g., feature combinations or transformations).

### 4. Model Development

- Experiment with regression models:
  - Linear Regression
  - Random Forest Regressor
  - Gradient Boosting (e.g., XGBoost, LightGBM)
  - Neural Networks (if applicable)
- Compare performance using metrics like RMSE, MAE, and R^2.

### 5. Model Evaluation

- Perform cross-validation to ensure robustness.
- Use feature importance techniques (e.g., SHAP, permutation importance) to interpret results.

### 6. Deployment (Optional)

- Develop a simple web application to showcase predictions.
- Use libraries like Flask or Streamlit for deployment.

---

## Tools and Technologies

- **Programming Language**: Python
- **Libraries**:
  - Data Analysis: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `scikit-learn`, `xgboost`, `lightgbm`
- **Development Environment**: Jupyter Notebook or Kaggle Notebooks
- **Version Control**: GitHub

---

## References

1. Tsanas A., Little M.A., McSharry P.E., Ramig L.O. (2009), "Accurate telemonitoring of Parkinson’s disease progression by non-invasive speech tests," IEEE Transactions on Biomedical Engineering.
2. Little M.A., McSharry P.E., Hunter E.J., Ramig L.O. (2009), "Suitability of dysphonia measurements for telemonitoring of Parkinson’s disease," IEEE Transactions on Biomedical Engineering.

---

## Citation

If you use this dataset, please cite:

- A Tsanas, M.A. Little, P.E. McSharry, L.O. Ramig (2009), "Accurate telemonitoring of Parkinson's disease progression by non-invasive speech tests," IEEE Transactions on Biomedical Engineering.

---

## Future Work

- Extend the analysis by incorporating additional voice datasets.
- Explore deep learning models for feature extraction and prediction.
- Investigate the feasibility of real-time voice-based Parkinson’s monitoring.

---

