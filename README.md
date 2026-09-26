# MAGIC Gamma Telescope Classification

A machine learning classification project using the MAGIC Gamma Telescope dataset.

The goal of this project is to classify observations as either **Gamma** or **Hadron** using multiple machine learning models and compare their performance.

## Project Workflow

The project includes:

- Data loading and inspection
- Exploratory Data Analysis (EDA)
- Data cleaning
- Handling missing and inconsistent values
- Feature engineering
- Train/test split
- Model training and comparison
- Hyperparameter tuning
- Model evaluation
- Feature importance analysis

## Dataset

The dataset contains observations collected from the MAGIC Gamma Telescope.

After loading, the dataset contains:

- 19,305 samples
- 10 input features
- 1 target class

The target contains two classes:

- `Gamma`
- `Hadron`

During preprocessing, duplicate rows, hidden missing values, and inconsistent class labels were handled.

Additional engineered features were created:

- `length_width_ratio`
- `area`
- `conc_ratio`
- `log_fSize`
- `log_fDist`

## Models

Three machine learning models were evaluated:

1. Logistic Regression
2. Random Forest
3. XGBoost

XGBoost was also optimized using `RandomizedSearchCV` with 5-fold cross-validation.

## Results

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | 0.8087 | 0.8654 |
| Random Forest | 0.8766 | 0.9340 |
| XGBoost (Baseline) | 0.8755 | 0.9342 |
| XGBoost (Optimized) | 0.8772 | 0.9350 |

The optimized XGBoost model achieved the highest overall performance.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC Curve

## Feature Importance

Feature importance was analyzed using the optimized XGBoost model.

Important features included:

- `fLength`
- `fWidth`
- `fAlpha`
- `length_width_ratio`

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost

## Files

```text
magic-gamma-classification/
├── magic_gamma_classification.ipynb
├── MAGIC_Gamma_Telescope.csv
└── README.md
