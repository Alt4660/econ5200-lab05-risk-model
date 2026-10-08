# Diagnosing a Flawed Risk Model: VaR, Expected Shortfall & Monte Carlo

## Objective

I diagnosed a junior analyst's normal-distribution Value at Risk model, showed that it understates tail risk, and compared it with better methods.

## Methodology

- Ran the analyst's normal VaR model on 2,520 simulated daily returns for a $10M portfolio and checked the descriptive statistics (excess kurtosis 4.28).
- Plotted the returns against the fitted normal curve to see where the normal assumption fails in the tails.
- Compared normal and historical VaR at 95% and 99%.
- Computed VaR and Expected Shortfall under historical, normal and Student-t methods (fitted df = 4.58).
- Priced a European call option with naive Monte Carlo and with antithetic variates, and compared the standard errors.
- Read and ran `risk_metrics.py` (`calculate_var`, `calculate_es`, `mc_var`) and its self-tests.
- Had an AI write a VaR backtest, revised my prompt once to fix the VaR sign convention, and checked the function against my own count.

## Key Findings

- At 99%, the analyst's normal VaR understated historical VaR by 12.7%, which is $40,393 on the portfolio.
- Antithetic variates cut the Monte Carlo standard error by 1.26x using the same number of paths.
- When I backtested the normal 99% VaR, it was breached on 1.71% of days, not the 1% it promises. The historical 99% VaR was breached on 1.03% of days.
- A model can run without errors and still be wrong if its distributional assumption does not match the data.

## Files

- `Copy_of_lab_ch05_diagnostic.ipynb`: the completed lab notebook
- `risk_metrics.py`: the VaR and Expected Shortfall module
