# Predicting Citi Bike Rides on different stations   :
# Provide a bike for each rider, who wants it

Data for this project is available on [NYC Citi Bike Website](https://s3.amazonaws.com/tripdata/index.html). Data was cleaned and modified for this project.



# Motivation:
Cycling is fun, healthy, convenient, and relaxing. I like riding bicycles. Especially in big cities like NYC, cycling is more appealing because of accessibility, traffic congestion, crowds, scarcity/non-affordability of parking space etc. I have been riding bicycles since I learned riding them in my teenage. I am not always able to take my own personal bike with me; So I occasionally use Citi bike services. Unfortunately, sometimes I am not able to get a bike from a particular bike station that I have planned earlier  because when I get there I see only empty docking stations, there is no bike available. Then I have to take alternative transportations or go to the nearest next station depending on the situation. 

It has been my desire to find out the bike riding  trend based on different stations and look into details about it to figure out if there is any way of predicting how many bike rides will start from that station and how many bikes will be needed for a particular day/hour to accommodate  customers’ demand. 
So, I chose to analyze this particular dataset of NYC Citi Bike of the  past Twelve months  to understand the trend and statistics of bike riders. 

# Objective  
I am analysing Twelve months of NYC City Citi Bike data ranging from March 2019 to February 2020. There are over 13million rows of data:
Out of 899 bike stations, I have analyzed data of most used bike station- stations ID: 519 (North Parsing Station)  for its trend. I would like to analyze the data and make predictions for how many bikes will be needed for next week or after that given the past riding trends. 

Through this project, I want to help Citi Bike maximize its revenue by applying the most efficient logistics management operations system for efficient utilization of  available resources and inventories. Also, I would like to  see happy and satisfied customers/riders from being able to get bikes from any stations and any time they want. Time Series forecasting model and Linear Regression algorithm along with python packages is used in the project. 

# Process

The data was collected directly from NYC Citi Bike database website. I downloaded the data from [Citi Bike website .](https://s3.amazonaws.com/tripdata/index.html). I analyzed last Twelve months of NYC City Citi Bike data ranging from March 2019 to February 2020. There were over 13million rows of data from which I selected 104 thousand rows of data for station ID: 519 after doing initial EDA.

# Steps taken  for the project:
* Downloaded the data from NYC Citi Bike 
* Converted to dataframe from .csv, cleaned, performed EDA and analyzed the data using Python Pandas and Jupyter notebook
* Created bar charts to visualize hourly, daily, weekly trend. 
* Tried different method to impute missing data
* Linear Regression Model used to predict missing values 
* Used Time Series Forecasting model 
* Observed for Seasonality and Trend to check for stationarity 
* Trained with  ARIMA Model
* Predicted the model with testing sample of last 30 days, and plotted 


# Most rides hourly, daily, weekly

As one would expect, the most rides occured in the evening rush hour around 5pm with second peak during morning rush hour around 9am.
![](img/Total_crashes_2017_.png)

Daily trend over a year: 
![](img/death_plot.png)

Weekly trend: Weekend has lower rides as compared to weekday: 

![](img/top10_reasons_of_crash.png)


# Data Imputation 
Out of considered 365 days, 109 days of data was missing. Five different imputation techniques - Fillmedian, Rolling Median, Interpolate Linear, InterpolateTime, and Linear regression -  were considered and  tested for better prediction for missing values. The different technique has been given 
Rolling Median and InterpolateTIme:
![](img/top10_reasons_of_crash.png)

FillMedian and InterpoleLinear
![](img/top10_reasons_of_crash.png)

Raw data and Linear Regression
![](img/top10_reasons_of_crash.png)

Linear Regression imputation: Decomposition 
![](img/killed_different_st.png)



# ARIMA Model: 
ARIMA (Auto Regressive Integrated Moving Average) model explains a given time series model based on its own past values, that is, its own lags and the lagged forecast errors, so that equation can be used to forecast future values. ARIMA model with parameters (4,1,2) was used to make prediction. 

ARIMA model fit 
![](img/killed_different_st.png)

ARIMA model prediction with 95% confidence interval. 
![](img/street_names.png)

ARIMA residual errors and Density curve :
![](img/killed_different_st.png)
![](img/killed_different_st.png)
# Conclusion :

# What Next? 
* Tune up model
* Where to build next station
* Predict where the biker will return next  from a location
* How many bikes need to add:
Around where bike trailer driver/mechanic should be
* Predict based on  user type,
* Density map, spoke map, one place to many/any station 





