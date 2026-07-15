# First Finance Real Data Project

This project is my first ever finance project. 
This is only a small real data project to get my hand dirty with messy real market data. 


The project is intended to calculate whether stock's momentum can determine its moving
direction in the future with spearman correlation. 

## Terminologies used in the report:

1. Sharpe ratio = Z-score = Return / Variance

Sharpe tells you how much of variance you deviate from the actual mean, and how much 
you can earn per unit of risk. 
If the variance is small(small risk) and return is high than you certainly have a lot of benefit. 

2. IC = Spearman(signal, next_return)
   ```
   Signal = (RR(t - 12) -> RR(t - 2) )/ 12
   ```
   IC determines if there is a spearman correlation between these two quantities. 
   If the correlation is positive -> we know the past momentum influence current
   price movements
   If the correlation is negative -> we see a short term selling signal. 


## Results

The results confirmed that there is no significant correlation between momentum in the last 12 months with the next return for next month under hypothesis testing. 

The Figure confirmed that the tail and the statistic are positively skewed, determining positive momentum often resonates with positive next month return. However
the signal is not strong enough

<img width="538" height="407" alt="Screenshot 2026-07-15 at 22 19 01" src="https://github.com/user-attachments/assets/927c3cab-626b-425a-be0e-5e9d354e415c" />

| Version | Mean IC | IR | t-stat | % positive |
|---|---|---|---|---|
| RAW | +0.0182 | +0.095 | +1.24 | 58.3% |
| SECTOR-NEUT | +0.0068 | +0.046 | +0.59 | 55.4% |


