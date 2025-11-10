# DA5401 Assignment 8 — Ensemble Learning for Bike Sharing Demand Prediction

**Name:** Nitesh Kumar Shah  
**Roll Number:** ID25M806  
**Course:** DA5401 – Foundations of Machine Learning  
**Institution:** IIT Madras (M.Tech in Data Science & AI)  
**Date:** 10  November 2025  

---

## 🧭 Problem Statement

The problem statement for this assignment focuses on developing a **predictive model to forecast the total number of bikes rented per hour** in a city’s bike-sharing program using the **Bike Sharing Demand Dataset** from the **UCI Machine Learning Repository**.  
This is a **complex regression problem** because the rental count (`cnt`) depends on several interrelated factors such as **weather conditions, time of day, season, and working-day status**, all of which interact in **non-linear and time-dependent** ways.  

The objective is to **build and compare three ensemble learning approaches — Bagging, Boosting, and Stacking** — to minimize prediction error measured through **Root Mean Squared Error (RMSE)**.  
The study aims to demonstrate how different ensemble techniques handle the **bias-variance trade-off**, improve model robustness, and outperform single regressors like **Decision Tree** and **Linear Regression**, ultimately leading to a **more reliable forecasting model** for operational planning and resource management in bike-sharing systems.

---

## ⚙️ Dataset Information

**Dataset:** [Bike Sharing Dataset – UCI Repository](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)  
**Creator:** Hadi Fanaee-T (2013)  
**Instances:** 17,389 hourly observations  
**Features:** 13 predictors + 1 target (`cnt`)  
**Target:** `cnt` — Total number of rented bikes per hour  

### 🧩 Key Features
| Feature | Description |
|----------|--------------|
| `dteday` | Date (2011–2012) |
| `season` | 1: Winter, 2: Spring, 3: Summer, 4: Fall |
| `yr` | Year (0 = 2011, 1 = 2012) |
| `mnth` | Month (1–12) |
| `hr` | Hour of day (0–23) |
| `holiday` | Whether the day is a holiday |
| `weekday` | Day of the week |
| `workingday` | 1 if working day, else 0 |
| `weathersit` | 1: Clear, 2: Mist, 3: Light Snow/Rain, 4: Heavy Rain/Snow |
| `temp`, `atemp`, `hum`, `windspeed` | Continuous weather features |
| `cnt` | Target variable – total bike rentals (casual + registered) |

---

## ⚙️ Modeling & Results

| Model | Type | RMSE | Improvement vs Baseline |
|--------|------|------|--------------------------|
| Decision Tree | Baseline | 99.38 | — |
| Linear Regression | Baseline | 137.92 | –38.8 % |
| Bagging Regressor | Ensemble | 96.10 | +3.3 % |
| Gradient Boosting | Ensemble | 41.85 | +57.9 % |
| **Stacking Regressor** | **Ensemble** | **41.12** | **+58.6 %** |

### Key Takeaways
- **Bagging** → reduced variance via bootstrap aggregation.  
- **Boosting** → reduced bias through sequential correction.  
- **Stacking** → combined strengths of all models using Ridge meta-learner → **best performance**.

---

