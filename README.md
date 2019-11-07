# Goddard_Shannon_World_Weather_Analysis

## Project Overview
As we build a variety of charts, we will leverage our knowledge of Python arrays and turples, and learn how to apply Pandas methods, functions, and conditional expresion, as well as perform mathematical calculations on Series and DataFrames.

By the end of this module, we will be able to:
- Create line, bar, scatter, bubble, pie, and box-and-whiskers plots using Matplotlib.
- Add and modify features of Matplotlib charts.
- Add error bars to line and bar charts.
- Determine mean, median, and mode using Pandas, NumPy, and SciPy statistics.

## Resources
- Data Source: city_data.csv, ride_data.csv 
- Software: Anaconda 4.7.12, PythonData, Jupyter Notebook, Pandas, SciPy, and NumPy

## Summary
![Fig1](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig1.png)<br/>
Bubble charts are useful when presenting financial, population, and weather data because you can add a third and fourth factor to convey more information.
The first two factors are the x- and y-axes data, which we have been using quite frequently. By changing the “dot” into a “bubble,” we are adding a third factor: size. If there is more than one dataset that uses the same axes, we can change the color of each marker for each dataset, which will add a fourth factor: color.

If we look at the final product, we can see that the bubble chart contains three different scatter plots, one for each type of city.

![Fig2](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig2.png)<br/>
we can visualize the summary statistics and determine if there are any outliers by using box-and-whisker plots.

There is one outlier in the urban ride count data. Also, the average number of rides in the rural cities is about 4- and 3.5-times lower per city than the urban and suburban cities, respectively.

![Fig3](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig3.png)<br/>
From the combined box-and-whisker plots, we see that there are no outliers. However, the average fare for rides in the rural cities is about $11 and $5 more per ride than the urban and suburban cities, respectively.

![Fig4](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig4.png)<br/>
The average number of drivers in rural cities is nine to four times less per city than in urban and suburban cities, respectively.

![Fig5](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig5.png)<br/>
Pie charts allow us to depict percentages of categories as wedges of a pie. One limitation of pie charts is that they can only represent one dataset or category. However, pie charts do have a high visual appeal. We can make them even more visually appealing by choosing vibrant colors and giving each pie wedge a label.

The first pie chart we created showcases the percentage of the overall fares for each type of city, where each pie wedge represents the percentage of total fares for each city type

![Fig6](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig6.png)<br/>
The second pie chart we created showcases the percentage of total rides for each type of city, where each pie wedge represents the percentage of total rides for each city type.

![Fig7](https://github.com/Shannon-Goddard/PyBer_Analysis/blob/master/analysis/Fig7.png)<br/>
The final pie chart is the percentage of the total drivers for each city type, where each pie wedge is the percentage of total drivers. 

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
### Part 1
###Get the Weather Description and Amount of Precipitation for Each City

###Our new DataFrame should look similar to the following image:

### WeatherPy_challenge DataFrame <br/>
| City | Country | Date | Lat | Lng| Max Temp | Humidity | Cloudiness | Wind Speed | Current Dscription | Rain Inches (last 3 hours | Snow Inches (last 3 hours) |  
| ------ |:--:|:-------------------:|:------:|:------:|:-----:|:--:|:--:|:-----:|:----------------:|:---------:|
| Castro | CL | 2019_08_11 17:25:49 | -42.48 | -73.76 | 48.20 | 61 | 40 | 14.99 | scattered clouds | 0.000 | 0 |
| Lebu   | ET | 2019_08_11 17:25:49 | 8.96   | 38.73  | 58.69 | 83 | 72 | 1.45  | light rain       | 2.187 | 0 |
| Sitka  | US | 2019_08_11 17:25:49 | 37.17  | -99.65 | 90.00 | 46 | 6  | 21.00 | clear sky        | 0.000 | 0 |




