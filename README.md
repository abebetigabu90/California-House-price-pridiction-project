<img width="129" height="77" alt="image" src="https://github.com/user-attachments/assets/3ad9fe3d-006f-470d-bb12-7a64036ebdc0" />



# DEBRE TABOR UNIVERSTY

# GAFAT INSTITUTE OF TECHNOLOGY

# DEPARTMENT OF COMPUTER SCIENCE

# Authors:

| Name        | ID_NO  |
|--------------|--------|
| Abebe Tigabu   | 0094  |
| Tesfaye Mihret | 0222  |
| Tomas  Bekele  | 0318  |
| Daniel Yirga   | 0706  |
| Hana Addis     | 0768  |
| Asmera Abiyu   | 0610  |

# California House Price Prediction using Random Forest

## Project Overview
This project uses the **California Housing Prices dataset** to predict the **median house value** for districts in California.  
The goal is to explore relationships between features like income, age of housing, location, and engineered metrics, and build a predictive model for house prices using **Random Forest Regression**.

---

## Features Used

- `median_income` — median income of households in the district  
- `housing_median_age` — median age of the houses  
- `longitude` & `latitude` — geographic location of the district  
- Engineered features:
  - `rooms_per_household`  
  - `bedrooms_per_room`  
  - `population_per_household`  

---

## Data Cleaning & Preprocessing

- Checked for **missing values** and filled `total_bedrooms` with median values  
- Removed **duplicate rows**  
- Applied **IQR winsorization** to reduce impact of outliers  
- Performed **train-test split** (80/20)  
- Filled missing values in test set using **training median**  
- Added **engineered features** for better model performance  

---

## Modeling

- Model used: **Random Forest Regressor**  
- Preprocessing pipeline:
  - Numeric features: median imputation + standard scaling  
  - Categorical features: most frequent imputation + one-hot encoding  
- Model trained on processed training data  

---

## Model Performance

- **R² Score:** ~0.82 (explains 82% of the variance in house prices)  
- **RMSE:** ~48,000 (predictions are reasonably close to actual values)  

**Most influential features:**

- Median income  
- Geographic location (`latitude` & `longitude`)  
- Engineered features (`rooms_per_household`, `bedrooms_per_room`, `population_per_household`)  

---

## Model Strengths

- Captures **nonlinear relationships** automatically  
- Handles **feature interactions** without manual engineering  
- More robust to **outliers**  
- Works well with both numeric and categorical features  

---

## Model Limitations

- Less interpretable than linear models  
- Computationally heavier  
- Can struggle with **extrapolation** (predicting outside the training range)  

---

## Possible Improvements

- Hyperparameter tuning with **GridSearchCV** or **RandomizedSearchCV**  
- Use gradient boosting models such as **XGBoost**, **LightGBM**, or **CatBoost**  
- Apply **cross-validation** to get more reliable performance estimates  
- Advanced feature engineering (e.g., spatial clustering, polynomial interactions)  
