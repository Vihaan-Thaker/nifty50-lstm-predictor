# nifty50-lstm-predictor
In this analysis, I employed an LSTM model, with separate models trained for each of the NIFTY50 companies, to predict the direction of their returns for the following day.
I figured out the hyperparameters for each LSTM model by manually going through multiple of hyperparameters for each model and finalluy picking the one which performed the best
The features utilized in this prediction process include returns, SMA_50, SMA_200, RSI, volatility, and returns for the NSEI. These features were employed in a rolling window fashion, with the companies initially sorted based on the accuracy of their predictions over the training examples.
For the top N companies, I generated predictions for the current day’s return direction and subsequently validated these predictions at the end of the day for the past week.
