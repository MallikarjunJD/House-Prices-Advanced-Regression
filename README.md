# House Prices - Advanced Regression Techniques

An end-to-end Machine Learning project built for the Kaggle **House Prices - Advanced Regression Techniques** competition.

This project focuses on predicting residential house prices using advanced regression models, feature engineering, hyperparameter optimization, and ensemble learning.

---
## Key Highlights

- End-to-end Machine Learning pipeline
- Feature Engineering with domain-specific features
- Ordinal & One-Hot Encoding
- Skewness Reduction using Log Transformation
- Hyperparameter Optimization using Optuna
- CatBoost & XGBoost Regression Models
- 10-Fold Cross Validation
- Weighted Ensemble Learning
- Kaggle Public Leaderboard Score: **0.11799**


## Project Overview

The objective of this project is to accurately predict house sale prices using structured tabular data.

The workflow includes:

- Data preprocessing
- Missing value handling
- Feature engineering
- Categorical feature encoding
- Skewness reduction
- Hyperparameter optimization
- Model training
- Cross-validation
- Ensemble learning
- Kaggle submission
  

---

```text
                        HOUSE PRICES ML PIPELINE

                     Kaggle House Prices Dataset
                               │
                               ▼
                 Merge Train & Test Datasets
         (Consistent preprocessing for both datasets)
                               │
                               ▼
                  Missing Value Imputation (FillNA)
                               │
                               ▼
                     Feature Engineering
        ├─ House Age
        ├─ Garage Age
        ├─ Years Since Remodel
        ├─ Total Finished Basement Area
        ├─ Total Floor Area
        ├─ Total Bathrooms
        └─ Garage Area Per Car
                               │
                               ▼
                  Skewness Reduction (log1p)
                               │
                               ▼
                   Categorical Feature Encoding
                 ├─ Ordinal Encoding
                 └─ One-Hot Encoding
                               │
                               ▼
              Split Back into Train & Test Sets
                               │
                               ▼
            Log Transform Target (SalePrice → log)
                               │
                               ▼
             Hyperparameter Optimization (Optuna)
                 ├─ CatBoost Regressor
                 └─ XGBoost Regressor
                               │
                               ▼
          10-Fold Cross Validation (RMSE Evaluation)
                               │
                               ▼
          Weighted Ensemble (80% CatBoost + 20% XGBoost)
                               │
                               ▼
                 Generate Predictions on Test Set
                               │
                               ▼
                  Kaggle Submission (submission.csv)
                               │
                               ▼
              Public Leaderboard Score: 0.11799
```

## Dataset

Competition:

**House Prices - Advanced Regression Techniques**

The dataset contains 79 explanatory variables describing various aspects of residential homes.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- CatBoost
- XGBoost
- Optuna

---

## Feature Engineering

Several domain-based features were engineered to improve predictive performance.

Created features include:

- House Age
- Garage Age
- Years Since Remodel
- Total Finished Basement Area
- Total Floor Area
- Total Bathrooms
- Garage Area Per Car

Redundant features were removed after creating the new features.

---

## Data Preprocessing

- Missing values were imputed without dropping observations.
- Numerical features with high skewness were transformed using `log1p`.
- Ordinal categorical variables were encoded using ordinal mapping.
- Remaining categorical variables were encoded using One-Hot Encoding.

To ensure consistent preprocessing, the training and testing datasets were combined before feature engineering and encoding, then split back before model training.

---

## Model Training

Two gradient boosting models were trained:

- CatBoost Regressor
- XGBoost Regressor

Hyperparameters for both models were optimized using **Optuna**.

Model performance was evaluated using:

- 10-Fold Cross Validation
- Root Mean Squared Error (RMSE)

---

## Ensemble Strategy

Final predictions were generated using a weighted ensemble:

- 80% CatBoost
- 20% XGBoost

This improved prediction stability and overall leaderboard performance.

---

## Results

**Kaggle Public Leaderboard Score**

**0.11799**

---

## Repository Structure

```
House-Prices-Advanced-Regression/
│
├── README.md
├── House-Price-AdvanceRegression.ipynb
├── submission.csv
├── data_description.txt
├── train.csv
└── test.csv
```

---

## Challenges & Learnings

During this project I learned:

- Feature engineering for tabular datasets
- Designing preprocessing pipelines
- Hyperparameter optimization using Optuna
- Training CatBoost and XGBoost models
- Model evaluation using K-Fold Cross Validation
- Building weighted ensemble models for improved performance

This project significantly improved my understanding of end-to-end machine learning workflows and practical regression modeling.

---

## Future Improvements

Future work may include:

- Experimenting with LightGBM
- Exploring stacking and blending techniques
- Advanced feature selection
- More extensive hyperparameter optimization
- Building a reusable machine learning pipeline

---

## Author

**Mallikarjun Jadi**

Computer Science Engineering Student

Machine Learning Engineer | Full Stack Developer
