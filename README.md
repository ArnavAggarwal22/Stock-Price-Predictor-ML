# 📈 Stock Price Prediction using K-Nearest Neighbors (KNN)

This project demonstrates how to use Machine Learning (KNN algorithm) for **predicting future stock prices** and **generating Buy/Sell signals** based on historical stock data.

It uses **publicly available financial data**, engineering features from them, and training two models:
- A **regressor** to forecast future closing prices
- A **classifier** to decide Buy or Sell action

Additionally, the notebook simulates and visualizes **the next 5 predicted closing prices** to aid human decision-making.

---

## 📌 Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Flow](#project-flow)
  - [1. Data Collection](#1-data-collection)
  - [2. Feature Engineering](#2-feature-engineering)
  - [3. Classification Model](#3-classification-model)
  - [4. Regression Model](#4-regression-model)
  - [5. Predicting & Plotting Future Days](#5-predicting--plotting-future-days)
- [How to Use](#how-to-use)
- [Visual Example](#visual-example)
- [Future Improvements](#future-improvements)
- [Author](#author)
- [License](#license)

---

## 🚀 Features

✅ Fetches historical stock data  
✅ Engineers features based on price movements  
✅ Trains:
- KNN Classifier to predict Buy/Sell
- KNN Regressor to predict Close Price  
✅ Uses `GridSearchCV` to optimize `k`  
✅ Predicts tomorrow’s action and price  
✅ Simulates & plots next 5 days’ predicted prices  
✅ Interactive, real-time prediction via notebook input

---

## 🛠️ Tech Stack

| Tool/Library        | Use Case                         |
|---------------------|----------------------------------|
| Python              | Programming Language             |
| Pandas              | Data manipulation                |
| NumPy               | Numerical operations             |
| Matplotlib          | Plotting graphs                  |
| yfinance            | Downloading stock market data    |
| scikit-learn        | Machine Learning models & tools  |

---

## 🔁 Project Flow

### 1. 📥 Data Collection
We use `yfinance` to fetch stock data:

```python
import yfinance as yf
data = yf.download("SYMBOL", start="2010-01-01")
