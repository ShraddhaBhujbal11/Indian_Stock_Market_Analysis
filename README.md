# 📈 Indian Stock Market Analysis and Return Prediction

A machine learning mini-project that analyzes historical Indian stock market data, explores price movements, and predicts the next trading session's stock return using regression models.

## 📌 Project Overview

The objective of this project is to study historical stock price trends, identify market ups and downs, engineer time-series features, and evaluate machine learning models for next-day return prediction.

The project is implemented in **Python using Google Colab**, with an interactive **Streamlit dashboard** for exploring stock data and viewing predictions.

## ✨ Features

- **Data preprocessing:** Upload ZIP, CSV, or Excel files containing historical stock market data.
- **Exploratory Data Analysis (EDA):** Visualize closing prices, daily returns, annual performance, and rolling volatility.
- **Market movement analysis:** Classify daily returns as Up, Down, or Flat.
- **Feature engineering:** Generate lagged returns, moving-average gaps, rolling volatility, intraday price ranges, opening gaps, and volume changes where data is available.
- **Machine learning:** Train and compare regression models for next-session return prediction.
- **Model evaluation:** Evaluate predictions using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and directional accuracy.
- **Feature importance:** Examine which engineered features contribute to Random Forest predictions.
- **Interactive GUI:** Explore the project through a Streamlit dashboard launched from Google Colab.

## 🤖 Machine Learning Models

The project compares three approaches:

| Model | Purpose |
|---|---|
| Zero-Return Baseline | Assumes the next session's return will be 0%. |
| Linear Regression | Models linear relationships between features and returns. |
| Random Forest Regressor | Captures nonlinear relationships in historical market features. |

Models are evaluated using a **chronological 80:20 train-test split** to preserve the time-series order and reduce information leakage from future observations.

## 🛠️ Tech Stack

- **Language:** Python
- **Environment:** Google Colab, Jupyter Notebook
- **Data Processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Interactive Dashboard:** Streamlit
- **Dashboard Access:** LocalTunnel

## 📊 Feature Engineering

The model uses historical information available at time *t* to predict the return for the next trading session.

Examples of engineered features include:

- One-day, two-day, five-day, and ten-day returns
- Closing-price gaps relative to moving averages
- Five-day and twenty-day rolling volatility
- Intraday price range percentage
- Opening gap percentage
- Trading volume changes, when available

The target variable is the next-session close-to-close percentage return:

\[
R_{t+1} = \left(\frac{Close_{t+1}}{Close_t}-1\right)\times100
\]

## 🚀 Getting Started

### Option 1: Run in Google Colab

1. Clone or download this repository.
2. Open `Indian_Stock_Market_Return_Prediction_with_Streamlit.ipynb` in Google Colab.
3. Run the notebook cells in order.
4. Upload your historical stock market dataset when prompted. ZIP archives containing CSV or Excel files are supported.
5. Review the data analysis, feature engineering, model training, and evaluation outputs.
6. Run the Streamlit GUI section.
7. Start the LocalTunnel cell and open the generated URL to access the dashboard.

**Note:** Keep the Colab runtime running while using the dashboard. The LocalTunnel URL is temporary and is not a permanent deployment.


## 📁 Project Structure

```text
Indian-Stock-Market-Return-Prediction/
│
├── Indian_Stock_Market_Return_Prediction_with_Streamlit.ipynb
```

## 📈 Evaluation Metrics

- **MAE:** Measures the average absolute difference between actual and predicted returns.
- **RMSE:** Penalizes larger prediction errors more heavily.
- **Directional Accuracy:** Measures how often the predicted return direction matches the actual direction.

  <img width="959" height="539" alt="Screenshot 2026-10-15 191723" src="https://github.com/user-attachments/assets/bcd2962a-13f0-459d-ae0b-d02a7958bfbb" />

  <img width="503" height="473" alt="Screenshot 2026-10-15 191804" src="https://github.com/user-attachments/assets/de2cc802-cff5-454f-82c6-659bc314439d" />

  <img width="833" height="476" alt="Screenshot 2026-10-15 191814" src="https://github.com/user-attachments/assets/d5343bf5-a91e-4d5b-a06e-8886968b719f" />

  <img width="754" height="445" alt="Screenshot 2026-10-15 192036" src="https://github.com/user-attachments/assets/8564915b-b3af-428f-9a78-71563b6189e3" />

  <img width="509" height="442" alt="Screenshot 2026-10-15 192011" src="https://github.com/user-attachments/assets/83ef2546-27c7-438c-91b7-2a6f2fa4a550" />







## ⚠️ Limitations

- Stock returns are noisy and difficult to predict reliably.
- Historical performance does not guarantee future results.
- The quality of predictions depends on the dataset, available features, and selected time period.
- Historical datasets ending in 2020 cannot provide a current-market forecast without updated data.
- The dataset may have survivorship bias or cover only selected stocks.
- The Streamlit dashboard launched through LocalTunnel is temporary.

## 🔮 Future Improvements

- Add interactive stock and date-range filters.
- Compare additional forecasting approaches.
- Improve model validation using walk-forward evaluation.
- Deploy the dashboard to a persistent hosting platform.
- Add downloadable prediction reports.


## 📄 Disclaimer

This project is intended for educational and research purposes only. It does not provide financial advice or guaranteed investment returns. Predictions should not be used as the sole basis for investment decisions.
