# Quantitative_Trading_with_AI
Some quantitative method and AI Algorithms used in trading.

## Trading_with_Momentum
### Resample Adjusted Prices
The trading signal you'll develop in this project does not need to be based on daily prices, for instance, you can use month-end prices to perform trading once a month. To do this, you must first resample the daily adjusted closing prices into monthly buckets, and select the last observation of each month.
### Compute Log Returns
Compute log returns ($R_t$) from prices ($P_t$) as your primary momentum indicator:
$$R_t = log_e(P_t) - log_e(P_{t-1})$$
### Shift Returns
Shift the log returns to the previous or future returns in the time series.
### Generate Trading Signal
A trading signal is a sequence of trading actions, or results that can be used to take trading actions. A common form is to produce a "long" and "short" portfolio of stocks on each date (e.g. end of each month, or whatever frequency you desire to trade at). This signal can be interpreted as rebalancing your portfolio on each of those dates, entering long ("buy") and short ("sell") positions as indicated.

Here's a strategy that we will try:

> For each month-end observation period, rank the stocks by previous returns, from the highest to the lowest. Select the top performing stocks for the long portfolio, and the bottom performing stocks for the short portfolio.
### test_normality.ipynb ###

Testing if a Distribution is Normal

#### Boxplot-Whisker Plot, Histogram and QQ-Plot ####

We can visually check if a distribution looks normally distributed. 
1. A box whisker plot lets us check for symmetry around the mean. 
2. A histogram lets us see the overall shape. 
3. A QQ-plot lets us compare our data distribution with a normal distribution (or any other theoretical "ideal" distribution).

#### Testing for Normality ####

##### Shapiro-Wilk #####

##### Kolmogorov-Smirnov #####

