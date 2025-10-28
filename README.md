# 💳 Customer Churn Prediction – Fintech Banking App

This project analyses and predicts **customer churn** for a digital banking app specialising in **credit card products**.

With **10,000 active users** and an **average Customer Lifetime Value (CLV) of $8,900**, the company experiences an **annual churn rate of 20%**, equating to roughly **$18M in lost lifetime value**.

---

## 🎯 Objectives

1. Quantify the financial impact of churn  
2. Identify key behavioural and demographic drivers  
3. Design data-backed retention strategies that reduce churn and improve profitability  

---

## 📈 Business Problem

Customer churn causes significant **revenue loss**.  
Even a small reduction in churn yields a large improvement in **lifetime revenue**, especially in fintech, where acquisition costs are high.

**Goal:** Predict at-risk customers and propose retention actions that could save **~$2.1M annually** through a **10% churn reduction**.

---

## ⚙️ Analytical Approach

### 1. Data Exploration (EDA)
**Tools:** Python (Pandas, NumPy, Matplotlib, Seaborn)

Key analyses:
- Cross-tabulations of churn by **demographics** (gender, geography, age)
- Correlation between **credit score, activity, and churn rate**
- **Tenure and product-based segmentation** to detect loyalty stagnation
- Visual summaries via **bar plots, heatmaps, and KDE distributions**

**Insights:**
- ~33% of churners had **moderate credit scores**
- **Female customers** showed slightly higher churn; cause likely multifactorial  
- 23% of churners were from **France**, 20% from **Germany** → possible localisation or trust gaps  
- **64% of churners** were inactive → engagement campaigns show strong ROI potential  
- **64% of churners** aged 37–54 → opportunity for midlife financial planning products  
- **31% of churners** had 3–5 years tenure → post-loyalty fatigue  

<img width="700" height="500" alt="python" src="https://github.com/user-attachments/assets/699c560b-6a1c-4932-a647-eade880c32ab" />


---

### 2. Predictive Modelling

| Model | Approach | Recall | Key Takeaway |
|--------|-----------|---------|--------------|
| Logistic Regression | Baseline | 0.19 | Poor churn detection due to class imbalance |
| **XGBoost (Weighted)** | Class weight = 3.7× | **0.81** | Captured 8/10 churners, strong recall |

- Addressed imbalance using **weighted loss**  
- Applied **SHAP (Shapley values)** for interpretability and fairness  

**Top Predictors (via SHAP):**
- ↑ **Age** → Higher churn probability  
- ↓ **Activity** → Higher churn  
- **Female gender** → Slightly higher churn  
- **Geography: Germany** → Higher churn risk  
- ↓ **Tenure** → Higher churn


<img width="800" height="600" alt="shap" src="https://github.com/user-attachments/assets/d2424540-ba7c-41f5-aaa4-f00c8a42befb" />

---

### 3. Business Impact & Retention Strategy

| Segment | Key Insight | Proposed Action | Est. Retention Lift |
|----------|--------------|------------------|----------------------|
| Low Credit Score | Financially vulnerable | Credit coaching & monitoring | +5% |
| Female Customers | Slightly higher churn | Personalised engagement, UX improvements | +4–6% |
| Inactive Members | Low engagement | Push notifications, gamified reactivation | +6–8% |
| Age 37–54 | Midlife financial needs | Retirement & family investment products | +3–5% |
| Tenure 3–5 Years | Loyalty fatigue | Rewards & milestone programs | +3–4% |

💰 **Estimated Outcome:**  
A **10% churn reduction** = **~$2.1M in retained lifetime value annually**.

---

### 4. Dashboard (Power BI)

Developed an **interactive retention dashboard** for real-time monitoring and ROI tracking.

**Features:**
- **KPIs:** CLV, ARPU, churn rate, retention rate, lost revenue  
- **Visuals:** CLV vs Tenure, churn by geography/gender, ARPU vs Balance  
- **Power Query:** Age, credit score, and engagement segmentation  
- **DAX Measures:** Financial KPI calculations  

🎯 Enables stakeholders to **track churn risk** and **measure retention ROI** dynamically.

<img width="1682" height="842" alt="dashboard" src="https://github.com/user-attachments/assets/22de7585-3d94-45d2-9236-69d3cc37dfaf" />


---

## 📊 Key Financial Formulas

1. Churn Impact = Churn Rate × Avg CLV × Total Customers
2. ARPU = (0.02 * Balance) + (NumOfProducts * 75) + (HasCrCard * 150) + (IsActiveMember * 100)
3. CLV = ARPU × Tenure
4. Savings = Current Churners × Churn Reduction × Avg CLV (Churners)

---

🧩 Tech Stack

1. Languages & Libraries: Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

2. Explainability: SHAP

3. Visualization: Power BI

4. Environment: Jupyter Notebook

---

🔮 Next Steps

1. Tune XGBoost hyperparameters for improved recall–precision balance

2. Engineer interaction features (e.g., gender × geography, activity × tenure)

---

💡 Key Takeaway

This project demonstrates how data analytics bridges customer behaviour and business impact.
By quantifying financial loss, predicting churn risk, and linking model outputs to actionable strategies, it proves that data analytics is a measurable profit lever in fintech.

---

👤 Author

Manisha Arugula
Data Analyst | Fintech Analytics | Business Intelligence
LinkedIn : www.linkedin.com/in/arugulamanisha
