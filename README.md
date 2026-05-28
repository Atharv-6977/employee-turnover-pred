# Employee Turnover Prediction

A Machine Learning project to predict employee attrition using HR analytics data.

## Project Overview

The goal of this project is to identify employees who are likely to leave the organization and support HR teams in taking timely retention actions.

The project includes data analysis, clustering, class imbalance handling, model training, evaluation, and employee risk categorization.

## Dataset

The dataset contains employee-related features such as:

- Satisfaction level
- Last evaluation score
- Number of projects
- Average monthly hours
- Time spent in company
- Work accident
- Promotion in last 5 years
- Department
- Salary
- Left status

## Work Done

- Data quality check
- Exploratory Data Analysis
- Correlation heatmap
- Distribution plots
- Project count analysis
- KMeans clustering of employees who left
- Categorical encoding using one-hot encoding
- Train-test split with stratification
- SMOTE for class imbalance handling
- 5-Fold Cross Validation
- Model training and comparison:
  - Logistic Regression
  - Random Forest Classifier
  - Gradient Boosting Classifier
- Evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
  - ROC-AUC
- Employee turnover probability prediction
- Risk zone classification for retention strategy

## Key Learnings

One of the biggest learnings from this project was understanding data leakage. During experimentation, an EDA-derived clustering feature was accidentally included in the model training data, which produced unrealistically perfect results. Removing it helped reinforce the importance of keeping analysis features separate from the actual prediction pipeline.

Another important learning was model selection. Instead of choosing the model only based on accuracy, I focused on recall, ROC-AUC, and the business objective. In employee attrition prediction, recall is especially important because missing an employee who is actually likely to leave can be costly for the organization.

## Best Model

Random Forest Classifier performed best among the models tested.

It achieved strong recall and accuracy because it was able to capture non-linear patterns and feature interactions better than Logistic Regression.

## Risk Zones

Employees were categorized into four risk zones based on predicted turnover probability:

- Safe Zone: Probability < 20%
- Low Risk Zone: 20% to 60%
- Medium Risk Zone: 60% to 90%
- High Risk Zone: > 90%

## Retention Strategy

- Safe Zone: Maintain engagement and monitor periodically
- Low Risk Zone: Provide feedback, recognition, and career discussions
- Medium Risk Zone: Review workload, compensation, and growth opportunities
- High Risk Zone: Immediate HR intervention and personalized retention plan

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- OpenPyXL

## Repository Structure

```text
employee-turnover-pred/
│
├── data/
│   └── hr_comma_sep.xlsx
│
├── notebooks/
│   └── employee_turnover_analysis.ipynb
│
├── visuals/
│   └── project visualizations
│
├── README.md
├── requirements.txt
└── .gitignore
