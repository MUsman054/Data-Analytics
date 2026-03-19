# 📊 Data Analytics Internship

A collection of five end-to-end data science projects covering exploratory data analysis, classification, and regression — implemented in Python using real-world datasets.

---

## 📁 Projects Overview

| # | Project | Type | Dataset | Key Algorithm |
|---|---------|------|---------|---------------|
| 1 | [Iris Dataset Visualization](#1-iris-dataset-visualization) | EDA & Classification | Iris Dataset | K-Nearest Neighbors |
| 2 | [Credit Risk Prediction](#2-credit-risk-prediction) | Binary Classification | Loan Prediction Dataset | Logistic Regression & Decision Tree |
| 3 | [Customer Churn Prediction](#3-customer-churn-prediction) | Binary Classification | Churn Modelling Dataset | Random Forest |
| 4 | [Insurance Claim Amount Prediction](#4-insurance-claim-amount-prediction) | Regression | Medical Cost Personal Dataset | Linear Regression & Random Forest |
| 5 | [Personal Loan Acceptance Prediction](#5-personal-loan-acceptance-prediction) | Binary Classification | UCI Bank Marketing Dataset | Logistic Regression & Decision Tree |

---

## 🔧 Tech Stack

- **Language:** Python 3.10+
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
- **Environment:** Jupyter Notebook

---

## 📂 Repository Structure

```
📦 Data-Analytics-Internship/
├── 📓 task1_iris_visualization.ipynb
├── 📓 task2_credit_risk_prediction.ipynb
├── 📓 task3_customer_churn_prediction.ipynb
├── 📓 task4_insurance_claim_prediction.ipynb
├── 📓 task5_loan_acceptance_prediction.ipynb
├── 📄 task2_dataset.csv
├── 📄 task3_dataset.csv
├── 📄 task4_dataset.csv
├── 📄 task5_dataset.csv
└── 📄 README.md
```

---

## 🗂️ Project Details

### 1. Iris Dataset Visualization

**Notebook:** `task1_iris_visualization.ipynb`

**Objective:** Explore and visualize the classic Iris dataset to understand feature distributions and inter-species relationships.

**Highlights:**
- Loaded and inspected dataset using `.shape`, `.columns`, and `.head()`
- Built scatter plots, histograms, and box plots to analyze feature distributions
- Generated a full pair plot and correlation heatmap
- Trained a KNN classifier as a baseline — confirmed strong species separability

**Key Insight:** Petal length and petal width are far more discriminative than sepal features. *Setosa* is linearly separable from the other two species.

**Skills Demonstrated:** Data loading & inspection · Visualization with `matplotlib` & `seaborn` · Basic classification

---

### 2. Credit Risk Prediction

**Notebook:** `task2_credit_risk_prediction.ipynb`  
**Dataset:** `task2_dataset.csv` — 367 loan applicants (Kaggle Loan Prediction Dataset)

**Objective:** Predict whether a loan applicant has good or bad credit history as a proxy for default risk.

**Highlights:**
- Handled missing values in 6 columns using mode/median imputation
- Encoded categorical features (`Gender`, `Education`, `Property_Area`, etc.) with Label Encoding
- Visualized loan amount, income, and credit distributions with histograms and box plots
- Compared Logistic Regression and Decision Tree classifiers
- Evaluated using accuracy, confusion matrix, ROC-AUC, and classification report

**Key Insight:** `Credit_History`, `Property_Area`, and `LoanAmount` are the strongest predictors of credit risk. Semiurban applicants and graduates show higher good-credit rates.

**Skills Demonstrated:** Missing value imputation · Categorical encoding · Binary classification · Model evaluation

---

### 3. Customer Churn Prediction

**Notebook:** `task3_customer_churn_prediction.ipynb`  
**Dataset:** `task3_dataset.csv` — 10,000 bank customers (Churn Modelling Dataset)

**Objective:** Identify bank customers likely to leave (churn) based on their profile and account behaviour.

**Highlights:**
- Dropped non-predictive identifier columns (`RowNumber`, `CustomerId`, `Surname`)
- Applied Label Encoding for `Gender` and One-Hot Encoding for `Geography`
- Analyzed churn by age, balance, number of products, active membership, and geography
- Trained a Random Forest classifier with feature importance analysis
- Validated with 5-fold cross-validation and ROC curve

**Key Insight:** Age, balance, and number of products are top churn drivers. Customers with 3+ products and inactive members churn at significantly higher rates. German customers show the highest churn rate by geography.

**Skills Demonstrated:** Categorical encoding (Label + One-Hot) · Feature importance analysis · Random Forest · Cross-validation

---

### 4. Insurance Claim Amount Prediction

**Notebook:** `task4_insurance_claim_prediction.ipynb`  
**Dataset:** `task4_dataset.csv` — 1,338 policyholders (Medical Cost Personal Dataset)

**Objective:** Estimate individual medical insurance charges based on personal and lifestyle attributes.

**Highlights:**
- Explored charge distributions (raw and log-transformed)
- Visualized the impact of BMI, age, and smoking status on charges with scatter plots and box plots
- Trained and compared Linear Regression and Random Forest Regressor
- Evaluated models using **MAE**, **RMSE**, and **R²**
- Plotted residuals to assess model fit

**Key Insight:** Smoking is the single most powerful predictor — smokers are charged 3× more on average. BMI and smoking interact strongly: high-BMI smokers face the highest charges. Linear Regression shows clear heteroscedasticity, while Random Forest handles non-linearities better.

| Metric | Linear Regression | Random Forest |
|--------|------------------|---------------|
| MAE    | ~$4,200          | ~$2,600       |
| RMSE   | ~$6,000          | ~$4,500       |
| R²     | ~0.78            | ~0.87         |

**Skills Demonstrated:** Regression modeling · MAE & RMSE evaluation · Residual analysis · Feature importance

---

### 5. Personal Loan Acceptance Prediction

**Notebook:** `task5_loan_acceptance_prediction.ipynb`  
**Dataset:** `task5_dataset.csv` — 41,188 customers (UCI Bank Marketing Dataset)

**Objective:** Predict which bank customers are likely to accept a personal loan / term deposit offer from a marketing campaign.

**Highlights:**
- Loaded semicolon-delimited UCI dataset with 21 features including economic indicators
- Replaced `'unknown'` string values with NaN and imputed with mode
- Encoded all categorical variables with Label Encoding
- Performed EDA on age, call duration, job type, marital status, and campaign contacts
- Trained Logistic Regression and Decision Tree models
- Evaluated with accuracy, ROC-AUC, confusion matrix, and 5-fold cross-validation

**Key Insight:** Call `duration` and economic indicators (`euribor3m`, `nr.employed`) are the strongest predictors. Previous campaign successes are highly predictive of future acceptance. The dataset has an ~11.3% acceptance rate, making ROC-AUC the critical evaluation metric.

**Skills Demonstrated:** Large dataset handling · Feature encoding · Imbalanced classification · Cross-validation · ROC analysis

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Running the Notebooks

1. Clone this repository:
   ```bash
   git clone https://github.com/MUsman054/Data-Analytics-Internship.git
   cd Data-Analytics-Internship
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Open any `.ipynb` file and run all cells (`Cell → Run All`).

> **Note:** Each notebook loads its dataset from a CSV file in the same directory. Make sure the `.csv` files are present alongside the notebooks before running.

---

## 📈 Skills Demonstrated Across All Projects

| Skill | Projects |
|-------|---------|
| Data loading & inspection (`pandas`) | All |
| Handling missing values | 2, 3, 5 |
| Label Encoding & One-Hot Encoding | 2, 3, 4, 5 |
| Exploratory Data Analysis (EDA) | All |
| Data visualization (`matplotlib`, `seaborn`) | All |
| Binary classification | 2, 3, 5 |
| Regression modeling | 4 |
| Model evaluation (Accuracy, Confusion Matrix) | 2, 3, 5 |
| MAE & RMSE evaluation | 4 |
| ROC-AUC & ROC curves | 2, 3, 5 |
| Feature importance analysis | 2, 3, 4, 5 |
| Cross-validation | 3, 5 |

---





*This portfolio was built as part of a hands-on data science learning journey, demonstrating practical skills in EDA, machine learning, and model evaluation using real-world datasets.*
