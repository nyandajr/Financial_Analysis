Apple Stock Data Analysis (2000-2020)
This project analyzes historical stock data for Apple Inc. (AAPL) from the years 2000 to 2020. It explores financial data using various techniques, including calculating returns, resampling data to different frequencies, visualizing time series data, and investigating stylized facts of asset returns.

Table of Contents
Data Acquisition
Calculating Returns
Resampling Data
Time Series Visualization
Outlier Detection
Investigating Stylized Facts
Data Acquisition
The notebook imports stock data for Apple Inc. using the yfinance library. The data spans from 2000-01-01 to 2020-12-31 and includes:

Open
High
Low
Close
Adjusted Close
Volume
The data is saved as aapl_2000_2020.csv.

Calculating Returns
We calculate both simple and logarithmic returns based on the adjusted closing prices:

Simple Return: Percentage change between consecutive days.
Log Return: Logarithmic change between consecutive days.
The data is saved as aapl_2000_2020_with_simple_and_log_returns.csv.

Resampling Data
The notebook resamples the stock data to different frequencies:

Monthly: Taking the last observation of each month.
Weekly: Taking the last observation of each week.
This allows for analysis at different time granularities and helps identify long-term trends.

Time Series Visualization
The notebook provides visualizations of the stock prices and returns using both Matplotlib and Plotly. The following plots are created:

Line Plot of the adjusted closing prices.
Interactive Plot of adjusted closing prices using Plotly.
Outlier Detection
Two methods are used to identify outliers in the data:

Z-Score Method: Outliers with Z-scores greater than 3.
Interquartile Range (IQR) Method: Outliers based on the 1.5 IQR rule.
The outliers are highlighted in the time series plot.

Investigating Stylized Facts
Key stylized facts of asset returns are explored:

Non-Gaussian Distribution of Returns: Identified using histograms and Q-Q plots.
Volatility Clustering: Observed by plotting rolling standard deviation of returns.
Absence of Autocorrelation in Returns: Checked using autocorrelation plots.
Small and Decreasing Autocorrelation in Squared Returns: Autocorrelation in squared returns is analyzed.
Leverage Effect: The relationship between returns and volatility is explored.
Dependencies
The following Python libraries are used:

yfinance
pandas
numpy
matplotlib
plotly
scipy
statsmodels

Usage
To run the notebook, ensure you have the necessary dependencies installed. You can install them using:

bash
Copy code
pip install yfinance pandas numpy matplotlib plotly scipy statsmodels
Open the Jupyter notebook and follow the instructions to reproduce the analysis.

This README provides an overview of the key sections of the notebook, guiding users through the analysis process.
