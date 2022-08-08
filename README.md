# Time_Series_Forecasting_From_Scratch

## Introduction to Time Series

![image](https://user-images.githubusercontent.com/99672298/183427582-d5790e2c-4793-473f-abec-56004695f926.png)

Timeseries forecasting in simple words means to forecast or to predict the future value over a period of time. There are different approaches to predict the value, consider an example there is a company XYZ records the website traffic in each hour and now wants to forecast the total traffic of the coming hour. If I ask you what will your approach to forecasting the upcoming hour traffic?

A different person can have a different perspective like one can say find the mean of all observations, one can have like take mean of recent two observations, one can say like give more weightage to current observation and less to past, or one can say use interpolation. There are different methods to forecast the values.

while Forecasting time series values, there are some important terms need to be taken care of and the main task of time series forecasting is to forecast these  terms.

![11 07 2022_15 44 34_REC](https://user-images.githubusercontent.com/99672298/183430156-3aaf9246-b8da-4d7b-be03-1eac766d12c8.png)

### 1) **`Seasonality`**

Seasonality is a simple term that means while predicting a time series data there are some months in a particular domain where the output value is at a peak as compared to other months. for example if you observe the data of tours and travels companies of past 3 years then you can see that in November and December the distribution will be very high due to holiday season and festival season. So while forecasting time series data we need to capture this seasonality.

### 2) **`Trend`**

The trend is also one of the important factors which describe that there is certainly increasing or decreasing trend time series, which actually means the value of organization or sales over a period of time and seasonality is increasing or decreasing.

### 3) **`Unexpected Events`**

Unexpected events mean some dynamic changes occur in an organization, or in the market which cannot be captured. for example a current pandemic we are suffering from, and if you observe the Sensex or nifty chart there is a huge decrease in stock price which is an unexpected event that occurs in the surrounding.

Rolling Statistics and Stationarity in Time-series
A stationary time series is a data that has a constant mean and constant variance. If I take a mean of T1 and T2 and compare it with the mean of T4 and T5 then is it the same, and if different, how much difference is there? So, constant mean means this difference should be less, and the same with variance.

If the time series is not stationary, we have to make it stationary and then proceed with modelling. Rolling statistics is help us in making time series stationary. so basically rolling statistics calculates moving average. To calculate the moving average we need to define the window size which is basically how much past values to be considered.

For example, if we take the window as 2 then to calculate a moving average in the above example then, at point T1 it will be blank, at point T2 it will be the mean of T1 and T2, at point T3 mean of T3 and T2, and so on. And after calculating all moving averages if you plot the line above actual values and calculated moving averages then you can see that the plot will be smooth.

![image](https://user-images.githubusercontent.com/99672298/183432317-07e7ba4c-512d-45e7-8465-5ad5b57b82ea.png)
![image](https://user-images.githubusercontent.com/99672298/183432383-d3471d23-38a2-4055-90ee-6c5f1a13c63c.png)

This is one method of making time series stationary, there are other methods also which we are going to study as Exponential smoothing

Methods and algorithms are using which we can capture seasonality and trend But the unexpected event occurs dynamically so capturing this becomes very difficult.
### Synopsis of Time Series Analysis
+ A Time-Series represents a series of time-based orders. It would be Years, Months, Weeks, Days, Horus, Minutes, and Seconds
+ A time series is an observation from the sequence of discrete-time of successive intervals.
+ A time series is a running chart.
+ The time variable/feature is the independent variable and supports the target variable to predict the results.
+ Time Series Analysis (TSA) is used in different fields for time-based predictions – like Weather Forecasting, Financial, Signal processing, Engineering domain – Control Systems, Communications Systems.
+ Since TSA involves producing the set of information in a particular sequence, it makes a distinct from spatial and other analyses.
+ Using AR, MA, ARMA, and ARIMA models, we could predict the future.

