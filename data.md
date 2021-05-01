# Data
## Foursquare data for restaurants
To find areas in a city that has dense amount of restaurants, we are going to use Foursquare data to find the restaurants and use their latitude and longitude to find their locations. 

These locations will be the input for our clustering algorithm to find dense clusters that would be good targets for our initial business investment in each city. 

We'll use **venues** api from FourSquare and search for nearby places given a latitude and longitude. These data will be aggregated for each neighbourhood to create a good repository for the city.