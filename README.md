# Predicting Customer Churn in the Credit Card Industry

---

## Team Members
- James Garcia
- David Williams
- Svetlana Kachina
- Ilknur Toptas

---

## Project Overview
This project tackles a critical challenge in the financial industry: **predicting customer churn** for credit card holders. Using machine learning, we built a predictive model that identifies customers likely to close their accounts. Early intervention helps reduce attrition and support customer retention strategies.

---

## Stakeholders

This project is designed to support decision-makers across various departments within a financial institution:

| **Stakeholder**            | **Interest**                                                                 |
|----------------------------|------------------------------------------------------------------------------|
| Marketing Team             | Target churn-prone customers with personalized retention offers             |
| Customer Success Managers  | Engage proactively with high-risk customers before they leave               |
| Product Managers           | Identify product features or services that may be contributing to attrition |
| Data Analysts              | Use model insights to develop ongoing reporting and trend analysis           |
| Executive Leadership       | Monitor churn KPIs and allocate resources to improve customer lifetime value |

---

## Stakeholder Questions

This project answers key business questions that stakeholders care about:

- **Which customers are most likely to churn?**  
  → Helps prioritize customer retention efforts.

- **What factors contribute most to customer attrition?**  
  → Enables data-driven decisions about policy and marketing strategy.

- **How can we proactively identify high-risk customers before they leave?**  
  → Supports building preventative outreach programs.

- **Can we segment customers based on their behaviors and churn risk?**  
  → Aids in tailoring offers and services to different customer groups.

- **How accurate is our ability to predict future churn based on customer data?**  
  → Builds confidence in the predictive model’s value and informs strategic planning.

---

## Objectives

- Analyze customer credit card behavior to understand factors leading to churn
- Clean and preprocess raw data for machine learning
- Explore patterns and correlations through EDA and visualization
- Upload cleaned dataset to AWS RDS (PostgreSQL) for remote accessibility
- Build and compare multiple classification models (Logistic Regression, Decision Tree, Random Forest)
- Optimize the best-performing model using GridSearchCV
- Evaluate model performance using accuracy, recall, and F1-score metrics
- Provide actionable insights based on model outputs and important features

---

## Project Timeline

| **Date**       | **Milestone**                                      |
|----------------|-----------------------------------------------------|
| April 8–10     | Dataset exploration, cleaning, and EDA             |
| April 11–14    | Model training, testing, and optimization          |
| April 15–17    | Tableau dashboard creation + GitHub repo cleanup   |
| April 18–19    | Finalize README, visuals, and model results        |
| April 20       | Group presentation prep and review                 |
| **April 21**   |  **Project Due – Submit and Present**              |


---


![02885488-7135-46b2-9759-433d4f13700250](https://github.com/user-attachments/assets/6fe0eb84-3d4d-4249-beb1-08f3ee9ec5e7)


---

## Machine Learning Strategy
- **Binary classification** task
- Target variable: `Churn` (mapped from `Attrition_Flag`)
- Models tested:
  - Logistic Regression  
  - Decision Tree  
  - **Random Forest** (best performer)
- Hyperparameter tuning using **GridSearchCV**

---

## Dataset

- **Source**: [Gigasheet Credit Card Customers](https://www.gigasheet.com/sample-data/credit-card-customers)  
Records: ~10,000 customers

- **Features**:
  - Demographics (e.g., Gender, Income Category, Education Level)
  - Account Metrics (e.g., Credit Limit, Revolving Balance, Avg Open to Buy)
  - Transaction Behavior (e.g., Total Transaction Count, Total Transaction Amount)
  - `Attrition_Flag`: Indicates whether the customer churned
  - **License**: Publicly available sample data; free for educational use
 

---

## Technologies Used

- `Python` – Core development language
- `Pandas`, `NumPy` – Data wrangling
- `Seaborn`, `Matplotlib` – EDA & visualizations
- `Scikit-learn` – Modeling and evaluation
- `PostgreSQL (AWS RDS)` – Cloud database for cleaned data
- `GitHub` – Version control and collaboration


---

## Model Optimization & Evaluation
- **Random Forest** optimized using GridSearchCV:
  - Max Depth: 10–15  
  - Estimators: 50–150  
- Metrics evaluated:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-Score

---

## Results Summary

| Model               | Accuracy | Recall | F1 Score |
|--------------------|----------|--------|----------|
| **Random Forest**  | **96.10%** | **98.30%** | **97.69%** |
| Decision Tree      | 94.13%   | 96.06% | 96.49%   |
| Logistic Regression| 91.31%   | 96.94% | 94.93%   |
> **Top predictors**: `Total_Trans_Ct`, `Total_Trans_Amt` , `Total_Ct_Chng_Q4_Q1`


---

## AWS Integration

- Cleaned data was uploaded securely to an **AWS RDS PostgreSQL** instance
- Access was limited to personal IP via **inbound rules**
- Data connection used SQLAlchemy with SSL encryption
