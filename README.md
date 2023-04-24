# Data Science - Weather and Energy Usage Prediction Model

### This repository is an inductory project in Data Science. Analyzing two datasets, one being about the weather and one being about energy usage, I will be looking for trends and training prediction models to predict future values.

In this Data Science project, I want to analyze the trends between the weather dataset (weather_data.csv) and the energy usage dataset (energy_data.csv). 

The features of the weather dataset (weather_data.csv) are as follows:

* temperature (the current temperature at the time of observation - measured in Celsius)
* icon (a text description of the current weather conditions)
* humidity (the relative humidity at the time of observation, expressed as a percentage)
* visibility (the visibility distance at the time of observation - measured in kilometers)
* summary (a brief text summary of the current weather conditions)
* pressure (the atmospheric pressure at the time of observation - measured in millibars)
* windSpeed (the current wind speed at the time of observation - measured in kilometers per hour)
* cloudCover (the percentage of the sky covered by clouds at the time of observation)
* time (the timestamp of the observation, usually in Unix time format)
* windBearing (the direction that the wind is coming from at the time of observation - measured in degrees)
* dewPoint (the dew point temperature at the time of observation - measured in Celsius)
* precipProbability (the probability of precipitation occurring at the time of observation, expressed as a percentage)

The features of the energy usage dataset (energy_data.csv) are as follows:

* Date & Time (the date and time of the energy usage measurement - format of YYYY-MM-DD HH:MM:SS)
* use [kW] (the total energy usage in kilowatts (kW) at the time of measurement)
* gen [kW] (the total energy generated in kilowatts (kW) at the time of measurement)
* Grid [kW] (the energy supplied to the building from the electrical grid in kilowatts (kW) at the time of measurement)
* AC [kW] (the energy usage of the air conditioning system in kilowatts (kW) at the time of measurement)
* Furnace [kW] (the energy usage of the furnace or heating system in kilowatts (kW) at the time of measurement)
* Cellar Lights [kW] (the energy usage of the cellar lights in kilowatts (kW) at the time of measurement)
* Washer [kW] (the energy usage of the washing machine in kilowatts (kW) at the time of measurement)
* First Floor lights [kW] (the energy usage of the first-floor lights in kilowatts (kW) at the time of measurement)
* Utility Rm + Basement Bath [kW] (The energy usage of the utility room and basement bathroom in kilowatts (kW) at the time of measurement)
* Garage outlets [kW] (the energy usage of the garage outlets in kilowatts (kW) at the time of measurement)
* MBed + KBed outlets [kW] (the energy usage of the master bedroom and kid's bedroom outlets in kilowatts (kW) at the time of measurement)
* Dryer + egauge [kW]: (the energy usage of the dryer and egauge (an electrical measurement device) in kilowatts (kW) at the time of measurement)
* Panel GFI (central vac) [kW] (the energy usage of the central vacuum system in kilowatts (kW) at the time of measurement)
* Home Office (R) [kW] (the energy usage of the home office in kilowatts (kW) at the time of measurement)
* Dining room (R) [kW] (the energy usage of the dining room in kilowatts (kW) at the time of measurement)
* Microwave (R) [kW] (the energy usage of the microwave in kilowatts (kW) at the time of measurement)
* Fridge (R) [kW] (the energy usage of the refrigerator in kilowatts (kW) at the time of measurement)

Because this is a Data Science project, I will be utilizing popular Python libraries such as Pandas and NumPy for data analysis and scientific computing. Pandas is able to create DataFrame objects, which are 2-Dimensional table-like structures, which closely resemble the data visualized within a CSV file. NumPy allows for efficient numerical operations on large datasets, which would otherwise require multiple lines of code to perform the same actions in otherprogramming languages. I will also be utilizing Seaborn and Matplotlib since they are two popular Python libraries that are used for data visualization. While Matplotlib is a low-level library that provides a wide range of visualization tools, Seaborn is a higher-level library that is more user-friendly.

In this Data Science project, there are few tasks to complete, which I have carefully labeled and commented within the Jupyter notebook aka the .ipynb file. I examined the datasets by printing them out, then checking to see if there are any missing values, to which I proceeded to impute values that would keep the mean consistent. I also parsed the time fields to be more usable as a feature of the dataset, whether it be converting the Unix based timestamp to a datetime value or converting Date and Time into separate features.

In this Data Science project, I set up a simple linear regression model to train, and predict the energy usage values for each day in the month of December. The goal was to get an understanding about how the Linear Regression model worked and have an actual applicable use of the model. By creating training and testing sets for both the x and y scales, I was able to utilize a Lienar Regression model from the Scikit-Learn package to predict the values. I also worked with a simple Logistic Regression model from the Scikit-Learn package, where I tried to predict the classification of the temperature in the month of December. My classification was 1 if temperature was greater than or equal to 35, or 0 if temperature was less than 35. 

With both of the models that I set up, the linear regression and logistic regression models, I sent the predicted values or classifications to external csv dumps, which I have provided in the repository labeled as 'Linear_Regression.csv' and 'Logistic_Regression.csv', respectively. The dataframes representing these csv files could be found within the Jupyter Notebook, but you could also check the output files, if desired. 

With the last task, I chose two devices specified within the energy_data.csv dataset and proceeded to analyze the trends of their usage after classifying the time entries based on the time of day it existed on. I classified the day as 1, where day started as 6 AM and ended 7 PM exclusively [6AM, 7PM), and night as 0, where night started at 7 PM and ended 6 AM exclusively [7PM, 6AM). I plotted some trends and gave some descriptions such as the time of day that the device was used more often, and the reasoning that could be made to possibly explain it. Also, there is a plotted lineplot of the device energy usage through the year to see if the mentioned device is used throughout the year or during certain times of the year.

Feel free to check the provided Jupyter/Python notebook to see more about the analysis done on the two datasets, weather_data.csv and energy_data.csv. From the several different plots and the well commented descriptions, you could follow my thought process step-by-step. There are also plenty of explanations to describe the findings with possible reasonings as to why that may be the case. I worked with a linear regression model, along with a logistic regression model, which are good statistial models that are commonly used in data science for predicting outcomes. 
