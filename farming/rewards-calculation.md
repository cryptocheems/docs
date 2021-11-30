# Rewards Calculation

The amount of Cheemscoin you will receive is in proportion to the number of LP tokens you deposited multiplied by the multiplier you chose compared to the amount of LP tokens other people deposited multiplied by the multipliers they chose. Essentially, you will get more Cheemscoin if you deposit more and/or other people deposit less.

After you make a deposit, you can "harvest" your Cheemscoin rewards whenever you want but you cannot withdraw your LP tokens until the lock duration has passed. Note that after the lock duration has passed the multiplier will be set to 1x. If you want a higher multiplier, you must withdraw and redeposit.

The APR that's shown on the website should only be used as a rough estimate of the reward rate if it was extrapolated over a year. Note that in reality the rewards will only be available until \[end date] so your deposit will not generate any more rewards after the end date, even if it is locked.

The 24 hour yield shown on the website is calculated by the equation below, where _CheemsPrice_ is the value of Cheemscoin in dollars, _Cheems24hr_ is the amount of Cheemscoin the pool (everyone's deposits for the specific LP token) will receive over the next 24 hours, _LPtokenPrice_ is the value of the specific LP token in dollars, and _PoolLPtokenBalance_ is the amount of the specific LP token in total deposited into the pool.

$$
\frac{100 \times CheemsPrice \times Cheems 24hr}{LPtokenPrice \times PoolLPtokenBalance}
$$

The 1 year yield (APR) is simply calculated by multiplying the 24 hour yield by 365.

This method of calculating APR/yield is generally fine for small deposits or when a large amount has already been deposited because your deposit won't affect the rate much; however, when the amount already in the pool is small or you are depositing a large amount, the real yield will be lower than displayed. For example, let's say there are currently 4 LP tokens deposited in the pool, each LP token is $1, the pool receives 40 Cheemscoin per day, and Cheemscoin is at $0.05. The APR that will be shown is 50%. Then you deposit 1 LP token. There's now 5 LP tokens in the pool so the new APR is 40%, lower than what was shown before you deposited.

Besides that, there are many other factors that can positively or negatively affect your real return on investment (ROI).

### Positive Factors (increase your ROI)

* The price of Cheemscoin increasing
* The price of the LP token increasing (this will decrease the displayed APR but it means you have an asset of a higher value now)
* People withdrawing their deposits (leaving you with a higher portion of the rewards)
* Compounding your investment (using your harvested Cheemscoin to buy more LP tokens and depositing them. This is like compound interest)

### Negative Factors (decrease your ROI)

* The price of Cheemscoin or the LP token decreasing
* People depositing more into your pool
* Slippage from selling a large amount of Cheemscoin with little liquidity
