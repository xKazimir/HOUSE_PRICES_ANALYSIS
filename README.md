# House Prices Prediction

**Project Description**  
This repository contains an end-to-end machine learning project focused on predicting house prices.  
It covers the complete pipeline including data loading, exploratory data analysis (EDA), preprocessing, feature engineering, model training, evaluation, and prediction.  

This work is based on the YouTube tutorial  
**“House Prices Prediction in Python | Machine Learning Project”**  
(https://www.youtube.com/watch?v=UqmulHG4IvY&t=3545s)  
and implements the original Kaggle competition **“House Prices – Advanced Regression Techniques”**  
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview.

---

## Table of Contents
- [Dataset](#dataset)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Exploratory Analysis](#exploratory-analysis)  
- [Preprocessing & Feature Engineering](#preprocessing--feature-engineering)  
- [Modeling](#modeling)  
- [Results](#results)

---

## Dataset  
The dataset comes directly from the Kaggle competition and contains detailed information about residential homes in Ames, Iowa.  

- **train.csv** – 1460 samples with features and target (`SalePrice`)  
- **test.csv** – 1459 samples without target values (to generate submissions)  

You can download them here:  
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data  

---

## Installation  
1. **Clone the repository**  
   ```bash
   git clone https://github.com/xKazimir/HOUSE_PRICES_ANALYSIS.git
   cd HOUSE_PRICES_ANALYSIS

2. **Create & activate a virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

## Usage
Open Jupyter Notebook in terminal:
   ```bash
   jupyter notebook
   ```
Run all the cells in the notebook HousePricePrediction.ipynb.

## Exploratory Analysis
The notebook contains a thorough exploratory data analysis, including:
 - Distribution of target variable (SalePrice)
 - Correlation heatmaps and scatter plots with top predictive features (e.g., GrLivArea, OverallQual)
 - Handling of missing values in numerical and categorical columns
 - Visualizations of relationships between house characteristics and price 
## Preprocessing & Feature Engineering
Key preprocessing steps include:
 - Imputing missing values (mean/median for numerical, mode for categorical features)
 - Encoding categorical variables (One-Hot Encoding)
 - Feature scaling (StandardScaler)
 - Removing outliers (e.g., extreme values in GrLivArea)
 - Train/test split
## Modeling
We evaluated several regression models using cross-validation:
 - Linear Regression
 - Ridge Regression
 - Random Forest Regressor
 - CatBoost Regressor
 - XGBoost Regressor
 - LGBM Regressor 
Hyperparameters were tuned using GridSearchCV and model performance was compared using RMSE (Root Mean Squared Error).
## Results
 - he tree-based ensemble models (Gradient Boosting, Random Forest, XGBoost) outperformed simple linear models.
 - The best-performing model achieved a significantly lower RMSE compared to baseline predictions.
 - The trained model can be used to generate predictions on the Kaggle test dataset (test.csv) and submit them to the competition.