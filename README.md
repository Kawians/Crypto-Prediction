# Crypto Price Prediction

## About this Project:
In this project, two separate models for each of three different crypto currency icluding Cardano (ADA), Bitcoin (BTC), and Ethereum (ETH) have been trained.

### 1- The Models:
For each one of the crypto currencies, a simple feed-forward neural network and an LSTM model has been trained. The reason was to see how much difference an LSTM model make when it comes to the time series dataset.

### 2- The Target
The next day closing price has been used as the target of each day features.

### 3- Feature Engineering
In order to include the impact of the previous days prices in the simple feed-forward neural network model, the MA5, MA10, and MA20 features have been generated which are the average of closing price for past 5, 10, and 20 days. As a result, to not have a null data, the first 19 days has been removed from the dataset (as they don't have the past 20 days price average).