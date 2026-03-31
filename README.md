# 🏠 House Price Predictor

A machine learning project that predicts residential house prices using **Linear Regression** and `scikit-learn`.

---

## 📋 Overview

This project trains a regression model on 20 synthetic housing records, evaluates it using MAE and R², and provides interactive command-line predictions for any custom house.

---

## 🧠 Features Used

| Feature    | Type       | Range          |
|------------|------------|----------------|
| `area`     | Continuous | 900 – 3500 sqft |
| `bedrooms` | Discrete   | 1 – 5          |
| `bathrooms`| Discrete   | 1 – 4          |
| `age`      | Continuous | 1 – 30 years   |
| `garage`   | Binary     | 0 = No, 1 = Yes |

**Target:** `price` ($130,000 – $610,000)

---

## ⚙️ Setup

### Install dependencies
```bash
pip install pandas scikit-learn
```

### Run the script
```bash
python house_price_predictor.py
```

---

## 🚀 Usage

After running the script, it will:

1. Print model metrics (MAE, R²)
2. Show which features increase/decrease price
3. Predict prices for 3 sample houses
4. Ask for your own house details (press Enter to use defaults)

**Example interaction:**
```
Area (sqft)  [default: 2000]: 1800
Bedrooms     [default: 3]   : 3
Bathrooms    [default: 2]   : 2
Age (years)  [default: 10]  : 7
Garage? 1=Yes 0=No [default: 1]: 1

  Estimated Price → $308,450
```

---

## 📊 Model Pipeline

```
Raw Data → pandas DataFrame
        → train_test_split (80/20, random_state=42)
        → StandardScaler (fit on train, transform both)
        → LinearRegression.fit()
        → Evaluate: MAE + R²
        → Predict new houses
```

---

## 📁 Project Structure

```
house-price-predictor/
├── house_price_predictor.py   # Main script
└── README.md                  # This file
```

---

## 🔧 Tech Stack

- **Python 3.x**
- **pandas** — data handling
- **scikit-learn** — ML model, scaling, metrics

---
