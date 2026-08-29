# Simple Price Predictor Model Using LSTM model to predict stock closing prices.

This notebook uses META stock data (`META`) from Yahoo Finance, trains on prices from 2020 through the start of 2026, and validates the model on 2026 data. It then plots the training/validation loss, compares predicted prices with actual prices, and reports RMSE.

## Changing the Stock
To predict a different stock, change the ticker in the notebook:
`ticker = "MSFT"`
`ticker = "AAPL"`

## Model Paramas
The model is a stacked LSTM built with PyTorch.

* Input dimension: 1
* Hidden dimension: 32
* Number of LSTM layers: 4
* Output dimension: 1
* Optimizer: Adam
* Learning rate: 0.01
* Epochs: 300
* Sequence length: 30 days

Each training example uses the first 29 days of a 30-day window to predict the final day's closing price.

## Outputs
After training, the notebook shows:
* Training loss
* Validation loss
* Train RMSE
* Test RMSE
* Actual vs predicted stock prices
* Prediction error over time

`train rmse: 5.604073524475098`
`test rmse 11.11147689819336`

## Preview of Outputs:-
 * <b>Training and Validation for Diff-Diff Epochs(1-300)</b>
<img width="1001" height="701" alt="image" src="https://github.com/user-attachments/assets/98ae8fd8-47df-431e-9f46-72f13e555c11" />

 * <b>Stock Price Prediction and Error from Base RMSE</b>
<img width="1187" height="989" alt="image" src="https://github.com/user-attachments/assets/1026be4a-0fc1-4932-8478-0e9288d947e6" />

## Motive of this prject
Just for understanding the real world implementation of LSTM. :) Thanks /\
