# README prompt — documentation only, no code

# PASTE THIS PROMPT INTO CLAUDE:
#
# "I need help writing a project description for my data science lab.
# **Important Rule:** Do NOT generate any Python code for me.
#
# **What I did in this lab:**
# * Diagnosed a junior analyst's normal-distribution VaR model: at 99% it
#   understated historical VaR by 12.7% ($40,393 on the
#   portfolio)
# * Computed VaR and Expected Shortfall under historical, normal and
#   Student-t (fitted df = 4.58) methods
# * Cut Monte Carlo standard error by 1.26x with antithetic variates
# * Used a risk_metrics.py module (calculate_var, calculate_es, mc_var)
#   and ran its self-tests
# * Had an AI write a VaR backtest, revised my prompt once, and checked it
#   against my own count: normal 99% VaR breached on 1.71% of days
#
# **Please write a README.md entry including:**
# 1. Project Title: Diagnosing a Flawed Risk Model — VaR, Expected Shortfall & Monte Carlo
# 2. Objective: one sentence
# 3. Methodology: Bullet points of technical steps
# 4. Key Findings: Summary of results
# Write it plainly, in the first person. No words like 'robust',
# 'comprehensive' or 'leverage'. Use only the numbers I gave you."
