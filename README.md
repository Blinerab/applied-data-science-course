# Applied Data Science Course

Teaching materials from two hands-on courses I designed and taught for working professionals in Prishtina, Kosovo: **Python for Data Science** and **Machine Learning**.

Every session is a Jupyter notebook built around a realistic business question: HR salary analysis, employee churn, local venue analysis, hotel booking cancellations. Each one ends with practice exercises. The notebooks are in **Albanian**, the language the courses were taught in. Code, function names and outputs are standard Python.

## What's inside

### Python for Data Science
| # | Notebook | Topics |
|---|----------|--------|
| 1 | [Python basics](python-for-data-science/01_python_basics.ipynb) | Variables, data types, lists, string formatting |
| 2 | [NumPy & Pandas](python-for-data-science/02_numpy_and_pandas.ipynb) | Arrays, DataFrames, exploring, filtering, sorting, `groupby` |
| 3 | [Data cleaning with Pandas](python-for-data-science/03_pandas_data_cleaning.ipynb) | Missing values, duplicates, type conversion, `apply`, `merge`, `concat`, pivot tables |
| 5 | [Data visualization](python-for-data-science/05_data_visualization.ipynb) | Matplotlib & Seaborn: choosing the right chart for the question |
| 6 | [Mini project: Prishtina venues](python-for-data-science/06_mini_project_prishtina_venues.ipynb) | End-to-end analysis: cleaning → feature engineering → answering business questions |

### Machine Learning
| # | Notebook | Topics |
|---|----------|--------|
| 1 | [Intro & linear regression](machine-learning/01_intro_linear_regression.ipynb) | Train/test split, MSE, RMSE, R² |
| 2 | [Multiple features](machine-learning/02_multiple_features.ipynb) | One-hot encoding, feature engineering, coefficient interpretation, residuals |
| 3 | [Logistic regression](machine-learning/03_logistic_regression.ipynb) | Classification, probabilities, confusion matrix, decision thresholds |
| 4 | [Metrics & overfitting](machine-learning/04_metrics_overfitting.ipynb) | Precision, recall, F1, class imbalance, learning curves |
| 5 | [Decision trees & random forest](slides/ml_05.pptx) *(slides)* | Gini & entropy, tree parameters, ensembles, bootstrap |
| 6 | [Cross-validation & bootstrapping](slides/ml_06.pptx) *(slides)* | K-fold, stratified, time-series & group CV, confidence intervals |
| 7 | [K-Nearest Neighbors](machine-learning/07_knn.ipynb) | Distance-based models, choosing *k*, why scaling matters |
| 8 | [Final project: hotel cancellations](machine-learning/08_final_project_hotel_cancellations.ipynb) | Full ML workflow, model comparison, **turning model errors into business cost (€)** |

## Teaching approach
- **Business question first.** Every dataset comes with a scenario and a stakeholder, for example a revenue manager asking "can we predict cancellations before they happen?"
- **Metrics in business terms.** Students learn to say "the model catches 6 in 10 cancellations and saves ~€45k", not just "75% accuracy".
- **Honest evaluation.** Stratified splits, cross-validation and pipelines are used to avoid lucky results and data leakage.
- **Practice after every concept**, with exercises that build towards a final project.

## Datasets
All datasets in [`data/`](data/) are **synthetic**, created for teaching. Names of people and venues are fictional, and any resemblance to real people or businesses is coincidental.

| File | Used in | Description |
|------|---------|-------------|
| `employees.csv` | Python 3, 5 | Small HR dataset with deliberate quality issues (mixed types, missing values, duplicates) |
| `products.csv` | Python 2 | Products with categories and prices |
| `lokalet_prishtine.csv` | Python 6 | 45 cafés, bars, pizzerias and restaurants across Prishtina neighbourhoods |
| `employees_enhanced.csv` | ML 1–2 | 100 employees with salary, bonus, tenure |
| `employees_churn.csv` | ML 3, 4, 7 | 350 employees with a churn label |
| `hotel_booking_cancellations.csv` | ML 8 | 5,000 hotel bookings with a cancellation label |

## Running the notebooks
```bash
git clone https://github.com/Blinerab/applied-data-science-course.git
cd applied-data-science-course
pip install -r requirements.txt
jupyter lab
```
The notebooks read data from `../data/`, so open them from inside their folders.

## About me
I'm **Blinera Berisha**, a data scientist with 8 years in banking and enterprise software. I currently build production forecasting and anomaly-detection models for a smart-building platform and teach applied data science at Data EDU.
[LinkedIn](https://linkedin.com/in/blineraberisha)
