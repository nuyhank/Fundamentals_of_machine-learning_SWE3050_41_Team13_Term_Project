# Bitcoin Volatility Regime Classification

colab url: https://colab.research.google.com/drive/1ZiQwmBT1nYG-x1G4j295L4w-yu8xIKyP#scrollTo=-4-0rDpP24T1

This repository contains a machine learning project designed to classify and predict Bitcoin volatility regimes (High/Low). The project utilizes various financial indicators, including cryptocurrencies, S&P 500, VIX, and bond yields, to train models such as Logistic Regression, LDA, Elastic Net, and Random Forest using a walk-forward cross-validation approach.

## 🚀 Overview

* **Goal:** Predict whether Bitcoin will experience high or low volatility in the next 5 days.
* **Data Source:** Real-time data fetched via Yahoo Finance API (`yfinance`).
* **Environment:** Optimized for **Google Colab**.
* **Key Features:**
    * Automated data collection and preprocessing (Outlier removal, Forward filling).
    * Feature Engineering (RSI, MACD, ATR, Rolling Correlations, Regime Scaling).
    * Walk-Forward Cross-Validation for time-series data.
    * Model performance comparison (AUC Scores & ROC Curves).

## 🛠️ Prerequisites

To run this code, you need:
* A **Google Account** (to access Google Colab).
* An active internet connection (to download financial data).
* No local Python installation is required.

## 📖 Execution Guide (Google Colab)

Follow these steps to run the notebook directly from this GitHub repository.

### 1. Open in Google Colab
1.  Navigate to [Google Colab](https://colab.research.google.com/).
2.  Go to **File** > **Open notebook**.
3.  Select the **GitHub** tab.
4.  Enter this repository's URL (or search for your username) and select `Bitcoin_Volatility_Regime_Classification.ipynb`.

### 2. Install Dependencies
The notebook requires the `yfinance` library, which is not pre-installed in Colab.
**Before running the analysis**, execute the first code cell containing:

```python
!pip install yfinance
