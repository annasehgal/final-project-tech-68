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

## Limitations and Future Improvements

While the Random Forest model demonstrated strong discrimination (ROC-AUC of 0.8849), its ability to identify damaging wildlife strikes was less satisfactory than I had hoped. With a recall of 43.68%, the model failed to identify more than half of the incidents that actually resulted in aircraft damage. For a problem involving aviation safety, this is a significant limitation.

The dataset's class imbalance presented an additional challenge, with only approximately 6.2% of reported incidents involving damage. Although class weighting improved recall, it came at the cost of lower precision and more false positives. Hyperparameter tuning and additional feature engineering were also explored, but neither produced a substantial enough improvement to resolve the underlying problem.

Another concern is the quality and completeness of the available data. Several features contained substantial missing information, and reporting practices may have influenced the patterns learned by the model. The model also relies on characteristics documented during or after a strike, limiting its usefulness for predicting incidents in advance.

**While I am satisfied with what the project revealed, I am not entirely satisfied with the model's final performance.** Its ability to rank incidents by damage probability is encouraging, but identifying fewer than half of the damaging incidents leaves considerable room for improvement.

Future work could investigate alternative classification algorithms, more informative features, improved handling of missing data, and additional threshold optimization. Incident-level data splitting and validation across different time periods would also help establish whether the results generalize beyond the current dataset.

Ultimately, this project was a useful exploration of how machine learning can support aviation safety analysis, but it also demonstrated that strong overall metrics do not necessarily translate into reliable predictions for the cases that matter most. The model remains an exploratory tool rather than a system suitable for operational safety decisions.

## Why Wildlife Strikes?

My interest in aviation accident investigations and understanding the factors behind aircraft incidents led me to explore the FAA Wildlife Strike Database.

While an unconventional choice for a machine learning project, the dataset offered an opportunity to investigate how wildlife, environmental conditions, and flight characteristics relate to aircraft damage.

Some findings were intuitive, such as larger wildlife being associated with higher damage rates. However, the more interesting challenge was determining whether machine learning could reliably identify damaging incidents from a highly imbalanced dataset.

Ultimately, this project became an exploration of both aviation safety and the limitations of predictive modeling, demonstrating that identifying meaningful patterns does not necessarily translate into reliable classification.

## Run the Notebook

Open `Anna_TECH_68_Machine_learning_for_business_in_Python.ipynb` in Google Colab or Jupyter Notebook to explore the analysis and results.
