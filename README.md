# Cryptocurrency-Social-Emotion-Index
2021_Winter-SNU_IAB_Class   
Seoul National University - College of Engineering   
Project done by Haksoon Kim   
Email: bafflesoon@snu.ac.kr   

# Project Description
Cryptocurrency index which reflects social sentiment by applying sentiment analysis   
Target cryptocurrency: doge coin(DOGE), binance coin(BNB)   
Data: Search volume(Google Trends), Trade volume(Binance API), Tweets(Twitter API)   
- 0-100 Normalized interests time series data found in Google Trends of search word - doge coin, binance coin (5 years around worlds)   
- Trade volume from daily trade data by using binance API since each cryptocurrency capitalized and also get time series data of price   
- Tweets done in 2021 from cryptocurrency-related accounts by using twitter scraper API 'Scweet'   

# Process
Search volume, Trade volume and Price
- Get first difference of each three time series
- Calculate a pearson correlation coefficient between (Search volume and Price) and (Trade volume and Price)
- Take an average and find the index

Tweets
- Preprocess the raw text data (remove stopwords and whitespaces)
- Set keywords related to cryptocurrency which are popular in terms of search volume
- Collect tweets which contain those keywords and count how many keywords exist in the text
- Use VADER Sentiment Analysis module to the tweets in order to calculate compound sentiment score
- Finally calculate a index which is weighted average accounting keyword counts and VADER score

Final Index
- Average of the indices calculated above
