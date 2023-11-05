# HackUTD
## Inspiration

### Goldman Sachs Challenge Problem

## What it does
Solution:

- Extracts news from NewsAPI and finds the sentiment regarding the company on that day by using bert model.
- The data with (date, sentiment) as its field is joined with the historical dataset which can be downloaded from the script below.
 
```
import yfinance as yf
data = yf.download('GS', start='2019-01-01', end='2023-11-4')
data.to_csv("GS_2019_01_01-2023_11_4.CSV", index=True)
```
- This joined dataset is used to forecast the stock price value by using a LSTM algorithm.

To get the data from NewsAPI we run the following file and download the result in a csv.
https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3043472558199087/2357835694434112/349226778481836/latest.html 

After acquiring the data run the LSTM model on the dataset (historical + sentiment)
https://colab.research.google.com/drive/1I3vo_vIU4XDCh3-hENs8xDcU2x7nLKJq?usp=sharing 

## Challenges Faced during development:
- Extracting data from news sources was a bit difficult as the API was not allowing to hit data in the past for more than 3-4 years. 
- News were not available for a lot of days, for that day was null after joining, The value was filled with the value that was previous to that position.
- The solution for this problem was divided into 2 parts that is the big data part where we used Pyspark to get the data and apply sentiment analysis and the second part where the data was used to forecast the stock values. 
- The project should be automated rather than doing it on 2 separate platforms.
- To acquire sentimental analysis data, datasets should be created such that they already have the sentiment about that company.

## Accomplishments that we're proud of
- Created a dataset that has the historical data as well as the sentiment of the company at that particular
period.

- Used open-source NLP technique to analyze sentiment of the company using current news of the 
company.

- Trained a LSTM model to predict the future stock prices.

![alt text](https://Created a dataset that has the historical data as well as the sentiment of the company at that particular
period.

Used open-source NLP technique to analyze sentiment of the company using current news of the 
company.

Trained a LSTM model to predict the future stock prices.
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/domain_model.png?raw=true)
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/classDiagram.png?raw=true)
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/sequenceDiagram.png?raw=true)
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/UI.png?raw=true)

## What we learned
- We learned a lot about the stock price prediction and LSTM over these 24 hours.
- also we learned about what are the factors that affect earnings and financial health of a company.

## What's next for HackUTD project
- More Fun and more problem statements.