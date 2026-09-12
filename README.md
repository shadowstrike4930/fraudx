# FraudX

A real-time fraud detection system that uses machine learning to identify anomalous transactions through an API and web dashboard.

## How It Works

```text
Transaction
     ↓
Feature Engineering
     ↓
Preprocessing
     ↓
ML Model
     ↓
Fraud / Anomaly Score
     ↓
FastAPI
     ↓
React Dashboard
```

FraudX processes transaction and user-behavior data, generates relevant features, applies preprocessing, and uses machine learning models to identify potentially fraudulent transactions.

The system provides real-time prediction through a **FastAPI backend**, stores transaction data using **PostgreSQL**, and displays results through a **React dashboard**.

## Features

* Real-time transaction fraud scoring
* Isolation Forest anomaly detection
* Feature engineering based on transaction and user behavior
* Numerical scaling and categorical encoding
* FastAPI REST API
* PostgreSQL database integration
* React monitoring dashboard
* Automated testing

## Machine Learning

The project uses an **Isolation Forest** for unsupervised anomaly detection.

The ML pipeline includes:

* Feature generation
* Data preprocessing
* Categorical encoding
* Numerical scaling
* Model inference
* Anomaly scoring

Serialized models and preprocessing components are stored as `.pkl` files for inference.

## Tech Stack

**ML:** Python, Scikit-learn, Pandas, NumPy
**Backend:** FastAPI, Uvicorn
**Database:** PostgreSQL
**Frontend:** React, Axios
**Testing:** Pytest
**Tools:** Docker, Joblib

## Project Structure

```text
FraudX/
├── app/                     # FastAPI backend
├── Database/                # Database files
├── frontend/                # React dashboard
├── model/                   # ML-related files
├── tests/                   # Automated tests
├── Feature_Generation.py    # Feature engineering
├── IsolationForest.ipynb    # ML experimentation
├── isolationforest.py       # Model implementation
├── generate_token.py        # Authentication utility
├── run.py                   # Application runner
├── iso_forest_model.pkl     # Trained model
├── xgb_model.pkl            # XGBoost model
├── onehot_encoder.pkl       # Preprocessing encoder
└── requirements.txt
```

## Running Locally

### Backend

```bash
pip install -r requirements.txt
cd app
uvicorn main:app --reload
```

API:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

### Frontend

```bash
cd frontend
npm install
npm start
```

Dashboard:

```text
http://localhost:3000
```

### Tests

From the project root:

```bash
pytest
```

