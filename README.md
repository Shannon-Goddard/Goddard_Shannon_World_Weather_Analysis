# Goddard_Shannon_World_Weather_Analysis

## Project Overview
In this module, we’ll practice our analysis, visualization, and statistical skills by retrieving and analyzing weather data for a hypothetical travel company, PlanMyTrip. Successfully completing the tasks will draw on our knowledge of Python, decision and repetition statements, data structures, Pandas, Matplotlib, and SciPy statistics.

## Resources
- Data Source: https://openweathermap.org/api
- Software: Jupyter Notebook, Pandas Library, CityPy, Python Request, APIs, JSON Traversals

## Summary
By the end of this module, we will be able to:
- Perform tasks using new Python libraries and modules.
- Retrieve and use data from an API “get” request to a server.
- Retrieve and store values from a JSON array.
- Use try and except blocks to resolve errors.
- Write Python functions.
- Create scatter plots using the Matplotlib library, and apply styles and features to a plot.
- Perform linear regression, and add regression lines to scatter plots.
- Create heatmaps, and add markers using the Google Maps API.

## Challenge Overview
For the new modifications to the PlanMyTrip app, we are asked to add more data to the database, or cities DataFrame, so that customers know the weather in the cities when they click on a pop-up marker. We’ll also need to add the amount of rainfall or snowfall within the last three hours so that customers can filter the DataFrame using input statements based on the temperature range and whether or not it is raining or snowing. Finally, we’ll need to create a directions layer Google map that shows the directions between multiple cities for travel.

### Objectives:
- Use nested try-except blocks
- Use Pandas methods and attributes on a DataFrame or Series.
- Create a new DataFrame from a new API search with new weather parameters.
- Filter DataFrames based on input and nested decision statements, and logical expressions.
- Create pop-up markers on a Google map from a filtered DataFrame.
- Add a directions layer on a Google map between cities in the filtered DataFrame.

## Challenge Summary
## Part 1
### Get the Weather Description and Amount of Precipitation for Each City

We generated a new set of 1,500 random latitudes and longitudes.<br/>
Got the nearest city using the citipy module.<br/>
Performed an API call with the OpenWeatherMap.<br/>
Retrieved the following information from the API call:<br/> 
- Latitude and longitude
- Maximum temperature
- Percent humidity
- Percent cloudiness
- Wind speed
- Weather description (e.g., clouds, fog, light rain, clear sky)
- Using a try-except block, if it is raining, get the amount of rainfall in inches for the last three hours. If it is not raining, add 0 inches for the city.
- Using a try-except block, if it is snowing, get the amount of snow in inches for the last three hours. If it is not snowing, add 0 inches for the city.
Add the data to a new DataFrame.

Our new DataFrame looks similar to the following image:

### WeatherPy_challenge DataFrame <br/>
| City    | Country | Date | Lat | Lng | Max Temp | Humidity | Cloudiness | Wind Speed | Current Dscription | Rain Inches (last 3 hours | Snow Inches (last 3 hours) |  
| ------- |:--:|:--------------------:|:-------:|:-------:|:-----:|:--:|:--:|:-----:|:----------------:|:-----:| --:|
| Castro  | CL | 2019_08_11 17:25:49  | -42.48  | -73.76  | 48.20 | 61 | 40 | 14.99 | scattered clouds | 0.000 | 0  |
| Lebu    | ET | 2019_08_11 17:25:49  | 8.96    | 38.73   | 58.69 | 83 | 72 | 1.45  | light rain       | 2.187 | 0  |
| Sitka   | US | 2019_08_11 17:25:49  | 37.17   | -99.65  | 90.00 | 46 | 6  | 21.00 | clear sky        | 0.000 | 0  |

## Part 2 
### Have Customers Narrow Their Travel Searches Based on Temperature and Precipitation
We imported the WeatherPy_vacation.csv file from Part 1 as a new DataFrame.
Filter the DataFrame for minimum and maximum temperature preferences, and if the rain or snow accumulation is 0 inches or not using conditional statements. Doing the following: 
- Prompt the customer for the minimum temperature preference.
- Prompt the customer for the maximum temperature preference.
- Prompt the customer to answer if he or she would like it to be raining or not, using input("Do you want it to be raining? (yes/no) ").
- Prompt the customer to answer if he or she would like it to be snowing or not, using input("Do you want it to be snowing? (yes/no) ").

Our new hotel DataFrame looks similar to the following image:

### WeatherPy_challenge DataFrame <br/>
| City    | Country | Max Temp | Current Description | Lat | Lng | Hotel Name |  
| ------- |:-------:|:--------:|:-------------------:|:---:|:---:| ----------:|
| Castro  | CL      | 48.20    | scatterd clouds     | -42.48  | -73.76 | Hotel Gulmarg  | 
| Lebu    | ET      | 58.69    | light rain          | 8.96    | 38.73  | Jolysable      | 
| Sitka   | US      | 90.00    | clearsky            | 37.17   | -99.65 | Village Belart | 
<br/>
From the filtered DataFrame we added the cities to a marker layer map with a pop-up marker for each city that includes: 

- Hotel name
- City
- Country
- Current weather description with the maximum temperature
<br/>
![WeatherPy_vacation_map1](https://github.com/Shannon-Goddard/Goddard_Shannon_World_Weather_Analysis/blob/master/weather_data/WeatherPy_vacation_map1.png)





