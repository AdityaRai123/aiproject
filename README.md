# Stock Price Prediction - ML Model

A complete machine learning and data science pipeline designed to predict next-day stock price movements (Up/Down) using historical trading data and technical analysis indicators.

---

## 🎓 Student Profile
- **Name:** Aditya Rai
- **Registration Number:** 23BIT0019
- **Institution:** Vellore Institute of Technology (VIT), Vellore
- **Department/Program:** Information Technology (IT)

---

## 📁 Project Structure
The repository is structured as follows:
- [Untitled0.ipynb](file:///d:/aiproject/Untitled0.ipynb) - Jupyter Notebook containing the Stock Price Prediction machine learning pipeline, data analysis, models training, evaluation, and visualizations.
- `archive.zip` - Dataset archive containing historical stock market data used for training the prediction models.

---

## 📈 Stock Price Prediction Machine Learning Model
This project builds an end-to-end predictive pipeline in Python (`Untitled0.ipynb`) to forecast whether a stock's closing price will rise or fall on the next trading day.

### Pipeline Steps:
1. **Data Loading & Preprocessing:** Handles file uploads (such as Kaggle NIFTY50 datasets), cleans headers, standardizes columns, sorts by date, and handles missing records.
2. **Exploratory Data Analysis (EDA):** Plots close prices against volumes and generates the distribution of daily returns.
3. **Technical Indicators Extraction:** Calculates and incorporates technical indicators using the `ta` library:
   - **Trend Indicators:** MACD (Moving Average Convergence Divergence), MACD Signal, MACD Difference, SMA (Simple Moving Average - 20, 50 days), EMA (Exponential Moving Average - 12, 26 days), ADX (Average Directional Index).
   - **Momentum Indicators:** RSI (Relative Strength Index - 14 days).
   - **Volatility Indicators:** Bollinger Bands (Upper, Middle, Lower), ATR (Average True Range).
   - **Volume Indicators:** OBV (On-Balance Volume).
4. **Feature Engineering:** Adds shifts/lags (1, 2, 3, 5 days) for Close price, Volume, and RSI; computes rolling means and standard deviations.
5. **Model Training & Evaluation:**
   Evaluates six different Machine Learning algorithms:
   - Logistic Regression
   - Random Forest Classifier
   - Gradient Boosting Classifier
   - XGBoost Classifier
   - Support Vector Machine (SVM)
   - K-Nearest Neighbors (KNN)
6. **Ensemble Majority Voting:** Combines predictions from all models to construct a robust consensus prediction with calculated confidence levels.
7. **Performance Analytics:** Produces detailed classification reports, confusion matrices, correlation heatmaps, and a horizontal bar chart summarizing accuracies/F1-scores.

---

## 🛠️ Tech Stack & Dependencies
The machine learning pipeline is built with:
- **Language:** Python 3
- **Data Wrangling:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn`, `xgboost`
- **Technical Indicators:** `ta` (Technical Analysis library)
- **Visualizations:** `matplotlib`, `seaborn`

---

## 🚀 How to Run the Project

1. **Ensure Python 3 is installed along with the required libraries:**
   ```bash
   pip install pandas numpy scikit-learn xgboost ta matplotlib seaborn
   ```
2. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook Untitled0.ipynb
   ```
3. **Upload Dataset:**
   When prompted, upload a stock CSV dataset (e.g. from the [Kaggle Nifty50 Dataset](https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data)).
4. **Run Cells:**
   Execute the cells sequentially to observe data loading, preprocessing, indicators generation, training, performance analysis, and next-day price forecast visualization.
