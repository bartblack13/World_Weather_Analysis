# World_Weather_Analysis
## Overview
The Purpose of this project was to learn how to collect, parse, and use data obtained from making API calls to online servers as part of my Week 6 module for DU Coding Bootcamp.  This project required that I perform the following:
* Perform tasks using new Python libraries and modules.
* Retrieve and use data from an API "get" request to a server.
* Retrieve and store values from a JSON array.
* Use try and except blocks to resolve errors.
* Write Python functions.
* Create scatter plots using the Matplotlib library, and apply styles and features to a plot.
* Perform linear regression, and add regression lines to scatter plots.
* Create heatmaps, and add markers using the Google Maps API.

As a real world scenario, I used the above methods to help develop an app for PlanMyTrip, a mock company.  The app will allow PlanMyTrip to recommend ideal hotels based on clients' weather preferences.  It will also allow users to plan routes to the hotels via embedded google maps.

## Methods
In order to complete the above obective, I made API calls to OpenWeatherMap.org and to Google Map Plateforms.  I used the numpy random function to generate a litst of 1500 random longitude and latitude pairs, then I used the citypy nearest_city function to find the nearest city based on the coordinates list.  This returned a new list of 615 cities.  I then made an api call to openweathermap.org and used JSON to parse collected data, generating a dataframe containing 558 cities, with 9 differnt columns of current information (see Table 1), which was then exported as a csv file for further use.

![This is an image]()
<br />**Table 1**

<br /><br />I then used this csv file to generate multiple scatter plot graphs.  In total I created 4 initial graphs where maximum temperature, humidity, cloudiness, wind speed, were each dependent on Latitude (See Figure 1).  I then sorted the cities by location in the northern or southern hemispheres, generated 8 new graphs, all of which have linear regression plots overlaid on top (See Figure 2).  The linear regressions were calculated by the linregress method from the scipy.stats library. This was done to show any correlation between latitude and the other weather patterns variables.  

![This is an image]()
<br />**Figure 1**<br /><br />

![This is an image]()
<br />**Figure 2**

<br /><br /> After generating the graphs, I used the city data from the csv file to build a heat map showing the temperature for each of the cities (See Figure 3). In order to do this I used the heat_layer function from the gmaps library.  This heat map required that the client using the app input minimum and maximum tempertures for their trip.

As a second interation for this process, I generated a new dataframe and csv that included a current "weather description" column (see Table 2), and I subsequently created a dataframe where a hotel name was listed for each city meeting the client's criteria (see Table 3).  This info was used to create a map with info markers (City name, hotel name, weather descriptions, etc) and route info (see Figures 3 and 4).

![This is an image]()
<br />**Table 2**

<br /><br />

![This is an image]()
<br />**Table 3**
<br /><br />

![This is an image]()
<br />**Figure 3**
<br /><br />

![This is an image]()
<br />**Figure 4**
<br /><br />

## Results
