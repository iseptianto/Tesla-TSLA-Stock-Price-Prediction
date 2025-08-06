# Tesla (TSLA) Stock Price Prediction with Machine Learning

[](https://opensource.org/licenses/MIT)
[](https://www.python.org/downloads/)
[](https://www.tensorflow.org/)

A machine learning project to predict the future closing price of Tesla (TSLA) stock using historical data and a Long Short-Term Memory (LSTM) neural network model.

-----

### ⚠️ Important Disclaimer

**This project was created purely for educational and research purposes.** Stock price prediction is highly volatile and is influenced by many external factors (news, market conditions, sentiment, etc.) that are not covered in this model. **DO NOT USE PREDICTIONS FROM THIS PROJECT AS A BASIS FOR MAKING INVESTMENT DECISIONS.** The author is not responsible for any financial gains or losses that may occur.

-----

### 📝 Project Description

This project aims to build and train a deep learning model capable of analyzing patterns in historical Tesla stock price data to predict the closing price (`Close Price`) for the next day. The project covers the entire workflow, from data collection, preprocessing, LSTM model creation, and training, to the evaluation and visualization of prediction results.

### 🎯 Background

The stock market is known for its high volatility, and technology stocks like Tesla ($TSLA) are among the most watched by investors and analysts. Predicting stock price movements is one of the most complex challenges in financial analysis. By using a time-series model like LSTM, we can attempt to capture long-term dependencies in historical data that might not be apparent with traditional statistical methods.

### ✨ Key Features

  - **Real-time Data Fetching**: Uses the `yfinance` library to fetch the latest historical stock price data directly from Yahoo Finance.
  - **Time-Series Analysis**: Conducts analysis and visualization of stock price data over time.
  - **LSTM Model**: Implements a Long Short-Term Memory (LSTM) network, which is highly suitable for sequential data like stock prices.
  - **Prediction Visualization**: Compares predicted prices against actual prices in a graph for visual evaluation.

### 📊 Dataset

The data used is the historical stock price data for Tesla (ticker symbol: `TSLA`) fetched using the `yfinance` library. This data includes the following information:

  - `Open`: The opening price
  - `High`: The highest price of the day
  - `Low`: The lowest price of the day
  - `Close`: **(Target Feature)** The closing price
  - `Volume`: The number of shares traded

### 🛠️ Tech Stack

  - **Language**: Python 3.8+
  - **Data Fetching**: `yfinance`
  - **Analysis & Computation**: Pandas, NumPy

### 🧠 Methodology and Model

The model used is the **Long Short-Term Memory (LSTM)**, a type of Recurrent Neural Network (RNN) specifically designed to handle problems with sequential data.

**Model Workflow:**

1.  **Data Fetching**: Download historical `TSLA` data.
2.  **Preprocessing**:
      - Use only the `Close` column as the primary feature.
      - Scale the data to a range of [0, 1] using `MinMaxScaler` to help with model convergence.
3.  **Sequence Creation**: Transform the data into sequences. For example, use data from the previous 60 days (`time step = 60`) to predict the data for the 61st day.
4.  **LSTM Model Architecture**: Build a sequential model with several LSTM layers, Dropout layers to prevent overfitting, and a `Dense` layer as the output.
5.  **Training**: Train the model on the training data.
6.  **Evaluation**: Evaluate the model's performance on the test data using the **Root Mean Squared Error (RMSE)** metric and visualize the predicted results against the actual data.

### 🤝 Contributing

Contributions for the improvement and development of this project are welcome. Please **Fork** the repository, create a new **Branch**, make your changes, and submit a **Pull Request**.

### 📄 License

This project is licensed under the **MIT License**.
