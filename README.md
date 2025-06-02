# Machine-Learning-for-Oilfield-Optimization Identifying Intervention Opportunities and Forecasting Production in Ecuadorian Mature Reservoirs
### **By:** Estefi Batallas
### **Tutor:** Ricardo Flores
This project Introduce an automated system powered by machine learning, leveraging historical data on production, pressure tests, and reservoir properties. 

🔍 Project Overview
This notebook presents a machine learning–based workflow designed to optimize well intervention decisions in mature oilfields in Ecuador. It aims to:

Phase 1: Classify the most suitable type of intervention per well (e.g., REPERF, Matrix Stimulation, PURE, Add Intervals).

Phase 2: Predict post-intervention fluid production (BFPD) to prioritize high-impact candidates.

🧾 Data Sources
The final dataset integrates over 76,000 records from four historical sources:

Well Coordinates – Spatial metadata and sand type.

Intervention History – 248 labeled activities (1977–2022) including BOPD, BSW, pressure, etc.

Reservoir Pressure Tests – 3,145 pressure records from various test types.

Production Tests – 70,935 records tracking oil, water, gas production, and well conditions.

🛠️ Workflow Summary
Data Collection & Integration – Excel files loaded from Google Drive, merged into a master dataset.

Exploratory Data Analysis – Distribution checks, t-SNE for class separability.

Feature Engineering – Handling missing values, encoding categories (zone, sand, activity).

Phase 1: Classification – Models: Random Forest, XGBoost, MLP, KNN.

Class balancing with SMOTE, ADASYN, SMOTE+TomekLinks

Best performance: RF + SelectKBest → F1-score: 0.79

Phase 2: Regression (REPERF only) – Models: XGBoost, RF, SVR, Linear/Polynomial.

Best model: XGBoost → R²: 0.71, MAE: 231

Model Evaluation – Cross-validation, hyperparameter tuning, confusion matrix, and feature importance.

🧰 Tools & Libraries
Language: Python

Environment: Google Colab

Libraries: pandas, scikit-learn, xgboost, matplotlib, seaborn, numpy

📂 File Structure
Tesis_EstefiBatallas.ipynb: Main notebook with the full workflow, charts, and model outputs.

All data files are referenced from Google Drive paths and should be adjusted if reused locally.

📌 Notes
This notebook focuses on REPERF prediction for regression due to class limitations.

t-SNE plots indicated significant class overlap; activity focus was reduced for stability.

The solution is extendable to real-time dashboards and alert-based systems.
