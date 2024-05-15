# About my stock data web scraping project
Since I created this Notebook using Anaconda, I did not need to install the libraries.
I just needed to import them.

So, first I imported the proper libraries:
* yfinance
* pandas
* requests
* beautifulSoup
* plotly

Then, I developed a function for creating the graphs that I wanted. 

1) I started off by creating a figure with **2 rows of subplots where both rows share the same x-axis (time)**, allowing for an easy comparison of share price and revenue over the same time periods.
2) I then filtered the stock data and revenue data to include data only up to specific dates (2021-06-14 for stock data and 2021-04-30 for revenue data), in order to focus the analysis on a relevant, and manageable timeframe.
3) Next, I added a scatter plot trace for the stock price. The **x-axis is the date** (converted to datetime format for better handling in Plotly) and the **y-axis is the closing stock price** converted to a float
