# Machine Learning Projects

Machine learning projects in Python, covering classification and regression on real-world datasets. Each project lives in its own folder with a notebook, its dataset and a README.

| Project | Task | Approach | Result |
|---|---|---|---|
| [Titanic Survival Prediction](titanic-survival-prediction/) | Binary classification | Logistic Regression | 84.3% accuracy |
| [Medical Insurance Cost Prediction](medical-insurance-cost-prediction/) | Regression | Linear Regression with statistical feature selection | R² = 0.78 |
| [Heart Disease Prediction](heart-disease-prediction/) | Binary classification | EDA, cleaning, encoding and scaling | Data prepared; modeling in progress |

## Tech stack

Python, pandas, NumPy, scikit-learn, SciPy, Matplotlib, seaborn, Google Colab

## Running the notebooks

The notebooks were written in Google Colab and load data from Google Drive. To run one:

1. Open the notebook in [Google Colab](https://colab.research.google.com/) (File → Upload notebook) or in Jupyter.
2. Upload the CSV file from the project's folder.
3. Change the file path in the data-loading cell to point to the uploaded file.

The Titanic notebook needs no upload because it loads the dataset from seaborn.
