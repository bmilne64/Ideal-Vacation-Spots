## Ideal Vacation Spots

![](Project/code/VacationPy/images/hotel_map.png)

Map Visualization of Ideal Vacation Spots using APIs

### Dataset:

 [Weather API](https://openweathermap.org/api),  [Google Maps API](https://mapsplatform.google.com/)

## Objective #1: Weather 

### Step 1 - Generate Cities List 

* Create a list of cities from a random set of latitudes and longitudes using citipy

### Step 2 - Perform API Calls

* Perform a weather check on each city using a series of successive API calls
    * Include a print log of each city as it'sbeing processed (with the city number and city name)

![](Project/code/WeatherPy/graph_pngs/list.png)

### Step 3 - Convert Raw Data to DataFrame

*  Export the city data into a .csv
*  Display the DataFrame 

![](Project/code/WeatherPy/graph_pngs/df.png)

### Step 4 - Plot the Data 

* This scatterplot shows the relationship between the cities' latitude and maximum temperature

![](Project/code/WeatherPy/graph_pngs/Lat_Vs_Temp.png)

* This scatterplot shows the relationship between the cities' latitude and humidity

![](Project/code/WeatherPy/graph_pngs/Lat_Vs_Humidity.png)

* This scatterplot shows the relationship between the cities' latitude and cloudiness

![](Project/code/WeatherPy/graph_pngs/Lat_Vs_Cloudiness.png)

* This scatterplot shows the relationship between the cities' latitude and wind speed

![](Project/code/WeatherPy/graph_pngs/Lat_Vs_Wind_Speed.png)

### Step 5 - Linear Regressions 

* This linear regression shows a strong negative correlation between the cities' latitude and maximum temperature in the northern hemisphere
    * As the cities' latitude increases, the maximum temperature decreases

![](Project/code/WeatherPy/graph_pngs/Northern_Hem_Lat_Vs_Temp.png)

* This linear regression shows a strong positive correlation between the cities' latitude and maximum temperature in the southern hemisphere
    * As the cities' latitude increases, the maximum temperature increases
    
![](Project/code/WeatherPy/graph_pngs/Southern_Hem_Lat_Vs_Temp.png)

* This linear regression shows a weak positive correlation between the cities' latitude and humidity in the northern hemisphere
    * As the cities' latitude increases, the humidity also increases slightly
    
![](Project/code/WeatherPy/graph_pngs/Northern_Hem_Lat_Vs_Humidity.png)

* This linear regression shows a weak positive correlation between the cities' latitude and humidity in the southern hemisphere
    * As the cities' latitude increases, the humidity also increases slightly
    
![](Project/code/WeatherPy/graph_pngs/Southern_Hem_Lat_Vs_Humidity.png)

* This linear regression shows a weak positive correlation between the cities' latitude and cloudiness in the northern hemisphere
    * As the cities' latitude increases, the cloudiness also increases slightly
    
![](Project/code/WeatherPy/graph_pngs/Northern_Hem_Lat_Vs_Cloudiness.png)

* This linear regression shows a weak positive correlation between the cities' latitude and cloudiness in the southern hemisphere
    * As the cities' latitude increases, the cloudiness also increases slightly
    
![](Project/code/WeatherPy/graph_pngs/Southern_Hem_Lat_Vs_Cloudiness.png)

* This linear regression shows a very weak positive correlation between the cities' latitude and wind speed in the northern hemisphere
    * As the cities' latitude increases, the wind speed also increases slightly
    
![](Project/code/WeatherPy/graph_pngs/Northern_Hem_Lat_Vs_Wind_Speed.png)

* This linear regression shows a weak negative correlation between the cities' latitude and wind speed in the southern hemisphere
    * As the cities' latitude increases, the wind speed decreases slightly
    
![](Project/code/WeatherPy/graph_pngs/Southern_Hem_Lat_Vs_Wind_Speed.png)

---------------------------------------------------

## Objective #2: Vacation

### Step 1 - Store Part I results into DataFrame

* Load the csv exported in Part I:Weather into a DataFrame

![](Project/code/VacationPy/images/df.png)

### Step 2 - Humidity Heatmap

* Configure gmaps
* Use the Lat and Lng as locations and Humidity as the weight
* Add Heatmap layer to map

![](Project/code/VacationPy/images/heat_map.png)

### Step 3 - Create New DataFrame Fitting Weather Criteria

*  Narrow down the cities to fit weather conditions
    * A max temperature lower than 80 degrees but higher than 70
    * Wind speed less than 10 mph
    * Zero cloudiness
*  Drop any rows will null values

![](Project/code/VacationPy/images/df2.png)

### Step 4 - Create Hotel Map

* Add a "Hotel Name" column to the DataFrame
* Set parameters to search for hotels with 5000 meters
* Hit the Google Places API for each city's coordinates
* Store the first Hotel result into the DataFrame
* Plot markers on top of the heatmap

![](Project/code/VacationPy/images/hotel_map.pngimages/hotel_map.png)

<b>Contact:</b> bronwynmilne64@gmail.com
