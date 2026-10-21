# Titanic Survival Prediction | EDA & Machine Learning

An end-to-end machine learning project exploring the factors associated with passenger survival aboard the Titanic and building classification models to predict survival outcomes.

## Project Overview

This project was developed as part of the [Kaggle Titanic — Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) competition.

The project focuses on exploratory data analysis, feature engineering, predictive modeling, and model evaluation using Python and Scikit-learn.

**Project Objectives:**
- Explore passenger demographics and survival patterns.
- Identify important features associated with survival.
- Build and compare classification models.
- Evaluate model performance using cross-validation and holdout validation.
- Generate predictions for Kaggle submission.

## Dataset

**Source:** [Kaggle Titanic Dataset](https://www.kaggle.com/competitions/titanic/data)

| Dataset | Records | Description |
|---|---:|---|
| Training Set | 891 | Passenger information with survival labels |
| Test Set | 418 | Passenger information without survival labels |

**Target Variable:** `Survived`

- `0`: Did not survive
- `1`: Survived

## Exploratory Data Analysis

The analysis investigates relationships between passenger survival and several features, including sex, passenger class, age, family size, and ticket fare.

### Key Findings

- Female passengers had a substantially higher survival rate (74.20%) than male passengers (18.89%).
- First-class passengers had the highest survival rate (62.96%), compared with 47.28% for second class and 24.24% for third class.
- Passengers traveling in small families demonstrated higher survival rates than those traveling alone or in larger families.
- Higher ticket-fare quartiles were associated with higher survival rates.

These findings describe associations in the observed data rather than causal relationships.

## Data Preprocessing & Feature Engineering

The preprocessing workflow includes:

- Missing-value imputation for numerical and categorical features.
- Numerical feature scaling using `StandardScaler`.
- Categorical feature encoding using `OneHotEncoder`.
- Reproducible preprocessing and modeling with Scikit-learn Pipelines.

Engineered features include:

- `FamilySize`: Number of family members traveling together, including the passenger.
- `FamilyGroup`: Family-size categories.
- `SexPclass`: Interaction between sex and passenger class.

## Machine Learning Models

Two classification algorithms were evaluated:

1. Logistic Regression
2. Random Forest Classifier

Model evaluation included stratified cross-validation, holdout validation, classification reports, and confusion matrices.

### Model Performance

| Model | Cross-Validation Accuracy | Holdout Accuracy |
|---|---:|---:|
| Logistic Regression | 81.32% | 81.01% |
| Random Forest | 81.74% | 80.45% |

Both models achieved comparable validation performance. Logistic Regression was selected for the final Kaggle submission.

## Kaggle Competition Result

**Public Leaderboard Score: 0.77511 (77.51%)**

The final submission was generated using Logistic Regression with engineered features.

The public score was evaluated on a hidden subset of the Kaggle test data and may differ from local validation results.

## Technologies Used

- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development Environment:** Kaggle Notebooks
- **Version Control:** GitHub

## Project Structure

```text
titanic-survival-prediction/
├── README.md
├── titanic-survival-prediction-eda-ml.ipynb
└── .gitignore
```

## How to Run

1. Open the Kaggle Notebook linked below.
2. Ensure the Titanic competition dataset is attached.
3. Run the notebook cells sequentially.
4. Review the exploratory analysis, model evaluation, and generated predictions.

The notebook uses Kaggle-specific dataset paths and is intended to run in the Kaggle environment.

## Project Links

- [Kaggle Notebook](https://www.kaggle.com/code/tan1906/titanic-survival-prediction-eda-ml)
- [Kaggle Competition](https://www.kaggle.com/competitions/titanic)

## Future Improvements

Potential improvements include extracting passenger titles, experimenting with alternative models, tuning hyperparameters, and evaluating model stability through repeated cross-validation.

---

*This project demonstrates an end-to-end machine learning workflow, from exploratory data analysis to Kaggle competition submission.*
