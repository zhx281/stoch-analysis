# stoch-analysis

Analysis for stock using a stochastic strategy

## The [base strategy](./jupyter/Stoch-Analysis-01.ipynb):

#### Part 1: Buying Requirements

1. The close price must be above the 200 sma (Simple Moving Average)
2. The Stochastic RSI K must below certain percentage (n%)
3. Placing a n % limit buy order the next period with an order limit of n periods

#### Part 2: Selling Requirements

1. The trailing stop is equal to n% of the limit buy percentage
2. Otherwise sell at trailing stop
