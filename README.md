Fraud Detection Data Analysis
📘 Overview

This project explores financial transaction data to identify behavioral and transactional patterns associated with fraudulent activity. The workflow focuses on data cleansing, feature selection, normalization, and hypothesis validation to build a statistically sound foundation for predictive modeling.

🧩 Project Objectives

Analyze missing values and handle data imbalance.

Apply low-variance and high-correlation filters to retain informative features.

Normalize skewed variables using Box–Cox and Tukey’s Ladder transformations.

Evaluate latent structure using Principal Component Analysis (PCA).

Determine key predictors through Random Forest Feature Importance and Forward/Backward Selection.

Statistically validate the impact of transformations on model readiness.

⚙️ Data Description
Feature	Description
Transaction_ID	Unique transaction identifier
User_ID	Unique customer ID
Transaction_Amount	Value of transaction
Transaction_Type	Transaction category
Device_Used	Device type for transaction
Location	Transaction location
Payment_Method	Mode of payment
Previous_Fraudulent_Transactions	Count of prior frauds by same user
Account_Age	Age of account (in days)
Number_of_Transactions_Last_24H	Transaction frequency indicator
Fraudulent	Target label (1 = Fraud, 0 = Legitimate)

🧮 Methodology

Data Cleaning:

Calculated missing-value ratios and imputed numeric and categorical fields.

Dropped columns exceeding 30% missing data.

Feature Filtering:

Applied Low Variance Filter and High Correlation Filter to reduce redundancy.

Normalization & Transformation:

Used Box–Cox (for positive values) and Tukey’s Ladder (for zero/negative) transformations to stabilize variance and normalize skewness.

Dimensionality Reduction:

Conducted PCA to assess cumulative variance and confirm independence across features.

Model-Based Feature Evaluation:

Trained Random Forest Classifier to identify most influential predictors.

Performed Forward and Backward Feature Selection to optimize model performance.

Hypothesis Testing:

H₀: Transaction features have no significant relationship with fraud.

H₁: Transformed and filtered features significantly improve fraud prediction accuracy.

📈 Key Findings

Data normalization reduced skewness and improved model assumptions.

PCA confirmed balanced feature independence post-filtering.

Random Forest analysis identified Transaction_Amount, Account_Age, and Recent Activity as top predictors.

Feature selection confirmed improved F1-score using optimized subsets.

Statistical evidence supported rejection of H₀, confirming meaningful predictor relationships.