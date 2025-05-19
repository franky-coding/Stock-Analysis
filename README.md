# Stock Analysis of Major Technology Stocks

## Instructions (To see code)

- open analysis.ipynb to take a quick look directly on github or [click here](https://github.com/franky-coding/Stock-Analysis/blob/main/analysis.ipynb)

or

- git clone the repository and run the analysis in your local code editor

Disclosure: The Y-finance API is a timeseries dataset, and I specified within my code to grab data from one year ago to now(5/5/2025) so depending on when you clone and run the notebook, your data will differ from the analysis in this ReadME.

## 📋 Table of Contents

- [Summary & Hypotheses](#introduction)
- [Closing Price Analysis](#closing-prices)
- [Volume Visualization](#volume-visualization)
- [Moving Averages - 10, 20, 45 Day](#moving-averages)

## Introduction

### Technologies Used:
- Python(Matplotlib, Numpys, Pandas, Seaborn)
- YFinance - Yahoo Finance for Stock Information

### Summary

The goal of this project is to clean, transform and visualize data on a selection of very large technology firms in which afterwards, I will analyze the visuals and draw important insights. Pandas and Numpys will be used to clean and transform data while Matplotlib and Seaborn will be used to make graphs and heatmaps. I will use a loop to iterate through each stock's dataframe from the YFinance API and store each of the stock's data in a python dictionary named 'stock_data'.

### Goal

Based off of my current working knowledge of the market, I went into this project predicting that the trend and correlation between AMD and Nvidia will be negative due to them being direct competitors in the chip market. I also assume Tesla will be extremely volatile and differ trend-wise from the rest of the stocks. Microsoft, Apple, and Google will follow a similar trend being the 'grandfathered' tech giants of our generation.

## Closing Prices

<img src="images/Closing prices for stock analysis project.png" alt="Closing Prices" width="1200" height='400'>

I found a two ways to graph the closing price, one being a subplot with each stock having their own graph and two being one single graph with all seven stocks plotted on it. I chose option two because it clearly displays the trend of each stock and how it compares to its counterparts.

From looking at the graph of all the closing prices from now to a year ago, it seems that all the stocks followed a similar trend over the past year besides Tesla. Tesla had a MAJOR spike from November of 2024 going into 2025, most likely due to Musk's involvement with Trumps election and Trump winning that election. Teslas price movements seem to be a lot more drastic compared to the other stocks as well but we can also get a better picture of that through comparing PCT changes later.

## Volume Visualization

<img src="images/Volume for stock analysis project.png" alt="Closing Prices" width="1200" height='400'>

Looking at the plot of volumes for all seven stocks, we can judge which stock has the most volatility through how many fluctuations or "spikes" we see. Volume is essentially the amount of buy/sell orders the stock has on a certain day. Judging based off just looks, Tesla seems to be the most volatile stock because it shows the most amount of spikes that are drastic. Additional evidence that backs this hypothesis is the fact that Tesla is known to be a volatile stock that doesn't follow common market trends.

## Moving Averages

<img src="images/Moving Averages for stock analysis project.png" alt="Closing Prices" width="1200" height='400'>
