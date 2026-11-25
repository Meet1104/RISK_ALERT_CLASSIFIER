# Risk Alert Classifier

A supervised machine learning classification project that predicts whether a customer is **Low Risk (0)** or **High Risk (1)** based on demographic, financial, behavioral, and transaction-related features.

## Project Overview

The goal is to identify potentially high-risk customers while paying special attention to missed high-risk cases (False Negatives). The dataset is imbalanced, so several approaches to class imbalance and model evaluation are explored.

## Dataset

- **Records:** 4,600 customers
- **Low Risk (0):** 4,043 (87.89%)
- **High Risk (1):** 557 (12.11%)
- **Features:** Customer demographics, income, credit score, credit utilization, payment history, transaction behavior, complaints, login activity, tenure, and debt information.
- **Target:** `risk_status`
  - `0` — Low Risk
  - `1` — High Risk

> Dataset file: `Risk_Alert_Classifier_Dataset_4600.xlsx` (place the dataset in the project folder before running the notebook, if you have permission to share it).

## Project Workflow

1. **Conceptual Understanding** — Logistic Regression, classification metrics, Type-I/Type-II errors, Precision, Recall, F1, TPR, FPR, ROC-AUC, and class imbalance.
2. **Dataset Understanding & Exploration** — Inspect rows, shape, columns, data types, missing values, and duplicate rows.
3. **Preprocessing** — Separate features and target, perform stratified train/test splitting, impute missing numeric and categorical values, one-hot encode categorical features, and prepare final feature matrices.
4. **Baseline Model** — Train Logistic Regression and evaluate with a confusion matrix and classification metrics.
5. **Imbalanced Data Handling** — Explore Random Under-Sampling, Random Over-Sampling, SMOTE, and ADASYN.
6. **Tree-Based Models** — Train and compare Decision Tree and Random Forest classifiers.
7. **Hyperparameter Tuning** — Use RandomizedSearchCV and GridSearchCV with cross-validation and Recall scoring.
8. **Model Evaluation** — Compare model performance and review ROC curves and AUC-ROC scores.
9. **Final Analysis** — Focus on identifying High-Risk customers, reducing False Negatives, and balancing recall with other metrics.

## Models & Techniques

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Random Under-Sampling
- Random Over-Sampling
- SMOTE
- ADASYN
- Randomized Search CV
- Grid Search CV

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Type-I Error (False Positive)
- Type-II Error (False Negative)
- ROC Curve
- AUC-ROC

**Why Recall matters:** In this project, a False Negative means a truly High-Risk customer is predicted as Low-Risk. The project therefore emphasizes High-Risk Recall and reducing False Negatives, while also considering precision and false alerts.

## Tools & Libraries

- Python
- Jupyter Notebook
- Pandas
- Scikit-learn
- Imbalanced-learn
- Matplotlib

## Repository Structure

```text
Risk-Alert-Classifier/
├── RISK_ALERT_CLASSIFIER.ipynb
├── Risk_Alert_Classifier_Dataset_4600.xlsx  # add locally if permitted
├── README.md
└── images/
    ├── dataset-preview.png                  # optional screenshot
    ├── model-comparison.png                 # optional screenshot
    └── roc-curve.png                       # optional screenshot
```

## How to Run

1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install pandas scikit-learn imbalanced-learn matplotlib openpyxl jupyter
   ```
3. Place the Excel dataset in the same folder as the notebook (if it is not included in the repository).
4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
5. Open `RISK_ALERT_CLASSIFIER.ipynb` and run the cells in order.

## Results

The notebook explores multiple classification models and imbalance-handling techniques, with model selection and tuning guided by cross-validation Recall. Add your **actual notebook outputs** here after running the complete notebook:


- Best model: `<!-- Add selected model -->`
- Recall: `<!-- Add actual Recall -->`
- Precision: `<!-- Add actual Precision -->`
- F1-Score: `<!-- Add actual F1 -->`
- AUC-ROC: `<!-- Add actual AUC -->`

## Conclusion

This project demonstrates a complete supervised classification workflow—from data exploration and preprocessing to baseline modeling, imbalance handling, tree-based models, hyperparameter tuning, and evaluation. The practical objective is to build a model that helps flag potentially high-risk customers, prioritizing strong detection of the high-risk class and fewer False Negatives.

## Disclaimer

This is an educational machine learning project. Model predictions should not be used as the sole basis for real financial, credit, or customer decisions. Any real-world deployment would require further validation, monitoring, fairness checks, and domain review.

## Author

**Meet Golakiya**
