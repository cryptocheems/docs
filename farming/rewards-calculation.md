# Rewards Calculation

{% hint style="warning" %}
This page is unfinished
{% endhint %}

The amount of Cheemscoin you will receive is in proportion to the number of LP tokens you deposited multiplied by the multiplier you chose compared to the amount of LP tokens other people deposited multiplied by the multipliers they chose. Essentially, you will get more Cheemscoin if you deposit more and/or other people deposit less.

After you make a deposit, you can "harvest" your Cheemscoin rewards whenever you want but you cannot withdraw your LP tokens until the lock duration has passed. Note that after the lock duration has passed the multiplier will be set to 1x. If you want a higher multiplier, you must withdraw and redeposit.

The APR that's shown on the website should only be used as a rough estimate of the reward rate if it was extrapolated over a year. Note that in reality the rewards will only be available until \[end date] so your deposit will not generate any more rewards after the end date, even if it is locked.

The 24 hour yield is calculated by the equation below, where _CheemsPrice_ is the value of Cheemscoin in dollars, _Cheems24hr_ is the amount of Cheemscoin the pool (everyone's deposits for the specific LP token) will receive over the next 24 hours, _LPtokenPrice_ is the value of the specific LP token in dollars, and _PoolLPtokenBalance_ is the amount of the specific LP token in total deposited into the pool.

$$
\frac{100 \times CheemsPrice \times Cheems 24hr}{LPtokenPrice \times PoolLPtokenBalance}
$$

Let's say there are currently 4 LP tokens deposited in the pool and the pool receives 40 Cheemscoin per day...
