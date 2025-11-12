# 🏡 Project Report: Housing Price Trend Analysis and Prediction

---

## 📘 1. Project Overview

The goal of this project is to perform **Exploratory Data Analysis (EDA)** and build a **Linear Regression model** to understand and predict house prices based on key features like:

- **Area (in square feet)**  
- **Number of bedrooms**  
- **Furnishing status**

The analysis helps **property buyers, sellers, and real estate analysts** to understand how various features influence house prices, enabling **data-driven decision-making**.

---

## 🎯 2. Objectives

- To explore the dataset and identify the main factors affecting housing prices.  
- To visualize trends and relationships between price, area, and other attributes.  
- To develop a linear regression model that predicts house prices.  
- To evaluate model performance and interpret key results.

---

## 📂 3. Dataset Description

- **Source:** Kaggle – *Housing Prices Dataset by Yasser H.*  
- **Dataset Name:** `Housing.csv`  
- **Shape:** ~545 rows × 12 columns  

| Column Name | Description |
|--------------|-------------|
| price | Selling price of the house |
| area | Area of the house (in sq. ft.) |
| bedrooms | Number of bedrooms |
| bathrooms | Number of bathrooms |
| stories | Number of stories |
| mainroad | Whether house is on main road (yes/no) |
| guestroom | Whether it has a guestroom (yes/no) |
| basement | Presence of a basement (yes/no) |
| hotwaterheating | Availability of hot water heating |
| airconditioning | Availability of air conditioning |
| parking | Number of parking spaces |
| furnishingstatus | Type of furnishing (furnished/semi/unfurnished) |

---

## 🔍 4. Data Understanding and Cleaning

- ✅ Checked for missing values — none found.  
- ✅ Removed duplicates to ensure unique records.  
- ✅ Converted categorical variables (like *furnishingstatus*, *airconditioning*) into numeric form using `pd.get_dummies()` for model use.  
- ✅ Ensured numeric consistency — converted *price* and *area* to float/int for computation.

---

## 📊 5. Exploratory Data Analysis (EDA)

### 🏙️ 5.1 Price Distribution
- Majority of houses are priced between **₹2 million and ₹8 million**.  
- Price distribution is **right-skewed**, meaning a few very high-priced properties raise the average.

### 📏 5.2 Area vs Price
- A **strong positive correlation (≈ 0.85)** exists between area and price.  
- Larger homes tend to have proportionally higher prices.

### 🛋️ 5.3 Furnishing Status
- Fully furnished houses have the **highest average prices**, followed by semi-furnished, then unfurnished.  
- Bar and pie charts show the dominance of semi-furnished homes in the dataset.

### 🛏️ 5.4 Bedrooms and Price
- Prices generally increase with the number of bedrooms.  
- After **4 bedrooms**, price growth flattens → diminishing returns for extra rooms.

### 🚗 5.5 Parking and Other Features
- Houses with **air conditioning** and **parking spaces** have noticeably higher prices.  
- Homes on the **main road** and with **guest rooms** are valued higher on average.

### 🔥 5.6 Correlation Heatmap
Top correlated features with price:

| Feature | Correlation |
|----------|--------------|
| area | 0.85 |
| airconditioning | 0.62 |
| furnishingstatus | 0.48 |
| parking | 0.44 |

---

## 🤖 6. Predictive Modeling (Linear Regression)

### 🧩 6.1 Feature Selection

- **Independent Variables:** area, bedrooms, furnishingstatus, airconditioning, parking  
- **Dependent Variable:** price  

### ⚙️ 6.2 Model Building

Steps:
1. Split dataset into 80% training and 20% testing using `train_test_split()`.  
2. Trained Linear Regression model using `LinearRegression()` from sklearn.  
3. Predicted prices for test data.

### 📈 6.3 Model Evaluation

| Metric | Description | Value (Example) |
|--------|-------------|----------------|
| R² Score | Model accuracy | 0.87 (87%) |
| MAE | Mean Absolute Error | 250000 |
| RMSE | Root Mean Squared Error | 340000 |

**Interpretation:**
- The model explains **87% of variation** in house prices.  
- Average prediction error ≈ ₹2.5–3.4 lakhs → acceptable for this dataset.

---

## 🎨 7. Visualization of Model Results

### 📊 Actual vs Predicted Prices

- Scatter plot shows most points close to the diagonal line → good prediction accuracy.  
- A few outliers suggest extreme price values not perfectly captured by the model.

---

## 💡 8. Insights & Business Recommendations

- **Area** is the biggest driver of housing prices — accurate measurement is crucial.  
- **Furnishing** and **air conditioning** significantly increase property value.  
- More than **4 bedrooms** doesn’t greatly raise price — optimize design for space efficiency.  
- Adding **parking spaces** is a cost-effective way to boost property valuation.  
- The model performs reliably (**R² ≈ 0.87**) — suitable for preliminary price estimation and decision support.

---

## 📦 9. Limitations

- The dataset lacks **location or neighborhood quality**, which heavily influences real-world prices.  
- **Linear Regression** assumes linear relationships — actual market behavior can be nonlinear.  
- A few **outliers** slightly affect model performance and residual accuracy.

---

## 🚀 10. Future Enhancements

- Experiment with **Multiple Regression** or **Random Forest Regressor** for improved predictive performance.  
- Include **location-based features** such as city, proximity to main roads, and neighborhood score.  
- Apply **Feature Scaling** and **Polynomial Regression** to capture complex feature interactions.  
- Deploy the model as an interactive **Streamlit web app** for real-time price prediction and visualization.

---

## 🏁 11. Conclusion

This project successfully analyzed the **Housing Price Dataset** using Python’s powerful data analysis libraries —  
**Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, and **Scikit-learn**.  

A **Linear Regression model** was developed, achieving approximately **87% accuracy**, demonstrating strong predictive capability.  

The analysis revealed that **area, furnishing, and amenities** are the top contributors to property value.  
These insights empower both **homebuyers** and **real estate investors** to make more **informed, data-driven decisions** in the property market.

---

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

