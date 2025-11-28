# 📈 Stock Forecast MLOps Platform

## Project Overview

This project is a comprehensive **Machine Learning Operations (MLOps)
platform** for **time series forecasting of stock prices**.\
It uses a modern, serverless architecture to automate data ingestion,
model training, persistence, and web deployment.

The application is built using:

-   **Python** → forecasting core\
-   **Streamlit** → interactive UI\
-   **Supabase** → database + model/prediction storage\
-   **GitHub Actions** → automated CI/CD pipeline\
-   **Vercel** → deployment host

## 🌟 Features

### Real-time Data Fetching

Fetches historical and live stock price data (e.g., via **yfinance**).

### Time Series Forecasting

Models: - Prophet - ARIMA - LSTM

### Interactive Visualization

Uses **Plotly** for charts: - Historical data\
- Forecast curve\
- Confidence intervals

### Persistent Predictions

Stores predictions, model metadata, and logs in **Supabase PostgreSQL**.

### Automated Retraining

A scheduled **GitHub Action** periodically retrains the model and
updates predictions.

### Responsive Web App

Streamlit app deployed on **Vercel**.

## 🛠️ Technology Stack

  ---------------------------------------------------------------------------------
  Component            Technology                                   Role
  -------------------- -------------------------------------------- ---------------
  Machine Learning     Python, Pandas, NumPy                        Data
                                                                    preprocessing &
                                                                    core logic

  Forecasting Model    Prophet / Scikit-learn / TensorFlow          Time series
                                                                    prediction
                                                                    models

  Frontend/App         Streamlit, Plotly                            UI +
                                                                    visualization

  Database/Backend     Supabase (PostgreSQL, Storage)               Storage for
                                                                    predictions &
                                                                    models

  CI/CD                GitHub Actions                               Automated
                                                                    training and
                                                                    deployment

  Deployment           Vercel                                       Hosting the
                                                                    Streamlit app
  ---------------------------------------------------------------------------------

## 📐 Architecture and MLOps Pipeline

1.  **Source Control** --- Code in GitHub.
2.  **Data Persistence** --- Supabase stores historical data and model
    artifacts.
3.  **Model Training** --- GitHub Action runs `train.py` on a schedule.
4.  **Web App** --- Streamlit app fetches latest predictions from
    Supabase.
5.  **Continuous Deployment** --- Push to `main` triggers Vercel
    deployment.

## 🚀 Local Setup & Run

### Prerequisites

-   Python 3.8+
-   A Supabase project

### 1. Clone repository

``` bash
git clone <repository_url>
cd stock-forecast-platform
```

### 2. Create virtual environment

**Linux/macOS:**

``` bash
python -m venv venv
source venv/bin/activate
```

**Windows:**

``` bash
python -m venv venv
.env\Scriptsctivate
```

### 3. Install dependencies

``` bash
pip install -r requirements.txt
```
