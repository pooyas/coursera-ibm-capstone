# Data
## Foursquare data for restaurants
To find areas in a city that has dense amount of restaurants, we are going to use Foursquare data to find the restaurants and use their latitude and longitude to find their locations. 

These locations will be the input for our clustering algorithm to find dense clusters that would be good targets for our initial business investment in each city. 

We'll use **venues** api from FourSquare and search for nearby places given a latitude and longitude. These data will be aggregated for each neighbourhood to create a good repository for the city.

URL that is going to be used for getting the data:

GET https://api.foursquare.com/v2/venues/search?ll=[LatLong]

Response is going to be:

```
{
  "meta": {
    "code": 200,
    "requestId": "5ac51d7e6a607143d811cecb"
  },
  "response": {
    "venues": [
      {
        "id": "5642aef9498e51025cf4a7a5",
        "name": "Mr. Purple",
        "location": {
          "address": "180 Orchard St",
          "crossStreet": "btwn Houston & Stanton St",
          "lat": 40.72173744277209,
          "lng": -73.98800687282996,
          "labeledLatLngs": [
            {
              "label": "display",
              "lat": 40.72173744277209,
              "lng": -73.98800687282996
            }
          ],
          "distance": 8,
          "postalCode": "10002",
          "cc": "US",
          "city": "New York",
          "state": "NY",
          "country": "United States",
          "formattedAddress": [
            "180 Orchard St (btwn Houston & Stanton St)",
            "New York, NY 10002",
            "United States"
          ]
        },
        "categories": [
          {
            "id": "4bf58dd8d48988d1d5941735",
            "name": "Hotel Bar",
            "pluralName": "Hotel Bars",
            "shortName": "Hotel Bar",
            "icon": {
              "prefix": "https://ss3.4sqi.net/img/categories_v2/travel/hotel_bar_",
              "suffix": ".png"
            },
            "primary": true
          }
        ],
        "venuePage": {
          "id": "150747252"
        }
      }
    ]
  }
}
```

For the purpose of this project, I'm only intereted in latitude and longitude of the restaurants. 