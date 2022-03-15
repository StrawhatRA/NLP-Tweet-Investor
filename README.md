# **Project 2: Investing in Beaten Down Stock**


<p align="center" width="40%">
    <img width="50%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/fat-twitter.png"> 
</p>


<br>

[Link to Presentation Slide](https://docs.google.com/presentation/d/1A7j_rd_NJ1f8fc_Icdgv4Cbkd_kK7q725bJMzFZ03ew/edit)

<br>


## **Using Fintech tools to identify Stock Investment Opportunities**

## Introduction: Joe tries day trading
Joe keeps hearing the same advice on r/WSB: “You should be like Warren Buffett, and ‘BTFD’!” and “Buy when there’s blood on the streets!” After learning in Project [#1](https://github.com/JakeKJShin/Project_1_Team_2) that he’ll never be able to afford a house doing passive investments he’s decided to try his hand at making money in speculative trading! Joe wanted to use his newly acquired fintech skills to help him with where to look for cheap stocks! Joe will use NLP to analyze sentiment and narrow down a list of candidate stocks. After which Joe will run a technical analysis of the the stock and lastly Joe wants to use a classification model that will help him predict if the stock price will go up or down the next day. This way Joe can rely on various techy tools instead of only relying on gossip or news articles recomending what he should invest in. 


## **Joe's approach**
Joe wanted up to date fresh news to find what stocks are being most talked about negatively. Unfortunately, Joe finds traditional media too unreliable! Instead, Joe decided to use Twitter. Thinking the info would arrive much quicker than news articles! Giving him some sort of edge over the "average Joe". Joe strictly means business and so he decided to look through the tweets of some big name traders only. Having fresh tweets by traders on what stocks they were talking about, Joe started his NLP analysis and narrow down a list of "beaten" stocks. Then he used technical analys and a self made decision tree to further identify if the stock will bounce back and make him money!  


## Process 

1) First Joe has to find a nice and bloody stock! pulling from the Twitter API a data frame of the tweets with tickers is created with their sentiment
2) TA analysis of what the charts say 
3) What does the decision tree model say about this stock pick? does it look like its moving up or down?  


## Data Source
Twitter API & Yahoo Finance.

## Libraries

This project requires the following libraries: pandas, numpy ,tweepy, hvplot, graphviz, matplotlib, nltk, sklearn & yfinance.


## Decision Tree Model 
Joe chooses to build a classification model to know whether the stock's price will go up or down during the next trading session in order to compliment it's 'buying the dip' strategy and make an optimal trading decision. Joe uses  7 years worth of historical pricing and volume data to build technical indicator features and train his model. He also uses PCA method to reduce the dimensionality of his features in an effort to improve the model's effectiveness.
(this next  part we can add to a Conclusions section of the readme maybe along with your conclusions)
Unfortunately the classification model only yield a 53% accuracy not making very reliable. Joe needs to take a better look at his feature selection and engineering and probably use more data to better train his model.

<p align="center" width="50%">
    <img width="50%" src="https://github.com/JakeKJShin/2_The_Moon_Investing_Beat_Down_Stock/blob/main/readme%20Images/Decision%20Tree.PNG"> 
</p>


## **Conclusion**
Joe was able to identify a few 'beat down' stocks from Twitter based on sentiment analysis. OLLI was considered the best option available among them. Joe has ran the stock pick through his checks and both the TA analysis & decision tree model give him the green light on investing! Unfortunately, his Decision Tree model needs some fine tuning as it was not great at predicting daily returns. 
