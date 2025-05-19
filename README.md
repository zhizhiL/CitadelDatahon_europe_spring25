# CitadelDatahon_europe_spring25
Citadel | Citadel Securities Women’s Datathon - Europe Challenge

# ⛽Squeezing the Pump: A Threshold-Regime Analysis of U.S. Refinery Utilization and Gasoline Price Dynamics

### 🧠 Project Summary

Retail gasoline prices in the U.S. respond sharply to shifts in refinery utilization, but the nature of this relationship is non-linear and regime-dependent. In this project, we identify and exploit a structural break in this relationship to build an early-warning system for gasoline price spikes and propose a regime-aware trading strategy.

Our core research question:

**Can we identify a structural regime in refinery utilization that reliably predicts gasoline price dynamics—and use it to forecast price spikes or trading opportunities?**

Using public datasets from the U.S. Energy Information Administration and commodity markets, we conduct a threshold-regression analysis and show that above 84.5% refinery utilization, gasoline prices exhibit amplified and reversed sensitivity to supply pressures. This insight underpins both a predictive spike model and a cross-over trading strategy.


### 📊 Key Results

- **Threshold Detected**: A structural break in price sensitivity occurs at 84.5% refinery utilization (via Hansen’s sup-LM test).

- **Predictive Model Performance**:

    Baseline ROC-AUC: 0.69 → Improved ROC-AUC: 0.74 with regime flag.

    Precision@100 improved from 3% → 7%.

- **Trading Strategy**: Regime cross-over strategy (long when stress eases, short when it returns) outperforms single-slope model and avoids major drawdowns.


### 🧪 Methodology

- **Data Sources**:

        Weekly U.S. gasoline prices, refinery utilization, WTI spot prices, and gasoline stock levels (EIA).

        Additional commodities and ETF prices from Alpha Vantage/Yahoo Finance.

-**Statistical Analysis**:

        Sup-LM threshold test to identify non-linearity.

        Rolling-window correlation and regime-wise OLS regression.

        Spike definition using quantiles and logistic classification modeling.

-**Modeling**:

        Regime-augmented logistic classifier for predicting price spikes.

        Cross-over trading logic tested out-of-sample.

-**Backtesting**:

        Strategy tested using historical data with transitions across stress regimes.
