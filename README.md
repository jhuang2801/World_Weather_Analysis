
# World_Weather_Analysis
## Objective - the objective of this exercise is to utilize API to create a custom weather map, vacation trip based on the desired weather, and finally a map to draw out the actual trip itinerary using google maps.

### Weather Database
-For the weather database, a new set of 2000 random numbers for latitude and longitudes is generated. These coordinates are then plotted using the citypy module to find the nearest city name. Using weather API, a set of information like max temp, % humidity, cloudiness, and other information are recalled for each city located. If there is no information found for the city in the API, a try/except block is used to skip the city and move on to the next city on the list until all information is obtained for all the city names in the generated randomized list. The final information is then outputed in a CSV filed named "Weather_Database.csv".

### Vacation Search
-From the "Weather_Database_csv" generated from last exercise, the same information is used to retrieve customized weather report based on user input. By filtering max and min tempratures (using user input), the database is then left with cities that are within the user preferred temperature ranges. Using the new list of cities, a list of nearby hotel names are also populated using Google Maps API. Finally the hotel information (hotel name, city, country, and current weather) are generated in a google map figure using markers and in a CSV file named "WeatherPy_vacation". 

### Vacation Itinerary
-From the two above exercises, a vacation itinerary is then created based on start point, 3 middle stops, and then return to the start point as the end point. The coordinates of city and hotel are retrieved from the "WeatherPy_vacation" csv file to generate a customized google map figure containing hotel info (hotel name, city, country, and current weather) as markers for each point on the itinerary (start point, 3 middle stops, and end point).
