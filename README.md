<img width="129" height="77" alt="image" src="https://github.com/user-attachments/assets/3ad9fe3d-006f-470d-bb12-7a64036ebdc0" />
DEBRE TABOR UNIVERSTY
GAFAT INSTITUTE OF TECHNOLOGY
DEPARTMENT OF COMPUTER SCIENCE
Authors:
    NAME                       ID NO
1. Abebe Tigabu .............. 0094
2. Tesfaye Mihret ............ 0222
3. Tomas  Bekele ............. 0318
4. Daniel Yirga .............. 0706
5. Hana Addis ................ 0768
6. Asmera Abiyu .............. 0610
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

🏘️ Dataset Description

This dataset does not represent individual houses.
Each row corresponds to a block group — a small neighborhood area defined by the U.S. Census Bureau, typically containing 600–3,000 people.

All values are aggregated statistics for that area.
For example:

median_income = median household income within the block group

median_house_value = median value of houses in that block group

total_rooms, total_bedrooms, households, and population = totals for all homes and residents in the area

Each block group may include a mix of housing types such as single-family homes, apartments, and condominiums.
The goal is to predict the median house value of each neighborhood, not the price of an individual property.
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
