# python-api-challenge

In this project, I used APIs to show the weather conditions of a random set of places in the world, and narrowed those conditions to specific preferences to determine the ideal places to vacation. 

__WeatherPy__
First I created a Python script that randomly selected at least 500 unique (non-repeated) cities based on latitude and longitude.

Second , I performed a weather check on each of the cities using a series of successive API calls. I included a print log of each city as it's being processed, with the city number and city name.

Then I created a series of scatter plots to showcase the following relationships:
* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

Finally, I saved a CSV of all retrieved data and a PNG image for each scatter plot.

__VacationPy__
First, I created a heat map that displays the humidity for every city from WeatherPy.

Second, I narrowed down the DataFrame to fit my ideal weather conditions and dropped any rows that didn't satisfy all three conditions. 
  * A max temperature lower than 80 degrees but higher than 70.
  * Wind speed less than 10 mph.
  * Zero cloudiness.

Then, I used Google Places API to find the first hotel for each city located within 5,000 meters of the coordinates.

Finally, I plotted the hotels on top of the humidity heatmap, with each pin containing the Hotel Name, City, and Country.
