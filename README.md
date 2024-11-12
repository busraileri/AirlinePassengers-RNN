# Airline Passengers - RNN
This project aims to forecast the number of international airline passengers using the International Airline Passengers dataset from Kaggle. 
A Recurrent Neural Network (RNN) is employed to predict future passenger numbers based on historical changes in passenger data.

The [dataset](https://www.kaggle.com/datasets/andreazzini/international-airline-passengers) contains monthly international airline passenger numbers from 1949 to 1960. 
This data can be used to observe the changes in passenger numbers over time and make future predictions.

## Dataset Features:
- Month: Date (in Year-Month format)
- Passengers: The number of passengers carried in that month (in thousands)
## Dataset Size:
- Number of Rows: 144 (12 years, 12 months per year)
- Number of Columns: 2 (Month, Passengers)

## Libraries and Data Loading
- numpy 
- pandas
- tensorflow 
- matplotlib 
- MinMaxScaler for data scaling,
- mean_squared_error to evaluate the model's performance.

## Data Preparation
- **Data Loading:** Data is loaded from a CSV file using Pandas.
- **Data Cleaning:** Missing values and outliers are cleaned.
- **Date Format:** The "Month" column is converted to datetime64 format.
- **Data Normalization:** Passenger numbers are normalized using MinMaxScaler.

## Model Architecture
- **Input Layer:** 1 timestep, 1 feature per timestep.
- **RNN Layer:** 50 units with relu activation function.
- **Dropout Layer:** Dropout rate of 20% to prevent overfitting.
- **Dense Layer:** 1 output unit

The model is trained over 50 epochs, and early stopping is used to prevent overfitting. During training, the loss function is minimized.
The model makes predictions on the test data, and errors are evaluated.
