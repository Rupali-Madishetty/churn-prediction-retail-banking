
# Customer Churn Prediction in Retail Banking

## Overview  
This project presents a machine learning-powered solution to predict customer churn in a retail banking environment. It integrates CRM behavior, sentiment analysis, and customer value metrics to support strategic retention efforts. The final insights are visualized in a Tableau dashboard designed for business stakeholders and decision-makers.

---

## Business Context

**Problem:**  
Retail banks face revenue loss due to high customer churn and lack visibility into early churn indicators through traditional reporting systems.

**Objective:**  
Develop a predictive analytics pipeline that identifies customers at high risk of churn, explains the drivers behind their churn behavior, and empowers the business with actionable segmentation and insights.

---

## Features and Insights

### Data Analysis:
- **Churn Distribution:** Overall churn rate visualized for high-level monitoring.
- **Customer Segmentation:** Churn trends by geography, age, and lifecycle stage.
- **Risk Profiling:** Visual identification of high-value, low-engagement customers.
- **Sentiment Insights:** Impact of customer feedback sentiment on churn likelihood.

### Key Metrics:
- **Churn Rate**
- **Predicted Churn Probability**
- **Customer Lifetime Value (CLV)**
- **Engagement Score**
- **Top Churn Drivers (via SHAP)**

---

## Technical Implementation

### Data Enrichment:
- Simulated CRM fields: customer interaction counts, resolution time, lifecycle stages
- Text sentiment scoring using VADER (via NLTK)
- Engineered features: CLV, Engagement Score, Sentiment Score

### Machine Learning Models:
- Logistic Regression
- Random Forest Classifier
- XGBoost (best performer with 85% accuracy, 0.85 AUC)

### Explainability:
- SHAP used to interpret model predictions and identify key churn factors

### Visualization:
- Tableau dashboard includes:
  - Churn Overview
  - Churn by Geography, Age, and Lifecycle Stage
  - Customer Risk Profile (CLV vs. Engagement)


---

## Business Impact

- **Early Risk Identification:** Enables targeted retention campaigns.
- **Strategic Segmentation:** Prioritizes customers by churn risk and value.
- **Actionable Insights:** Lifecycle and engagement insights drive tailored outreach.
- **Improved Forecasting:** Informs budgeting and customer acquisition planning.

---

## Data

The dataset is based on a public churn dataset and enhanced with simulated CRM features:

- **Customer Profile:** Age, geography, account balance, tenure
- **CRM Features:** Support interaction frequency, resolution metrics, lifecycle stage
- **Sentiment Data:** Simulated feedback text used to compute sentiment scores
- **Churn Label:** Binary churn status for supervised learning

---

## How to Use

1. **Load Dataset:**
   - Use the enriched churn dataset (`Final_Churn_Data.csv`) for model training and dashboarding.

2. **Run Churn Model:**
   - Train and evaluate models using Python (Colab or Jupyter)

3. **View Dashboard:**
   - Open Tableau dashboard file 

---

## Results

- **85% Model Accuracy using XGBoost**
- **SHAP-based Feature Attribution**
- **Interactive Tableau Dashboard**
- **Churn Segments Identified by Geography, Age, and Lifecycle**

---

## Files

- `Churn_Modeling.csv`: Raw Dataset
- `churn_modeling_pipeline.ipynb`: Model training and analysis
- `Final_Churn_Data.csv`: Enriched dataset for dashboard
- `Tableau_Dashboard.twbx`: Interactive churn dashboard
- `README.md`: Project documentation

---

## Business Recommendations

- Focus retention efforts on customers with high CLV and low engagement scores
- Prioritize outreach to Dormant and At Risk lifecycle segments
- Use sentiment monitoring to flag early churn signals
- Implement churn probability scoring into CRM systems for ongoing targeting

---

## Dependencies

- Python (Pandas, Scikit-learn, XGBoost, SHAP, NLTK)
- Tableau Desktop / Tableau Public
- Jupyter Notebook / Google Colab

---

## Acknowledgments

Inspired by real-world CRM churn modeling techniques. Dataset structure adapted from Kaggle’s Bank Customer Churn Modeling dataset.
