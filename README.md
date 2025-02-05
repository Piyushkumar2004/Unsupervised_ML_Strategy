# Unsupervised Learning-Based Trading Strategy

This repository contains a Python script that implements an unsupervised learning-based trading strategy using technical analysis and financial indicators. The strategy optimizes portfolio weights based on historical data and compares it with a benchmark (S&P 500).

## Table of Contents

- [Overview](#overview)
- [Technical Indicators Used](#technical-indicators-used)
- [Steps and Calculations](#steps-and-calculations)
- [Clustering and Strategy](#clustering-and-strategy)
- [Comparison with Benchmark](#comparison-with-benchmark)
- [Dependencies](#dependencies)
- [Usage](#usage)

## Overview

This project applies machine learning techniques to financial data for constructing a trading strategy. It starts with downloading historical stock data for S&P 500 companies and technical indicator RSI.  K-Means clustering is used to identify groups of stocks.

The final strategy is compared with a buy-and-hold strategy for the S&P 500.

## Technical Indicators Used

1. **RSI (Relative Strength Index)** - Indicates Momentum of the stocks.


## Steps and Calculations

1. **Download Stock Data**: The stock data for the S&P 500 constituents is downloaded from Yahoo Finance for the last 8 years.
2. **Calculate Technical Indicators**: RSI is computed for each stock using the `pandas-ta` library.
3. **Return Calculation**: each day returns are calculated.

## Clustering and Strategy

### Unsupervised Learning

1. **K-Means Clustering**: Unsupervised learning is applied to the dataset to cluster stocks into 4 groups based on technical indicators and returns. This helps identify different behaviors in stock groups.
2. **Cluster Visualization**: The clusters are visualized using scatter plots where different clusters are represented by different colors.

## Comparison with Benchmark

The cumulative return of the optimized strategy is compared with the cumulative return of a buy-and-hold S&P 500 strategy (`SPY`). This comparison is plotted and displayed.

## Dependencies

- `yfinance`: For downloading historical stock data.
- `pandas-ta`: To compute technical indicators like RSI, MACD, Bollinger Bands, ATR.
- `scikit-learn`: For clustering using K-Means.
- `pandas`: Data manipulation and resampling.
- `matplotlib`: Plotting results.

## Results of the trading stratergies
![Results of Trading Strategy](./Results.png)


