# Trader Performance vs Market Sentiment - Report

## Objective

In this project, I tried to understand how market sentiment (Fear and Greed) affects trader performance on Hyperliquid. The main goal was to find patterns in trading behavior and see whether sentiment has any impact on profitability.

---

## What I did

First, I loaded both datasets (market sentiment and trader data). Then I cleaned the data by handling missing values, removing duplicates, and converting timestamps into daily format so that both datasets could be merged properly.

After that, I merged the datasets on the date column.

Then I created some important features like:
- Win rate
- Trade frequency (frequent vs infrequent traders)
- Position size (large vs small trades)
- Daily closed PnL
- Buy/Sell behavior
- Fees

After feature creation, I performed exploratory data analysis to understand patterns between sentiment and trader behavior.

I also trained a simple Random Forest model to predict profitability buckets.

---

## Key Insights

### 1. Sentiment does not strongly predict profit
Market sentiment like Fear or Greed does not directly control trader profitability. The correlation between sentiment and PnL is very weak.

---

### 2. Trader behavior changes with sentiment
Even though profit is not strongly affected, traders behave differently in different sentiment conditions. For example, in Greed markets, trading activity changes compared to Fear markets.

---

### 3. Frequent vs Infrequent traders
Frequent traders are more consistent but earn smaller profits. Infrequent traders take fewer trades but sometimes earn higher profits.

---

### 4. Position size matters
Large position trades generate much higher profit compared to small trades, even though win rates are almost similar.

---

## Model

I used a Random Forest model to predict profitability buckets (Low, Medium, High). The model performed well with around 95% accuracy. SMOTE was used to handle class imbalance.

---

## Conclusion

Overall, sentiment alone is not enough to predict profitability. Trader behavior, position size, and trade frequency play a bigger role in determining success.

---

## Future Improvements

In the future, I would like to:
- Try time-series models for better prediction
- Cluster traders into different behavioral groups
- Build a dashboard to visualize insights
- Try more advanced models like XGBoost
