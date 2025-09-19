# Assignment-1-APR
Machine learning Project
Here is a simple, code‑free README suited for a GitHub repository of the TSLA linear regression project.

TSLA Close Price Prediction
A lightweight project that predicts Tesla’s daily Close price using a linear regression model trained on OHLCV data.

Overview
Goal: Predict the Close price from same‑day Open, High, Low, and Volume.

Outputs: Evaluation metrics (R², RMSE), a small predictions preview, and three diagnostic plots.

Notes: Very high R² is expected because Close is tightly related to the daily price range (High/Low).

Dataset
Input file: TSLA.csv (daily OHLCV with Date, Open, High, Low, Close, Adj Close, Volume).

Assumption: File is placed at the project root.

What it produces
Metrics file with R², RMSE, intercept, and feature coefficients.

Preview CSV showing a few rows of Actual vs Predicted for the test set.

Plots:

Predicted vs Actual (with identity line).

Residuals vs Predicted.

Actual vs Predicted over time for the test fold.

How it works
Splits the data into training and testing sets (80/20) with a fixed random seed.

Trains an ordinary least squares regression on Open, High, Low, and Volume to predict Close.

Evaluates on the test set and saves metrics and plots.

Results (example)
R² near 1.0 and low RMSE on the test split, reflecting the strong relationship of Close with same‑day High/Low.

High and Low typically show the strongest positive influence; Volume is often negligible in this configuration.

Limitations
Not a forward‑looking forecast: it uses same‑day features that co‑move with Close.

Multicollinearity among OHLC features can inflate interpretability of coefficients.

Next steps
Add lagged features and rolling indicators for true forecasting.

Use time‑series cross‑validation.

Compare with regularized linear models and non‑linear baselines.

Evaluate against naive benchmarks (e.g., previous Close).
