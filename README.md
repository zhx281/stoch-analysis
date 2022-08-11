# stoch-analysis

Analysis for stock using stochastic rsi strategy

---

## The [base strategy](./jupyter/Stoch-Analysis-01.ipynb):

#### Part 1: Buying Requirements

1. The close price must be above the 200 sma (Simple Moving Average)
2. The Stochastic RSI K must below certain percentage (n%)
3. Placing a n % limit buy order the next period with an order limit of n periods

#### Part 2: Selling Requirements

1. The trailing stop is equal to n% of the limit buy percentage
2. Otherwise sell at trailing stop

---

## [Buy Low Strategy](./jupyter/Stoch-Analysis-02.ipynb)

This strategy taking the newest low in n periods as a trigger with Stochastic RSI oversold.

#### Part 1: Buying Requirements

1. Stochastic RSI K and D line must be in the oversold area (> n%)
2. Stochastic RSI K line is below D line
3. The stock made an n period low during this period of Stochastic RSI oversold
4. Buy at close or at n% above new low

#### Part 2: Selling Requirements

1. Set Trailling stop to n% of high prices
2. Set sell limit to a static % gain of buy price

---

## [Buy Low With Volume Strategy](./jupyter/Stoch-Analysis-03.ipynb)

This strategy taking the newest low in n periods as a trigger with Stochastic RSI oversold, then using the volume as a filter.

#### Part 1: Buying Requirements

1. Stochastic RSI K and D line must be in the oversold area (> n%)
2. Stochastic RSI K line is below D line
3. The stock made an n period low during this period of Stochastic RSI oversold
4. Then check if the volume is above the volume simple moving avreage within a n periods
5. If above then Buy at close or at n% above new low

#### Part 2: Selling Requirements

1. Set Trailling stop to n% of high prices
2. Set sell limit to a static n% gain of buy price or trailling of high prices

---
