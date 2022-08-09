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

#### The Time Series Integrants
Any time-series problem or data can be broken down or decomposed into several integrants, which can be useful for performing analysis and forecasting. Transforming time series into a series of integrants is called Time Series Decomposition.

A quick thing worth mentioning is that the integrants are broken further into 2 types-

1. Systematic — components that can be used for predictive modelling and occur recurrently. Level, Trend, and Seasonality come under this category.
2. Non-systematic — components that cannot be used for predictive modelling directly. Noise comes under this category.

while Forecasting time series values, there are some important terms need to be taken care of and the main task of time series forecasting is to forecast these  terms.

![11 07 2022_15 44 34_REC](https://user-images.githubusercontent.com/99672298/183430156-3aaf9246-b8da-4d7b-be03-1eac766d12c8.png)

### 1.) Level — The most common integrant in every time series data is the level. It is nothing but the mean or average value in the time series. It has 0 variances when plotted against itself.

### 2) **`Seasonality`**

Seasonality is a simple term that means while predicting a time series data there are some months in a particular domain where the output value is at a peak as compared to other months. for example if you observe the data of tours and travels companies of past 3 years then you can see that in November and December the distribution will be very high due to holiday season and festival season. So while forecasting time series data we need to capture this seasonality.

Seasonal variations refer to the changes that take place due to the rhythmic forces which operate in a regular and periodic manner. These forces usually have the same or most similar pattern year after year. When we record data weekly, monthly or quarterly, we can see and calculate seasonal variations. Thus, when a time series consists of data only based on annual figures, there will be seen no seasonal variations. These variations may be due to seasons, weather conditions, habits, customs or traditions. For example, in summers the sale of ice-cream increases and at the time of Diwali the sale of diyas, crackers, etc. go up.

Note — If seasonality doesn’t occur at the same frequency, we call it a cycle. A cycle does not have any predefined and fixed signal or frequency is very uncertain, in terms of probability. It may sometimes be random, which poses a great challenge in forecasting.

### 3) **`Trend`**

The trend is also one of the important factors which describe that there is certainly increasing or decreasing trend time series, which actually means the value of organization or sales over a period of time and seasonality is increasing or decreasing.
 
 Secular trend refers to the general tendency of data to increase or decrease or stagnate over a long period of time. Time series relating to Economic, Business, and Commerce may show an upward or increasing tendency. Whereas, the time series relating to death rates, birth rates, share prices, etc. may show a downward or decreasing tendency
 
### 4) **`Unexpected Events`**

Unexpected events mean some dynamic changes occur in an organization, or in the market which cannot be captured. for example a current pandemic we are suffering from, and if you observe the Sensex or nifty chart there is a huge decrease in stock price which is an unexpected event that occurs in the surrounding.

Methods and algorithms are using which we can capture seasonality and trend But the unexpected event occurs dynamically so capturing this becomes very difficult.

### 5) **`Cyclical:`** In which there is no fixed interval, uncertainty in movement and its pattern

 A particular time-series pattern that repeats itself after a large gap or interval of time, like months, years, or even decades.
 
Cyclical variations are due to the ups and downs recurring after a period from time to time. These are due to the business cycle and every organization has to phase all the four phases of a business cycle some time or the other. Prosperity or boom, recession, depression, and recovery are the four phases of a business cycle.

### 6) **`Irregularity:`** Unexpected situations/events/scenarios and spikes in a short time span.

Random variations are fluctuations which are a result of unforeseen and unpredictable forces. These forces operate in an absolutely random or erratic manner and do not have any definite pattern. Thus, these variations may be due to floods, famines, earthquakes, strikes, wars etc.

![image](https://user-images.githubusercontent.com/99672298/183436930-c6338af7-f442-4d3a-a2d5-74f214e03bca.png)

### 7) Noise — A irregularity or noise is a randomly occurring integrant, and it’s optional and arrives under observation if and only if the features are not correlated with each other and, most importantly, variance is the similar across the series. Noise can lead to dirty and messy data and hinder forecasting, hence noise removal or at least reduction is a very important part of the time series data pre-processing stage.

### 8) **`Additive and Multiplicative Time series`**
In the real world, we meet with different kinds of time series data. For this, we must know the concepts of Exponential smoothing and for this first, we need to study types of time series data as additive and multiplicative. As we studied there are 3 components we need to capture as Trend(T), seasonality(S), and Irregularity(I).

The Additive Methodology —

When the time series trend is a linear relationship between integrants, i.e., the frequency (width) and amplitude(height) of the series are the same, the additive rule is applied.

Additive methodology is used when we have a time series where seasonal variation is linear or constant over timestamps.

It can be represented as follows-

y(t) or x(t) = level + trend + seasonality + noise

where the model y(multivariate) or x(univariate) is a function of time t.

The Multiplicative Methodology — 

When the time series is not a linear relationship between integrants, then modelling is done following the multiplicative rule.

The multiplicative methodology is used when we have a time series where seasonal variation increases with time — which may be exponential or quadratic.

It is represented as-

y(t) or x(t)= Level * Trend * Seasonality * Noise

Additive time series is a combination(addition) of trend, seasonality, and Irregularity while multiplicative time series is the multiplication of these three terms.

![image](https://user-images.githubusercontent.com/99672298/183433289-da9ff34e-8ace-45b1-85f9-8ab29d95a69f.png)

### 9) **`Rolling Statistics and Stationarity in Time-series`**
A stationary time series is a data that has a constant mean and constant variance. If I take a mean of T1 and T2 and compare it with the mean of T4 and T5 then is it the same, and if different, how much difference is there? So, constant mean means this difference should be less, and the same with variance.

### 10) **`Data Types of Time Series`**
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

Stationary time series is when the mean and variance are constant over time. It is easier to predict when the series is stationary.

Differencing is a method of transforming a non-stationary time series into a stationary one. This is an important step in preparing data to be used in an ARIMA model.

The first differencing value is the difference between the current time period and the previous time period. If these values fail to revolve around a constant mean and variance then we find the second differencing using the values of the first differencing. We repeat this until we get a stationary series

##### Transformation: This includes three different methods they are Power Transform, Square Root, and Log Transfer., most commonly used one is Log Transfer.

If the time series is not stationary, we have to make it stationary and then proceed with modelling. Rolling statistics is help us in making time series stationary. so basically rolling statistics calculates moving average. To calculate the moving average we need to define the window size which is basically how much past values to be considered.

For example, if we take the window as 2 then to calculate a moving average in the above example then, at point T1 it will be blank, at point T2 it will be the mean of T1 and T2, at point T3 mean of T3 and T2, and so on. And after calculating all moving averages if you plot the line above actual values and calculated moving averages then you can see that the plot will be smooth.

![image](https://user-images.githubusercontent.com/99672298/183432317-07e7ba4c-512d-45e7-8465-5ad5b57b82ea.png)
![image](https://user-images.githubusercontent.com/99672298/183432383-d3471d23-38a2-4055-90ee-6c5f1a13c63c.png)

This is one method of making time series stationary, there are other methods also which we are going to study as Exponential smoothing

### Moving Average Methodology
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

#### Types of Exponential Smoothing
There are three main types of exponential smoothing time series forecasting methods.

A simple method that assumes no systematic structure, an extension that explicitly handles trends, and the most advanced approach that add support for seasonality.

#### Simple Exponential Smoothing
Single Exponential Smoothing, SES for short, also called Simple Exponential Smoothing, is a time series forecasting method for univariate data without a trend or seasonality.

It requires a single parameter, called alpha (a), also called the smoothing factor or smoothing coefficient.

This parameter controls the rate at which the influence of the observations at prior time steps decay exponentially. Alpha is often set to a value between 0 and 1. Large values mean that the model pays attention mainly to the most recent past observations, whereas smaller values mean more of the history is taken into account when making a prediction

A value close to 1 indicates fast learning (that is, only the most recent values influence the forecasts), whereas a value close to 0 indicates slow learning (past observations have a large influence on forecasts).

st = αxt+(1 – α)st-1 = st-1 + α(xt – st-1)

Hyperparameters:

+ Alpha: Smoothing factor for the level.

This method is suitable for forecasting data with no clear trend or seasonal pattern. For example, the data in Figure below do not display any clear trending behaviour or any seasonality. (There is a rise in the last few years, which might suggest a trend. We will consider whether a trended method would be better for this series later in this chapter.) We have already considered the naïve and the average as possible methods for forecasting such data 

![image](https://user-images.githubusercontent.com/99672298/183699903-54cfb5d9-f725-4c6f-b0e4-eace8081cbfa.png)

For example, it may be sensible to attach larger weights to more recent observations than to observations from the distant past. This is exactly the concept behind simple exponential smoothing. Forecasts are calculated using weighted averages, where the weights decrease exponentially as observations come from further in the past — the smallest weights are associated with the oldest observations:

where 0 ≤α ≤ 1 is the smoothing parameter. The one-step-ahead forecast for time T + 1 is a weighted average of all of the observations in the series  1,…,yT . The rate at which the weights decrease is controlled by the parameter α.

The table below shows the weights attached to observations for four different values of α when forecasting using simple exponential smoothing. Note that the sum of the weights even for a small value of α will be approximately one for any reasonable sample size.

![image](https://user-images.githubusercontent.com/99672298/183702145-181c6a69-58a0-4ffe-8c60-95c1b183ab01.png)

For any α between 0 and 1, the weights attached to the observations decrease exponentially as we go back in time, hence the name “exponential smoothing”.

#### Double Exponential Smoothing
Double Exponential Smoothing is an extension to Exponential Smoothing that explicitly adds support for trends in the univariate time series.

In addition to the alpha parameter for controlling smoothing factor for the level, an additional smoothing factor is added to control the decay of the influence of the change in trend called beta (b).

The method supports trends that change in different ways: an additive and a multiplicative, depending on whether the trend is linear or exponential respectively.

Double Exponential Smoothing with an additive trend is classically referred to as Holt’s linear trend model, named for the developer of the method Charles Holt.

Additive Trend: Double Exponential Smoothing with a linear trend.
Multiplicative Trend: Double Exponential Smoothing with an exponential trend.
For longer range (multi-step) forecasts, the trend may continue on unrealistically. As such, it can be useful to dampen the trend over time.

Dampening means reducing the size of the trend over future time steps down to a straight line (no trend).

S1 = x1

B1 = x1-x0

For t>1,

st = αxt + (1 – α)(st-1 + bt-1)

βt = β(st – st-1) + (1 – β)bt-1

Here,

st = smoothed statistic, it is the simple weighted average of current observation xt

st-1 = previous smoothed statistic

α = smoothing factor of data; 0 < α < 1

t = time period

bt = best estimate of trend at time t

β = trend smoothing factor; 0 < β <1

+ Additive Dampening: Dampen a trend linearly.
+ Multiplicative Dampening: Dampen the trend exponentially.

This method involves a forecast equation and two smoothing equations (one for the level and one for the trend):
Forecast equation

![image](https://user-images.githubusercontent.com/99672298/183702888-5ee64b02-28fa-4fdb-a3aa-704d985d6f17.png)
 
##### Hyperparameters:

+ Alpha: Smoothing factor for the level.
+ Beta: Smoothing factor for the trend.
+ Trend Type: Additive or multiplicative.
+ Dampen Type: Additive or multiplicative.
+ Phi: Damping coefficient.

#### Triple Exponential Smoothing

Triple Exponential Smoothing is an extension of Exponential Smoothing that explicitly adds support for seasonality to the univariate time series.

This method is sometimes called Holt-Winters Exponential Smoothing, named for two contributors to the method: Charles Holt and Peter Winters.

In addition to the alpha and beta smoothing factors, a new parameter is added called gamma (g) that controls the influence on the seasonal component.

As with the trend, the seasonality may be modeled as either an additive or multiplicative process for a linear or exponential change in the seasonality.

Additive Seasonality: Triple Exponential Smoothing with a linear seasonality.
Multiplicative Seasonality: Triple Exponential Smoothing with an exponential seasonality.
Triple exponential smoothing is the most advanced variation of exponential smoothing and through configuration, it can also develop double and single exponential smoothing models.

![image](https://user-images.githubusercontent.com/99672298/183703127-e1a4a60f-6117-44aa-a8fd-c141789d6f44.png)

There are two variations to this method that differ in the nature of the seasonal component. The additive method is preferred when the seasonal variations are roughly constant through the series, while the multiplicative method is preferred when the seasonal variations are changing proportional to the level of the series.

![image](https://user-images.githubusercontent.com/99672298/183703623-23c39358-9daf-4e7a-81a6-8aff8df8d69f.png)

##### Hyperparameters:

+ Alpha: Smoothing factor for the level.
+ Beta: Smoothing factor for the trend.
+ Gamma: Smoothing factor for the seasonality.
+ Trend Type: Additive or multiplicative.
+ Dampen Type: Additive or multiplicative.
+ Phi: Damping coefficient.
+ Seasonality Type: Additive or multiplicative.
+ Period: Time steps in seasonal period.

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

In other words, it is a summary of the relationship between an observation in a time series with observations at prior time steps with the relationships of intervening observations removed.

The partial autocorrelation function, like the ACF, indicates only the association between two data that the shorter lags between those observations do not explain. The partial autocorrelation for lag 3 is, for example, merely the correlation that lags 1 and 2 do not explain. In other words, the partial correlation for each lag is the unique correlation between the two observations after the intermediate correlations have been removed.

As previously stated, the autocorrelation function aids in determining the qualities of a time series. The partial autocorrelation function (PACF), on the other hand, is more beneficial during the definition phase for an autoregressive model. Partial autocorrelation plots can be used to specify regression models with time series data as well as Auto-Regressive Integrated Moving Average (ARIMA) models.

![image](https://user-images.githubusercontent.com/99672298/183571802-c1831827-965e-4303-bb42-5382b8cb2a8c.png)

From the above PACF plot if you observe the values at regular intervals, at the 12th lag it is correlated to 0th lag and for 24 lag correlation further decreases and further, it is getting weaker and weaker. 

#### **`Both the ACF and PACF start with a lag of 0, which is the correlation of the time series with itself and therefore results in a correlation of 1.`**

#### **`The difference between ACF and PACF is the inclusion or exclusion of indirect correlations in the calculation.`**

#### **`Additionally, you can see a blue area in the ACF and PACF plots. This blue area depicts the 95% confidence interval and is an indicator of the significance threshold. That means, anything within the blue area is statistically close to zero and anything outside the blue area is statistically non-zero.`**

#### **`The ACF and PACF are used to figure out the order of AR, MA, and ARMA models.`**

#### **`ACF plots show autocorrelation decaying towards zero`**
#### **`PACF plot cuts off quickly towards zero`**

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

Autoregressive Model (AR)
The autoregressive model is a statistical model that expresses the dependence of one variable on an earlier time period. It’s a model where signal $S_{t}$ depends only on its own past values. For example, AR(3) is a model that depends on 3 of its past values and can be written as

 $\begin{align*} S_{t} =\beta_{0} + \beta_{1}S_{t-1} + \beta_{2}S_{t-2} + \beta_{3}S_{t-3} + \epsilon_{t}, \end{align*}$

where $\beta_{0}$, $\beta_{1}, \beta_{2}, \beta_{3}$ are coefficients and $\epsilon_{t}$ is error. We can select the order p for AR(p) model based on significant spikes from the PACF plot. One more indication of the AR process is that the ACF plot decays more slowly.

For instance, we can conclude from the example below that the PACF plot has significant spikes at lags 2 and 3 because of the significant PACF value. In contrast, for everything within the blue band, we don’t have evidence that it’s different from zero. Also, we could try for p other values of lag that are outside of the blue belt. To conclude, everything outside the blue boundary of the PACF plot tell us the order of the AR model:

![image](https://user-images.githubusercontent.com/99672298/183626771-c8fa5ac6-02de-49d1-b7ee-ed4d3fb27ca3.png)

### Moving Average Model

The Moving Average (MA) model assumes that the current value (y_t) is dependent on the error terms including the current error (𝜖_t, 𝜖_(t-1),…). Because error terms are random, there’s no linear relationship between the current value and the error terms.

![image](https://user-images.githubusercontent.com/99672298/183572308-bb7b93ac-2d58-4798-aeb1-1e9159abf791.png)

The moving average model is a time series model that accounts for very short-run autocorrelation. It basically states that the next observation is the mean of every past observation. The order of the moving average model, q, can usually be estimated by looking at the ACF plot of the time series.
To figure out the order of an MA model, you need to look at the ACF.

Moving Average (MA)
The MA(q) model calculates its forecast value by taking a weighted average of past errors. It has the ability to capture trends and patterns in time series data. For example, MA(3) for a signal $S_{t}$ can be formulated as

$\begin{align*} S_{t} = \mu + \epsilon_{t} + \gamma_{1}\epsilon_{t-1} + \gamma_{2}\epsilon_{t-2} + \gamma_{3}\epsilon_{t-3} \end{align*}$

where $\mu$ is the mean of a series, $\gamma_{1}, \gamma_{2}, \gamma_{3}$ are coefficients and $\epsilon_{t}, \epsilon_{t-1}, \epsilon_{t-2}, \epsilon_{t-3}$ are errors that have a normal distribution with mean zero and standard deviation one (sometimes called white noise).

In contrast to the AR model, we can select the order q for model MA(q) from ACF if this plot has a sharp cut-off after lag q. One more indication of the MA process is that the PACF plot decays more quickly.

Similar to selecting p for the AR  model, in order to select the appropriate q order for the MA model, we need to analyze all spikes higher than the blue area. In that sense, from the image below, we can try using q=6 or q=3.

![image](https://user-images.githubusercontent.com/99672298/183629986-247d9cd8-1de2-4cc9-89d1-41133fe94126.png)

Precondition: Stationarity
ACF and PACF assume stationarity of the underlying time series.

### ARMA 
The ARMA(p, q) model is a time series forecasting technique used in economics, statistics, and signal processing to characterize relationships between variables. This model can predict future values based on past values and has two parameters, p and q, which respectively define the order of the autoregressive part (AR) and moving average part (MA).

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

Autoregressive Integrated Moving Average Model: ARIMA(p,d,q)

This model is the same as the previous, except now it has this weird d argument. What does this d stand for? d represents the number of nonseasonal differences needed for stationarity. Simply, d just makes nonstationary data stationary by removing trends!

How do you pick your differencing term?

Usually, small terms are picked for the differencing term. If you pick too high, you will likely cause your model to incorrectly represent your data. Some general rules for picking your differencing term are that differencing should not increase your variance and the autocorrelation of the model should be less than -0.5.

Thus, I tried a few differencing terms and concluded that  
d=1 would be best for the model as it had the lowest variance and the autocorrelation was less than -0.5.

**`ARIMA`**

+ AR ==> Uses the past values to predict the future
+ MA ==> Uses the past error terms in the given series to predict the future
+ I==> uses the differencing of observation and makes the data stationary 
+ AR+I+MA= ARIMA

Understand the Signature of ARIMA
+ p==> log order => No of lag observations.
+ P = Periods to lag for eg: (if P= 3 then we will use the three previous periods of our time series in the autoregressive portion of the calculation) P helps adjust the line that is being fitted to forecast the series
+ Purely autoregressive models resemble a linear regression where the predictive variables are P number of previous periods
+ d==> degree of differencing => No of times that the raw observations are differenced.
+ D = In an ARIMA model we transform a time series into stationary one(series without trend or seasonality) using differencing. D refers to the number of differencing transformations required by the time series to get stationary.
+ In an ARIMA model we transform a time series into stationary one(series without trend or seasonality) using differencing
+ q==>order of moving average => the size of the moving average window
+ Q = This variable denotes the lag of the error component, where error component is a part of the time series not explained by trend or seasonality

![image](https://user-images.githubusercontent.com/99672298/183579676-93dd366e-a796-48e4-8d91-fc836d8bb583.png)

##### Machine Learning Approach for Choosing p, d and q Order
Sometimes it’s very hard and time expensive to find the right order of p, d and q for the ARIMA model by analyzing ACF and PACF plots as we mentioned above. Therefore, there are some easier approaches where it comes to tuning this model. 

Since our search space is not big, usually values p, d and q are not higher than 12, we can apply a popular technique for hyperparameter optimization called grid search. Grid search is simply an exhaustive search through a manually specified subset of the hyperparameter space of a learning algorithm. Basically, it means that this method will try each combination of p and q from the specified subset that we provided.

Also, in order to find the best combination of p, d and q, we need to have some objective function that will measure model performance on a validation set.  Usually, we can use Loss function that purpose. The lower the value of these criteria, the better the model is.

Today, most statistical tools have integrated functionality that is often called “auto ARIMA”.
Usually, we can use AIC and BIC for that purpose. The lower the value of these criteria, the better the model is.

Akaike Information Criteria (AIC)
AIC stands for Akaike Information Criteria, and it’s a statistical measure that we can use to compare different models for their relative quality. It measures the quality of the model in terms of its goodness-of-fit to the data, its simplicity, and how much it relies on the tuning parameters. The formula for AIC is

$\begin{align*} AIC = 2k - 2l, \end{align*}$

where l is a log-likelihood, and k is a number of parameters. For example, the AR(p) model has p+1 parameters. From the formula above, we can conclude that AIC prefers a higher log-likelihood that indicates how strong the model is in fitting the data and a simpler model in terms of parameters.

6.2. Bayesian Information Criteria (BIC)
In addition to AIC, the BIC (Bayesian Information Criteria) uses one more indicator n that defines the number of samples used for fitting. The formula for BIC is

$\begin{align*} BIC = k\log n - 2l. \end{align*}$

**`SARIMAX`** builds on ARMA, and it can handle Seasonality, Integrates differencing into the model to remove trends, and allows for eXogenous regressors (i.e. predictive features other than the target variable being predicted; there is an important caveat that you must have the exogenous regressor for the period that will be predicted).

Designed and developed as a beautiful extension to the ARIMA, SARIMAX or, Seasonal Auto-Regressive Integrated Moving Average with eXogenous factors is a better player than ARIMA in case of highly seasonal time series. There are 4 seasonal components that SARIMAX takes into account.

easonal Autoregressive Integrated Moving Average Model: SARIMA(p,d,q)(P,D,Q)s

The SARIMA model is an extension of the ARIMA model. The only difference now is that this model added on a seasonal component. As we saw, ARIMA is good for making a non-stationary time series stationary by adjusting the trend. However, the SARIMA model can adjust a non-stationary time series by removing trend and seasonality.

As we know:

p - the order of the autoregressive trend
d - the order of the trend differencing
q - the order of the moving average trend
What do (P,D,Q)s mean?

P - the order of the autoregressive seasonality
D - the order of the seasonal differncing
Q - the order of the moving average seasonality
s - the number of periods in your season

In our example, we may not have a SARIMA model because our time series did not have seasonality. Therefore, it may follow a SARIMA(2,1,5)(0,0,0)12.

The s term would be 12 because there would be 12 periods (months) in the season if we had seasonality.

They are -

 1. Seasonal Autoregressive Component

 2. Seasonal Moving Average Component

 3. Seasonal Integrity Order Component

 4. Seasonal Periodicity

Final steps

Step 1 — Check stationarity: If a time series has a trend or seasonality component, it must be made stationary before we can use ARIMA to forecast. .
Step 2 — Difference: If the time series is not stationary, it needs to be stationarized through differencing. Take the first difference, then check for stationarity. Take as many differences as it takes. Make sure you check seasonal differencing as well.
Step 3 — Filter out a validation sample: This will be used to validate how accurate our model is. Use train test validation split to achieve this
Step 4 — Select AR and MA terms: Use the ACF and PACF to decide whether to include an AR term(s), MA term(s), or both.
Step 5 — Build the model: Build the model and set the number of periods to forecast to N (depends on your needs).
Step 6 — Validate model: Compare the predicted values to the actuals in the validation sample.

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

![image](https://user-images.githubusercontent.com/99672298/183704027-c2f3a8e3-a6c6-4363-8427-8c9db99478d6.png)

### What are the advantages of using Time series analysis?

Answer:

#### The advantages of time series analysis are as follows:

+ **Reliability:** Time series analysis uses historical data to represent conditions along with a progressive linear chart. The information or data used is collected over a period of time say, weekly, monthly, quarterly or annually. This makes the data and forecasts reliable.
+ **Seasonal Patterns:** As the data related to a series of periods, it helps us to understand and predict the seasonal pattern. For example, the time series may reveal that the demand for ethnic clothes not only increases during Diwali but also during the wedding season.
+ **Estimation of trends:** The time series analysis helps in the identification of trends. The data tendencies are useful to managers as they show an increase or decrease in sales, production, share prices, etc.
+ **Growth:** Time series analysis helps in the measurement of financial growth. It also helps in measuring the internal growth of an organization that leads to economic growth.

## Resampling
Resampling involves changing the frequency of your time series observations.

Two types of resampling are:

+ Upsampling: Where you increase the frequency of the samples, such as from minutes to seconds.
+ Downsampling: Where you decrease the frequency of the samples, such as from days to months.
In both cases, data must be invented.

In the case of upsampling, care may be needed in determining how the fine-grained observations are calculated using interpolation. In the case of downsampling, care may be needed in selecting the summary statistics used to calculate the new aggregated values.

There are perhaps two main reasons why you may be interested in resampling your time series data:

+ Problem Framing: Resampling may be required if your data is not available at the same frequency that you want to make predictions.
+ Feature Engineering: Resampling can also be used to provide additional structure or insight into the learning problem for supervised learning models.

There is a lot of overlap between these two cases.

For example, you may have daily data and want to predict a monthly problem. You could use the daily data directly or you could downsample it to monthly data and develop your model.

A feature engineering perspective may use observations and summaries of observations from both time scales and more in developing a model.



<div style="display:fill;
            border-radius: false;
            border-style: solid;
            border-color:#000000;
            border-style: false;
            border-width: 2px;
            color:#CF673A;
            font-size:15px;
            font-family: Georgia;
            background-color:#E8DCCC;
            text-align:center;
            letter-spacing:0.1px;
            padding: 0.1em;">

**<h2>♡ Thank you for taking the time ♡**
