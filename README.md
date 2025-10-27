# Customer-Churn-Prediction - Fintech-Banking-App
This project analyses and predicts customer churn for a digital banking app specializing in credit card products.
With 10,000 active users and an average Customer Lifetime Value (CLV) of $8,900, the company experiences an annual churn rate of 20%, equating to roughly $18M in lost lifetime value.

The objective is to:

1. Quantify the financial impact of churn,

2. Identify key behavioral and demographic drivers

3. Design data-backed retention strategies that reduce churn and improve profitability.

📈 Business Problem

Revenue loss from customer churn.
Even a small reduction in churn significantly improves lifetime revenue in fintech, where acquisition costs are high and margins depend on customer longevity.

Goal: Predict at-risk customers and propose retention actions that could save ~$2.1M annually through a 10% churn reduction.

⚙️ Analytical Approach
1. Data Exploration (EDA)

Performed in Python (Pandas, NumPy, Matplotlib, Seaborn).
Key analyses:

i. Cross-tabulations of churn by demographics (gender, geography, age).

ii. Correlation between credit score, activity, and churn rate.

iii. Tenure and product-based segmentation to spot loyalty stagnation.

iv. Visual summaries via bar plots, heatmaps, and KDE distributions.

Insights:

i. ~33% of churners had moderate credit scores.

ii. Female customers showed slightly higher churn rates; no single cause identified.

iii. 23% of churners were from France, 20% from Germany — possible localization or trust factors.

iv. 64% of churners were inactive; engagement campaigns present strong ROI potential.

v. 64% of churners aged 37–54, indicating an opportunity for midlife-focused products.

vi. 31% of churners had 3–5 years tenure, suggesting post-loyalty fatigue.

2. Predictive Modelling
i. Logistic Regression:	Baseline model with recall	0.19, generated	Poor detection of churners due to imbalance
ii. XGBoost (Weighted): Implemented	Class weight = 3.7×	and produced	strong recall of 0.81, generating business-relevant predictions. Addressed class imbalance using weighted loss.

Implemented SHAP (Shapley values) for feature explainability.Interpretable outputs directly informed business strategy.

Top Predictors (via SHAP):

↑ Age → Higher churn probability

↓ Activity → Higher churn

Female gender → Slightly higher churn

Geography: Germany → Higher churn risk

↓ Tenure → Higher churn

3. Business Impact and Retention Strategy
a. Segment	Key Insight	Proposed Action	Est. Retention Lift
b. Low Credit Score	Financially vulnerable	Credit coaching, monitoring	+5%
c. Female Customers	Slightly higher churn	Personalized engagement, UX improvements	+4–6%
d. Inactive Members	Low engagement	Push notifications, gamified reactivation	+6–8%
e. Age 37–54	Midlife segment	Retirement & family products	+3–5%
f. Tenure 3–5 Years	Loyalty fatigue	Rewards & milestone programs	+3–4%

Estimated Financial Outcome:

A 10% churn reduction equates to $2.1M in retained lifetime value annually.

4. Dashboard (Power BI)

Developed an interactive dashboard to track churn metrics and engagement indicators:

i. KPIs: CLV, ARPU, churn rate, retention rate, lost revenue.

ii. Visuals: CLV vs. Tenure, churn by geography/gender, ARPU by balance.

iii. Power Query transformations for segmentation (age, credit score, engagement).

iv. DAX measures for financial KPI calculations.

🎯 Enables stakeholders to monitor churn risk in real time and measure retention ROI.

📊 Key Formulas
i. Churn Impact = Churn Rate × Avg CLV × Total Customers
ii. ARPU = (0.02 * Balance) + (NumOfProducts * 75) + (HasCrCard * 150) + (IsActiveMember * 100)
iii. CLV = ARPU × Tenure
iv. Savings = Current Churners × Churn Reduction × Avg CLV (Churners)

🧩 Tech Stack

1. Languages & Libraries: Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
2. Explainability: SHAP
3. Visualization: Power BI
4. Environment: Jupyter Notebook

🔮 Next Steps

1. Tune XGBoost hyperparameters for improved recall–precision balance.

2. Engineer interaction features (e.g., gender × geography, activity × tenure).


💡 Key Takeaway

This project demonstrates how data analytics bridges customer behavior and business impact.
By quantifying financial loss, predicting risk, and linking model outputs to strategy, it turns analytics into a measurable profit lever for fintech companies.

👤 Author

Manisha Arugula
Data Analyst | Fintech Analytics | Business Intelligence
https://www.linkedin.com/in/arugulamanisha/
