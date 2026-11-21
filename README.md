# Predicting Aircraft Damage from Wildlife Strikes

A machine learning project using the FAA Wildlife Strike Database to predict aircraft damage based on reported flight characteristics, wildlife attributes, and environmental conditions.

## Dataset

**FAA Wildlife Strike Database** (`data/Public.xlsx`)

Contains reported wildlife strike incidents, including aircraft characteristics, flight conditions, wildlife information, and damage outcomes.

## Objective

Predict whether a reported wildlife strike resulted in aircraft damage and identify factors associated with damage risk.

## Methods

- Exploratory data analysis and visualization
- Data cleaning, feature engineering, and preprocessing
- Logistic Regression, Decision Tree, and Random Forest
- Class imbalance analysis and hyperparameter tuning
- Model evaluation using classification metrics, confusion matrices, and ROC/precision-recall curves
- Feature importance and damage-risk analysis

## Results

Random Forest was selected as the final model.

| Metric | Test Performance |
|---|---:|
| Accuracy | 93.39% |
| Precision | 46.44% |
| Recall | 43.68% |
| F1-score | 0.4502 |
| ROC-AUC | 0.8849 |
| Average Precision | 0.4457 |

The model demonstrates the potential to prioritize reported wildlife-strike incidents for further safety analysis, although it is not intended to replace aircraft inspections or predict strikes before they occur.

## Run the Notebook

Open `Anna_TECH_68_Machine_learning_for_business_in_Python.ipynb` in Google Colab or Jupyter Notebook to explore the analysis and results.
