# Stock Price Prediction using Machine Learning

## Project Overview

This project uses Machine Learning techniques to predict the next day’s stock closing price using historical stock market data. The data was retrieved from Yahoo Finance using the yfinance Python library.

The goal of the project is to analyze historical stock trends and build regression models capable of estimating future closing prices based on previous market indicators.

This project demonstrates the application of regression algorithms in financial data analysis and predictive modeling.

---

## Problem Statement

Predict the next day’s stock closing price using historical stock data.

The prediction is based on the following features:

* Open Price
* High Price
* Low Price
* Trading Volume

Target variable:

* Next Day Closing Price

This is a **regression problem** because the output is a continuous numerical value.

---

## Dataset

Dataset Source: Yahoo Finance

Historical stock market data was downloaded using the yfinance Python library.

Selected stock:

* Apple Inc. (AAPL)

### Features Used

* **Open** — Stock opening price of the day
* **High** — Highest stock price during the day
* **Low** — Lowest stock price during the day
* **Close** — Closing price of the day
* **Volume** — Number of shares traded

### Target

The target variable was created by shifting the Close column by one day:

Target = Next Day Close Price

This means the model learns to predict tomorrow’s closing price using today’s market data.

---

## Project Objectives

* Load historical stock data
* Prepare features and target variable
* Train regression models
* Compare model performance
* Evaluate predictions using regression metrics
* Visualize actual vs predicted prices

---

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* yfinance

---

## Data Collection

Stock data was downloaded using:

```python
import yfinance as yf
df = yf.download("AAPL", start="2020-01-01", end="2025-01-01")
```

The dataset contained daily stock prices over multiple years.

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Selected relevant columns:

   * Open
   * High
   * Low
   * Close
   * Volume

2. Created target column using shifted Close prices

3. Removed missing rows after shifting

4. Split data into:

   * Training set
   * Testing set

This ensured clean input for model training.

---

## Machine Learning Models Used

### 1. Linear Regression

Linear Regression models the relationship between input features and target using a linear equation.

Formula:

y = b0 + b1x1 + b2x2 + b3x3 + b4x4

Where:

* x1 = Open
* x2 = High
* x3 = Low
* x4 = Volume

Advantages:

* Simple and fast
* Easy to interpret
* Works well on linear relationships

---

### 2. Random Forest Regressor

Random Forest is an ensemble learning algorithm that combines multiple decision trees.

Each tree predicts a value, and the final output is the average of all trees.

Advantages:

* Handles nonlinear relationships
* High predictive power
* Reduces overfitting compared to single trees

---

## Model Training

Input features:

X = [Open, High, Low, Volume]

Target:

Y = Next Day Close Price

The dataset was split into:

* 80% Training Data
* 20% Testing Data

The models were trained on historical stock data and tested on unseen samples.

---

## Evaluation Metrics

### Mean Absolute Error (MAE)

MAE measures the average prediction error.

Formula:

MAE = Average(|Actual - Predicted|)

Lower MAE indicates better performance.

---

### R² Score

R² measures how well the model explains variance in the data.

Interpretation:

* 1 → Perfect prediction
* 0 → Poor model
* Negative → Worse than baseline

Higher R² indicates better performance.

---

## Model Results

### Linear Regression

* MAE: 2.2369847298353185
* R² Score: 0.9942324837367363

### Random Forest

* MAE: 2.376202865782238
* R² Score: 0.994062191993983

---

## Performance Comparison

Linear Regression slightly outperformed Random Forest:

* Lower Mean Absolute Error
* Slightly higher R² score

This suggests that stock features in this dataset had a strong linear relationship with the target variable.

---

## Visualization

The project includes a line plot comparing:

* Actual Closing Prices
* Predicted Closing Prices

This visualization helps evaluate how closely predictions follow real market behavior.

Observations:

* Predicted values closely follow actual values
* Small deviations indicate low prediction error
* Model captures price trend effectively

---

## Key Insights

Important observations from this project:

* Open, High, and Low prices strongly influence next-day closing price
* Linear Regression performed better than Random Forest
* Stock prices showed strong linear correlation
* Simple models can perform very well on structured financial data

---

## Project Workflow

1. Import libraries
2. Download stock data
3. Select features
4. Create target variable
5. Split dataset
6. Train regression models
7. Evaluate performance
8. Plot actual vs predicted prices

---

## Future Improvements

Possible enhancements:

* Use LSTM for time-series forecasting
* Include technical indicators (RSI, MACD, Moving Average)
* Use time-series cross-validation
* Predict multi-day future prices
* Deploy as stock prediction dashboard

---

## Conclusion

This project demonstrates the use of Machine Learning for financial forecasting. Historical stock market data was used to train regression models capable of predicting future closing prices.

Both models achieved excellent performance, with Linear Regression slightly outperforming Random Forest. The results indicate that machine learning can be effective for short-term stock price prediction when strong feature correlations exist.
