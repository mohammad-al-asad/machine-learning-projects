# Heart Disease Prediction

Prepares clinical patient data for predicting whether a patient has heart disease.

**Status:** exploratory analysis and preprocessing are done. Model training and evaluation are next.

**Notebook:** [heart_disease_prediction.ipynb](heart_disease_prediction.ipynb)

## Dataset

[heart.csv](heart.csv): 918 patients and 12 columns, including age, sex, chest pain type, resting blood pressure, cholesterol, maximum heart rate and ST slope. The target is `HeartDisease` (0 or 1); 508 patients (55%) have heart disease. This is the [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) from Kaggle.

## Approach so far

1. **Exploratory analysis:**
   - histograms of every feature
   - heart disease counts by sex and chest pain type
   - age distribution by outcome (violin plot)
   - a correlation heatmap
2. **Cleaning:** some patients have impossible values of 0 for `Cholesterol` and `RestingBP`. These were replaced with the mean of the valid (non-zero) values.
3. **Encoding:** one-hot encoded the categorical columns.
4. **Scaling:** standardized `Age`, `RestingBP`, `Cholesterol`, `MaxHR` and `Oldpeak`.

## Next steps

- Split the data into train and test sets.
- Train and compare classifiers such as Logistic Regression, KNN, Random Forest and a simple neural network.
- Evaluate with accuracy, precision, recall and a confusion matrix.

## Tech stack

Python, pandas, scikit-learn, Matplotlib, seaborn
