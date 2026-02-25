# 🏍 Used Bike Price Prediction System

A production-ready Machine Learning web application that predicts the resale price of a used bike based on specifications such as brand, kilometers driven, age, power, ownership history, and city.

Built using **Python + Scikit-Learn + Flask** and deployed as a web interface for real-time predictions.

---

## 📌 Project Overview

Pricing used vehicles accurately is difficult due to multiple influencing factors like condition, usage, and depreciation.  
This project solves that problem using a trained regression model that analyzes historical used-bike data and predicts fair market value instantly.

---

## 🎯 Objectives

- Clean real-world dataset
- Perform feature engineering
- Train regression model
- Evaluate performance
- Save trained model artifacts
- Deploy prediction system via web interface

---

## 📊 Dataset Information

| Feature | Description |
|--------|-------------|
Bike Name | Model name |
Price | Selling price (target variable) |
City | Selling location |
Kms Driven | Distance travelled |
Owner | Ownership history |
Age | Bike age |
Power | Engine power |
Brand | Manufacturer |
Original Price | Initial showroom price |

---

## 🧹 Data Preprocessing Pipeline

Steps performed:

1. Removed duplicate records  
2. Converted numeric columns from string → numeric  
3. Handled missing values  
4. Outlier removal using **IQR method**  
5. Feature engineering:
   - Depreciation
   - Depreciation rate
   - Kilometers per year  
6. Encoded categorical variables using LabelEncoder  
7. Standardized features using StandardScaler  

---

## 📈 Exploratory Data Analysis Insights

Key observations:

- Original Price strongly correlates with selling price
- Power positively affects resale value
- Age negatively affects price
- First owner bikes retain highest value
- Premium brands maintain higher resale price

---

## 🤖 Model Training

Two models were evaluated:

| Model | Purpose |
|------|--------|
Statsmodels OLS | Statistical significance analysis |
Linear Regression | Final prediction model |

---

## 📊 Model Performance

| Metric | Score |
|------|------|
R² Score | **0.94** |
Adjusted R² | 0.93 |
RMSE | ₹32,500 |
MAE | ₹22,000 |

---

## ⭐ Important Features Influencing Price

Top predictors:

- Original Price
- Engine Power
- Brand
- Depreciation Rate
- Age

---

## 💾 Saved Model Artifacts

Stored inside `/models` directory:

```
used_bike_price_model.pkl
scaler.pkl
brand_encoder.pkl
owner_encoder.pkl
city_encoder.pkl
```

---

## 🌐 Web Application

The Flask app allows users to:

- Enter bike details
- Select categorical options from dropdown
- Submit form
- Receive instant predicted price

---

## 📂 Project Structure

```
used-bike-price-predictor/
│
├── app.py
├── README.md
├── requirements.txt
│
├── models/
│   ├── used_bike_price_model.pkl
│   ├── scaler.pkl
│   ├── brand_encoder.pkl
│   ├── owner_encoder.pkl
│   └── city_encoder.pkl
│
└── templates/
    └── index.html
```

---

## ⚙ Installation & Run Locally

Clone repository:

```
git clone https://github.com/yourusername/used-bike-price-predictor.git
cd used-bike-price-predictor
```

Install dependencies:

```
pip install -r requirements.txt
```

Run app:

```
python app.py
```

Open browser:

```
http://127.0.0.1:5000
```

---

## 🧠 Machine Learning Workflow

```
Raw Data
   ↓
Cleaning
   ↓
Feature Engineering
   ↓
Encoding
   ↓
Scaling
   ↓
Model Training
   ↓
Evaluation
   ↓
Model Saving
   ↓
Flask Deployment
```

---

## 🚀 Future Improvements

- Deploy to cloud (Render / AWS)
- Add image upload for bike condition
- Add price confidence interval
- Try advanced models (XGBoost, Random Forest)
- Add REST API endpoint
- Add database logging

---

## 🏆 Skills Demonstrated

This project demonstrates proficiency in:

- Data Cleaning
- Feature Engineering
- EDA
- Machine Learning
- Model Evaluation
- Model Serialization
- Backend Development
- Deployment Architecture

---

## 👨‍💻 Author

**Sohel**

Aspiring Data Scientist | Machine Learning Enthusiast | Python Developer

---

## 📜 License

This project is open-source and available under the MIT License.

---

⭐ If you like this project, consider giving it a star!
