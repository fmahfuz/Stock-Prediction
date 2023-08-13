# Stock-Prediction of Microsoft data
The main goal of this project is to build ARIMA model that would analyze and predict Microsoft time series data.

# Dataset
This dataset contains the stock information of Microsoft from 04/01/2015 to 04/01/2021. This data was acquired in google sheets using the command 'GOOGLEFINANCE'

# Data Cleaning
The dataset has 1511 rows and 5 columns with no null values. Upon checking the histogram of the column 'Volume', it was observed that the dataset had some outliers which was removed.

Next, Augumented Dicky Fuller test was performed to check the data was stationary or not. From the test it showed that the p-value is 1.9448635302165584 which is much greater than .05, thus the timeseries is non-stationary.

To make the timeseries stationary, log transform was performed to the timeseries.

# Model selection
ARIMA model was chosen for the model selection. For best p,d,q values for the model we performed a search with lowest AIC score. It was found that p=0,q=0,q=1 performed the best with the lowest AIC score and RMSE.
