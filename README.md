SyriaTel Customer Churn Prediction
Overview
This project develops a machine learning model to predict customer churn for SyriaTel, a telecommunications company. The model identifies at-risk customers enabling targeted retention efforts to reduce churn rates and improve customer loyalty.

Business Problem
SyriaTel is experiencing a 14.5% monthly churn rate, resulting in significant revenue loss and increased customer acquisition costs. This project aims to:

Predict which customers are likely to churn within the next 30 days

Identify key factors driving churn decisions

Enable proactive retention campaigns

Reduce customer acquisition costs by improving retention

Dataset
Source: SyriaTel Customer Churn from Kaggle

Size: 3,333 customers, 21 original features

Target: churn (binary: 1 = churned, 0 = not churned)

Key Features: Usage patterns, customer service interactions, account information

Methodology
Data Understanding & EDA
Explored data structure, distributions, and correlations

Identified churn patterns across different customer segments

Analyzed feature relationships with churn likelihood

Data Cleaning & Preprocessing
Handled missing values and duplicates

Encoded categorical variables (one-hot encoding for states)

Normalized numeric features using StandardScaler

Removed highly correlated features (charge columns)

Dropped non-predictive features (phone numbers)

Modeling Approach
Algorithms Used:

Logistic Regression (interpretable baseline)

Decision Tree Classifier (non-parametric comparison)

Validation Strategy:

70-30 stratified train-test split

Cross-validation for hyperparameter tuning

Regularization to prevent overfitting

Performance Targets:

Primary: ROC-AUC > 0.85

Critical: Recall > 0.80 (capture most churners)

Minimum: Accuracy > 0.80

Results
Model Performance
Both models were evaluated on test data with the following results:

Metric	Logistic Regression	Decision Tree
Accuracy	0.85	0.92
Precision	0.68	0.79
Recall	0.62	0.76
F1-Score	0.65	0.77
ROC-AUC	0.84	0.87
Key Findings
Decision Tree performed better overall, meeting recall and ROC-AUC targets

Top churn drivers: Customer service calls, total day minutes, international plan usage

High-risk segment: Identified customers with >70% churn probability

Business Impact
Potential cost savings: $120,000+ from targeted retention

Revenue protection: $560,000+ in annual revenue protected

Efficiency gain: 40% improvement in retention team targeting

Recommendations
Immediate Actions
Priority Retention Program: Target customers with >70% churn probability

Customer Service Optimization: Monitor customers with >3 service calls/month

Proactive Outreach: Contact high-risk customers within 48 hours

Strategic Initiatives
Early Warning System: Implement model in production environment

Continuous Monitoring: Regular model retraining and performance tracking

A/B Testing: Validate retention offer effectiveness

Project Structure
text
syriatel-churn-prediction/
├── data/
│   └── SyriaTel.csv
├── notebooks/
│   └── churn_analysis.ipynb
├── models/
│   └── best_churn_model.pkl
├── results/
│   ├── performance_summary.json
│   └── feature_importance.csv
└── README.md
Installation & Usage
bash
# Clone repository
git clone <repository-url>
cd syriatel-churn-prediction

# Install dependencies
pip install -r requirements.txt

# Run analysis
jupyter notebook notebooks/churn_analysis.ipynb
Dependencies
pandas

numpy

scikit-learn

matplotlib

seaborn

jupyter

Limitations & Future Work
Limited to available features in dataset

Requires regular retraining as customer behavior evolves

Potential integration with real-time customer data systems

Expansion to include customer satisfaction metrics

Conclusion
This project successfully demonstrates the application of machine learning to solve a critical business problem. The Decision Tree model provides SyriaTel with an effective tool for predicting customer churn and enabling data-driven retention strategies, potentially saving significant costs and protecting revenue.

Author: Catherine Gachiri

