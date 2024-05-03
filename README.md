# Project name: Regression model to predict the Bike sharing demand.

![image](https://github.com/charliethomasct82/Bike_sharing_regression/assets/93368865/495ac807-93d8-421b-8cf2-978de7ebc0ef)


## Problem statement:

> A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:Which variables are significant in predicting the demand for shared bikes.

How well those variables describe the bike demands based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.

Business Goal:

To model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features.They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.


## General Information
Company want to understand the factors affecting the demand for these shared bikes in the American market. 
The company wants to know:Which variables are significant in predicting the demand for shared bikes.

Dataset characteristics
day.csv have the following fields:

- instant: record index
- dteday : date
- season : season (1:spring, 2:summer, 3:fall, 4:winter)
- yr : year (0: 2018, 1:2019)
- mnth : month ( 1 to 12)
- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
+ weathersit : 
    - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
    - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp : temperature in Celsius
- atemp: feeling temperature in Celsius
- hum: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered



 
---  ------      --------------  -----  
 0   instant     731 non-null    int64  
 1   dteday      731 non-null    object 
 2   season      731 non-null    int64  
 3   yr          731 non-null    int64  
 4   mnth        731 non-null    int64  
 5   holiday     731 non-null    int64  
 6   weekday     731 non-null    int64  
 7   workingday  731 non-null    int64  
 8   weathersit  731 non-null    int64  
 9   temp        731 non-null    float64
 10  atemp       731 non-null    float64
 11  hum         731 non-null    float64
 12  windspeed   731 non-null    float64
 13  casual      731 non-null    int64  
 14  registered  731 non-null    int64  
 15  cnt         731 non-null    int64  
dtypes: float64(4), int64(11), object(1)


## Technologies Used 
Anaconda
panda version: 1.2.4
Numpy version: 1.20.1
Seaborn version: 0.11.1
Sk learn libraries
Stats model Libraries
MS-excel


## Linear Model:Findings


Linear equation of Regression model:model_3:
count_rental_bikes = 0.2216 + (0.4399 * temperature_felt) - (0.1316 * season_spring) + (0.0744 * season_winter) + (0.2335 * year_2019) + (0.0449 * month_Mar) - (0.0390 * month_Nov) + (0.0706 * month_Sep) + (0.0604 * month_Sep) - (0.0667 * weather_condition_Cloudy) - (0.2977 * weather_condition_Light_Rain)-(0.3140 * weekday_work_Thu_not_workingday) Interpretation of Coefficients:

Intercept:The Constant value of ‘0.2216’ indicated that, in the absence of all other predictor variables (i.e. when x1,x2...xn =0), The bike rental can still increase by 0.2216 units.

temperature_felt: A coefficient value of ‘0.4399’ indicated that a unit increase in temp variable, increases the bike hire numbers by 0.4399 units.

season_spring: A coefficient value of ‘-0.1316’ indicated that a unit increase in season_spring variable, decreases the bike hire numbers by 0.1316 units.

season_winter: A coefficient value of ‘0.0744 ’ indicated that a unit increase in season_winter variable increases the bike hire numbers by 0.0744 units.

year: A coefficient value of ‘0.2335’ indicated that a unit increase in year variable, increases the bike hire numbers by 0.2335 units.

month_Mar: A coefficient value of ‘0.0499’ indicated that, a unit increase in workingday variable increases the bike hire numbers by 0.0499 units.

month_Nov: A coefficient value of ‘-0.0390’ indicated that, a unit increase in month_Nov variable decreases the bike hire numbers by 0.0390 units.

month_Sep: A coefficient value of ‘0.0706’ indicated that a unit increase in month_Sep variable increases the bike hire numbers by 0.0706 units.

weather_condition_Cloudy: A coefficient value of ‘-0.0667’ indicated that a unit increase in weather_condition_Cloudy variable decreases the bike hire numbers by 0.0667 units.

weather_condition_Light_Rain: A coefficient value of ‘-0.2977’ indicated that a unit increase in weather_condition_Light_Rain variable decreases the bike hire numbers by 0.2977 units.

weekday_work_thu_not_workingday: A coefficient value of ‘-0.3140’ indicated that a unit increase in weather_condition_Light_Rain variable decreases the bike hire numbers by 0.3140 units.

As per our final Model, the top 3 predictor variables that influences the bike booking are:

temperature_felt: A coefficient value of ‘0.4399’ indicated that a unit increase in temp variable, increases the bike hire numbers by 0.4399 units.

week_work_thu_not_workingday: A coefficient value of ‘-0.3140’ indicated that a unit increase in year variable, decreases the bike hire numbers by -0.3140 units.

weather_condition_Light_Rain: A coefficient value of ‘-0.2977’ indicated that a unit increase in weather_condition_Light_Rain variable decreases the bike hire numbers by 0.2977 units.

## Summary of Results:
Key Predictors:
1. Temperature_felt: An increase in temperature leads to a corresponding increase in bike hire numbers. This suggests that warmer weather is associated with higher demand for rental bikes.
2. Week_work_Thu_not_workingday: Thursday being a workday (rather than a non-working day) is associated with a decrease in bike hire numbers. This could imply that people are less likely to rent bikes on weekdays, 
   especially when it's a working day.
3. Weather_condition_Light_Rain: The occurrence of light rain is associated with a decrease in bike hire numbers. This indicates that adverse weather conditions, even mild ones like light rain, can deter people 
   from renting bikes.


## Acknowledgements
Special thanks to Mr. Vikas UnniKKannan to help me understand the linear regression algorithm.


## Contact
Created by [@charliethomasct82] - feel free to contact me!


