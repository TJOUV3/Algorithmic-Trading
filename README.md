# Algorithmic-Trading

Algorithmic Trading Project: Predicting Daily Returns of Bitcoin Using a Multilinear Approach

This algorithmic trading project aims to predict the daily returns of financial assets using a multilinear regression model. We have chosen Bitcoin (BTC) as our primary asset due to its high volatility—an essential characteristic for maximizing profit potential in our strategy.

Our explanatory variables were carefully selected to capture three complementary dimensions:
  1.	Price-Driven Indicators: These include technical indicators based on historical prices, such as the previous day's After Close movement, the Relative Strength Index     (RSI), and moving averages like the MACD (Moving Average Convergence Divergence).
  2.	Market Sentiment: We analyzed data from Reddit and Google Trends to assess overall investor sentiment using Natural Language Processing (NLP) techniques.
  3.	Macroeconomic Indicators: We incorporated the DXY index, which measures the relative strength of the US dollar—a significant factor influencing both traditional         financial markets and crypto-assets.

Each variable was statistically tested to validate its significance and contribution to the model. We then calibrated the regression coefficients through backtesting on historical data, splitting our dataset into training and testing sets.

Trading Strategy

Our strategy was designed to be both simple and effective, with a clear decision rule to ensure profitability after transaction costs:
  •	Each day, the model estimated the expected return of Bitcoin.
  •	If the predicted return was positive and exceeded transaction costs (10 bps), we entered a long position (buy).
  •	If the predicted return was negative and its absolute value exceeded transaction costs (10 bps), we took a short position (sell).
  •	If the predicted return was within ±10 bps, no trade was executed to avoid unprofitable transactions.
  •	All positions were closed at the end of the day to mitigate overnight market risks.
  
This refinement ensured that only trades with a positive expected net return were executed, enhancing the overall efficiency and profitability of the strategy.

Results and Performance

Our model demonstrated strong performance, achieving:
  •	A success rate above 50%, outperforming a simple buy-and-hold strategy.
  •	A higher net profitability than a long-only strategy (buying every day without prediction).
  •	Performance exceeding that of a randomized daily long/short strategy, proving the predictive power of our model.
