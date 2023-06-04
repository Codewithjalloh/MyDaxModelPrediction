# MyDaxModelPrediction
This code is an example of using a Long Short-Term Memory (LSTM) neural network for time series prediction. It predicts the stock price of the DAX index using historical data.

Here's a breakdown of the code:

Import the required libraries: pandas for data manipulation, numpy for numerical operations, matplotlib.pyplot for plotting, and various modules from sklearn and keras for machine learning.

Load the data from a CSV file named 'DAX.csv' and set the 'Date' column as the index. Remove any rows with missing values.

Scale the 'Close' column of the data using a MinMaxScaler to transform the values to the range [0, 1].

Split the data into training and testing sets. The training set contains 70% of the data, and the testing set contains the remaining 30%.

Prepare the training data for the LSTM model. It creates input sequences (x_train) and corresponding target values (y_train) by sliding a window of size 60 over the training data.

Prepare the testing data in a similar manner as step 5.

Reshape the input data to fit the input shape expected by the LSTM model.

Create an LSTM model using the Sequential class from Keras. It consists of two LSTM layers with 50 units each and a dense output layer.

Compile the model using the Adam optimizer and mean squared error loss.

Fit the model to the training data for 10 epochs with a batch size of 32.

Use the trained model to make predictions on the testing data.

Inverse transform the scaled predictions back to the original scale.

Calculate the root mean squared error (RMSE) between the actual test values and the predicted values.

Plot the original training data, the actual test values, and the predicted values using matplotlib.pyplot.

The code demonstrates the process of training an LSTM model on historical stock price data and evaluating its performance by predicting future prices.
