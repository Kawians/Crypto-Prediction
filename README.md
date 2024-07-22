# Crypto Price Prediction

## Summary of the Project:
In this project, two separate models for each of three different crypto currency icluding Cardano (ADA), Bitcoin (BTC), and Ethereum (ETH) have been trained. The price of tomorrow has been used as the target for the features of each day.
The dataset includes the open, low, high, and close price of a numerous crypto currencies. It could be found using the link below on Kaggle:</br>
https://www.kaggle.com/datasets/svaningelgem/crypto-currencies-daily-prices/data
</br>
![Crypto-Price-History](https://github.com/user-attachments/assets/3d30a8c4-c804-4d94-9bd3-5774ecdf8e94)

</br>
In this project, Cardano, Bitcoin, and Ethereum crypto has been used to train models.
</br>
In order to include the effect of the crypto price history in the feed forward model, an average of last 5, 10, and 20 days has been generated and added to each row (day).

## The purpose of the project:
The main purpose of this project is to train a simple model to be able to predict the next day crypto price with the highest possible accuracy. To achieve this goal, a feed forward and an LSTM model has been trained for each one of the mentioned crypto currencies.

## Crypto Price Prediction:
There are three main parts in this project. Each one of them is related to one of the crypto currencies, and the concept of the modeling and training is the same for all three.</br>
There are   steps in each modeling:</br>
1- Investigating the Data Frame</br>
2- Visualizing the price history</br>
3- Feature Engineering and adding the average of closing price for the last 5, 10, and 20 days</br>
4- Normalizing Features and Target</br>
5- Designing feed-forward neural network</br>
6- Training the feed-forward model</br>
7- Plotting the training curves for evaluation of model performance</br>
8- Making a prediction using the trained feed-forward model</br>
9- Generating sequential data to be fed into LSTM model</br>
10- Designing LSTM model architecture</br>
11- Training LSTM model</br>
12- Plotting LSTM model traning curves</br>
13- Making a prediction using the LSTM model</br>


### 1- The Models:
For each one of the crypto currencies, a simple feed-forward neural network and an LSTM model has been trained. The reason was to see how much difference an LSTM model make when it comes to the time series dataset.

### 2- The Target
The next day closing price has been used as the target of each day features.

### 3- Feature Engineering
In order to include the impact of the previous days prices in the simple feed-forward neural network model, the MA5, MA10, and MA20 features have been generated which are the average of closing price for past 5, 10, and 20 days. As a result, to not have a null data, the first 19 days has been removed from the dataset (as they don't have the past 20 days price average).

### 4- Generating sequential data for LSTM model
In order to feed the data to LSTM model, we need the data to be in the format of Features, Target, and the time steps. The time steps are the historical window that the model will be trained on for each data point.

### 5- Conclusion
As it was expected, the LSTM model performed better in all three cases for Cardano, Bitcoin, and Ethereum. The loss during the training stage was lower for the LSTM model rather than the feed forward model. Also, the trainig curve was more stable during training the LSTM, while it was fluctuated for training the feed-forward model that it showed the model didn't learn the pattern very well in feed-forward modeling. The prediction was the final evidence that showed the performance of the LSTM model was way better than the feed-forward model as it could be seen below:</br>
![Crypto-Price-Prediction](https://github.com/user-attachments/assets/c1e41418-3f86-430c-8afb-853adfa4adf6)
