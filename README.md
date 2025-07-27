# Credit Card Behaviour Score Prediction Using Classification and Risk-Based Techniques

## Overview
This project aims to enhance **Bank A's credit risk management framework** by developing a forward-looking **Behaviour Score** classification model.This model predicts whether a credit card customer will default on their payment in the following mont. Utilizing historical behavioral data from **over 30,000 anonymized credit card customers** , the goal is to accurately flag potential defaulters in advance, enabling the bank to adjust credit exposure, trigger early warning systems, and prioritize risk-based actions.Beyond mere prediction, the project focuses on creating a **financially interpretable model** that helps the bank understand default patterns and manage credit exposure effectively.

## Dataset
The project utilizes an anonymized dataset of historical credit card customer behavior. Key variables include:
*`Customer Id`: Unique identifier for each customer.
* `marriage`: Marital status.
* `sex`: Gender.
* `education`: Education level.
* `LIMIT_BAL`: Credit limit assigned.
* `Age`: Age of the customer.
* `Pay_m (Pay_0 to 6)`: Payment status in various months.
* `Bill_amt_m (Bill_amt1 to 6)`: Total bill amount at the end of various months.
* `Pay_amt_m (Pay_amt1 to 6)`: Payment amount made in various months.
* `AVG_Bill_amt`: Average bill amount over 6 months.
* `PAY_TO_BILL_ratio`: Ratio of total payment to total bill amount over 6 months.
* `next_month_default`: Target variable (1 = default, 0 = no default).

The dataset is split into:
* **Train Dataset:** ~25,000 records, including features and the `next_month_default` target variable.
* **Validation Dataset:** ~5,000 records, containing the same features without the target variable, for which predictions must be generated.

## Objectives
The key objectives of this project are:
* **Build a binary classification model** to predict customer default (`next_month_default`).
* **Handle class imbalance** using appropriate techniques (e.g., SMOTE, class weighting, downsampling). 
* **Perform exploratory and financial analysis** to understand how key behavioral variables influence default risk.
* **Analyze behavioral trends** such as payment delays, repayment consistency, and utilization beyond basic EDA. 
* **Engineer financially meaningful and predictive features and transformations**, like credit utilization ratio and delinquency streaks.]
* **Test and compare multiple classification models**, including Logistic Regression, Decision Trees, and Ensemble Methods (e.g., XGBoost, LightGBM).
* **Choose and justify evaluation metrics** that reflect real-world credit risk trade-offs (e.g., Accuracy, Precision, F1-score, AUC-ROC). 
* **Set a classification threshold** aligned with the bank's risk appetite and discuss business implications of false positives and false negatives. 
* **Generate production-style predictions** on an unlabeled validation dataset, maximizing the chosen evaluation metric. 

## Deliverables
1.  **Prediction File (CSV)**: A CSV file with two columns: `Customer` and `next_month_default` (1 or 0). 
2.  **Code**: A clean, reproducible Jupyter notebook, Colab file, or Python script covering:
    * Data loading and preprocessing 
    * Exploratory Data Analysis (EDA) 
    * Financial insights from key variables 
    * Feature engineering and transformations 
    * Model training and validation 
    * Final predictions 
3.  **Report (in notebook or as separate PDF)**: A clear and structured summary of the process, including:
    * Overview of approach and modeling strategy 
    * EDA findings and visualizations 
    * Financial analysis of variables driving default 
    * Model comparison and justification for final selection 
    * Evaluation methodology and metric prioritization 
    * Discussion on classification cutoff selection 
    * Business implications
    * Summary of findings and key learnings 
    * Data Description 

## Tools and Libraries
* **Python packages**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `imbalanced-learn`, `xgboost`, `lightgbm`.
* **Optional**: `SHAP` or `LIME` for explainability of model predictions.


