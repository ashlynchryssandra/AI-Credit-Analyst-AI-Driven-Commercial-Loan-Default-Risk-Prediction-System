# AI-Credit-Analyst-AI-Driven-Commercial-Loan-Default-Risk-Prediction-System
The AI Credit Analyst is an explainable ML system that modernizes lending by analyzing financial, operational, and behavioral data. It generates a Risk Probability Score, enabling banks to adopt risk-based pricing, cut loan losses, and improve profitability.

Project Prudence: AI-Driven Loan Default Risk Prediction

Overview
Project AI-Credit-Analyst is a comprehensive Machine Learning project developed for an academic assignment to address a critical challenge in modern finance: accurately predicting commercial loan default risk.
It moves beyond rudimentary credit scores to deploy an AI Credit Analyst that provides a precise, explainable, and multi-dimensional assessment of borrower risk. The final output is not just a decision, but a Risk Probability Score that enables financial institutions to implement Risk-Based Pricing strategies, dramatically reducing potential losses and optimizing their lending portfolio.

Business & Project Value

The core value of this system is its ability to transition lending from a subjective, rules-based process to a transparent, data-driven system.

The AI Advantage:

-> Holistic Risk Assessment: Traditional lending relies on a Static Credit Score. Our Prudence Engine uses a 360° view of the borrower, incorporating financial health, transactional history, and tax compliance data.

-> Precision Output: We replace the inflexible Hard 'Yes/No' Decision with a precise Risk Probability Score, giving the bank flexibility to manage marginal cases.

-> Optimized Strategy: The system enables Risk-Based Pricing, shifting from a one-size-fits-all interest rate to dynamic pricing that directly reflects the borrower's calculated risk.

-> Decision Explainability: While traditional methods offer no explanation, the AI provides the Top 3 Risk Drivers for every decision, transforming a 'black-box' rejection into a transparent and actionable conversation.

Top 3 Risk Drivers provided for every decision

Technical Implementation

1. Data Source
The system utilizes a synthetic dataset (combine the files and make it one excel sheet.xlsx - combine the files and make it o.csv) containing 25 features across financial, operational, and behavioral categories.

2. Technologies Used

Language: Python
-Platform: Google Colaboratory (Colab)
-Core Libraries: pandas, numpy, matplotlib, seaborn
-Machine Learning: scikit-learn (Pipeline, ColumnTransformer, RandomForestClassifier)

3. Feature Engineering Highlights: The predictive power of the model was significantly boosted by creating key financial ratios and indicators:
-current_ratio: Measuring a company's short-term liquidity.
-debt_to_ebitda: A core metric for assessing a company's ability to pay off its debt.
-company_age_years: Derived from incorporation and report dates, serving as a proxy for stability.
-days_since_last_payment: A measure of recent transactional behavior.

4. Modeling Pipeline

The entire workflow is encapsulated in a robust sklearn.Pipeline to ensure reproducibility and prevent data leakage:

Preprocessing:
-Numerical: Imputation (Median) followed by Standard Scaling.
-Categorical: Imputation ('missing' constant) followed by One-Hot Encoding.
-Model: RandomForestClassifier (selected for its high predictive accuracy and strong feature importance metrics).

Key Results and Explainability
The most crucial component of this project is proving why the AI's predictions are trustworthy.

A. Performance Metrics

The model achieved a strong performance in distinguishing between the two classes:
-AUC-ROC Score: 1.0000 (Indicates the probability the model ranks a randomly chosen positive case higher than a randomly chosen negativecase).
-Classification Report:  Showing high precision and recall, particularly for the Default class (Class 1), which is critical for loss prevention.

B. Feature Importance

The analysis confirmed that the AI looks past the surface, prioritizing transactional behavior over static scores. The top predictors included:
-GST/Tax Filing Delays (Past 12 Months)
-Debt-to-EBITDA Ratio
-Profit After Tax
-Interest Rate (As an indicator of initial risk pricing)

How to Run the Project
-Open Google Colab: Navigate to the Google Colab environment.
-Create New Notebook: Create a new Python 3 notebook.
-Paste Code: Copy the contents of the provided loan_risk_prediction.py file into a cell.
-Upload Data: Run the cell. When prompted, upload the CSV file (combine the files and make it one excel sheet.xlsx - combine the files and make it o.csv).
-Analyze Output: Review the printed metrics (Classification Report, AUC-ROC) and the generated plots (EDA, Confusion Matrix, ROC Curve, Feature Importance).

Conclusion

This project successfully demonstrates the application of Machine Learning in a high-stakes financial domain. By focusing on explainability and incorporating rich, diverse features, the Prudence Engine offers a tangible pathway for banks to make smarter, more profitable, and risk-aware decisions.
