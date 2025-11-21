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
This project predicts the **median house value** for districts in California using the **California Housing Prices dataset**.  
Each record represents a **block group** (600–3,000 residents) with aggregated demographic and housing features.  

The model leverages **Random Forest Regression** to capture complex, nonlinear relationships between housing values and predictors such as income, housing age, and geographic location.

---

## Objective
- Predict `median_house_value` based on features like:
  - Median household income (`median_income`)
  - Housing median age (`housing_median_age`)
  - Average rooms, bedrooms, and population per household
  - Geographic coordinates (`longitude`, `latitude`)
  - Engineered features:
    - `rooms_per_household`
    - `bedrooms_per_room`
    - `population_per_household`

---

## Dataset Description
| Feature | Description |
|---------|-------------|
| `longitude` | Geographic longitude of the area |
| `latitude` | Geographic latitude of the area |
| `housing_median_age` | Median age of houses in the block group |
| `total_rooms` | Total number of rooms in the block group |
| `total_bedrooms` | Total number of bedrooms (missing values handled) |
| `population` | Total population in the block group |
| `households` | Total households in the block group |
| `median_income` | Median household income (in tens of thousands of dollars) |
| `median_house_value` | Median house value in USD (target variable) |
| `ocean_proximity` | Categorical: proximity to the ocean (`<1H OCEAN`, `NEAR BAY`, etc.) |

---

## Data Cleaning & Preprocessing
- Checked for **missing values**; filled `total_bedrooms` with median  
- Removed **duplicate rows**  
- Applied **IQR winsorization** to reduce impact of outliers  
- Added **engineered features**:
  - `rooms_per_household`  
  - `bedrooms_per_room`  
  - `population_per_household`  
- Performed **train-test split** (80% training, 20% testing)  
- Scaled numeric features and **one-hot encoded** categorical features

---

## Exploratory Data Analysis (EDA)
- Summary statistics for numeric features using `describe()`  
- Visualizations:
  - Histograms for distributions  
  - Heatmap for correlations  
  - Scatter plots (e.g., median_income vs. median_house_value)  
- Observed strong correlation between **median_income** and **house prices**  

---

## Modeling
- **Algorithm:** Random Forest Regressor  
- **Pipeline:**
  - Numeric: median imputation + StandardScaler  
  - Categorical: most frequent imputation + OneHotEncoder  
- Model trained on **cleaned and preprocessed training data**

---

## Model Performance
| Metric | Value |
|--------|-------|
| RMSE | ~48,000 |
| R² Score | ~0.82 |

**Top Features (importance):**
- `median_income`  
- Geographic coordinates (`latitude`, `longitude`)  
- Engineered features (`rooms_per_household`, `bedrooms_per_room`, `population_per_household`)  

---

## Strengths
- Captures **nonlinear relationships** automatically  
- Handles **feature interactions** without manual engineering  
- Robust to **outliers**  
- Supports both **numeric and categorical features**  

---

## Limitations
- Less interpretable than linear models  
- Computationally heavier  
- Can struggle with **extrapolation** outside training data range  

---

## Possible Improvements
- **Hyperparameter tuning** using GridSearchCV or RandomizedSearchCV  
- Experiment with gradient boosting models: **XGBoost**, **LightGBM**, **CatBoost**  
- Use **cross-validation** for reliable performance estimates  
- Advanced feature engineering: spatial clusters, polynomial interactions  

---

## Tools & Libraries
- Python 3.x  
- Pandas  
- NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Google Colab
