    <img width="129" height="77" alt="image" src="https://github.com/user-attachments/assets/3ad9fe3d-006f-470d-bb12-7a64036ebdc0" />

DEBRE TABOR UNIVERSTY

GAFAT INSTITUTE OF TECHNOLOGY

DEPARTMENT OF COMPUTER SCIENCE

👩‍💻 Authors:

    NAME                     ID NO    
1. Abebe Tigabu .............. 0094
2. Tesfaye Mihret ............ 0222
3. Tomas  Bekele ............. 0318
4. Daniel Yirga .............. 0706
5. Hana Addis ................ 0768
6. Asmera Abiyu .............. 0610

🏠 House Price Prediction using Linear Regression
📘 Project Overview

This project aims to predict the median house value for neighborhoods in California using data from the California Housing Prices dataset.
Each record in the dataset represents a block group — a small area with 600–3,000 residents — rather than an individual house.
The model uses various demographic and housing-related features to estimate housing prices and uncover relationships between income, location, and home values.

🎯 Objective

To build a Linear Regression model that predicts median_house_value based on factors such as:

Median household income

Housing median age

Average number of rooms, bedrooms, and people per household

Geographical coordinates (latitude, longitude)

🗂️ Dataset Description

The dataset provides aggregated census data for California districts.
It does not represent individual houses, but rather average statistics for each neighborhood (block group).

Column	Description	Example	Notes
longitude	Longitude coordinate of the block group	-122.23	Western location
latitude	Latitude coordinate of the block group	37.88	Northern location
housing_median_age	Median age of houses in the area	41	Older = more established area
total_rooms	Total number of rooms within the block group	880	Used for density calculation
total_bedrooms	Total number of bedrooms in the block group	129	May contain missing values
population	Total number of people living in the block group	322	Used for population density
households	Total number of households (families) in the block group	126	Used for ratio features
median_income	Median household income (in tens of thousands of USD)	8.0	8.0 = $80,000/year
median_house_value	Median house value for the block group (USD)	452600	Target variable
ocean_proximity	Category describing distance to ocean	"NEAR BAY"	Categorical feature

💡 Note: median_income values are expressed in tens of thousands of dollars.
For example, 8.0 = $80,000 annual income.

🧹 Data Cleaning & Preprocessing

Checked dataset information and missing values

Filled missing total_bedrooms values with the median

Created new derived features:

rooms_per_household = total_rooms / households

bedrooms_per_room = total_bedrooms / total_rooms

population_per_household = population / households

Verified data types and summary statistics

These new features help the model better capture housing density and household structure, which strongly influence house values.

🔍 Exploratory Data Analysis (EDA)

Examined summary statistics using describe()

Visualized distributions and correlations using:

Histograms for numerical features

Heatmap for correlations

Scatter plots (e.g., income vs. house value)

Found strong positive correlation between median_income and median_house_value.

🧠 Model Building

Model Used: Linear Regression

Data Split: 80% training, 20% testing

Scaling: Numerical features normalized

Encoding: Categorical feature ocean_proximity encoded using One-Hot Encoding

📊 Model Evaluation

Performance metrics:

RMSE (Root Mean Squared Error): Measures how far predictions are from actual prices

R² Score: Measures how well the model explains variance in house prices

Example (typical results):

Metric	Value
RMSE	~68,000
R² Score	~0.75

This means the model explains roughly 75% of the variation in house prices.

💬 Conclusion & Discussion

Median Income is the most important predictor of housing prices.

Geographic location (latitude/longitude) also plays a major role.

🧩 Tools & Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Google Colab
