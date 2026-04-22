# trader-sentiment-performance-analysis
Analysis of trader performance and market sentiment to uncover behavioral patterns and build predictive models for profitability.

#  Trader Performance vs Market Sentiment Analysis (Hyperliquid)

---

##  Project Objective

This project analyzes how Bitcoin market sentiment (Fear / Greed) impacts trader behavior and profitability on Hyperliquid.

The goal is to:

* Understand trading behavior under different sentiment regimes
* Identify performance patterns
* Build simple predictive models
* Extract actionable trading insights

---

##  Dataset Description

### 1. Market Sentiment Dataset

* Date
* Classification: Extreme Fear, Fear, Neutral, Greed, Extreme Greed

### 2. Trader Dataset

* Account ID
* Symbol
* Trade size
* Side (BUY/SELL)
* Execution price
* Closed PnL
* Fees
* Timestamp

---

##  Data Preparation

* Loaded both datasets
* Removed missing values and duplicates
* Converted timestamps to date format
* Merged datasets using date-level alignment
* Standardized classification labels

---

##  Feature Engineering

Created key analytical features:

* Daily closed PnL per sentiment
* Win rate per segment
* Trade frequency segmentation (Frequent / Infrequent)
* Position size segmentation (Large / Small)
* Buy vs Sell ratio
* Fee analysis
* Profitability buckets (Low / Medium / High)

---

##  Exploratory Data Analysis (EDA)

* Sentiment vs trader profitability
* Win rate distribution across market conditions
* Trading behavior changes under different sentiments
* Impact of trade size on returns
* Frequency-based trader performance comparison

---

##  Machine Learning Model

* Model used: Random Forest Classifier
* Target variable: Profitability bucket
* Train-test split: 80/20
* SMOTE applied for class imbalance
* Evaluation: Accuracy, Precision, Recall, F1-score

---

##  Model Performance

* Accuracy: ~95%
* Strong performance on majority class
* Improved minority class prediction after SMOTE
* Balanced macro F1-score achieved

---

## 🔍 Key Insights

### 1. Sentiment affects behavior more than profit

Market sentiment strongly influences trading behavior but has very weak direct correlation with profitability.

---

### 2. Frequency vs Profit tradeoff

Frequent traders show more consistent but smaller gains, while infrequent traders show higher but less stable profits.

---

### 3. Position size drives returns

Large position trades generate significantly higher PnL, even though win rates remain similar across sizes.

---

##  Strategy Recommendations

* In **Extreme Greed markets** → focus on execution efficiency, not risk expansion
* In **Fear markets** → reduce position size and avoid aggressive trading
* Frequent traders → focus on consistency-based strategies
* Infrequent traders → focus on high-conviction trades

---

##  Conclusion

Market sentiment alone is not a strong predictor of profitability.
However, it significantly influences trader behavior.

Profitability is mainly driven by:

* Position sizing
* Trading frequency
* Execution strategy

rather than sentiment alone.

---

##  Future Improvements

* Time-series modeling for sentiment impact prediction
* Clustering traders into behavioral archetypes
* Build Streamlit dashboard for interactive insights
* Feature importance analysis for better interpretability
* Try advanced models like XGBoost / LightGBM

---

##  Requirements

```txt id="6n2c1p"
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn
```

---

##  How to Run

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open notebook in Jupyter/Colab
4. Run all cells step-by-step

---

##  Deliverable Summary

This project demonstrates:

* Data cleaning & preprocessing
* Feature engineering
* EDA insights
* Machine learning modeling
* Business interpretation
* Actionable trading strategies
