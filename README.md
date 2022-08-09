# Time_Series_Forecasting_From_Scratch

## Introduction to Time Series

![image](https://user-images.githubusercontent.com/99672298/183427582-d5790e2c-4793-473f-abec-56004695f926.png)

Time Series Analysis is the way of studying the characteristics of the response variable with respect to time, as the independent variable. To estimate the target variable in the name of predicting or forecasting, use the time variable as the point of reference

Timeseries forecasting in simple words means to forecast or to predict the future value over a period of time. There are different approaches to predict the value, consider an example there is a company XYZ records the website traffic in each hour and now wants to forecast the total traffic of the coming hour. If I ask you what will your approach to forecasting the upcoming hour traffic?

A different person can have a different perspective like one can say find the mean of all observations, one can have like take mean of recent two observations, one can say like give more weightage to current observation and less to past, or one can say use interpolation. There are different methods to forecast the values.

## Time Series – Analysis Vs. Forecasting
Time-series analysis is the scientific extraction of useful information from time-series data to gather insights from it. It consists of a series of data that varies with time. It is non-static in nature. Likewise, it may vary from hours to minutes and even seconds (milliseconds to microseconds). Due to its continuous and non-static nature, working with time-series data is challenging!

As time-series data consists of a series of observations taken in sequences of time, it is entirely non-static in nature.

Thus, it’s a descriptive Vs. predictive strategy based on your time-series problem statement.

In a nutshell, time series analysis is the study of patterns and trends in a time-series data frame by descriptive and inferential statistical methods. Whereas, time series forecasting involves forecasting and extrapolating future trends or values based on old data points (supervised time-series forecasting), clustering them into groups, and predicting future patterns (unsupervised time-series forecasting).

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

Seasonal variations refer to the changes that take place due to the rhythmic forces which operate in a regular and periodic manner. These forces usually have the same or most similar pattern year after year. When we record data weekly, monthly or quarterly, we can see and calculate seasonal variations. Thus, when a time series consists of data only based on annual figures, there will be seen no seasonal variations. These variations may be due to seasons, weather conditions, habits, customs or traditions. For example, in summers the sale of ice-cream increases and at the time of Diwali the sale of diyas, crackers, etc. go up.

### 2) **`Trend`**

The trend is also one of the important factors which describe that there is certainly increasing or decreasing trend time series, which actually means the value of organization or sales over a period of time and seasonality is increasing or decreasing.
 
 Secular trend refers to the general tendency of data to increase or decrease or stagnate over a long period of time. Time series relating to Economic, Business, and Commerce may show an upward or increasing tendency. Whereas, the time series relating to death rates, birth rates, share prices, etc. may show a downward or decreasing tendency
 
### 3) **`Unexpected Events`**

Unexpected events mean some dynamic changes occur in an organization, or in the market which cannot be captured. for example a current pandemic we are suffering from, and if you observe the Sensex or nifty chart there is a huge decrease in stock price which is an unexpected event that occurs in the surrounding.

Methods and algorithms are using which we can capture seasonality and trend But the unexpected event occurs dynamically so capturing this becomes very difficult.

### 4) **`Cyclical:`** In which there is no fixed interval, uncertainty in movement and its pattern

Cyclical variations are due to the ups and downs recurring after a period from time to time. These are due to the business cycle and every organization has to phase all the four phases of a business cycle some time or the other. Prosperity or boom, recession, depression, and recovery are the four phases of a business cycle.

### 5) **`Irregularity:`** Unexpected situations/events/scenarios and spikes in a short time span.

Random variations are fluctuations which are a result of unforeseen and unpredictable forces. These forces operate in an absolutely random or erratic manner and do not have any definite pattern. Thus, these variations may be due to floods, famines, earthquakes, strikes, wars etc.

![image](https://user-images.githubusercontent.com/99672298/183436930-c6338af7-f442-4d3a-a2d5-74f214e03bca.png)

### 6) **`Additive and Multiplicative Time series`**
In the real world, we meet with different kinds of time series data. For this, we must know the concepts of Exponential smoothing and for this first, we need to study types of time series data as additive and multiplicative. As we studied there are 3 components we need to capture as Trend(T), seasonality(S), and Irregularity(I).

Additive time series is a combination(addition) of trend, seasonality, and Irregularity while multiplicative time series is the multiplication of these three terms.

![image](https://user-images.githubusercontent.com/99672298/183433289-da9ff34e-8ace-45b1-85f9-8ab29d95a69f.png)

### 7) **`Rolling Statistics and Stationarity in Time-series`**
A stationary time series is a data that has a constant mean and constant variance. If I take a mean of T1 and T2 and compare it with the mean of T4 and T5 then is it the same, and if different, how much difference is there? So, constant mean means this difference should be less, and the same with variance.

### 8) **`Data Types of Time Series`**
Let’s discuss the time series’ data types and their influence. While discussing TS data-types, there are two major types.
+ **`Stationary`**
+ **`Non- Stationary`**
+ **Stationary: A dataset should follow the below thumb rules, without having Trend, Seasonality, Cyclical, and Irregularity component of time series
The MEAN value of them should be completely constant in the data during the analysis
The VARIANCE should be constant with respect to the time-frame
The COVARIANCE measures the relationship between two variables.**

+ **Non- Stationary: This is just the opposite of Stationary.**
![image](https://user-images.githubusercontent.com/99672298/183439986-f42b4b82-2ba8-4d01-b2cc-1d6b0945ccbf.png)

#### Methods to check Stationarity 
During the TSA model preparation workflow, we must access if the given dataset is Stationary or NOT. Using Statistical and Plots test.
+ **`Statistical Test: There are two tests available to test if the dataset is Stationary or NOT.`**
+ **Augmented Dickey-Fuller (ADF) Test**
+ **Kwiatkowski-Phillips-Schmidt-Shin (KPSS) Test**
+ **Augmented Dickey-Fuller (ADF) Test or Unit Root Test:** The ADF test is the most popular statistical test and with the following assumptions.
+ + Null Hypothesis (H0): Series is non-stationary
+ + Alternate Hypothesis (HA): Series is stationary
+ + p-value >0.05 Fail to reject (H0)
+ + p-value <= 0.05 Accept (H1)
+ **Kwiatkowski–Phillips–Schmidt–Shin (KPSS):** these tests are used for testing a NULL Hypothesis (HO), that will perceive the time-series, as stationary around a deterministic trend against the alternative of a unit root. Since TSA looking for Stationary Data for its further analysis, we have to make sure that the dataset should be stationary.

#### Converting Non- stationary into stationary
Let’s discuss quickly how to convert Non- stationary into stationary for effective time series modeling. There are two major methods available for this conversion.
+ **`Detrending`**
+ **`Differencing`**
+ **`Transformation`**

##### Detrending: It involves removing the trend effects from the given dataset and showing only the differences in values from the trend. it always allows the cyclical patterns to be identified.

##### Differencing: This is a simple transformation of the series into a new time series, which we use to remove the series dependence on time and stabilize the mean of the time series, so trend and seasonality are reduced during this transformation.
Yt= Yt – Yt-1
Yt=Value with time

##### Transformation: This includes three different methods they are Power Transform, Square Root, and Log Transfer., most commonly used one is Log Transfer.

If the time series is not stationary, we have to make it stationary and then proceed with modelling. Rolling statistics is help us in making time series stationary. so basically rolling statistics calculates moving average. To calculate the moving average we need to define the window size which is basically how much past values to be considered.

For example, if we take the window as 2 then to calculate a moving average in the above example then, at point T1 it will be blank, at point T2 it will be the mean of T1 and T2, at point T3 mean of T3 and T2, and so on. And after calculating all moving averages if you plot the line above actual values and calculated moving averages then you can see that the plot will be smooth.

![image](https://user-images.githubusercontent.com/99672298/183432317-07e7ba4c-512d-45e7-8465-5ad5b57b82ea.png)
![image](https://user-images.githubusercontent.com/99672298/183432383-d3471d23-38a2-4055-90ee-6c5f1a13c63c.png)

This is one method of making time series stationary, there are other methods also which we are going to study as Exponential smoothing

### 10) Moving Average Methodology
The commonly used time series method is Moving Average. This method is slick with random short-term variations. Relatively associated with the components of time series.

The Moving Average (MA) (Or) Rolling Mean: In which MA has calculated by taking averaging data of the time-series, within k periods.

Let’s see the types of moving averages:
+ Simple Moving Average (SMA),
+ Cumulative Moving Average (CMA)
+ Exponential Moving Average (EMA)
#### **Simple Moving Average (SMA)**
The SMA is the unweighted mean of the previous M or N points. The selection of sliding window data points, depending on the amount of smoothing is preferred since increasing the value of M or N, improves the smoothing at the expense of accuracy\

![image](https://user-images.githubusercontent.com/99672298/183445596-c9d47c25-1248-440a-9816-62175d094d4d.png)

![image](https://user-images.githubusercontent.com/99672298/183445684-cfa2e9f5-af74-40b9-a355-0643451c757c.png)

#### **Cumulative Moving Average (CMA)**
The CMA is the unweighted mean of past values, till the current time.

![image](https://user-images.githubusercontent.com/99672298/183445809-8bc42ac4-a71e-4d6e-adfc-a6710522617b.png)
![image](https://user-images.githubusercontent.com/99672298/183445834-20a857fd-4330-4c50-b3cf-5b6cacff6c3e.png)

#### **Exponential Moving Average (EMA)**

EMA is mainly used to identify trends and to filter out noise. The weight of elements is decreased gradually over time. This means It gives weight to recent data points, not historical ones. Compared with SMA, the EMA is faster to change and more sensitive.
α –>Smoothing Factor.

Represents the weighting applied to the very recent period.
Lets will apply the exponential moving averages with a smoothing factor of 0.1 and 0.3 in the given dataset.

![image](https://user-images.githubusercontent.com/99672298/183445981-dfd0a717-18b3-430f-8ce9-7e463430b77a.png)
![image](https://user-images.githubusercontent.com/99672298/183446018-531f6fe3-4321-480b-b06e-942db973065a.png)

### 10) **`Time series Exponential Smoothing`**
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

### 11) **`Time Series Analysis in Data Science and Machine Learning`**
When dealing with TSA in Data Science and Machine Learning, there are multiple model options are available. In which the Autoregressive–Moving-Average (ARMA) models with [p, d, and q].
+ P==> autoregressive lags
+ q== moving average lags
+ d==> difference in the order
Before we get to know about Arima, first you should understand the below terms better.

**Autocorrelation** analysis is an important step in the Exploratory Data Analysis of time series forecasting. The autocorrelation analysis helps detect patterns and check for randomness. It’s especially important when you intend to use an autoregressive–moving-average (ARMA) model for forecasting because it helps to determine its parameters. The analysis involves looking at the Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots.

+ **Auto-Correlation Function (ACF)**
+ **Partial Auto-Correlation Function (PACF)**

##### What is correlation?
In statistics, correlation or dependence refers to any statistical association between two random variables or bivariate data, whether causal or not. Correlation refers to any statistical association in the broadest sense, but it actually relates to the degree to which two variables are linearly connected. 

##### Basics of Autocorrelation and Partial Autocorrelation
The degree of resemblance between a certain time series and a lagged version of itself over subsequent time intervals is represented mathematically as autocorrelation. Autocorrelation is similar to the correlation between two different time series in theory, but it uses the same time series twice: once in its original form and again with one or more time periods added.

For example, If it is raining now, the autocorrelation implies that it will also rain tomorrow than if it is rainy today. When it comes to investment, a stock’s positive autocorrelation of returns may be strong, which implies that if it’s up today, it’s more likely to be up tomorrow.

A partial autocorrelation, on the other hand, is a description of the relationship between an observation in a time series and data from earlier time steps that do not take into account the correlations between the intervening observations. The correlation between observations at successive time steps is a linear function of the indirect correlations. These indirect connections are eliminated using the partial autocorrelation function.

**Auto-Correlation Function (ACF):** ACF is used to indicate and how similar a value is within a given time series and the previous value. (OR) It measures the degree of the similarity between a given time series and the lagged version of that time series at different intervals that we observed. This is used to identify a set of trends in the given dataset and the influence of former observed values on the currently observed values.

Autocorrelation is the relationship between two values in a time series. To put it another way, the time series data are correlated, hence the word. “Lags” are the term for these kinds of connections. When a characteristic is measured on a regular basis, such as daily, monthly, or yearly, time-series data is created. 

The number of intervals between two measurements is known as the lag. For example, there is a one-second lag between current and past observations. The lag grows to two if you go back to another interval, and so on.

The observations at yt and yt–k are separated by k time units in mathematical terms. The lag is denoted by K. Depending on the nature of the data, this lag can be measured in days, quarters, or years. When k=1, you’re evaluating observations that are next to each other. 

There is a correlation with each latency. The autocorrelation function (ACF) evaluates the correlation between observations in a time series over a given range of lags. Corr(yt,yt-k), k=1,2,…. gives the ACF for the time series y. We generally use graphs to demonstrate this function

![image](https://user-images.githubusercontent.com/99672298/183568512-2a69fabf-a28a-45cc-9c17-495f8ee6cffa.png)

Blue bars on an ACF plot above are the error bands, and anything within these bars is not statistically significant. It means that correlation values outside of this area are very likely a correlation and not a statistical fluke. The confidence interval is set to 95% by default.

![image](https://user-images.githubusercontent.com/99672298/183568701-da8485d0-48b8-44c4-a45a-ef4c9e62c27f.png)

Notice that for a lag zero, ACF is always equal to one, which makes sense because the signal is always perfectly correlated with itself.

**Partial Auto-Correlation (PACF):** PACF is similar to Auto-Correlation Function and is a little challenging to understand. It always shows the correlation of the sequence with itself with some number of time units per sequence order in which only the direct effect has been shown, and all other intermediary effects are removed from the given time series.

The partial autocorrelation function, like the ACF, indicates only the association between two data that the shorter lags between those observations do not explain. The partial autocorrelation for lag 3 is, for example, merely the correlation that lags 1 and 2 do not explain. In other words, the partial correlation for each lag is the unique correlation between the two observations after the intermediate correlations have been removed.

As previously stated, the autocorrelation function aids in determining the qualities of a time series. The partial autocorrelation function (PACF), on the other hand, is more beneficial during the definition phase for an autoregressive model. Partial autocorrelation plots can be used to specify regression models with time series data as well as Auto-Regressive Integrated Moving Average (ARIMA) models.

![image](https://user-images.githubusercontent.com/99672298/183571802-c1831827-965e-4303-bb42-5382b8cb2a8c.png)

From the above PACF plot if you observe the values at regular intervals, at the 12th lag it is correlated to 0th lag and for 24 lag correlation further decreases and further, it is getting weaker and weaker. 

#### **`Both the ACF and PACF start with a lag of 0, which is the correlation of the time series with itself and therefore results in a correlation of 1.`**

#### **`The difference between ACF and PACF is the inclusion or exclusion of indirect correlations in the calculation.`**

#### **`Additionally, you can see a blue area in the ACF and PACF plots. This blue area depicts the 95% confidence interval and is an indicator of the significance threshold. That means, anything within the blue area is statistically close to zero and anything outside the blue area is statistically non-zero.`**

#### **`The ACF and PACF are used to figure out the order of AR, MA, and ARMA models.`**

#### Interpret ACF and PACF plots

![image](https://user-images.githubusercontent.com/99672298/183576590-f662c1da-9b60-4cbb-ae7e-1cc1008f0510.png)

### Auto-Regressive and Moving Average Models
Auto-Regressive Model

The Auto-Regressive (AR) model assumes that the current value (y_t) is dependent on previous values (y_(t-1), y_(t-2), …). Because of this assumption, we can build a linear regression model. This is a simple model, that predicts future performance based on past performance. mainly used for forecasting, when there is some correlation between values in a given time series and the values that precede and succeed (back and forth).
An AR model is a Linear Regression model, that uses lagged variables as input

![image](https://user-images.githubusercontent.com/99672298/183572275-e42c2d33-e8e1-492c-85f2-bc2db72757bc.png)

Yt =C+b1 Yt-1+ b2 Yt-2+……+ bp Yt-p+ Ert

Key Parameters

p=past values
Yt=Function of different past values
Ert=errors in time
C=intercept

To figure out the order of an AR model, you need to look at the PACF.

### Moving Average Model

The Moving Average (MA) model assumes that the current value (y_t) is dependent on the error terms including the current error (𝜖_t, 𝜖_(t-1),…). Because error terms are random, there’s no linear relationship between the current value and the error terms.

![image](https://user-images.githubusercontent.com/99672298/183572308-bb7b93ac-2d58-4798-aeb1-1e9159abf791.png)

To figure out the order of an MA model, you need to look at the ACF.

Precondition: Stationarity
ACF and PACF assume stationarity of the underlying time series.

### ARMA 
This is a combination of the Auto-Regressive and Moving Average model for forecasting. This model provides a weakly stationary stochastic process in terms of two polynomials, one for the Auto-Regressive and the second for the Moving Average

ARMA is the combination of an Auto-regressive Model and Moving Average Model.

The auto-regressive model is when a time series value is regressed on previous values from the same time series. The underlying mathematical idea is:

Today’s Value = Mean + Slope×Yesterday’s Value+ Noise

The moving average model is a regression on the weighted sum of today’s and yesterday’s noise. The underlying mathematical idea is:

Today’s Value = Mean + Slope×Yesterday’s Noise + Noise

With the mathematical idea of the combined ARMA model being:

Today’s Value= Mean + Noise + AR_Slope×Yesterday’s Value + MA_Slope×Yesterday’s Noise + Noise

Higher order ARMA models look further back than just yesterday, and the order can be different for the AR model and the MA model within the same ARMA.

ARMA requires stationary data, so any trends need to be removed before modeling and then reintroduced to adjust the result (i.e. inverse transform the result by any transforms that were used to remove the trend), and cannot handle seasonality.

**`ARMA is best for predicting stationary series. So ARIMA came in since it supports stationary as well as non-stationary.`**

+ AR ==> Uses the past values to predict the future
+ MA ==> Uses the past error terms in the given series to predict the future
+ I==> uses the differencing of observation and makes the data stationary 
+ AR+I+MA= ARIMA

Understand the Signature of ARIMA
+ p==> log order => No of lag observations.
+ d==> degree of differencing => No of times that the raw observations are differenced.
In an ARIMA model we transform a time series into stationary one(series without trend or seasonality) using differencing
+ q==>order of moving average => the size of the moving average window

![image](https://user-images.githubusercontent.com/99672298/183579676-93dd366e-a796-48e4-8d91-fc836d8bb583.png)

**`SARIMAX`** builds on ARMA, and it can handle Seasonality, Integrates differencing into the model to remove trends, and allows for eXogenous regressors (i.e. predictive features other than the target variable being predicted; there is an important caveat that you must have the exogenous regressor for the period that will be predicted).

**`FBProphet`** is a time series forecasting library released by Facebook. It is easier to implement and tune with more approachable and intuitive parameters and customizations. The API is also more similar to scikit-learn that the StatsModels models discussed previously. It is based on an additive regression model, which is built up from multiple regression models for various time series decomposed from the original one. Its core formulation has 4 separate components to address the time series’ overall trend, weekly seasonality, annual seasonality and holiday behavior (i.e. atypical days).

#### What are the limitations of Time Series Analysis?
Time series has the below-mentioned limitations, we have to take care of those during our analysis,
Similar to other models, the missing values are not supported by TSA
The data points must be linear in their relationship.
Data transformations are mandatory, so a little expensive.
Models mostly work on Uni-variate data.

### Synopsis of Time Series Analysis
+ A Time-Series represents a series of time-based orders. It would be Years, Months, Weeks, Days, Hours, Minutes, and Seconds
+ A time series is an observation from the sequence of discrete-time of successive intervals.
+ A time series is a running chart.
+ The time variable/feature is the independent variable and supports the target variable to predict the results.
+ Time Series Analysis (TSA) is used in different fields for time-based predictions – like Weather Forecasting, Financial, Signal processing, Engineering domain – Control Systems, Communications Systems.
+ Since TSA involves producing the set of information in a particular sequence, it makes a distinct from spatial and other analyses.
+ Using AR, MA, ARMA, and ARIMA models, we could predict the future.

