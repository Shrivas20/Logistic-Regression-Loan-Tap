# LoanTap Loan Default Prediction

This repository contains a detailed business case study for **LoanTap**, a leading Indian fintech company. The project focuses on building a machine learning model to predict the likelihood of a customer defaulting on a loan (i.e., being "Charged Off").

The analysis moves from in-depth data exploration and feature engineering to building and evaluating a robust classification model, all while keeping key business objectives in focus.

---

## 🎯 Project Goal

The primary objective is to develop a predictive model that can accurately identify high-risk applicants. This helps LoanTap make informed lending decisions, minimize financial losses, and optimize its loan portfolio.

## 🛠️ Tech Stack

This project leverages the core Python data science and machine learning stack:

* **Data Analysis:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy`, `statsmodels`
* **Machine Learning:** `scikit-learn`

---

## 🚀 Project Workflow

This analysis follows a structured machine learning workflow:

### 1. Data Cleaning & Exploration (EDA)
* Loaded the `LoanData.csv` dataset.
* Conducted initial data checks (missing values, duplicates, data types).
* Performed deep **Univariate and Bivariate Analysis** to understand the data's characteristics.
* Key visualizations included:
    * Histograms and box plots for numerical features (e.g., `loan_amnt`, `int_rate`, `annual_inc`).
    * Count plots for categorical features (e.g., `home_ownership`, `grade`, `loan_status`).
    * A correlation heatmap to identify relationships between variables.

### 2. Feature Engineering & Preprocessing
* This was a critical phase to prepare the data for modeling:
* **Handled outliers** using statistical methods.
* **Encoded categorical features:**
    * Mapped binary and ordinal features (like `loan_status` and `emp_length`).
    * Extracted new features from existing ones (e.g., `zip_code` and `state` from `address`, `issue_year` from `issue_d`).
* **Performed Feature Selection:**
    * Checked for multicollinearity using **VIF** (Variance Inflation Factor) and dropped highly correlated features (like `installment`).
    * Used the **Chi-Square test** to select the most significant categorical features for the model.
* **One-Hot Encoded** the final set of categorical variables.

### 3. Model Building
* The problem was framed as a binary classification task (1 = Fully Paid, 0 = Charged Off).
* Split the cleaned data into training and testing sets.
* Scaled numerical features using `MinMaxScaler`.
* Built and trained a **Logistic Regression** model, chosen for its effectiveness and high interpretability in the financial sector.

### 4. Model Evaluation
* The model's performance was evaluated using a suite of metrics critical for a banking context:
    * **Accuracy Score**
    * **Confusion Matrix** (to analyze False Positives vs. False Negatives)
    * **Classification Report** (Precision, Recall, F1-Score)
    * **ROC AUC Score** and **ROC Curve**
* A **Precision-Recall Curve** was also plotted and analyzed to understand the trade-offs, which is essential for a business where the cost of a False Negative (approving a bad loan) is high.

### 5. Business Insights
* The project concludes by answering several key business questions, using insights from the EDA and the model. This includes:
    * The percentage of customers who have fully paid.
    * Identifying the top afforded job titles.
    * Determining which metric (e.g., Recall, Precision) is most important for a bank.
    * Identifying the features that most heavily influence the loan outcome.

---

## 📂 How to Use

To run this analysis yourself:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
    cd YOUR_REPO_NAME
    ```

2.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn statsmodels scikit-learn jupyter
    ```

3.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook "LoanTap Business Case Study.ipynb"
    ```
