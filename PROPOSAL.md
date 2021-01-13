# A/B Testing Proposal
### Luke Swanson  

## Question of Interest  

On average did the stock market have higher levels of volatility on days that Donald Trump tweeted to the public?  
  
## Definition of Variables  
  
*The difference between the daily high and low of the SPX will be used as a proxy for volatility*. SPX is an ETF that tracks the movements of the S&P500 index. The choice of S&P500 (as oppoosed to Dow Jones or NASDAQ) was made because the at 500+ companies the S&P500 can be assumed to approximate the population of American businesses. The NASDAQ was not chosen because of it's over-exposure to technology relative to the S&P500. Using high-low scores as opposed to using more standard measures of volatility (such as the Vix) is due to the distrubtion of data. The Vix is far from normal.


A *tweet* from Donald Trump to the general public is defined as: 
1. Not being a retweet.
2. Not being a link.  

All other tweets are assumed to be him talking to the people.  

- Group A: differences in high-low on days Donald Trump tweeted to the general public.
- Group B: differences in high-low on days Donald Trump did not tweet to the general public.

## Data
The data set used for testing is actually two data sets left-outer-joined on date.
- The left data set is [daily prices of SPX](https://www.wsj.com/market-data/quotes/index/SPX/historical-prices)  
- the right data set is [Donald Trump's tweets since he was elected](https://drive.google.com/file/d/1xRKHaP-QwACMydlDnyFPEaFdtskJuBa6/view?usp=sharing).   
- [Here is a link to the data sets after they've been joined/formatted](https://github.com/luke-swans0n/DonaldTrumpSPX/blob/main/market_and_tweets.csv)

## Design
*Null Hypothesis:* the mean difference in differences between high-low prices of SPX on days that Donald Trump tweeted is zero. 

By splitting the data into groups (A: tweet, B: no-tweet) and then running student's t-test. 

## Audience  

This project is written for the benefit of everyone, but would be of particular interest to fund-managers, traders, government-overwatch organizations, and financial regulators. Traders would benefit from the potential to profit off of volatility increase, fund-managers would benefit from finding another known-risk so they can work to mitigate, the government would be able to use the results to set controls on online conduct by officials.

## Implications

The implications of rejecting the hypothesis that Donald Trump's tweets had no effect on volatility in the market are vast, and surely this is no complete list:  
>1. It is possible to profit off the raised levels of volatility due to the President's twitter activity.
>2. It would be possible to create a scheme to commit market manipulation based on Presidential tweets, implying one could get the President to collude.  
>3. The nation may need to impliment some means of constraining the social media accounts of sitting Presidents
>4. Other government officials may also be able to cause markets to move by posting to social media.

## Additional Research if Time Permits
- Did Donald Trump's tweets effect other indices (NASDAQ, Dow Jones Industrial Average, Russell 5000)  
- Did the content of the tweet have an effect?  
- Did former presidents experience a similar effect?  
- Did tweets before COVID-19 have a larger or smaller effect than after? 
