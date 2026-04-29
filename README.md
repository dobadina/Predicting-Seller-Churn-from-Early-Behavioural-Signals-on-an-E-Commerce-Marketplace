📊 Seller Churn Prediction (E-Commerce Marketplace)

Machine learning project focused on predicting seller churn early and turning predictions into clear business actions.

🚀 What this project does
- Predicts which sellers will churn within 12 months
- Uses only the first 60 days of behaviour
- Flags risk early enough for intervention
🎯 Business problem

Marketplace teams typically act too late.

Support is triggered by revenue decline, but by then the seller has already disengaged.

This project shifts the approach:

- From reactive → proactive
- From revenue signals → behavioural signals
- From analysis → daily operational decisions
  
🧠 Key results
- AUC-ROC: 0.7643
- Behavioural signals alone matched full model performance
- Revenue features added no meaningful lift
- Early engagement is the strongest predictor of retention
  
📊 Data
- 3,806 sellers
- 3 years of marketplace activity
- 11 source tables
- Binary target: active at 12 months
  
⚙️ Approach
Framework: CRISP-DM

Feature engineering
- 121 features
- Engagement, activity, logistics, operational signals
- Missing data treated as signal (MNAR)

Models tested
- Logistic Regression
- Random Forest
- XGBoost

Best model
- Logistic Regression (L2)
- Behavioural features only
- Strong calibration and interpretability
  
📈 Evaluation
- AUC-ROC
- Brier Score
- Calibration Error
- F2 Score (recall prioritised due to cost of missed churn)
  
🔍 Key insights
- Sellers disengage before revenue drops
- Login frequency and session time are leading indicators
- Second-month activity is critical
- Logistics issues influence churn independently of seller behaviour
  
🧩 Outputs
This project is built for real use, not just modelling.

1. Churn prediction model
Probability score for each seller
Based on first 60 days

2. Intervention playbook
Clear rules for action:
- Who to target
- When to act
- What to do

Includes:
- Segmentation matrix
- Behavioural triggers
- Action guidelines
  
3. Power BI dashboard
Daily decision tool:

- Risk scoring
- Priority seller list
- Trigger alerts
- Seller-level drill-down
  
🎯 Segmentation logic
Sellers are grouped using:

- Risk score
- Engagement level

Focus is on:
Persuadables:
  - High risk
  - Still active
  - Most responsive to intervention

Avoids wasting time on sellers unlikely to respond.

🧪 Validation
- Temporal split
- Train: 2022–2023
- Test: 2024

Reflects real deployment conditions and avoids leakage.

🛠️ Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Power BI
  
📌 Why this matters
- Moves churn prediction earlier in the lifecycle
- Removes reliance on lagging revenue signals
- Connects model output to daily operations
- Designed for non-technical teams to use
