# Trader Performance vs Market Sentiment  

## Introduction
This project explores the relationship between Bitcoin market sentiment (Fear / Greed)
and trader behavior on the Hyperliquid platform. The motivation behind this analysis
is to understand whether trader performance and decision-making patterns change
under different market sentiment conditions.

Rather than building complex models, the focus of this assignment is on clean data
processing, clear analysis, and practical insights.

## Objective
- Examine how trader performance (PnL, win rate) varies during Fear vs Greed periods.
- Study changes in trader behavior such as trade frequency and position sizing.
- Segment traders based on observable behavior.
- Translate findings into simple, actionable trading guidelines.

## Data Description
Two datasets were used:

1. **Bitcoin Fear & Greed Index**  
   - Provides daily market sentiment labels (Fear / Greed).

2. **Hyperliquid Historical Trader Data**  
   - Trade-level data including account, execution price, trade size, timestamp,
     and realized PnL.

## Approach & Methodology

### Data Preparation
- Loaded both datasets using pandas.
- Checked for missing values and duplicates.
- Converted trade timestamps into daily dates to align with sentiment data.
- Merged trader-level metrics with daily market sentiment.

### Feature Engineering
Daily metrics were created at the trader level:
- Daily PnL
- Win rate
- Average trade size
- Number of trades per day

### Analysis
- Compared trader performance across Fear and Greed periods.
- Analyzed behavioral changes in trading activity based on sentiment.
- Traders were segmented into:
  - High vs Low trade size traders
  - Frequent vs Infrequent traders

## Key Insights
- Traders generally achieve higher average daily PnL during Greed periods.
- Trade frequency tends to increase when market sentiment shifts to Greed,
  indicating higher risk appetite.
- Fear periods show deeper negative PnL outcomes, highlighting increased downside risk.

## Strategy Takeaways
Based on the analysis, the following practical rules of thumb emerge:
1. During Fear periods, reducing trade size and leverage can help limit drawdowns.
2. During Greed periods, increased trading activity can be effective when paired
   with disciplined risk management.

## Project Structure
- `DS_Assesment.ipynb` – Main analysis notebook
- `README.md` – Project overview and methodology

## How to Run
1. Install required dependencies:
   pip install pandas numpy matplotlib seaborn
2. Open the notebook:
   jupyter notebook DS_Assesment.ipynb
3. Run the notebook cells sequentially.


