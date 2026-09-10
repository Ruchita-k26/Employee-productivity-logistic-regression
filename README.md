# Employee Productivity Loss Prediction Using Logistic Regression

## Project Overview

Employee productivity can be influenced by several factors, including work environment, work hours, manager support, team collaboration, job satisfaction, stress level, and work-life balance.

This project uses **Logistic Regression** to predict whether an employee is likely to experience **productivity loss** based on employee and workplace-related characteristics.

The project covers data preprocessing, exploratory data analysis (EDA), feature preparation, model building, and model evaluation.

---

## Objective

The main objectives of this project are to:

* Analyze employee and workplace-related factors associated with productivity.
* Perform data cleaning and preprocessing.
* Create a binary target variable, `Productivity_Loss`.
* Build a Logistic Regression classification model.
* Evaluate the model using multiple classification metrics.
* Interpret the model results from a business perspective.

---

## Dataset

The dataset contains **1,500 employee records** and includes demographic, work-related, workplace, survey, and productivity information.

The dataset contains **30 original columns**, including:

* Employee demographics
* Work experience
* Work-from-home information
* Department and job level
* Company and industry information
* Home-office and internet conditions
* Work hours and meetings
* Manager support and team collaboration
* Job satisfaction and stress
* Work-life balance
* Productivity-related scores

The target variable `Productivity_Loss` is created during preprocessing from `Productivity_Score`.

---

## Target Variable

The original dataset contains a continuous variable called `Productivity_Score`.

For this classification problem, `Productivity_Loss` is created using the median of `Productivity_Score`.

| Value | Meaning              |
| ----- | -------------------- |
| `0`   | No Productivity Loss |
| `1`   | Productivity Loss    |

Employees with a productivity score below the median are assigned `1`, while employees with a score equal to or above the median are assigned `0`.

This converts the problem into a **binary classification problem**.

---

## Methodology

The project follows the following workflow:

```text
Dataset
   ↓
Data Understanding
   ↓
Data Cleaning & Preprocessing
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Encoding / Feature Preparation
   ↓
Train-Test Split
   ↓
Logistic Regression
   ↓
Model Evaluation
   ↓
Business Interpretation
```

---

## Model Used

### Logistic Regression

Logistic Regression was selected because the target variable has two possible outcomes:

* `0` → No Productivity Loss
* `1` → Productivity Loss

The model predicts the probability of an employee belonging to the productivity-loss category.

---

## Model Performance

The Logistic Regression model achieved the following results on the test dataset:

| Metric   |     Result |
| -------- | ---------: |
| Accuracy | **92.67%** |
| ROC-AUC  |  **0.976** |

### Classification Performance

| Class                | Precision | Recall | F1-Score |
| -------------------- | --------: | -----: | -------: |
| No Productivity Loss |      0.92 |   0.94 |     0.93 |
| Productivity Loss    |      0.94 |   0.91 |     0.93 |

The model correctly classified the majority of test observations and achieved a strong ROC-AUC score, indicating good ability to distinguish between employees with and without productivity loss.

---

## Key Evaluation Techniques

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* ROC-AUC
* ROC Curve

These metrics provide a broader view of model performance than accuracy alone.

---

## Business Interpretation

A model like this can help organizations identify employees who may be at higher risk of productivity loss.

Potential business applications include:

* Identifying productivity-related patterns.
* Understanding workplace factors associated with productivity.
* Supporting employee engagement initiatives.
* Helping managers identify areas where additional support may be required.
* Using data-driven insights to improve workplace productivity.

The model should be treated as a **decision-support tool**, rather than as the sole basis for decisions about individual employees.

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**

---

## Project Structure

```text
employee-productivity-logistic-regression/
│
├── README.md
├── Employee_Productivity_Logistic_Regression.ipynb
│
├── data/
│   └── remote_worker_productivity.csv
│
├── images/
│   ├── productivity_distribution.png
│   ├── confusion_matrix.png
│   └── roc_curve.png
│
├── requirements.txt

```

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the project folder

```bash
cd employee-productivity-logistic-regression
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
Employee_Productivity_Logistic_Regression.ipynb
```

---
# Business Insights

The Logistic Regression model achieved an accuracy of **92.67%** and a ROC-AUC of approximately **0.976**, indicating strong classification performance.

From a business perspective, the model can be used to identify patterns associated with potential productivity loss and support data-driven workplace improvement initiatives.

The predictions could help organizations:

* Identify employees or employee groups that may require additional workplace support.
* Investigate factors such as manager support, stress, work-life balance, work hours, and collaboration.
* Prioritize areas for employee engagement and productivity improvement.
* Support managers in making data-driven decisions.

However, model predictions should be used as an input for further investigation rather than as the sole basis for decisions affecting individual employees.

---
## Conclusion

This project demonstrates how Logistic Regression can be applied to an employee productivity dataset to classify potential productivity loss.

The model achieved **92.67% accuracy** and a **0.976 ROC-AUC**, demonstrating strong classification performance on the test dataset.

The project also demonstrates the complete machine learning workflow, from data preprocessing and exploratory analysis to model evaluation and business interpretation.


