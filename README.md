# Load Type Prediction Using Machine Learning

## Overview
This project focuses on building a machine learning classification model to
predict the **Load_Type** of a power system based on historical energy usage
and operational parameters. The load categories include **Light_Load**,
**Medium_Load**, and **Maximum_Load**.

The objective of this assignment is to demonstrate a complete and structured
machine learning workflow, including data preprocessing, exploratory data
analysis, model training, and evaluation using real-world constraints.

---

## Dataset Description
The dataset consists of historical power system measurements with the
following key features:

- **Usage_kWh** – Industry energy consumption (kWh)
- **Lagging_Current_ReactivePower_kVarh**
- **Leading_Current_Reactive_Power_kVarh**
- **CO2tCO2** – Carbon dioxide emission indicator
- **Lagging_Current_Power_Factor**
- **Leading_Current_Power_Factor**
- **NSM** – Number of seconds from midnight
- **Load_Type** – Target variable (categorical)

The dataset represents continuous-time measurements and reflects realistic
operational behavior of a power system.

---

## Approach
The project follows a structured machine learning pipeline:

1. **Data Loading and Validation**
   - Loaded dataset using Pandas
   - Verified data types and checked for missing values

2. **Exploratory Data Analysis (EDA)**
   - Analyzed class distribution
   - Visualized feature behavior across load categories
   - Identified class imbalance and feature relevance

3. **Data Preprocessing**
   - Standardized column names
   - Removed timestamp-based features with low predictive value
   - Handled missing values using median imputation
   - Encoded target labels using Label Encoding

4. **Feature Scaling**
   - Applied StandardScaler to normalize numerical features

5. **Train–Test Split**
   - Implemented a **time-based split**
   - Used the most recent 10% of data as the test set to simulate
     real-world forecasting scenarios

6. **Model Building**
   - Logistic Regression (baseline model)
   - Decision Tree Classifier
   - Random Forest Classifier

7. **Model Evaluation**
   - Evaluated models using Accuracy, Precision, Recall, and F1-score
   - Used a confusion matrix for class-wise performance analysis

---

## Results Summary
- Logistic Regression provided a baseline performance.
- Decision Tree achieved the highest accuracy but showed potential overfitting.
- Random Forest demonstrated more stable and generalized performance across
  all load categories.

Model selection was based on **overall robustness and generalization**, not
accuracy alone.

---

## Tools and Technologies
- **Python**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---
## Conclusion
This project demonstrates a complete end-to-end machine learning workflow
aligned with industry best practices. The use of time-based validation,
multiple models, and comprehensive evaluation ensures that the solution is
both realistic and production-aware.
