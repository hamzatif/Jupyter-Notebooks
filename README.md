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
3) Next, I added a scatter plot trace for the stock price. The **x-axis is the date** (converted to datetime format for better handling in Plotly) and the **y-axis is the closing stock price** converted to a float.
4) Then I added an identical scatter plot trace for revenue, with dates one the x-axis and reported revenues on the y-axis.
5) All I had to do now was to call the function later once my data was loaded.

I created an instance of the **Ticker** class from the **yfinance library** for the Tesla stock, and then created a dataframe for the stock's data. I then used the history method to retrieve historical stock data over the maximum available period of time. 

To gather Tesla's revenue data, I used web scraping techniques. I specified the URL containing the data I needed to scrape, and then used the **requests library** to retrieve the HTML content. To parse the HTML, I used the BeatifulSoup library.

Once I had the data, I needed to clean it. So, I renamed my columns appropriately, changed the character type for the revenue column, and dropped any rows with missing values to maintain data integrity.

All I had to do then was to call the function I created earlier to create a graph based on Tesla's data.
I also repeated the process for GameStop stock data.
