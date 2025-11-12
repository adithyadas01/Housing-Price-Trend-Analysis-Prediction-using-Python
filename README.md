# 🏡 Housing Price Trend Analysis & Prediction using Python

## 📘 Project Overview
This project focuses on performing **Exploratory Data Analysis (EDA)** and developing a **Linear Regression Model** to understand and predict **housing prices** based on property features such as **area**, **bedrooms**, **furnishing status**, and **amenities**.  

The goal is to uncover insights into how different factors affect property prices and to build a simple, interpretable model for price prediction.

---

## 🎯 Objectives
- Explore and visualize housing price trends using Python libraries.  
- Identify the most significant features affecting property prices.  
- Build and evaluate a Linear Regression model for price prediction.  
- Provide actionable insights for buyers, sellers, and real estate analysts.

---

## 📂 Dataset Information
- **Source:** [Kaggle – Housing Prices Dataset by Yasser H.](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)  
- **File Name:** `Housing.csv`  
- **Size:** ~545 rows × 12 columns  

| Column | Description |
|---------|-------------|
| price | Selling price of the house |
| area | Area of the house (sq. ft.) |
| bedrooms | Number of bedrooms |
| bathrooms | Number of bathrooms |
| stories | Number of stories |
| mainroad | Whether house is on a main road |
| guestroom | Presence of a guestroom |
| basement | Presence of a basement |
| hotwaterheating | Availability of hot water heating |
| airconditioning | Availability of air conditioning |
| parking | Number of parking spaces |
| furnishingstatus | Type of furnishing (furnished/semi/unfurnished) |

---

## 🧹 Data Preprocessing
- Checked and handled missing values and duplicates.  
- Converted categorical variables using `pd.get_dummies()`.  
- Ensured numerical consistency for model features.  
- Selected relevant features for prediction:  
  `area`, `bedrooms`, `furnishingstatus`, `airconditioning`, `parking`

---

## 📊 Exploratory Data Analysis (EDA)
- Analyzed **price distribution** (right-skewed data).  
- Found strong positive correlation between **area** and **price (≈ 0.85)**.  
- Observed that **furnished** and **air-conditioned** homes have higher prices.  
- Visualized relationships using **Seaborn** and **Matplotlib**:
  - Scatter plots for Area vs Price  
  - Bar charts for Furnishing Status  
  - Correlation heatmap of numerical features  

---

## 🤖 Model Development
- **Algorithm:** Linear Regression (from `sklearn.linear_model`)  
- **Train-Test Split:** 80% training, 20% testing  
- **Performance Metrics:**
  - **R² Score:** 0.87  
  - **MAE:** 250000  
  - **RMSE:** 340000  

---

## 📈 Visualization
```python
plt.scatter(y_test, y_pred, color='blue')
plt.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], color='red', linewidth=2)
plt.xlabel("Actual Price")
plt.ylabel("Predicted Price")
plt.title("Actual vs Predicted House Prices")
plt.show()

