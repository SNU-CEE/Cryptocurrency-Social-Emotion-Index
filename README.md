# Cryptocurrency-Social-Emotion-Index
2021_Winter-SNU_IAB_Class   
Seoul_National_University - College_of_Engineering   
Project done by Haksoon Kim   
Email: bafflesoon@snu.ac.kr   

# Project Description
Cryptocurrency Index which reflects Social Sentiment by applying Sentiment Analysis
Target Cryptocurrency: Doge Coin(DOGE), Binance Coin(BNB)
Data: Search Volume(Google Trends), Trade Volume(Binance API), Tweets(Twitter API)
- 0-100 Normalized Interests Time Series Data found in Google Trends of Search Word - Doge Coin, Binance Coin (5 years around worlds)
- Trade Volume from Daily Trade Data by using Binance API since each cryptocurrency capitalized and also get time series data of price
- Tweets done in 2021 from cryptocurrency-related accounts by using twitter scraper API 'Scweet'

# Process
Search Volume, Trade Volume and Price
- Get first difference of each three time series
- Calculate a pearson correlation coefficient between (Search Volume and Price) and (Trade Volume and Price)
- Take an average and find the Index

Tweets
- Preprocess the raw text data (remove stopwords and whitespaces)
- Set keywords related to cryptocurrency which are popular in terms of search volume
- Collect tweets which contain those keywords and count how many keywords exist in the text
- Use VADER Sentiment Analysis module to the tweets in order to calculate compound sentiment score
- Finally calculate weighted average from (keyword counts and VADER score) and take it as a Index

Final Index
- Average of the indices calculated above
