# Automated Stock Market Financial Analysis and Investment Strategy in Python & Tableau

# Synopsis 

**Problem**: Develop a data-driven approach for periodic long-term investing. 

**Solution**: Built a Python API automation pipeline to extract, clean, and rank stocks, integrating results into Tableau dashboards for real-time visualization. Used presentation skills to present.

**Insights**: Certain equities consistently outperform market benchmarks.

**Recommendation**: Implement systematic investing strategy using ranked performance metrics.

# Introduction

This project was originally completed in Python and Tableau Public and you can see my Tableau work here: 
<a href="https://public.tableau.com/app/profile/harvest.mondello/viz/Capstone2StocksAnalysisFinal/0_CoverPage"> Harvest Mondello's Tableau Public</a> And my Python code will be added to Github in the near future.
See the Python code here: [notebooks folder](/notebooks/)

In this analysis I will look at risk, prices and financials of the largest 500 US publicly traded stocks and compare them to the market as a whole. I will look at historical risk, historical price changes adjusted for re-invested dividends and current fundamentals from the companies financial statements.

I will then create a ranking system to balance risk, returns and fundamental sustainability as a criteria for which stocks to invest in today. My Python code can be run at any time and the visuals updated to select the best stocks to invest in on any given day.

# Tools I used
In this project, I utilized a variety of tools to conduct my analysis:

- **Tableau** To run final analysis and visualize.
- **Python** in VS Code: to write the code to pull the data, clean the data and conduct exploratory data analysis.
- **Visual Studio Code (VS Code)**: This open-source administration and development platform helped me manage my Python code. 
- **Gitub and Git**: To share my analysis, visualizations and code
- **ChatGPT** Used for routine formating tasks to be more efficient.
- **Python Libraries** multiple python libraries for manipulation of data, visualization and api. 
- **Python API** yfinance API to import historical stock data


# Cover Page
![Cover Page](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-1.png)

# Executive Summary
![Executive Summary](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-2.png)

# Structured Approach of the Analysis and Solution
![Structured Approach of the Analysis and Solution](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-3.png)

# Risk Analysis: Inflation and Risk Free Returns
For risk analysis I looked at the 30 most recent years of data. 
![Risk Analysis: Inflation and Risk Free Returns](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-4.png)

# Risk Analysis: Systematic and Unsystematic Risk
![Risk Analysis: Systematic and Unsystematic Risk](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-5.png)

# Risk Analysis: Standard Deviation as Volatility Risk
![Risk Analysis: Standard Deviation as Volatility Risk](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-6.png)

# Equities Price Analysis: Historical Stock Market Price & Dividend Returns 
For price analysis I looked at the 30 most recent years of data.
![Equities Price Analysis: Annual Historical Stock Market Price Returns, Adjusted for Dividends](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-7.png)

# Equities Price Analysis: Returns of Top Performers
![Equities Price Analysis: Returns of Top Performers](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-8.png)

# Equities Price Analysis: Ranked Returns of Top Performers
![Equities Price Analysis: Ranked Returns of Top Performers](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-9.png)

# Fundamental Equities Analysis: Overview
![Fundamental Equities Analysis: Overview](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-10.png)

# Fundamental Equities Analysis: Top Performers
To get the best view of a companies current financials, I looked at current fundamentals instead of historical. 
![Fundamental Equities Analysis: Top Performers](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-11.png)

# Weighted Ranking of Returns, Risks and Fundamentals
For the most relevant ranking I used data the 10 most recent years of data.
![Weighted Ranking of Returns, Risks and Fundamentals](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-12.png)

# Conclusion and Recommendation
![Conclusion and Recommendation](https://github.com/HarvestMondello/automate-stock-market-financial-analysis-and-investment-strategy/blob/main/assets/stock-financial-analysis-13.png)

# About the Project
For this analysis I combined, cleaned up and conducted a preliminary exploratory analysis in Python and then conducted a financial analyzed, used a weighted ranked system and visualized in Tableau. 

Some select Python code, the rest is in the Python folder

```python
#get price data from yfinance, status bar is nice

#create today variable
Today = datetime.now().strftime("%Y-%m-%d")
print(Today)

# Download Close prices and Dividends, 1962-current
df = yf.download(ticker_list, period="max", start="1962-01-01", end=Today, actions=True) #auto_adjust=True is the default for Close, ie Close+Dividends
# df_prices = yf.download(ticker_list, period="max", start="2025-3-07", end=Today, actions=True)

print("SP500 ticker list has been stored with current price data and dividends to df.")
print(df.columns.levels)
```

The Data for this project came from three sources:
1. Historical data going back top 1962 comes from the open source yfiance API which pulls from Yahoo Finance.
2. Fundamental data came from Google Finance.
3. Inflation data comes from statbureau.org

My Python code can be run at any time and the visuals updated to select the best stocks to invest in on any given day.







