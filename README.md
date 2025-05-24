# Stock Analysis of Major Technology Stocks

## Instructions (To see code)

- [click here](https://github.com/franky-coding/Stock-Analysis/blob/main/analysis.ipynb) or open analysis.ipynb

or

- git clone the repository and run the analysis in your local code editor

Disclosure: The Y-finance API is a timeseries dataset, and I specified within my code to grab data from one year ago to now(5/5/2025), thus depending on when you clone and run the notebook, your data will differ from the analysis in this ReadME.

## 📋 Table of Contents

- [Summary & Hypotheses](#introduction)
- [Closing Price Analysis](#closing-prices)
- [Volume Visualization](#volume-visualization)
- [Moving Averages - 10, 20, 45 Day](#moving-averages)
- [Percentage Change](#percentage-change)
- [Linear Relationships between Daily Percentage Changes](#Linear-Relationships-between-Daily-Percentage-Changes)
- [Correlation of Daily Percent Changes](#Correlation-of-Daily-Percent-Changes)

## Introduction

### Technologies Used:
- Python(Matplotlib, Numpys, Pandas, Seaborn)
- YFinance - Yahoo Finance for Stock Information

### Summary

The goal of this project is to clean, transform and visualize data on a selection of very large technology firms in which afterwards, I will analyze the visuals and draw important insights. Pandas and Numpys will be used to clean and transform data while Matplotlib and Seaborn will be used to make graphs and heatmaps. I will use a loop to iterate through each stock's dataframe from the YFinance API and store each of the stock's data in a python dictionary named 'stock_data'.

### Hypotheses

Based off of my current working knowledge of the market, I went into this project predicting that the trend and correlation between AMD and Nvidia will be negative due to them being direct competitors in the chip market. I also assume Tesla will be extremely volatile and differ trend-wise from the rest of the stocks. Microsoft, Apple, and Google will follow a similar trend being the 'grandfathered' tech giants of our generation.

## Closing Prices

<img src="images/Closing prices for stock analysis project.png" alt="Closing Prices" width="1200" height='400'>

- ### Thought Process:
I found a two ways to graph the closing price, one being a subplot with each stock having their own graph and two being one single graph with all seven stocks plotted on it. I chose option two because it clearly displays the trend of each stock and how it compares to its counterparts.

- ### Insights:
From looking at the graph of all the closing prices from now to a year ago, it seems that all the stocks followed a similar trend over the past year besides Tesla. Tesla had a MAJOR spike from November of 2024 going into 2025, most likely due to Musk's involvement with Trumps election and Trump winning that election. Teslas price movements seem to be a lot more drastic compared to the other stocks as well but we can also get a better picture of that through comparing PCT changes later.

## Volume Visualization

<img src="images/Volume for stock analysis project.png" alt="Volume" width="700" height='600'>

- ### Insights:
Looking at the plot of volumes for all seven stocks, we can judge which stock has the most volatility through how many fluctuations or "spikes" we see. Volume is essentially the amount of buy/sell orders the stock has on a certain day. Judging based off just looks, Tesla seems to be the most volatile stock because it shows the most amount of spikes that are drastic. Additional evidence that backs this hypothesis is the fact that Tesla is known to be a volatile stock that doesn't follow common market trends.

## Moving Averages

<img src="images/Moving Averages for stock analysis project.png" alt="Moving Avgs" width="900" height='700'>

- ### Insights:
From looking at the moving averages of these stocks, we can evidently see that Microsoft, Google, Amazon, and Nvidia all follow a similar trend when it comes to the 45 day moving average. The reason I chose to look at the 45 day average is because the higher amount of days means the data points are more "averaged out". Through the moving average, we are able to see the average price over an 'x' amount of days which can show us, more accurately, the trend/direction of a stock. This will not give us predictions on where the stock goes, but we are able to see which companies move similarly while which don't. Nvidia moving like those other three tech stocks tells us that Nvidia has become one of the tech giants, as seen in their insane growth in market cap. AMD has been going down gradually and not following any trend due to Nvidias growth and its inability to catch up to Nvidias chip and AI technology. This is evident because although AMD is still making earnings and profit, they are still slowly tanking as seen in the MA's.

## Percentage Change

<img src="images/pct change for stock analysis project.png" alt="Pct Change" width="900" height='700'>

- ### Technical Process:
I looped through each stocks dataframe and created a new column within each one named 'Daily Pct Changes' where I found the daily pct changes for each stock using '.pct_change()' in python pandas.

- ### Insights:
Through the plot, we can draw insights through understanding that, the more fluctuations a graph has, the more volatile that stock is. As we previously predicted from the closing prices and volatility, we can see that Tesla is evidently the most volatile stock as it has the most fluctuation for pct change in prices. This can be great for swing trading strategies that involve large and frequent price changes. On the contrary, Apple seems like the stock with the least fluctuation, hence we can hypothesize that it is a great stock to invest in as a more low-risk, long-term investment. Of course there are other metrics we need to look at but this can be a useful assumption that can be backed by other evidences.

## Linear Relationships between Daily Percent Changes

<img src="images/correlation for stock analysis project.png" alt="Linear Relationships" width="700" height='600'>

- ### Technical Process:
In order to cleanly plot the linear relationship between the percentage changes of each stock, I first create a single dataframe that contains just the percentage changes for every company. This would allow us to simply use seaborn to plot that entire dataframe in multiple ways, saving us time and time complexity in the long-run if we were to be reusing the daily change information.

- ### Insights:
From merely looking at the plot, we can safely assume that our choice of technology stocks all have a similar linear relationship. Since these are some of the largest tech giants in the industry as of May 2025, we can also safely infer that the technology industry follows a similar trend. If we look more closely, we can see that Microsoft and Amazon have the most linear relationship since their plots all squeeze tighter to the line. This means that investing in both Amazon and Microsoft would have likely yielded similar results over the past year.

## Correlation of Daily Percent Changes

<img src="images/correlation heatmap for stock analysis project.png" alt="Linear Relationships" width="500" height='400'>

- ### Insights:
From utilizing seaborn and a heatmap to calculate the correlation instead of visually looking at it in the previous plot, we are able to prove our hypotheses correct! Amazon and Microsoft do have the largest correlation. According to statistics, a correlation of over 0.7 is considered high while a correlation between 0.3 and 0.7 is considered moderate. We can then assume that most technology stocks are moderately correlated, and in this case, MSFT & AMZN are strongly correlated. There are a multitude of other factors but we can safely assume that we should not invest a high amount of capital in both MSFT and AMZN due to their correlation, we need to hedge our portfolio so that if AMZN or MSFT price drops, we have another stock that moves in the opposite direction.

Through the assumption that all tech stocks are moderately correlated, we can choose our investment strategy dependent on things like how much risk we are willing to take and whether we are investing long-term or short-term. For example, assuming 20% of our portfolio is technology stocks, we can choose to put 5/20% into a more volatile hence risky stock like tesla and the other 15/20% into stocks correlated with Apple since Apple had the least volatile percentage changes seen from out [Percentage Change](#percentage-change) graph.
