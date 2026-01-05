# Weather-Prediction-2025


Absolutely! Here’s a **professional, GitHub-ready README** for your weather prediction project. I wrote it to be **portfolio-friendly**, suitable for your Master’s background and German-style clarity. You can copy-paste and adjust if needed.

---

# Weather Prediction Project (Kaggle Competition)

## 📌 Overview

This project aims to **predict the minimum temperature for the next day** given **two weeks of historical weather data**.
The dataset comes from a Kaggle competition ([Weather Prediction 2025](https://www.kaggle.com/competitions/weather-prediction-2025)).

The project demonstrates:

* Data preprocessing for messy weather data
* Feature engineering from **dates** and weather columns
* Regression modeling using **Random Forest**
* Handling of **missing values** and categorical features
* Evaluation using **Mean Absolute Percentage Error (MAPE)**
* Production of a **submission-ready CSV** for Kaggle

---

## 🗂 Dataset

The dataset contains:

| Column                          | Type   | Description                          |
| ------------------------------- | ------ | ------------------------------------ |
| Date                            | object | Observation date                     |
| Maximum Temperature degrees (F) | float  | Max temperature for the day          |
| Minimum Temperature degrees (F) | float  | Min temperature for the day (target) |
| Precipitation (inches)          | object | Precipitation amount                 |
| Snow (inches)                   | object | Snowfall amount                      |
| Snow Depth (inches)             | object | Snow depth                           |

* The **target** column is `Minimum Temperature degrees (F)`
* Test set contains same features **without target**

---

## 🛠 Tools & Libraries

* Python 3.11
* Jupyter Notebook
* Pandas, NumPy
* Scikit-learn (`RandomForestRegressor`)
* Matplotlib / Seaborn (optional for visualization)

---

## ⚡ Steps

### 1. Data Preprocessing

* Convert **date column** to numeric features: `year`, `month`, `day`, `dayofweek`, `day_of_year`
* Convert object weather columns to numeric using `pd.to_numeric`
* Fill missing values using **median imputation**

### 2. Feature Engineering

* Extract **lag features** for previous days’ temperatures
* Compute **rolling averages** (optional, improves performance)
* Include **weekend / weekday indicators**

### 3. Model Training

* Split dataset into train / validation
* Train **Random Forest Regressor**
* Evaluate using **safe MAPE** to handle zero targets

### 4. Prediction

* Apply same preprocessing to test set
* Predict `Minimum Temperature degrees (F)`
* Export `submission.csv` for Kaggle

---

## 🧪 Evaluation

* Metric: **Mean Absolute Percentage Error (MAPE)**
* Local validation ensures model correctness before submission

---

## 💡 Potential Improvements

* Use **Gradient Boosting Models** (`XGBoost`, `LightGBM`)
* Fine-tune hyperparameters
* Include **additional lag and rolling features**
* Use **cross-validation for time-series**

---

## 📂 Repository Structure

```
Weather-Prediction/
│
├─ train.csv
├─ test.csv
├─ notebook.ipynb
├─ submission.csv
└─ README.md
```

---

## 🔗 References

* Kaggle Competition: [Weather Prediction 2025](https://www.kaggle.com/competitions/weather-prediction-2025)
* Random Forest documentation: [scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)

---

## 🚀 Outcome

This project demonstrates **end-to-end data science workflow**:

* Data cleaning & preprocessing
* Feature engineering from date and weather columns
* Model training & evaluation
* Submission-ready output for Kaggle competition

It’s **portfolio-ready** and showcases practical skills in **Python, Pandas, scikit-learn, and regression modeling**, which are valuable for **data analyst and data science roles in Germany**.

---

If you want, I can also write a **more “eye-catching” version** with badges, visuals, and GitHub markdown styling so it looks **professional and portfolio-ready** when someone visits your repo.

Do you want me to do that?
