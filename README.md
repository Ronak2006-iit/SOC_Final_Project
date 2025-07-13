# SOC_Final_Project
## Project Overview

This project leverages the power of **Long Short-Term Memory (LSTM)** networks to predict stock prices. The model is trained on historical stock data, collected via the `yfinance` library. The goal is to forecast future stock prices based on past trends and user-defined parameters.

## Project Components

- **Notebook File:** `final Project_Ronak_24b4202.ipynb`
- **Language:** Python 3
- **Libraries Used:**  
  - `pandas` for data manipulation  
  - `numpy` for numerical operations  
  - `matplotlib` and `seaborn` for visualizations  
  - `yfinance` for downloading stock data  
  - `tensorflow` for building the LSTM model  
  - `sklearn` for preprocessing and data splitting  

## How the Project Works

1. **User Input:**  
   The program prompts the user for:
   - Stock ticker (e.g., "AAPL" for Apple, "GOOGL" for Alphabet)
   - Start and end dates for fetching the stock data
   - Timeframe (daily, weekly, or monthly)

2. **Data Collection:**  
   The stock data is fetched from Yahoo Finance using the `yfinance` library. The user specifies the timeframe for the data (daily, weekly, or monthly), and the program handles the interval fetching accordingly.

3. **Data Preprocessing:**  
   - Data is normalized using **MinMaxScaler** to scale the values between 0 and 1.
   - The dataset is then split into training and testing sets, preparing the data for the model.

4. **Model Building:**  
   A **Sequential LSTM model** is created using `tensorflow.keras`. The LSTM layers are designed to capture temporal dependencies in the stock price trends, with additional Dense and Dropout layers to prevent overfitting.

5. **Model Training:**  
   The model is trained using the training data, and the loss is calculated over each epoch. The training process optimizes the model's weights to minimize prediction error.

6. **Prediction and Visualization:**  
   After the model is trained, it predicts future stock prices, and the results are visualized by plotting:
   - Actual stock prices vs. predicted values
   - Training loss over epochs

## Instructions to Run

### 1. Install Dependencies

You can install the necessary libraries using `pip`:

```bash
pip install pandas numpy matplotlib seaborn yfinance tensorflow scikit-learn
```

### 2. Run the Jupyter Notebook

- Open the `final Project_Ronak_24b4202.ipynb` in Jupyter Notebook or JupyterLab.
- Run all cells sequentially. The notebook will ask for the following user inputs:
  - **Stock Ticker Symbol** (e.g., "AAPL")
  - **Start Date** (in `YYYY-MM-DD` format)
  - **End Date** (in `YYYY-MM-DD` format)
  - **Timeframe** (choose from daily, weekly, or monthly)

### 3. View Results

- The notebook will generate visualizations comparing predicted stock prices with the actual ones.
- You will also see a graph displaying the loss curve over the epochs, showing how the model improves with training.

## Results

After training, the model's predictions will be displayed alongside actual stock prices. The performance is evaluated based on how well the model fits the training data and how accurately it predicts future values.

## Author

Ronak Solanki  
BTech, Environmental Science Department, IIT Bombay  
24b4202
