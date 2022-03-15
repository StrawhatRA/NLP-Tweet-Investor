# **Project 2: Investing in BTFD!**
## When's the best time to buy that beaten down stock?


<p align="center" width="35%">
    <img width="50%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/fat-twitter.png"> 
</p>


<br>

[Link to Presentation Slide](https://docs.google.com/presentation/d/1A7j_rd_NJ1f8fc_Icdgv4Cbkd_kK7q725bJMzFZ03ew/edit)

<br>


# **Using Fintech tools to identify Stock Investment Opportunities**
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/Average_Joe.png"> 
</p>
Poor Trader Joe. After learning in <a href="https://github.com/JakeKJShin/Project_1_Team_2">Project #1</a> that he’ll never be able to afford a house by solely completing passive investments, he’s decided to try his hand in speculative trading! Joe is looking to buy when there's 'blood in the streets'by using Natural Language Processing (NLP's) to analyze sentiment and narrow down a list of candidate stocks. Then, Joe will run technical analysis to see if there are anomolies or outlier deviations from moving averages. Lastly, if the potential stock passes both of these filters, Joe will utilize a classification model to help him predict if the stock will go up or down the next day. By using this 'goldilocks' approach as a pre-trade checklist, Joe takes control of his destiny instead of relying on blind recommendatioon from gossip or news articles!
</p>

## Joe's Approach

Joe's on the prowl for hot-of-the-press bearish news of pummeled stocks. Unfortunately, Joe finds traditional media too unreliable and always late to the party! Instead, Joe turns to Twitter. Reasoning that any new info would arrive much quicker than average news articles, Joe decides to look through the tweets of some big name traders. Joe builds a list of traders he respects, then begins his NLP analysis to narrow down a list of "beaten down" stocks. Once he narrows the list, he'll use technical analys and a custom decision tree to further identify potential performance of the stock. Maybe this way he'll be able to post his 'gainz' on r/WSB! 


## Process 

1) First, Joe needs to find a nice and bloody stock! He'll utilize the Twitter API to create a custom dataframe of tweets containing negative sentiment. 
2) Next, Joe will perform Technical Analysis and compare the stock price vs. the 21/50/200 EMAs. He'll look for extreme outliers, generate signals, then compare the general perfomance of the signals 1 month after relative to SPY. 
3) Lastly, what does the decision tree model say about this stock? Will the model forecast the next trading session to move up or down?  


## Data Source
We utilized tthe Twitter API and Yahoo Finance.

## Libraries

This project required the following libraries: pandas, numpy ,tweepy, hvplot, graphviz, matplotlib, nltk, sklearn & yfinance.

## Twitter API
Joe

## Technical Analysis
Joe pulls 5 years of data of **$OLLI** and **$SPY**. He then plots the closing prices and the 21, 50, and 200 EMAs. He builds a dataframe comparing the current price vs. the three EMAs, standardizes the deltas, and looks for anomolies. He uses a 1.5 std.dev equivalent (or 13th percentile) to find the extreme outliers of %moves away from the EMAS. From here, he can see that the range of price moves away from the 21EMA.
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/ticker_21_range.png"> 
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/occurrence.png"> 
</p>

He builds a dataframe, initiates a signal, then plots his findings.
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/ema_signals_plot.png"> 
</p>
In order to backtest the performance of his signal, Joe plots the average returns of his stock 1 trading month after the signal. Is the price higher or lower? How about %return relative to the SPY?
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/21signal_performance.png"> 
    </p>
Lastly, Joe wants to try his hand at linear regression. He's looking to see if there are any correlations between the "%away from the 21EMA" compared to the average return of the stock 20 days later. Unfortunatley, the r-squared value is incredibly low, and therefore his model is unreliable!
<p align="center" width="50%">
    <img width="75%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/21EMA.png"> 
    </p>
    
## Decision Tree Model 
Joe chooses to build a classification model to help him determine if the stock's price will go up or down during the next trading session. Joe uses 7 years of historical pricing and volume data to build technical indicator features and train his model. He then uses a PCA method to reduce the dimensionality of his features in an effort to improve the model's effectiveness

<p align="center" width="50%">
    <img width="50%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/Decision%20Tree.PNG"> 
</p>


## **Conclusion**
Joe was able to identify a few 'beat down' stocks from Twitter based on sentiment analysis. OLLI was considered the best option avaiilable (because it was the worst!), so Joe ran his pre-trade checklist BTFD system. His NLP analysis found the stock, then his TA analysis measured some EMA vs. price anomolies, and finally his decision tree model provided the green light to investing! As for the accuracy of his system, although his TA analysis gave relatively good returns, unfortunately his Decision Tree model needs fine tuning. The classification model only yielded a 53% accuracy, proving it's not very reliable. Joe needs to take a better look at his feature selection, engineering, and probably use more data to better train his model. You live you learn (and hopefully earn along the way!)
