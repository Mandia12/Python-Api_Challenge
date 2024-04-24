# Python-Api_Challenge

Description:

This project consists of two parts (WeatherPy and VacationPy) that both interact with apis and work in conjunction with one another. Firstly, Openweathermap is used to select specific data on cities' weather conditions which are then used to generate scatter plots and their linear regressions. The second part uses the same city data frame and creates a visual map with points on the cities. From a more narrowed down version of the same data frame, geoapify's api is used to locate the closest hotel to the cities and another visual map is generated.


WeatherPy Steps:

Citipy is used to collect city names based on random coordinates generated using numpy.

Then looping through the list of city names to search through openweathermap's api database, information on each city including latitude, longitude, max temperature, humidity, cloudiness, and windspeed are collected. All of the information is stored in a dictionary and is then turned into a pandas data frame. 

The data frame is exported as a CSV and then read back in. 

Four scatter plots are created comparing max temperature, humidity, cloudiness, and windspeed to latitude.

The city data frame is then split into two more data frames. One for either hemisphere. The same weather comparisons are made to latitude but now for each hemisphere and with their a plotted linear regression. 

VacationPy Steps:

The city data frame is read into the file and a map is generated showing where the cities are and with the size of their points being fitted to each city's humidity.

Another data frame called "fave_cities" is created from the original city data frame only selecting for the data the meets chosen conditions.

The data in "fave_cities" are used when accessing geoapify's api to find the closest hotel to each city within a 10,000 meter radius. A new map is designed to plot only these cities and to include the closest hotel in the hover message.
