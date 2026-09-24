# CAPM Model

For every stock *i*:

$$
R_i - R_f = \alpha_i + \beta_i\,(R_m - R_f) + \varepsilon_i
$$

| Symbol | Meaning | Data used |
|---|---|---|
| $R_i$ | return of stock *i* | yfinance adjusted close |
| $R_m$ | return of the market | **SPY** (S&P 500 ETF) |
| $R_f$ | risk-free rate | **^IRX** (13-week T-bill yield) |
| $\beta_i$ | change in the stock's excess return per 1 unit of market excess return | estimated |
| $\alpha_i$ | average daily excess return not explained by the market | estimated |


# Excess Returns

In the CAPM, we do not use raw returns directly. Instead, we use **excess returns**, which measure how much a return exceeds the risk-free rate.

Let:

- $R_i$ = return of stock $i$
- $R_m$ = return of the market (SPY)
- $R_f$ = risk-free rate (^IRX)

We define:

$$
y = R_i - R_f
$$

This is the **stock's excess return**: the return of stock $i$ above the risk-free rate.

$$
x = R_m - R_f
$$

This is the **market's excess return**: the return of the market above the risk-free rate.

So in the CAPM:

$$
y = \alpha_i + \beta_i x + \varepsilon_i
$$

where:

- $y$ is the stock excess return,
- $x$ is the market excess return,
- $\alpha_i$ is the intercept,
- $\beta_i$ is the slope,
- $\varepsilon_i$ is the error term.
---


## Beta ($\beta_i$)

### What beta means

Beta measures the sensitivity of a stock's excess return to the market's excess return.

It answers:

> If the market excess return changes by 1%, how much does the stock's excess return change on average?


### Interpretation of beta

| Beta value | Interpretation |
|---|---|
| $\beta < 0$ | Stock tends to move opposite to the market |
| $\beta = 0$ | No systematic market exposure |
| $0 < \beta < 1$ | Defensive stock; less volatile than the market |
| $\beta = 1$ | Same systematic risk as the market |
| $\beta > 1$ | Aggressive stock; more volatile than the market |
| Example: $\beta = 1.2$ | A 1% market excess return is associated with a 1.2% stock excess return on average |

---

## Alpha ($\alpha_i$)

### What alpha means

Alpha is the average daily excess return not explained by market exposure.

It captures whether the stock outperformed or underperformed after adjusting for market risk.


### Interpretation of alpha

| Alpha value | Interpretation |
|---|---|
| $\alpha > 0$, significant | Outperformance after market risk adjustment |
| $\alpha < 0$, significant | Underperformance after market risk adjustment |
| $\alpha \approx 0$ or not significant | No evidence of abnormal performance |
| Annualized alpha | $\alpha_{\text{annual}} \approx \alpha_{\text{daily}} \times 252$ |

A significant positive alpha suggests the stock earned more than its market risk would predict.  
A significant negative alpha suggests it earned less than its market risk would predict.