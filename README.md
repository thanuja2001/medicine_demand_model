# PharmaCast: AI-Driven Pharmacy Demand Forecasting & Inventory Management System

PharmaCast is an intelligent, end-to-end machine learning and web backend system designed to forecast monthly medicine demand, optimize inventory levels, and prevent medicine stockouts. It combines **Polynomial Regression with LassoCV**, **SARIMA time-series analysis**, and a **Flask REST API** to deliver actionable supply chain insights.

---

## Key Features

* **Advanced Machine Learning Forecasting:** Uses polynomial feature expansion coupled with `LassoCV` regularization to predict monthly medicine requirements accurately.
* **Seasonal Adjustments:** Incorporates regional seasonal patterns (e.g., South-West Monsoon, North-East Monsoon, Inter-Monsoon) into the prediction logic.
* **Automated Stock Buffer & Reorder Alerts:** Calculates safety stock thresholds (Buffer Rate: 1.20) and automatically flags low-stock medicines needing replenishment.
* **Flask REST API:** Exposes endpoints for frontend dashboards to fetch medicine lists and query real-time demand forecasts.
* **Robust Data Cleaning:** Cleans and normalizes messy pharmacy sales data, standardizes medicine names, and handles date parsing reliably.

---

## Tech Stack

* **Language:** Python 3.10+
* **Machine Learning & Data Processing:** `scikit-learn`, `statsmodels`, `pandas`, `numpy`
* **Backend & API:** `Flask`, `Flask-CORS`
* **Visualization:** `matplotlib`, `seaborn`
* **Persistence:** `joblib`

---

## Project Structure

```text
pharma-cast/
│
├── Medicine.csv                  # Raw historical sales dataset
├── Current stock.csv             # Current inventory levels dataset
├── train_forecast.py             # Data preprocessing, model training & artifact generation
├── server.py                     # Flask backend REST API
├── medicine_demand_model.pkl     # Saved model & metadata artifacts (generated)
├── requirements.txt              # Python dependencies
└── README.md                     # Project documentation
