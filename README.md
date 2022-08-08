# Time_Series_Forecasting_From_Scratch

## Introduction to Time Series

![image](https://user-images.githubusercontent.com/99672298/183427582-d5790e2c-4793-473f-abec-56004695f926.png)

Time Series Analysis is the way of studying the characteristics of the response variable with respect to time, as the independent variable. To estimate the target variable in the name of predicting or forecasting, use the time variable as the point of reference

Timeseries forecasting in simple words means to forecast or to predict the future value over a period of time. There are different approaches to predict the value, consider an example there is a company XYZ records the website traffic in each hour and now wants to forecast the total traffic of the coming hour. If I ask you what will your approach to forecasting the upcoming hour traffic?

A different person can have a different perspective like one can say find the mean of all observations, one can have like take mean of recent two observations, one can say like give more weightage to current observation and less to past, or one can say use interpolation. There are different methods to forecast the values.

#### How to analyze Time Series?
+ Collecting the data and cleaning it
+ Preparing Visualization with respect to time vs key feature
+ Observing the stationarity of the series
+ Developing charts to understand its nature.
+ Model building – AR, MA, ARMA and ARIMA
+ Extracting insights from prediction

#### Significance of Time Series and its types
+ TSA is the backbone for prediction and forecasting analysis, specific to the time-based problem statements.
+ Analyzing the historical dataset and its patterns.
+ Understanding and matching the current situation with patterns derived from the previous stage.
+ Understanding the factor or factors influencing certain variable(s) in different periods.
+ With help of “Time Series” we can prepare numerous time-based analyses and results.
+ Forecasting
+ Segmentation
+ Classification
+ Descriptive analysis
+ Intervention analysis

while Forecasting time series values, there are some important terms need to be taken care of and the main task of time series forecasting is to forecast these  terms.

![11 07 2022_15 44 34_REC](https://user-images.githubusercontent.com/99672298/183430156-3aaf9246-b8da-4d7b-be03-1eac766d12c8.png)

### 1) **`Seasonality`**

Seasonality is a simple term that means while predicting a time series data there are some months in a particular domain where the output value is at a peak as compared to other months. for example if you observe the data of tours and travels companies of past 3 years then you can see that in November and December the distribution will be very high due to holiday season and festival season. So while forecasting time series data we need to capture this seasonality.

### 2) **`Trend`**

The trend is also one of the important factors which describe that there is certainly increasing or decreasing trend time series, which actually means the value of organization or sales over a period of time and seasonality is increasing or decreasing.

### 3) **`Unexpected Events`**

Unexpected events mean some dynamic changes occur in an organization, or in the market which cannot be captured. for example a current pandemic we are suffering from, and if you observe the Sensex or nifty chart there is a huge decrease in stock price which is an unexpected event that occurs in the surrounding.

Methods and algorithms are using which we can capture seasonality and trend But the unexpected event occurs dynamically so capturing this becomes very difficult.

### 4) **`Cyclical:`** In which there is no fixed interval, uncertainty in movement and its pattern

### 5) **`Irregularity:`** Unexpected situations/events/scenarios and spikes in a short time span.

![image](https://user-images.githubusercontent.com/99672298/183436930-c6338af7-f442-4d3a-a2d5-74f214e03bca.png)

### 6) **`Additive and Multiplicative Time series`**
In the real world, we meet with different kinds of time series data. For this, we must know the concepts of Exponential smoothing and for this first, we need to study types of time series data as additive and multiplicative. As we studied there are 3 components we need to capture as Trend(T), seasonality(S), and Irregularity(I).

Additive time series is a combination(addition) of trend, seasonality, and Irregularity while multiplicative time series is the multiplication of these three terms.

![image](https://user-images.githubusercontent.com/99672298/183433289-da9ff34e-8ace-45b1-85f9-8ab29d95a69f.png)

### 7) **`Rolling Statistics and Stationarity in Time-series`**
A stationary time series is a data that has a constant mean and constant variance. If I take a mean of T1 and T2 and compare it with the mean of T4 and T5 then is it the same, and if different, how much difference is there? So, constant mean means this difference should be less, and the same with variance.

If the time series is not stationary, we have to make it stationary and then proceed with modelling. Rolling statistics is help us in making time series stationary. so basically rolling statistics calculates moving average. To calculate the moving average we need to define the window size which is basically how much past values to be considered.

#### Data Types of Time Series
Let’s discuss the time series’ data types and their influence. While discussing TS data-types, there are two major types.
+ **`Stationary`**
+ **`Non- Stationary`**
+ **Stationary: A dataset should follow the below thumb rules, without having Trend, Seasonality, Cyclical, and Irregularity component of time series
The MEAN value of them should be completely constant in the data during the analysis
The VARIANCE should be constant with respect to the time-frame
The COVARIANCE measures the relationship between two variables.**

+ **Non- Stationary: This is just the opposite of Stationary.**
![image](https://user-images.githubusercontent.com/99672298/183439986-f42b4b82-2ba8-4d01-b2cc-1d6b0945ccbf.png)

For example, if we take the window as 2 then to calculate a moving average in the above example then, at point T1 it will be blank, at point T2 it will be the mean of T1 and T2, at point T3 mean of T3 and T2, and so on. And after calculating all moving averages if you plot the line above actual values and calculated moving averages then you can see that the plot will be smooth.

![image](https://user-images.githubusercontent.com/99672298/183432317-07e7ba4c-512d-45e7-8465-5ad5b57b82ea.png)
![image](https://user-images.githubusercontent.com/99672298/183432383-d3471d23-38a2-4055-90ee-6c5f1a13c63c.png)

This is one method of making time series stationary, there are other methods also which we are going to study as Exponential smoothing

### 8) **`Time series Exponential Smoothing`**
Exponential smoothing calculates the moving average by considering more past values and give them weightage as per their occurrence, as recent observation gets more weightage compared to past observation so that the prediction is accurate. hence the formula of exponential smoothing can be defined as.

         yT = α * XT + α(1−α) * yT−1

Alpha is a hyperparameter that defines the weightage to give. This is known as simple exponential smoothing, But we need to capture trend and seasonality components so there is double exponential smoothing which is used to capture the trend components. only a little bit of modification in the above equation is there.

        Yt =  α * Xt + (1-α) (yt-1 + bt-1)  #trend component

        where, bt = beta * (Yt – Yt-1) +  (1-beta) * bt-1

hence here we are taking 2 past observations and what was in the previous cycle, which means we are taking two consecutive sequences, so this equation will give us the trend factor.

If we need to capture trend and seasonality for both components then it is known as triple exponential smoothing which adds another layer on top of trend exponential smoothing where we need to calculate trend and seasonality for both.

        Y = alpha * (Xt / Ct-1) + (1 – alpha)*(Y t-1 + bt-1)

       where, ct = gamma * (xt/yt) + (1-alpha) * ct-alpha

here we are capturing trends as well as seasonality. Using smoothing we will be able to decompose our time series data and our time-series data will become easy to work with because in real-world scenarios working with time series is a complex task so you have to adopt such methods to make the process smooth.

#### What are the limitations of Time Series Analysis?
Time series has the below-mentioned limitations, we have to take care of those during our analysis,
Similar to other models, the missing values are not supported by TSA
The data points must be linear in their relationship.
Data transformations are mandatory, so a little expensive.
Models mostly work on Uni-variate data.

### Synopsis of Time Series Analysis
+ A Time-Series represents a series of time-based orders. It would be Years, Months, Weeks, Days, Horus, Minutes, and Seconds
+ A time series is an observation from the sequence of discrete-time of successive intervals.
+ A time series is a running chart.
+ The time variable/feature is the independent variable and supports the target variable to predict the results.
+ Time Series Analysis (TSA) is used in different fields for time-based predictions – like Weather Forecasting, Financial, Signal processing, Engineering domain – Control Systems, Communications Systems.
+ Since TSA involves producing the set of information in a particular sequence, it makes a distinct from spatial and other analyses.
+ Using AR, MA, ARMA, and ARIMA models, we could predict the future.

