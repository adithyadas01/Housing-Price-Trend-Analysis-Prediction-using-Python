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

The scatter plot shows most predictions close to the diagonal line → good accuracy.

Outliers represent extreme cases not perfectly captured by the model.

### 💡 Key Insights

Area is the strongest determinant of price.

Furnishing and air conditioning significantly increase property value.

More than 4 bedrooms do not proportionally raise prices — diminishing returns.

Parking spaces provide affordable value improvements.

### 🚀 Future Enhancements

Use Random Forest Regressor or Multiple Linear Regression for improved results.

Add location-based features (e.g., city, distance to main road).

Apply feature scaling and polynomial regression for nonlinear trends.

Deploy as a Streamlit web app for real-time predictions.

### 🛠️ Tools & Libraries

**🐍 Python**

**🔢 NumPy**

**🧮 Pandas**

**📊 Matplotlib**

**🎨 Seaborn**

**🤖 Scikit-learn**

### 🏁 Conclusion

This project demonstrates how data analysis and machine learning can be used to predict real estate prices effectively.
With an accuracy of around 87%, the model provides meaningful insights for property valuation and investment decisions.

📎 Author

👤 Adithya D
💬 Data Enthusiast | Python | Data Analysis | Machine Learning

📫 Connect with me on LinkedIn:The scatter plot shows most predictions close to the diagonal line → good accuracy.

Outliers represent extreme cases not perfectly captured by the model.

### 💡 Key Insights

Area is the strongest determinant of price.

Furnishing and air conditioning significantly increase property value.

More than 4 bedrooms do not proportionally raise prices — diminishing returns.

Parking spaces provide affordable value improvements.

🚀 Future Enhancements

Use Random Forest Regressor or Multiple Linear Regression for improved results.

Add location-based features (e.g., city, distance to main road).

Apply feature scaling and polynomial regression for nonlinear trends.

Deploy as a Streamlit web app for real-time predictions.

🛠️ Tools & Libraries

🐍 Python

🔢 NumPy

🧮 Pandas

📊 Matplotlib

🎨 Seaborn

🤖 Scikit-learn

🏁 Conclusion

This project demonstrates how data analysis and machine learning can be used to predict real estate prices effectively.
With an accuracy of around 87%, the model provides meaningful insights for property valuation and investment decisions.

📎 Author

👤 Adithya D
💬 Data Enthusiast | Python | Data Analysis | Machine Learning

📫 Connect with me on LinkedIn :The scatter plot shows most predictions close to the diagonal line → good accuracy.

Outliers represent extreme cases not perfectly captured by the model.

💡 Key Insights

Area is the strongest determinant of price.

Furnishing and air conditioning significantly increase property value.

More than 4 bedrooms do not proportionally raise prices — diminishing returns.

Parking spaces provide affordable value improvements.

🚀 Future Enhancements

Use Random Forest Regressor or Multiple Linear Regression for improved results.

Add location-based features (e.g., city, distance to main road).

Apply feature scaling and polynomial regression for nonlinear trends.

Deploy as a Streamlit web app for real-time predictions.

🛠️ Tools & Libraries

🐍 Python

🔢 NumPy

🧮 Pandas

📊 Matplotlib

🎨 Seaborn

🤖 Scikit-learn

🏁 Conclusion

This project demonstrates how data analysis and machine learning can be used to predict real estate prices effectively.
With an accuracy of around 87%, the model provides meaningful insights for property valuation and investment decisions.

📎 Author

👤 Adithya D
💬 Data Enthusiast | Python | Data Analysis | Machine Learning

📫 Connect with me on LinkedIn :www.linkedin.com/in/adithya-d30

⭐ Feel free to star this repo if you found it helpful!

🏷️ Tags

#Python #DataAnalysis #MachineLearning #LinearRegression #EDA #Matplotlib #Pandas #Seaborn #Kaggle #PortfolioProject

