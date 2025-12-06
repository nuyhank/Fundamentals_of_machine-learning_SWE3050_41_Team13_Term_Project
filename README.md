Bitcoin Volatility Regime Classification
This repository contains a machine learning project designed to classify and predict Bitcoin volatility regimes (High/Low). The project utilizes various financial indicators, including cryptocurrencies, S&P 500, VIX, and bond yields, to train models such as Logistic Regression, LDA, Elastic Net, and Random Forest using a walk-forward cross-validation approach.

🚀 Overview
Goal: Predict whether Bitcoin will experience high or low volatility in the next 5 days.

Data Source: Real-time data fetched via Yahoo Finance API (yfinance).

Environment: Optimized for Google Colab.

Key Features:

Automated data collection and preprocessing (Outlier removal, Forward filling).

Feature Engineering (RSI, MACD, ATR, Rolling Correlations, Regime Scaling).

Walk-Forward Cross-Validation for time-series data.

Model performance comparison (AUC Scores & ROC Curves).

🛠️ Prerequisites
To run this code, you need:

A Google Account (to access Google Colab).

An active internet connection (to download financial data).

No local Python installation is required.

📖 Execution Guide (Google Colab)
Follow these steps to run the notebook directly from this GitHub repository.

1. Open in Google Colab
Navigate to Google Colab.

Go to File > Open notebook.

Select the GitHub tab.

Enter this repository's URL (or search for your username) and select Bitcoin_Volatility_Regime_Classification.ipynb.

2. Install Dependencies
The notebook requires the yfinance library, which is not pre-installed in Colab. Before running the analysis, execute the first code cell containing:

Python

!pip install yfinance
3. Run the Pipeline
In the top menu, click Runtime > Run all (or press Ctrl + F9).

The notebook will execute the following steps sequentially:

Data Collection: Downloads 5 years of OHLCV data.

Preprocessing: Cleans data and handles outliers (3-Sigma capping).

Feature Engineering: Generates technical and macro indicators.

EDA: Visualizes volatility clusters and correlations.

Modeling: Trains and evaluates models using Rolling Origin CV.

📊 Expected Outputs
Upon successful execution, the notebook will generate:

Data Logs: Confirmation of data download for tickers (BTC, ETH, VIX, etc.).

Plots:

Volatility Regime Barcode Chart.

Feature Correlation Heatmap.

Violin Plots for feature distributions.

ROC Curves for all models.

Metrics: Final AUC Scores for Logistic Regression, LDA, Elastic Net, and Random Forest.

📦 Libraries Used
yfinance (Data Source)

pandas & numpy (Data Manipulation)

scikit-learn (Machine Learning & Preprocessing)

matplotlib & seaborn (Visualization)

Note: Since the model fetches real-time data, the evaluation metrics (AUC) may vary slightly depending on the date of execution.
