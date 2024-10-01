Project Overview: Risk-Optimized Momentum Strategy for Stock Portfolio Allocation
This project involves a comprehensive analysis of stock data across Energy, Consumer Staples, and Financial sectors to develop an optimized portfolio investment strategy using a momentum trading approach and non-linear optimization techniques. Here’s a breakdown of the process to help prepare for a financial data analyst interview:

1. Data Collection and Stock Selection:
Objective: Select 30 stocks from Energy, Consumer, and Financial sectors and collect historical stock data from 2017 to 2022.
Data Source: Yahoo Finance API (or similar).
Key Consideration: Stock selection from diverse sectors allows for risk diversification and sector-specific insights.
2. Data Cleaning:
Handling Outliers and Missing Data:
Approach: Outliers in stock prices were identified but left unhandled due to limited financial knowledge.
Sector-specific Verdict:
Consumer Staples had lower price volatility (less variation in medians), making it more stable.
Energy and Financials showed more significant fluctuations.
Summary of Price Variation:
Energy Sector: More volatility due to oil price fluctuations and market events like the 2020 COVID-19 pandemic.
Consumer Staples Sector: Displayed stability with steady growth, which is typical due to the constant demand for essential products.
Financial Sector: Showed volatility during 2020 but had strong post-pandemic recovery, with certain stocks showing significant growth due to rising interest rates and economic outlook.
3. Time Series Analysis:
Sector-wise Analysis:
Energy Sector: Significant volatility, particularly around 2020. Recovery was uneven, with some stocks (e.g., PSX, VLO) showing stronger performance than others (e.g., XOM).
Consumer Staples: Displayed steady growth, with stable demand during economic downturns.
Financials Sector: Showed sharp fluctuations during the pandemic but recovered post-2020. A sector-wide decline in late 2022 may signal market concerns about future downturns.
4. Momentum Trading Strategy:
Objective: Implement a simple momentum strategy based on moving averages.
Methodology:
Calculate 8-day and 21-day moving averages.
Generate buy (when 8-day MA crosses above 21-day MA) and sell (when 8-day MA crosses below 21-day MA) signals.
Log returns were calculated to assess strategy performance.
Results:
Energy Sector: WMB, MPC, and PSX showed the highest momentum-driven returns.
Consumer Staples: COST, DLTR, and LW performed best.
Financials: AXP, BX, and AIG led in returns.
5. Portfolio Optimization:
Step 1: Calculate the daily returns and covariance matrix for the selected stocks.

Step 2: Develop a non-linear optimization model using Pyomo to maximize returns while controlling risk.

Objective Function: Maximize weighted returns of the portfolio.
Constraints:
The sum of stock weights must equal 1.
Set bounds for the acceptable risk levels.
Covariance Matrix: Used to measure risk (portfolio variance), and each iteration of the model adjusts stock allocations based on the risk levels.

6. Running the Optimization Model:
Approach: Iteratively adjust the risk constraint and calculate the optimal stock allocation for each risk level using the IPOPT solver.
Output:
Proportions of stocks allocated at each risk level.
The model calculates the expected return based on the stock weightings and risk.
7. Parameter Analysis:
Active Stocks Selection: Analyze portfolio compositions where exactly three stocks have significant allocations (above a 25% threshold). This helps in identifying a concentrated, high-impact portfolio for each risk level.
8. Efficient Frontier Creation:
Efficient Frontier: Plots different portfolio compositions against risk to visually represent the trade-off between risk and return.
Key Insight: Helps to identify optimal portfolios for investors with varying risk appetites.
Conclusion:
This project showcases a complete financial analysis workflow, involving sector-specific insights, time series analysis, a momentum trading strategy, and portfolio optimization. The optimization model helps create an efficient frontier that assists in making informed investment decisions based on risk and return preferences.

This methodology provides a solid foundation for discussing quantitative methods, risk management, and portfolio optimization in your interview. It reflects skills in data wrangling, financial analysis, machine learning, and Python-based financial modeling.
