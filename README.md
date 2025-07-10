This project implements a simple Long Short-Term Memory (LSTM) neural network from scratch (using NumPy) to predict stock prices. The model is trained on Netflix (NFLX) historical stock data and attempts to forecast future closing prices.

-> Features
Uses custom-built LSTM architecture (no deep learning libraries like TensorFlow or PyTorch)

Trains the model using the L-BFGS-B optimization algorithm

Visualizes actual vs. predicted stock prices

Reports Root Mean Squared Error (RMSE) for performance evaluation

-> Dataset
File: NFLX.csv

The dataset must contain at least two columns:

Date: Date of the stock data

Close: Daily closing price of Netflix stock

Make sure the CSV file is placed in the same directory as the code.

-> Requirements
Install required Python libraries (if not already available):

bash
Copy
Edit
pip install numpy pandas scikit-learn matplotlib scipy

-> How It Works
Data Preprocessing

Loads and normalizes the Close price using MinMaxScaler.

Splits the data into training and testing sets (80:20 ratio).

Model Architecture

An LSTM is implemented from scratch using NumPy.

Uses tanh for activation and a simple linear output layer.

Training

A custom objective function (MSE) is minimized using scipy.optimize.minimize.

Prediction and Evaluation

The trained LSTM model is used to predict stock prices on the test set.

Predictions are inverse-transformed to the original scale.

RMSE is calculated and plotted for evaluation.

-> Sample Output
bash
Copy
Edit
Root Mean Squared Error (RMSE): 12.0456
A plot of actual vs. predicted stock prices will also be displayed using matplotlib.

-> Note
This is a conceptual prototype to demonstrate how LSTMs work internally. It is not production-grade and omits key features like:

Input/output windowing for time-series modeling

Gate mechanisms of standard LSTMs (forget, input, output gates)

Backpropagation and gradient updates

-> Future Improvements
Add full LSTM gate mechanisms

Implement gradient-based training (Backpropagation Through Time)

Use sliding windows for multi-step forecasting

Compare with standard models (ARIMA, RNN, etc.)

Extend to multiple stock tickers or features

-> Author
Julia Grace Muddada
juliagrace424@gmail.com
Linkedin- www.linkedin.com/in/julia-grace-muddada-6708271b3
