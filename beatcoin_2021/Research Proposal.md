# Research Proposal: 
by Chuyu Chen, Shujin Gong, Jiaming Yao, Ziyi Zhuang

## Research Question

### Bigger Picture - What factors drive the returns of cryptocurrency?

### Specific Research Question
   - If the stock market drives the returns of cryptocurrency?
   - If the public news / events drive the returns of cryptocurrency?
   - If the three-factor-model (market return of cryptocurrency, Size (SMB), and network-value-to-transaction ratio (LMH)) explains the returns of cryptocurrency?

### Our Hypotheses
   - The returns of cryptocurrency has little relationship with the traditional stock market.
   - The price of cryptocurrency is mainly driven by investors’ expectations, which are highly influenced by the public news and events. 
   - The three-factor model can explain the price change of cryptocurrency to some extent.
   - The R2 of a market model of cryptocurrencies returns would be poor.
   - The R2 of a 3-factor model would be better.
   - The R2 of the 3-factor model PLUS a control for investor expectations and news could be best.


### Metrics of Success
To see how well our regression models fit the observed data, looking at the R squared (R^2) value could be an optimal way. In general, a higher R squared value indicates a better fit for the model. If we get a relatively lower R squared value in the beginning, it could be a bad sign for our models and we need to improve our model to get a higher R Squared value. Besides R squared, mean absolute error(MAR), which is a risk metric corresponding to the expected value of the absolute error loss, also could be one of our metrics of success. For the three-factor model, we will base on the statistics of variables by computing the t-stats and p-value to justify our confidence level.

## Necessary Data

Our final datasets need to include one dataset with Return information for S&P 500 index (from 03/2019 to 04/2021), and another dataset is the Top 10 market cap cryptocurrencies listed on Coinbase (from 03/2019 to 04/2021).The sample period is from March 2019 till April 2021.

For the sample conditions, first, the S&P 500 index is the representative of the US stock market (from 03/2019 to 04/2021). Also, the top 10 cryptocurrencies that are traded on Coinbase including Bitcoin (BTC), Ethereum (ETH), Binance Coin (BNB), XRP (XRP), Tether (USDT), Dogecoin (DOGE), Cardano (ADA), Bitcoin Case (BCH), Litecoin (LTC), Chainlink (LINK). The restriction that we anticipate is that 2020 is considered a not normal year for the stock market and many industries. For example, sectors like Industrials and Oil & Gas Products/Services seemed to stagnate, while information technology and biotechnology boosted. Thus, the stock market might be influenced by some factors that usually would not. Also, the top 10 cryptocurrencies rank is changing going forward, so that the ranking selected might not present the updated top 10 cryptocurrencies.

The variables that are absolutely necessary are: 
   - S&P 500 returns 
   - Top 10 Market Cap Cryptocurrency prices 
   - Risk-free rate 
   - Market return rate
   
If possible, we want to have the following variables:
   - Transaction volume in dark web 
   - Private investment of executives and stakeholders 
   - Undiscloased investing of public companies

Data we have: 
   - S&P 500 returns in US market
   - Top 10 cryptocurrency price information on Coinbase
   - Risk-free rates in the U.S.
   - Market return rates in the U.S.

Data we need: 
   - Coefficients and statistics like R2 through regression model between S&P 500 returns and cryptocurrency prices 
   - Coefficients and statistics like R2 through time series model between public events and cryptocurrency prices 
   - Compute coefficients of variables (Beta) through three-factor model and the statistics to justify Beta
   - Significant Public Events:
      - Event 1: Litecoins Halving Event (2019-08-05)
      - Event 2: CoronaVirus Outbreak and Travel Ban (2020-03-12)
      - Event 3: Bitcoin Halving Event (2020-04-08)
      - Event 4: Elon Musk’ Tweets (2021-01-01 to 2021-04-30)

To collect more data, we need to 
   - Find more indexes of public companies in the US to see more return information from different stock trading platforms 
   - Find more cryptocurrency price information from different trading platforms (e.g. coinmarketcap) 

There is one folder called `input` to store data downloaded from websites: 
   - input/sp500_return.xlxs
   - input/top_10_cryptocurrencies.xlxs
   - input/three_factors_model.xlxs
   - input/risk_free_rate.xlxs
   - input/market_return_rate.xlxs

How we will transform the raw data into the final form: 

Part 1： 
   - Get data about the S&P 500 and the price information of top 10 market cap cryptocurrency on Coinbase (from 03/2019 to 04/2021), save them in our input folder
   - Run regression analysis and visualizations to explore the correlation between stock returns and price of cryptocurrency

Part 2: 
   - Get data about risk-free rate and market return rate in the US
   - Apply 75% of data to train the three-factor model, and choose the best beta
   - Use the determined three-factor model to test the model on 25% data

Part 3: 
   - Discover the important public events that might relate to price changes of cryptocurrencies (from 03/2019 to 04/2021)
   - Visualize the effect on daily prices and daily returns by the event
   
Final Form: 

The final conclusion will be based on the above three parts. According to the statistics of our dataset, we will determine the possible factors that will influence the price change of cryptocurrencies and the best-fit three-factor model.
