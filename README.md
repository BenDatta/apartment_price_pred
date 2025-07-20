🏡 Cluj Housing Price Prediction with Random Forest
Welcome to my machine learning project where I built a predictive model to estimate house prices in Cluj, Romania 🇷🇴 using real-world property data and Random Forest Regression 🌲.
----------------------------------------------------
📌 Project Overview
This project demonstrates my data science workflow, from data wrangling to model deployment. It highlights my ability to:

Clean and transform raw datasets 🧹

Visualize patterns 📊

Engineer meaningful features 🛠️

Build and evaluate regression models 📈

Package the model for reuse with pickle 📦
----------------------------------------------------
🧠 Objective
The goal was to predict the price (in euros) of houses based on various features such as:

Number of rooms 🛏️

Property size 📐

Number of bathrooms 🚿

Year built 🏗️

Neighborhood 📍
----------------------------------------------------
🗃️ Data Preprocessing
✅ Loaded dataset from a .pkl file using pickle.

✅ Converted all relevant string columns to lowercase and encoded categorical features with LabelEncoder.

✅ Removed outliers based on price and size using boxplots and logical filtering.

✅ Added a log transformation of the target variable for better distribution (price_euro_lg).
----------------------------------------------------
📊 Exploratory Data Analysis
Used seaborn.pairplot() to identify relationships between numerical features.

Checked for outliers with box plots.

Discovered that size and year built showed meaningful variation with price.
----------------------------------------------------
🤖 Model Building
Model Used: RandomForestRegressor from sklearn.ensemble

500 estimators

Max features: 3

Subsampling: 60 samples

Out-of-bag score enabled for validation

Training/Test Split: 95% / 5%

Features Used:

rooms

size

bathrooms

neighbourhood (encoded)

year_built
----------------------------------------------------
📈 Results
Metric	Value
OOB Score	0.67 🌟
MAE	~€17,552 💰
RMSE	~€22,959 📉

These results show the model performs decently and captures important pricing signals.
----------------------------------------------------
💾 Model Export
The trained model was serialized and saved using pickle:

python
Copy
Edit
with open("rf_model.pkl", "wb") as f:
    pkl.dump(rf, f)
🔍 Feature Importance
The most important features according to the model were:

Property size 📐

Year built 🏗️

Neighborhood 📍
----------------------------------------------------
Plotted using seaborn.barplot() for interpretability.

🧰 Tech Stack
Python 🐍

Pandas, NumPy

Scikit-learn

Seaborn & Matplotlib

Pickle for model serialization
