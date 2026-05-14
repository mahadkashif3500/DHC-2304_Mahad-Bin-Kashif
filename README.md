# DHC-2304 | Mahad Bin Kashif
## Data Science & Analytics Internship — DevelopersHub Corporation

This repository contains my completed internship tasks as part of the **Data Science & Analytics Internship** at DevelopersHub Corporation. I completed **3 out of 5 tasks**, covering data exploration, classification modeling, and churn prediction using Python.

---

## Repository Contents

| File | Description |
|------|-------------|
| `DHC-2304_Mahad Bin Kashif.ipynb` | Main Jupyter Notebook with all 3 completed tasks |
| `loan_prediction.csv` | Dataset used for Task 2 (Credit Risk Prediction) |
| `Churn_Modelling.csv` | Dataset used for Task 3 (Customer Churn Prediction) |

---

## Task 1: Exploring and Visualizing the Iris Dataset

### Objective
Understand how to load, summarize, and visualize a dataset using pandas, matplotlib, and seaborn.

### Dataset
Iris Dataset — loaded directly via `seaborn.load_dataset('iris')` (150 samples, 3 species, 4 features).

### Approach
- Loaded the dataset and inspected its structure using `.shape`, `.columns`, and `.head()`
- Generated a statistical summary with `.describe()`
- Created the following visualizations:
  - **Scatter plot**: Sepal Length vs Petal Length, colored by species
  - **Pair plot**: All feature combinations across species
  - **Histogram**: Distribution of all 4 features
  - **Box plots**: Spread and outliers for each feature by species

### Results & Insights
- The Iris dataset is clean with no missing values
- **Setosa** is clearly separable from the other two species
- **Versicolor** and **Virginica** show slight overlap
- **Petal length and width** are the most discriminative features for classification
- The pair plot confirms that petal dimensions provide the best 2D separation between species

---

## Task 2: Credit Risk Prediction

### Objective
Predict whether a loan applicant is likely to get their loan approved based on personal and financial data.

### Dataset
Loan Prediction Dataset — `loan_prediction.csv` (614 rows, 13 columns including applicant income, loan amount, credit history, and loan status).

### Approach
- **Data Cleaning**: Handled missing values — categorical columns filled with mode, `LoanAmount` filled with median
- **EDA**: Visualized property area distribution, income by education, loan amount by education, and credit history distribution
- **Encoding**: Applied Label Encoding to all categorical columns
- **Modeling**: Trained two classifiers:
  - Logistic Regression
  - Decision Tree (max_depth=5)
- **Evaluation**: Compared both models using accuracy scores and confusion matrices

### Results & Insights
- **Credit History** is the strongest predictor of loan approval
- Both models achieved reasonable accuracy on the test set
- Decision Tree is slightly more prone to overfitting without further pruning
- Missing data was minimal (~5–10%) and handled without dropping rows

---

## Task 3: Customer Churn Prediction (Bank Customers)

### Objective
Identify bank customers who are likely to leave (churn) based on demographic and account information.

### Dataset
Churn Modelling Dataset — `Churn_Modelling.csv` (10,000 rows, 14 columns including geography, age, balance, credit score, and exit status).

### Approach
- **Data Cleaning**: Dropped non-informative columns (`RowNumber`, `CustomerId`, `Surname`)
- **Encoding**:
  - Label Encoding for `Gender`
  - One-Hot Encoding for `Geography`
- **EDA**: Visualized churn distribution, age distribution by churn, account balance by churn, and a full feature correlation heatmap
- **Feature Scaling**: Applied `StandardScaler` before model training
- **Modeling**: Trained and compared three classifiers:
  - Logistic Regression
  - Random Forest (100 estimators)
  - Gradient Boosting (100 estimators)
- **Feature Importance**: Extracted and visualized top features from the Random Forest model

### Results & Insights
- Overall churn rate is approximately **20.4%**
- **Random Forest** and **Gradient Boosting** both outperformed Logistic Regression
- Top 5 features driving churn: **Age**, **Balance**, **NumOfProducts**, **IsActiveMember**, **EstimatedSalary**
- Customers aged **40–60 with high balances** are significantly more likely to churn
- **Inactive members** have a disproportionately higher churn rate — engagement is key to retention

---

## 🛠️ Libraries Used

- `pandas` — data loading and manipulation
- `numpy` — numerical operations
- `matplotlib` — base plotting
- `seaborn` — statistical visualizations
- `scikit-learn` — preprocessing, model training, and evaluation

---

## Author

**Mahad Bin Kashif**  
Data Science & Analytics Intern - DevelopersHub Corporation  
Intern ID: DHC-2304
