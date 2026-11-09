# 🏠 House Price Prediction

A machine learning project that predicts **median house values** from housing data such as location, rooms, population and income. It compares a linear model with a tuned Random Forest using **scikit-learn**.

---

## ✨ What it does

1. **Exploratory data analysis:** histograms, a correlation heatmap and a latitude/longitude price map
2. **Data cleaning:** removes rows with missing values
3. **Feature engineering:**
   - Log-transforms skewed features (`total_rooms`, `total_bedrooms`, `population`, `households`)
   - One-hot encodes `ocean_proximity`
   - Adds new features: `bedroom_ratio` and `household_rooms`
4. **Scaling:** standardizes features with `StandardScaler`
5. **Modelling:** trains Linear Regression and Random Forest, then tunes the forest with `GridSearchCV` (5-fold cross-validation)

## 📊 Results (R² on the test set)

| Model | R² score |
|---|---|
| Linear Regression | **0.68** |
| Random Forest | **0.82** |
| Random Forest (GridSearchCV) | **0.82** |

The Random Forest explains about **82%** of the variation in house prices, a big improvement on the linear baseline.

## 📁 Project structure

```
├── House-Price-Prediction.ipynb   # Full notebook: EDA → features → models
└── housing.csv                    # Dataset
```

## 🚀 Run it

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook House-Price-Prediction.ipynb
```

## 🛠️ Tech stack

Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Jupyter

---

👤 **Tushara Dassanayake** · [LinkedIn](https://www.linkedin.com/in/tushara-dassanayake-4b428530a) · tusharadassanayake99@gmail.com
