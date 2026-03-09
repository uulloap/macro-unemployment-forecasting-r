# Regional Unemployment Forecasting & Structural Breakpoint Analysis

![R](https://img.shields.io/badge/Language-R-blue.svg)
![Topic](https://img.shields.io/badge/Domain-Macroeconomics-green.svg)
![Method](https://img.shields.io/badge/Method-Time_Series_Forecasting-orange.svg)

## 📌 Project Overview
This project analyzes and forecasts regional unemployment rates across the US using 20+ years of monthly data. The primary objective was to evaluate model performance during structural economic shifts, specifically the 2020 pandemic shock, by comparing traditional statistical methods with neural network approaches.

## 📊 Business Problem
Standard forecasting models often fail when faced with "structural breaks"—sudden changes in the underlying data-generating process. This project identifies those breaks to create more accurate "New Normal" forecasts for the 2021-2024 period.

## 🛠️ Technical Stack
- **Languages:** R
- **Libraries:** `fable`, `tsibble`, `forecast`, `strucchange`, `ggplot2`, `patchwork`
- **Models:** ARIMA, ETS (Exponential Smoothing), NNETAR (Neural Network Autoregression)
- **Diagnostics:** Augmented Dickey-Fuller (ADF) Test, Ljung-Box Test, Residual ACF Plots

## 🚀 Key Features
- **Breakpoint Detection:** Automated identification of structural shifts to segment training data.
- **Model Benchmarking:** Comparative analysis of ARIMA vs. Neural Networks.
- **Out-of-Sample Validation:** Models were trained on pre-2021 data and tested against 3+ years of actual post-pandemic recovery data.
- **Automated Pipeline:** Full R Markdown implementation from data cleaning to visualization.

## 📈 Key Insights & Results
- **Resilience:** The **NNETAR** (Neural Network) model showed superior performance in capturing the non-linear "V-shaped" recovery in the West and South regions.
- **Accuracy:** Implementing breakpoints reduced the Root Mean Square Error (RMSE) by **[X]%** compared to models that ignored the 2020 structural shift.
- **Diagnostics:** All final models passed the Ljung-Box test, confirming that residuals behaved as white noise.

## 📂 Project Structure
```text
├── data/               # Regional Excel datasets (Midwest, Northeast, South, West)
├── notebooks/          # .Rmd file containing the full analytical pipeline
├── output/             # Forecast plots, Accuracy tables, and Residual diagnostics
├── Time_Series_Project.html # Polished final report
└── README.md           # Project documentation
