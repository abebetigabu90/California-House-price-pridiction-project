# 🏡 California Housing Price Prediction

## 📘 Project Overview
This project analyzes the **California Housing Prices** dataset and builds a **Linear Regression model** to predict median house values based on factors such as income, house age, and location characteristics.

## 🎯 Objectives
- Understand relationships between demographic and geographic variables.
- Explore correlations between income, house age, and median house value.
- Build a simple predictive model using Linear Regression.
- Visualize key findings for clear interpretation.

## 📂 Dataset
Dataset Source: [California Housing Prices - Kaggle](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

**Key Features:**
- `MedInc`: Median income in block group  
- `HouseAge`: Median house age in block group  
- `AveRooms`: Average number of rooms per household  
- `AveBedrms`: Average number of bedrooms per household  
- `Population`: Population of block group  
- `AveOccup`: Average household size  
- `Latitude` & `Longitude`: Coordinates  
- `MedHouseVal`: Median house value (Target variable)

## 🧹 Data Cleaning
- Handled missing values.
- Dropped non-numeric columns for correlation analysis.
- Converted `ocean_proximity` to categorical (encoded later if used in model).

## 📊 Exploratory Data Analysis (EDA)
- Visualized feature correlations.
- Found that `MedInc` (median income) has the **strongest positive correlation** with house prices.
- Mapped geographic distribution using scatter plots.

## 🤖 Model Building
Used **Linear Regression** from `sklearn`:
- Split data into training (80%) and test (20%).
- Evaluated using **Mean Squared Error (MSE)** and **R² score**.

**Example Result:**
| Metric | Value |
|--------|--------|
| R² Score | 0.64 |
| MSE | 0.45 |

## 📈 Key Visualizations
- Correlation Heatmap  
- Income vs. House Value Scatter Plot  
- Predicted vs. Actual Values Plot  

## 📁 Files in this Repository
- `california_housing_price_prediction.ipynb` — Colab notebook
- `README.md` — Project overview and results

## 🧠 Tools Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Google Colab
