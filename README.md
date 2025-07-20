#**Top 5 Cryptocurrency Portfolio Analysis(2014–2022)**#

**Project Overview**
This project explores the historical trends, volatility, trading volumes, and portfolio valuation of 5 major cryptocurrencies: BTC, ETH, MATIC, OCEAN, and SOL from 2014 to 2022. A Power BI dashboard was created to deliver interactive and data-driven insights for crypto investors and enthusiasts.

**📂 Dataset**
**Source:** https://www.kaggle.com/datasets/tr1gg3rtrash/time-series-top-100-crypto-currency-dataset

**Period Covered:** 2014 – 2022

**Coins Analyzed:**

  - Bitcoin (BTC)

  - Ethereum (ETH)

  - Polygon (MATIC)

  - Ocean Protocol (OCEAN)

  - Solana (SOL)

**Data Points:**

  - Adjusted Close Price

  - Daily Trading Volume

  - Standard Deviation of Volume (Volatility)

  - Coin Prices and Portfolio Value Over Time

**⚙️ Project Workflow**
1. Data Collection & Preprocessing
  - Imported CSV or API-extracted data into Power BI

  - Cleaned nulls and ensured consistent date formatting

  - Standardized fields for price, volume, and time across coins

  - Created calculated columns to convert volumes to meaningful units (Bn/M)

2. Feature Engineering
  - Created Standard Deviation of volume to represent volatility

  - Aggregated portfolio value by summing adjusted close prices of all five coins

  - Built dynamic time filters using slicers to allow custom time period analysis

3. DAX Measures
Defined custom DAX measures for interactive KPIs:

       Latest BTC Price = CALCULATE(LASTNONBLANKVALUE('BTC'[Date], MAX('BTC'[Adj Close])), LASTDATE('BTC'[Date]))
       Portfolio Value = SUMX(VALUES('Date'), [BTC] + [ETH] + [MATIC] + [OCEAN] + [SOL])

5. Visualizations in Power BI
  - Line Area Chart: Adjusted Close Price Trends for all 5 coins

  - Bar Chart: Volume Volatility (Standard Deviation)

  - Stacked Bar Chart: Daily Trading Volume Share by Coin (Year-wise)

  - Line Chart: Total Portfolio Value (Year-wise)

  - Slicers: Date range for dynamic time filtering

  - KPI Cards: Latest prices and volumes of each coin

5. Insights Extracted
  - BTC showed the highest volatility and dominated trading volume (~60–70%)

  - Portfolio peaked in 2021 with ~18M value before declining in 2022

  - MATIC and OCEAN had minimal trading impact compared to BTC/ETH

  - SOL showed a sharp rise in both price and volume during 2021–2022

  - Custom date slicers allowed viewing of market behavior during crypto booms or crashes

**📌 Key Metrics Tracked**
Metric	Description:
  - Adjusted Close Price	End-of-day prices adjusted for splits/dividends
    
  - Volume Volatility (Std Dev)	Variation in trading volume (risk indicator)
    
  - Trading Volume Share	Contribution of each coin in daily volume
    
  - Portfolio Value	Total valuation of all 5 coins over time
    
  - Latest Prices & Volumes	Most recent values for investor reference

**🛠 Tools & Technologies**
  - Power BI – Visualization and Dashboard Design

  - DAX – Calculated columns and measures

  - Excel/CSV – Raw data management and formatting

  - GitHub – Version control and project sharing
