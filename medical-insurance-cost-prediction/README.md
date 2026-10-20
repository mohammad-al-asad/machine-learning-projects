# Medical Insurance Cost Prediction

Predicts a person's yearly medical insurance charges from their age, sex, BMI, number of children, smoking status and region.

**Notebook:** [insurance_cost_prediction.ipynb](insurance_cost_prediction.ipynb)

## Dataset

[insurance.csv](insurance.csv): 1,338 people and 7 columns (`age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`), with no missing values. The target is `charges`. This is the [Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance) from Kaggle.

## Approach

1. **Exploratory analysis:** distributions, box plots and a correlation heatmap for the numeric columns.
2. **Feature engineering:**
   - encoded `sex` and `smoker` as binary columns
   - one-hot encoded `region`
   - grouped BMI into categories (Underweight, Normal, Overweight, Obese)
   - standardized `age`, `bmi` and `children`
3. **Feature selection:**
   - Pearson correlation of each feature with `charges`. Smoking status is by far the strongest predictor, at 0.79.
   - chi-square tests of the categorical features against binned charges.
   - final features: `age`, `isMale`, `bmi`, `children`, `isSmoker`, `region_southeast`, `bmi_category_Obese`
4. **Model:** Linear Regression on an 80% / 20% train/test split.

## Results

| Metric | Value |
|---|---|
| R² | **0.781** |
| Adjusted R² | 0.775 |

The model explains about 78% of the variation in insurance charges on unseen data.

## Tech stack

Python, pandas, NumPy, scikit-learn, SciPy, Matplotlib, seaborn
