# Customer-Lifetime-value-

Customer Lifetime Value (CLV) Prediction – README

Project Overview:

This project builds an end-to-end machine learning pipeline to predict Customer Lifetime Value (CLV) using advanced feature engineering, LightGBM modeling, hyperparameter tuning, and SHAP explainability.
The goal is not only to achieve strong predictive performance but also to deliver transparent, interpretable insights for marketing and retention strategy.

Objectives:

Predict 12-month Customer Lifetime Value (CLV).

Engineer behavioral, demographic, and monetary features.

Build and tune a LightGBM model using RandomizedSearchCV.

Provide full model explainability using SHAP (global + local).

Generate actionable business insights based on top drivers of CLV.

Create individual-level explanations for Low/Medium/High-value customers.

📂 Project Structure
📁 project/
│
├── version_2_0.ipynb        # Jupyter notebook with full pipeline
├── version_2_0.py           # Python script version (exported)
├── README.md                # Documentation (this file)
├── best_model_lgbm.joblib   # Saved trained model (optional)
├── results_summary.json     # Model performance summary (optional)
└── marketing_campaign.csv    # Dataset (original)

🛠️ Technologies Used

Python 3.x

Pandas & NumPy – Data preparation and feature engineering

Matplotlib & Seaborn – Visualization & EDA

LightGBM – High-performance gradient boosting model

Scikit-Learn – Training, tuning, and evaluation

SHAP – Global and local explainability

PartialDependenceDisplay – ICE & PDP plots

📊 Key Steps Performed
1. Exploratory Data Analysis (EDA)

Inspected dataset structure, missing values, and distributions.

Visualized correlations and purchase patterns.

Identified useful customer and transactional indicators.

2. Data Cleaning

Standardized inconsistent categorical values.

Imputed missing Income using median.

Removed IDs and date fields that may cause leakage.

3. Feature Engineering

Created highly predictive CLV features including:

TotalSpend

TotalPurchases

Customer_Tenure

Age, Children

AvgBasket Value

These features capture both customer behavior and purchase intensity.

4. Model Building & Hyperparameter Tuning

Split data into train/test using train_test_split.

Defined a LightGBM regressor with tunable parameters.

Tuned using RandomizedSearchCV (40 iterations, 3-fold CV).

Selected the best_model based on RMSE.

5. Model Evaluation

Metrics computed on unseen test set:

RMSE

MAE

R² Score

These metrics confirm strong predictive performance.

6. SHAP Global Explainability

Computed SHAP values using TreeExplainer.

Generated:

Summary Plot

Bar Plot for Feature Importance

Identified Top-3 CLV drivers.

7. Local Explainability (Customer-Level)

For Low, Medium, and High CLV customers:

Generated SHAP force/waterfall plots.

Explained feature-by-feature contributions to predicted CLV.

8. ICE / PDP Analysis

Created ICE/PDP plots for the top 3 most impactful features.

Showed how varying each feature changes predicted CLV.

9. Executive Summary

Included a business-ready summary highlighting:

Model performance

Key drivers of CLV

Customer segment insights

Top 3 strategic recommendations

🔍 Top 3 Insights (Example from SHAP Output)

High purchase frequency strongly increases CLV.

Customers with larger average basket value remain more valuable long-term.

Customer tenure influences loyalty and CLV growth.

🚀 How to Run the Project
Prerequisites

Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn lightgbm shap

Run Notebook
jupyter notebook version_2_0.ipynb

Run Script
python version_2_0.py

💼 Business Impact

This CLV prediction pipeline empowers marketing teams to:

Identify high-value customers early

Target low-value customers with reactivation strategies

Optimize personalized offers based on customer behavior

Support data-driven acquisition and retention planning

Raja R
Machine Learning & Data Science Practitioner
(Ready for real-world ML deployment and explainable AI projects)
