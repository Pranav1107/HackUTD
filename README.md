# HackUTD
## Goldman Sachs Challenge Problem
Solution:

- get the historical data and create a LSTM model that predicts the earnings and financial performance using historical data.
- Get data about NewsAPI and search for “Goldman Sachs” and find the sentiment of the news using a sentiment analyser.
- Combine the result of both the models and predict the forecasting
inorder to get the historical data use yfinance and label as 
```
import yfinance as yf
data = yf.download('GS', start='2019-01-01', end='2023-11-4')
data.to_csv("GS_2019_01_01-2023_11_4.CSV", index=True)
```

upload this data to databricks.

To get the data from NewsAPI we run the following file and download the result in a csv.
https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3043472558199087/2357835694434112/349226778481836/latest.html 

After acquiring the data run the LSTM model on the dataset (historical + sentiment)
https://colab.research.google.com/drive/1I3vo_vIU4XDCh3-hENs8xDcU2x7nLKJq?usp=sharing 


![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/domain_model.png?raw=true)
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/classDiagram.png?raw=true)
![alt text](https://github.com/Pranav1107/HackUTD/blob/main/DesignDiagrams/sequenceDiagram.png?raw=true)