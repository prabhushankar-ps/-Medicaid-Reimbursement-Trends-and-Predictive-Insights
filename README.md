# Dosage Disparities: Medicaid Reimbursement Trends and Predictive Insights

## 📊 Overview

This project investigates Medicaid drug reimbursement trends across U.S. states from 2019 to 2024, focusing on dosage disparities and the influence of socioeconomic conditions. The goal is to identify drivers of reimbursement differences and build predictive models that enhance cost transparency and resource planning within Medicaid.

## 👨‍💻 Team

- **Prabhu Shankar**
- **Raheela Charania**
- **Rajivini Tiruveedhula**

Faculty Advisor: **Dr. Myriam Quispe Agnoli**

Capstone Project | Master of Science in Business Analytics  
Stetson-Hatcher School of Business, Mercer University

---

## 🧠 Objectives

- Analyze Medicaid drug utilization and reimbursement patterns
- Explore socioeconomic and environmental factors affecting reimbursements
- Predict reimbursed drug dosage volume using machine learning models
- Quantify potential cost savings through improved predictive accuracy

---

## 📂 Dataset

- **Primary Source:** [Medicaid Drug Utilization Database](https://data.medicaid.gov)
- **Time Frame:** 2019–2024
- **Supplemental Sources:** U.S. Census, BEA, NOAA
- **Features Include:**
  - Drug name, NDC, prescriptions, units reimbursed, reimbursement amount
  - State-level socioeconomic indicators (GDP, poverty index, income, temperature, etc.)

---

## 🧹 Data Preprocessing

- Filtered for Managed Care Organization (MCO) claims (75%+ Medicaid coverage)
- Removed redundant columns like `package_size`, `labeler_code`
- Applied Min-Max scaling
- Handled categorical variables using **target mean encoding** with 5-fold cross-validation to avoid data leakage

---

## 📈 Exploratory Data Analysis

- Correlation heatmaps for socioeconomic & reimbursement relationships
- U.S. choropleth maps:
  - Top reimbursed drugs by state
  - Total Medicaid reimbursement per capita
  - Regional and climate-based dosage trends
- Time-series plots showing units reimbursed vs population growth

---

## 🤖 Modeling

### Models Used:
1. **Multiple Linear Regression (MLR)**
2. **LightGBM**
3. **XGBoost**

### Key Features:
- Number of prescriptions
- Medicaid/Non-Medicaid reimbursements
- GDP, poverty index, temperature index, personal income

### Model Performance:

| Model     | R²   | RMSE        |
|-----------|------|-------------|
| Linear    | 0.67 | $74,401.75  |
| LGBM      | 0.89 | $61,231.16  |
| XGBoost   | 0.93 | $41,991.16  |

XGBoost showed the highest accuracy with the lowest error.

---

## 💰 Cost-Benefit Insights

- Baseline misallocation cost (8% RMSE): **$274.4M**
- Optimized model (1% RMSE): **$34.3M**
- Potential savings with just 10% implementation efficiency: **$24M**

---

## ✅ Conclusions

- **Prescription volume** is the most significant predictor of drug units reimbursed
- **Socioeconomic factors** added marginal improvement, but their standalone predictive power was limited
- **Advanced modeling** (e.g., XGBoost) significantly reduces forecasting errors and supports better Medicaid budgeting

---

## 🛠 Tech Stack

- **Python** (pandas, scikit-learn, xgboost, lightgbm)
- **Tableau / matplotlib / seaborn** (for visualizations)
- **Jupyter Notebooks**
- **Data sources:** Medicaid.gov, BEA.gov, NOAA, U.S. Census

---

## 📌 Future Work

- Expand analysis to include more granular demographic breakdowns (race, gender, age)
- Incorporate drug type classification (generic vs. brand vs. specialty)
- Evaluate policy-level impacts (e.g., Medicaid expansion timelines)

---

## 📎 References

Citations include CMS, Kaiser Family Foundation, peer-reviewed journals, and Medicaid open data portals. See full bibliography in the [report](./Project_report.pdf).

---

## 📬 Contact

For questions or collaboration inquiries:
**Prabhu Shankar**  
prabhushankargv@gmail.com

