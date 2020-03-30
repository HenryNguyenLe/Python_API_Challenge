# Global Weather Analysis
## Project Idea
As scientists recognized, due to the angle of the sun beaming at earth, weather conditions are expected to vary with latitudes. Of course, there are other factors contributed to the variation of global climate, but in this project, the main focus is to "examine" the latitude factor.

![Image description](WorldMap.png)

## Languages, Tools and Techniques
* Python | Pandas | MatPlotLib | Gmaps | Google Places API | JSON | NumPy |  SciPy | Math | CityPy 
* List Comprehension | DataFrame | Linear Regression   
Note: CityPy is for looking up nearest cities by geo-coordinates

## Table of Contents
* Images : folder contains all exported plots
* output_data : folder contains database of 500+ cities generated randomly across the globe by CityPy
* .gitignore : contains file names that were not pushed to GitHub
* README.md : overview of projects and outcomes
* WeatherPy.ipynb : source codes to randomly generate cities and analyze global climate 
* VacationPy.ipynb : source codes to find ideal potential vacation location based on weather conditions 
* WorldMap.png : map of the earth embedded in the README.md file

## Process Overview
### File Name : WeatherPy.ipynb
#### Activities
* Randomly create 500+ coordinates/ cities scattered around the world
* Perform analysis on weather conditions at generated locations
* Build JSON to retrieve data from API host and select relevant data
* Plot weather condition parameters and find relationship between weather parameters with latitudes  
        - Temperature (deg-F) vs. Latitude
        - Humidity (%) vs. Latitude
        - Cloudiness (%) vs. Latitude
        - Wind Speed (mph) vs. Latitude

#### Summary of Observations
* Max temperatures occur around the earth's equator and drop off towards the poles
* Out of all linear regression and correlation determinations, Max Temperature has excellent trend line with R**2 ~ 0.9
* Other parameters beside Temperature don't correlate well with linear regression
* Majority of the world has humidity of 60+% regardless of earth polarity. This is indicated by the density of data distribution on the Humidity plot
* Most parts of the world are fairly calm (storms not accounted) with wind speed ~ 15-20 mph. Very few are in the 25+ mph range

### File Name : VacationPy.ipynb
This file is a further step: analyze weather data and find the next ideal location for vacation
The criteria for ideal location:
* Max temperature between 70 & 80 deg-F
* Wind speed less than 10 mph
* "Zero" cloudiness (0.0 %)

#### Activities
* Plot humidity distribution (profile) across the globe by Gmaps module & heatmap_layer
* Locate ideal cities by Google API's near-by search fucntion for hotels within 5,000m or 3.1 miles radius
* Pinpoint hotel locations with gmaps module and marker_layer

#### Summary of Observations
* Quite predictably, the ideal locations are in the Temperate or Coastal climate types
* Out of 500+ cities being analyzed, only a few have hotels within 5,000 meters (3.1 miles). Majority is in Africa (could be an ideal continent for next summer vacation)


