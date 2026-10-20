# Titanic Survival Prediction

Predicts whether a Titanic passenger survived, based on details such as ticket class, sex, age and fare.

**Notebook:** [titanic_survival_prediction.ipynb](titanic_survival_prediction.ipynb)

## Dataset

The Titanic dataset bundled with seaborn (`sns.load_dataset("titanic")`): 891 passengers and 15 columns. The target is `survived` (0 or 1).

## Approach

1. **Cleaning:** dropped columns that repeat other information (`deck`, `embark_town`, `alive`, `class`, `who`, `adult_male`), filled missing ages with the mean age and dropped the 2 rows with no port of embarkation.
2. **Encoding:** converted `sex` and `embarked` to numbers with `LabelEncoder`.
3. **Model:** trained a Logistic Regression classifier on a train/test split (75% / 25%).
4. **Evaluation:** confusion matrix, accuracy and a classification report.

## Results

| Metric | Value |
|---|---|
| Accuracy | **84.3%** |
| Precision (survived) | 0.76 |
| Recall (survived) | 0.84 |
| F1-score (weighted) | 0.84 |

Confusion matrix on 223 test passengers:

| | Predicted: died | Predicted: survived |
|---|---|---|
| **Actual: died** | 118 | 22 |
| **Actual: survived** | 13 | 70 |

## Tech stack

Python, pandas, NumPy, scikit-learn, Matplotlib, seaborn
