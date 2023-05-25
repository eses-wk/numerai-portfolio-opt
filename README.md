# Numerai Portfolio Optimizer
<a target="_blank" href="https://colab.research.google.com/github/eses-wk/numerai-portfolio-opt/blob/main/Portfolio_optimizer.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

# Why use a portfolio optimizer?
Are you:
- Testing 20+ live models but don't know how to best allocate your NMR stakes?
- Suffered from BIG burn in 1-2 over-staked models, while all the other models were doing fine?
- Not sure what Numerai corr/ True Contribution metric multiplier (0,1x,2x) to pick for your models?

**Portfolio Optimizer is here to help!**

Portfolio Optimization originates from Harry Markowitz's Model Portfolio Theory (1952). The objective is to find the **optimal weights of a set of assets (Numerai models)** to: 
1. **Maximize the risk-adjusted return** (Sharpe ratio) 
    - Higher Sharpe ratio => better model (return is yummy😋)
2. **Minimize the volatility** (standard deviation)
    - Lower standard deviation => better model (burn is painful...)

<img src="assets/example_ef.png" alt="Example Efficient Frontier" />

# How does it work?
- Step 1: Extract model performance metrics (Numerai Correlation / True Contribution) using Numerai API (or compute model performance from validation set)
- Step 2: Use the optimizer to find the optimal weights of the models
- Step 3: Review and select your optimal portfolio mix for model staking

# Status - Work in progress
- Currently only support portfolio mix with fixed **1x** Correlation Multiplier
- WIP: add support for variable Correlation Multiplier (corr + TC with different multiplier)


# Reference 
- [bor's R example of a Numerai portfolio optimizer](https://github.com/BorisVSchmid/vladthestaker)
- [Medium post on Efficient Frontier](https://towardsdatascience.com/efficient-frontier-portfolio-optimisation-in-python-e7844051e7f)
- [Medium post about Model Portfolio Theory](https://medium.com/python-data/effient-frontier-in-python-34b0c3043314)
- [Numerai's official docs on model staking](https://docs.numer.ai/numerai-tournament/staking)


# Disclaimer
- The information and code provided in this GitHub repository are for educational and entertainment purposes only. Any information in this repository is not intended to be used as financial advice, and the owner, contributor of this repository are not financial advisors.
- The owner and contributor of this repository do not guarantee the accuracy or completeness of the information provided, and they are not responsible for any losses or damages that may arise from the use of this information or code. 
