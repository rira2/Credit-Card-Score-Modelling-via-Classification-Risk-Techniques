# Credit Card Behaviour Score Prediction Using Classification and Risk-Based Techniques

## Overview
This project aims to enhance **Bank A's credit risk management framework** by developing a forward-looking **Behaviour Score** classification model. [cite_start]This model predicts whether a credit card customer will default on their payment in the following month[cite: 68]. [cite_start]Utilizing historical behavioral data from **over 30,000 anonymized credit card customers** [cite: 69][cite_start], the goal is to accurately flag potential defaulters in advance, enabling the bank to adjust credit exposure, trigger early warning systems, and prioritize risk-based actions[cite: 71]. [cite_start]Beyond mere prediction, the project focuses on creating a **financially interpretable model** that helps the bank understand default patterns and manage credit exposure effectively[cite: 72].

## Dataset
[cite_start]The project utilizes an anonymized dataset of historical credit card customer behavior[cite: 69]. Key variables include:
* [cite_start]`Customer Id`: Unique identifier for each customer[cite: 75].
* [cite_start]`marriage`: Marital status[cite: 75].
* [cite_start]`sex`: Gender[cite: 75].
* [cite_start]`education`: Education level[cite: 75].
* [cite_start]`LIMIT_BAL`: Credit limit assigned[cite: 75].
* [cite_start]`Age`: Age of the customer[cite: 75].
* [cite_start]`Pay_m (Pay_0 to 6)`: Payment status in various months[cite: 75].
* [cite_start]`Bill_amt_m (Bill_amt1 to 6)`: Total bill amount at the end of various months[cite: 76].
* [cite_start]`Pay_amt_m (Pay_amt1 to 6)`: Payment amount made in various months[cite: 76].
* [cite_start]`AVG_Bill_amt`: Average bill amount over 6 months[cite: 76].
* [cite_start]`PAY_TO_BILL_ratio`: Ratio of total payment to total bill amount over 6 months[cite: 76].
* [cite_start]`next_month_default`: Target variable (1 = default, 0 = no default)[cite: 76, 90].

The dataset is split into:
* [cite_start]**Train Dataset:** ~25,000 records, including features and the `next_month_default` target variable[cite: 125, 126, 128].
* [cite_start]**Validation Dataset:** ~5,000 records, containing the same features without the target variable, for which predictions must be generated[cite: 129, 130, 131].

## Objectives
[cite_start]The key objectives of this project are[cite: 88]:
* [cite_start]**Build a binary classification model** to predict customer default (`next_month_default`). [cite: 89, 90]
* [cite_start]**Handle class imbalance** using appropriate techniques (e.g., SMOTE, class weighting, downsampling). [cite: 91]
* [cite_start]**Perform exploratory and financial analysis** to understand how key behavioral variables influence default risk. [cite: 92]
* [cite_start]**Analyze behavioral trends** such as payment delays, repayment consistency, and utilization beyond basic EDA. [cite: 94, 95]
* [cite_start]**Engineer financially meaningful and predictive features and transformations**, like credit utilization ratio and delinquency streaks. [cite: 96]
* [cite_start]**Test and compare multiple classification models**, including Logistic Regression, Decision Trees, and Ensemble Methods (e.g., XGBoost, LightGBM). [cite: 97, 98, 99, 100]
* [cite_start]**Choose and justify evaluation metrics** that reflect real-world credit risk trade-offs (e.g., Accuracy, Precision, F1-score, AUC-ROC). [cite: 101, 103]
* [cite_start]**Set a classification threshold** aligned with the bank's risk appetite and discuss business implications of false positives and false negatives. [cite: 102]
* [cite_start]**Generate production-style predictions** on an unlabeled validation dataset, maximizing the chosen evaluation metric. [cite: 103]

## Deliverables
1.  [cite_start]**Prediction File (CSV)**: A CSV file with two columns: `Customer` and `next_month_default` (1 or 0). [cite: 105, 106]
2.  [cite_start]**Code**: A clean, reproducible Jupyter notebook, Colab file, or Python script covering[cite: 107, 108]:
    * [cite_start]Data loading and preprocessing [cite: 109]
    * [cite_start]Exploratory Data Analysis (EDA) [cite: 109]
    * [cite_start]Financial insights from key variables [cite: 110]
    * [cite_start]Feature engineering and transformations [cite: 110]
    * [cite_start]Model training and validation [cite: 111]
    * [cite_start]Final predictions [cite: 112]
3.  [cite_start]**Report (in notebook or as separate PDF)**: A clear and structured summary of the process, including[cite: 113, 114]:
    * [cite_start]Overview of approach and modeling strategy [cite: 115]
    * [cite_start]EDA findings and visualizations [cite: 116]
    * [cite_start]Financial analysis of variables driving default [cite: 117]
    * [cite_start]Model comparison and justification for final selection [cite: 118]
    * [cite_start]Evaluation methodology and metric prioritization [cite: 119]
    * [cite_start]Discussion on classification cutoff selection [cite: 120]
    * [cite_start]Business implications [cite: 121]
    * [cite_start]Summary of findings and key learnings [cite: 122]
    * [cite_start]Data Description [cite: 123]

## Tools and Libraries
* [cite_start]**Python packages**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `imbalanced-learn`, `xgboost`, `lightgbm`[cite: 133].
* [cite_start]**Optional**: `SHAP` or `LIME` for explainability of model predictions[cite: 134].

## Evaluation Criteria
[cite_start]The project will be evaluated based on the following[cite: 135]:
* [cite_start]**EDA & Financial Insight**: 30% (Visuals, trends, financial interpretation) [cite: 136, 137]
* [cite_start]**Class Imbalance & Model Performance**: 30% (Balancing, tuning, metric evaluation) [cite: 138, 139]
* [cite_start]**Feature Engineering & Metric Justification**: 20% (New features, threshold reasoning) [cite: 140, 141]
* [cite_start]**Code Quality & Report**: 20% (Clean code, clear summary) [cite: 142, 143]
