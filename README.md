# Telecom Customer Churn Analysis & Prediction

An end-to-end customer churn analysis project using Python, statistical analysis, feature engineering, customer segmentation, and machine learning.

## 📌 Project Overview

Customer churn is an important business problem for telecommunications companies because retaining existing customers can be more valuable than continuously acquiring new customers.

In this project, I analyze customer-level telecom data to understand:

- Customer demographics and service characteristics
- Churn patterns across different customer groups
- Relationships between numerical variables
- Statistical associations between categorical variables and churn
- Differences in numerical distributions between churned and non-churned customers
- Customer value and churn segments
- Factors that can be used to predict customer churn

The project combines exploratory data analysis, statistical testing, business-oriented feature engineering, and predictive modeling.

---

## 🎯 Objectives

The main objectives of this project are to:

1. Assess and clean the dataset
2. Explore customer characteristics and churn patterns
3. Identify categorical variables associated with churn
4. Compare numerical features between churned and non-churned customers
5. Apply statistical significance tests
6. Measure the strength of categorical associations
7. Engineer business-oriented features
8. Segment customers based on value and churn status
9. Build a Logistic Regression model to predict churn
10. Evaluate classification performance using multiple metrics

---

## 🗂️ Dataset

The project uses the IBM Telco Customer Churn dataset.

The dataset contains customer-level information including:

- Demographics
- Account information
- Services subscribed
- Contract type
- Payment method
- Monthly charges
- Total charges
- Customer tenure
- Churn status

---

## 🧹 Data Cleaning

The following data-quality and cleaning steps were performed:

- Standardized column names
- Converted `TotalCharges` to a numeric data type
- Investigated missing `TotalCharges` values
- Checked for duplicate customer IDs
- Reviewed missing values
- Validated unique categorical values
- Checked numerical ranges and business rules

The cleaning process was designed to preserve meaningful customer information while improving consistency for analysis and modeling.

---

## 📊 Exploratory Data Analysis

The analysis examined churn across several customer characteristics.

### Categorical Analysis

Churn rates were compared across:

- Contract type
- Internet service
- Payment method
- Other customer service categories

### Numerical Analysis

Numerical variables examined included:

- Tenure
- Monthly charges
- Total charges

Mean, median, and standard deviation were used to summarize numerical differences between churned and non-churned customers.

Distribution plots were also used to examine differences in the shape and spread of these variables.

---

## 📈 Correlation Analysis

Correlation analysis was performed on numerical variables to identify relationships between features.

The analysis included:

- Senior citizen status
- Tenure
- Monthly charges
- Total charges
- Churn

Correlation was interpreted as an association rather than evidence of causation.

---

## 🧪 Statistical Analysis

Visual differences were followed by statistical testing to investigate whether observed patterns were statistically significant.

### Chi-Square Test of Independence

The Chi-Square test was used to examine whether categorical variables were statistically associated with churn.

### Cramér's V

Cramér's V was used alongside the Chi-Square test to measure the strength of association between categorical variables and churn.

This helped distinguish statistical significance from the practical strength of an association.

### Mann-Whitney U Test

The Mann-Whitney U test was used to compare numerical-variable distributions between churned and non-churned customers.

This provides a non-parametric alternative when the assumptions of a traditional t-test may not be appropriate.

---

## 🛠️ Business-Oriented Feature Engineering

Additional features were created to translate customer-level data into business-oriented metrics.

### Estimated Annual Revenue

Estimated annual revenue was calculated using:

`Monthly Charges × 12`

This provides an estimate of annual recurring revenue assuming the customer's current monthly charge remains constant.

### Estimated Total Charges

Estimated total charges were calculated using:

`Tenure × Monthly Charges`

This estimate was compared with recorded total charges to create a charge difference measure.

---

## 👥 Customer Segmentation

Customers were segmented using two dimensions.

### Value Segment

Customers were grouped into:

- Low-value
- Medium-value
- High-value

based on total charges.

### Risk Segment

Customers were grouped according to churn status:

- Active
- Churned

The two dimensions were cross-tabulated to examine the relationship between customer value and churn.

---

## 🤖 Predictive Modeling

A Logistic Regression classification model was developed to predict customer churn.

### Preprocessing

Numerical features were processed using:

- Median imputation
- Standardization

Categorical features were processed using:

- Most-frequent-value imputation
- One-hot encoding

A `ColumnTransformer` was used to apply the appropriate preprocessing to each feature type.

The preprocessing and Logistic Regression model were combined using a scikit-learn `Pipeline`.

This ensures that preprocessing is consistently applied during both training and prediction.

---

## 📏 Model Evaluation

The model was evaluated using several classification metrics.

### Classification Report

The classification report provides:

- Precision
- Recall
- F1-score
- Support

### ROC-AUC

ROC-AUC evaluates how well the model distinguishes between churned and non-churned customers across different classification thresholds.

### PR-AUC

Precision-Recall AUC evaluates the trade-off between precision and recall and is particularly useful when the positive class is less common.

---

## 🔍 Key Analytical Areas

The project investigates questions such as:

- Which customer groups have different churn rates?
- How are contract types associated with churn?
- How does tenure differ between churned and non-churned customers?
- Are monthly and total charges related to churn?
- Which categorical variables show statistically significant associations with churn?
- How strong are these associations?
- How do customer value and churn status intersect?
- Can customer characteristics be used to predict churn?

---

## 🧰 Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook / Google Colab
- GitHub

---

## 📁 Project Structure

```text
telecom-customer-churn-analysis/
│
├── README.md
├── notebook/
│   └── telecom_customer_churn_analysis.ipynb
├── data/
│   └── README.md
├── images/
└── requirements.txt
