# Time Series Analysis using Python

## Overview

This repository contains code and examples for performing time series analysis using Python. Time series analysis involves analyzing and finding patterns in datasets that are collected over time intervals. Examples of time series data include stock prices, monthly sales figures, daily weather data, and more. The focus of this analysis is on stock price data for Apple Inc. (`AAPL`), showcasing various techniques for visualizing and interpreting time series data.

## Key Features

### 1. Data Collection
- **API Used:** `yfinance`
- **Data Source:** Apple Inc. stock prices over the past 720 days.
- **Data Retrieved:** Open, High, Low, Close, Adjusted Close, and Volume.

### 2. Visualizations
- **Line Plot:** Displays the trends in the close prices over time.
- **Candlestick Chart:** Visualizes open, high, low, and close prices, ideal for financial data analysis.
- **Bar Plot:** Highlights the overall trend in close prices over a longer time period.
- **Custom Date Range Analysis:** Allows for focused analysis on specific date intervals.
- **Interactive Candlestick Chart with Buttons and Slider:** Enhances the user experience by enabling manual selection of time intervals.

## How to Use

### 1. Prerequisites
- Python 3.x
- Required Libraries: `pandas`, `yfinance`, `plotly`

### 2. Running the Analysis
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/time-series-analysis.git
   cd time-series-analysis
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas yfinance plotly
   ```

3. **Run the Jupyter Notebook or Python script:**
   Open the notebook in Jupyter or run the script to see the analysis and visualizations.

### 3. Examples
- **Line Plot:**
  ```python
  figure = px.line(data, x = data.index, y = "Close", title = "Time Series Analysis (Line Plot)")
  figure.show()
  ```

- **Candlestick Chart:**
  ```python
  figure = go.Figure(data=[go.Candlestick(x = data.index, open = data["Open"], high = data["High"], low = data["Low"], close = data["Close"])])
  figure.update_layout(title = "Time Series Analysis (Candlestick Chart)", xaxis_rangeslider_visible = False)
  figure.show()
  ```

- **Interactive Candlestick with Slider:**
  ```python
  figure.update_xaxes(
      rangeslider_visible = True,
      rangeselector = dict(
          buttons = list([
              dict(count = 1, label = "1m", step = "month", stepmode = "backward"),
              dict(count = 6, label = "6m", step = "month", stepmode = "backward"),
              dict(count = 1, label = "YTD", step = "year", stepmode = "todate"),
              dict(count = 1, label = "1y", step = "year", stepmode = "backward"),
              dict(step = "all")
          ])
      )
  )
  figure.show()
  ```

## Summary

Time series analysis is a powerful tool for understanding trends and making predictions based on historical data. This repository demonstrates how to perform basic time series analysis using Python, with a focus on financial data. The examples provided offer a foundation for exploring more complex analyses and applying these techniques to various domains.

Feel free to explore the code, adapt it to your needs, and contribute to the repository with improvements or new features. Happy analyzing!

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

For any questions or feedback, please contact me at [your email address] or connect with me on [LinkedIn](your-linkedin-profile).
