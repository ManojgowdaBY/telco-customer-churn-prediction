# telco-customer-churn-prediction
End-to-end churn prediction pipeline on the IBM Telco Customer Churn dataset (7,043 records). Covers data cleaning, EDA, feature engineering, and three ML models (Logistic Regression, Decision Tree, Random Forest — best ROC-AUC 0.852). Includes segment-level churn insights and business retention recommendations.
# Customer Behavior Analysis & Churn Prediction

A data analytics and machine learning workflow utilizing the **IBM Telco Customer Churn dataset** ($7,043$ customer records) to identify high-risk customer segments and predict churn probability using classification algorithms.

---

## 📌 Project Overview
This project is broken down into two core phases:
*   **Phase 1: Exploratory Data Analysis (EDA) & Preprocessing:** Focused on data engineering, handling missing values, identifying churn correlations, and visualizing customer characteristics.
*   **Phase 2: Predictive Modeling & Machine Learning:** Focused on building early-warning classification models to predict customer departures and establishing a data-driven retention roadmap.

---

## ⚙️ Tools & Technologies
*   **Languages:** Python
*   **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
*   **Environment:** Jupyter Notebook / GitHub / Excel

---
## Dataset
[Telco Customer Churn – Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
7,043 customers | 21 features | Binary churn classification

---

## 📊 Pipeline Workflow
1. **Data Collection:** Load and inspect the Telco dataset structure.
2. **Data Preprocessing:** Handle missing whitespace values in `Total Charges` and map nulls in `Churn Reason` to "Not Applicable". 
3. **Feature Engineering:** Derive behavioral indicators such as `Tenure Group`, `Average Monthly Spend`, and `Service Count`.
4. **Encoding & Scaling:** One-hot encode multi-categorical fields and standardize numeric features with `StandardScaler`.
5. **Model Training:** Fit and evaluate performance using class-weighted classification algorithms.
6. **Insight Extraction:** Formulate targeted business strategies based on feature impact.

---

## 📈 Model Performance Matrix

Class weights were implemented to balance the ~3:1 ratio of retained to churned customers.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Random Forest (Best)** | **0.773** | **0.555** | **0.727** | **0.630** | **0.852** |
| Logistic Regression | 0.750 | 0.519 | 0.791 | 0.627 | 0.850 |
| Decision Tree | 0.740 | 0.507 | 0.821 | 0.627 | 0.837 |

> 💡 **Key Takeaway:** The **Random Forest** ensemble model achieved the highest overall capability ($AUC = 0.852$) while yielding an optimized recall ($72.7\%$), vital for catching at-risk revenue early.

---

## 🔍 Key Risk Segments Identified

*   **Contract Risk:** Month-to-month subscribers exhibit a **42.7%** churn rate, whereas 2-year contract users sit below **3%**.
*   **Tenure Risk:** New customers ($0-1$ year) show an alarming **47.4%** churn rate.
*   **Service & Billing Friction:** Fiber optic internet subscribers (**41.9%**) and Electronic Check payment users (**45.3%**) represent the highest-risk clusters.

---

## 🚀 Actionable Business Recommendations
*   **Targeted Outreach:** Proactively engage new fiber-optic customers during their first year.
*   **Contract Incentives:** Deploy upgrade campaigns pushing month-to-month clients toward stable long-term contracts.
*   **Autopay Migration:** Nudge Electronic Check users toward automatic payment methods to remove recurring renewal friction.
*   **Model Deployment:** Set up the Random Forest pipeline quarterly as an automated early-warning system to score active users.
*   ## Requirements

Before running this project, ensure you have the following installed:

* Python 3.10 or later
* pip (Python package manager)
* Jupyter Notebook or JupyterLab (for running the notebook)

### Python Dependencies

Install all required packages with:

```bash
pip install -r requirements.txt
```

The project uses the following Python libraries:

* pandas – Data manipulation and analysis
* numpy – Numerical computations
* matplotlib – Data visualization
* seaborn – Statistical visualizations
* scikit-learn – Machine learning algorithms and model evaluation
* scipy – Scientific computing
* joblib – Model serialization
* jupyter – Interactive notebook environment
* notebook – Jupyter Notebook interface
* ipykernel – Python kernel for Jupyter
* openpyxl – Reading and writing Excel files
* plotly – Interactive visualizations (optional)
* xgboost – Gradient boosting model (optional)
* lightgbm – Light Gradient Boosting Machine (optional)
* catboost – Gradient boosting for categorical features (optional)

### Recommended Environment

It is recommended to use a virtual environment before installing the dependencies:

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

**Linux/macOS**

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
License

This internship project was developed for educational, learning, and research purposes.

Author

ManojGowda B Y 

If you find this project helpful, consider giving the repository a ⭐ on GitHub.
