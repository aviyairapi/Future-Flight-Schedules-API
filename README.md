# Future-Flight-Schedules-API
Future-date airport timetable data with aircraft and flight details, for airports around the world.

<div id="header" align="center">
  <img src="https://media.giphy.com/media/LRZc4dV2kf787nbOB3/giphy.gif" width="100"/>
</div>

[Aviyair’s Future Flight Schedules API](https://aviyair.com/future-flight-schedules-api/) is a JSON REST API that you can use to get future airport timetable data that goes up to 1 year ahead of the current date. The global coverage allows the integration of future flight timetable and airline schedule data by businesses that have focused on the global or any local market. GET requests return fast data, in line with the [Service Level Agreement](https://aviyair.com/service-level-agreement/) of Aviyair. Besides JSON, other formats may be added in the future. Let us know if you have a demand for a specific format!

The API provides future airport schedule data with general information such as the flight number, airline, departure and arrival dettails, originally scheduled flight time and more, in addition to changeable data such as gate, terminal and aircraft based on the most common value of the item.

Get complete future airport schedule data for an airport in a single call or narrow down the data to flights of a certain airline, flight number, status and others. 

--------

## Main Endpoint and Filters with Description

**GET** `https://data.aviyair.com/data/v1/futureschedule?key=[APIKEY]&airport_iata=IAD&type=departure&date =YYYY-MM-DD`

Airport IATA code, date and schedule type (can be either departure or arrival) are obligatory fields. You can add the below filters to narrow down the flights within the schedule. 

| Request Parameter  | Description |
| ------------- | ------------- |
| airport_iata  | The IATA code of the requested airport |
| type  | Schedule type (can be departure or arrival) |
| date | Requested future date |
| departure_iata | IATA code for the departure airport|
| departure_icao | ICAO code for the departure airpor|
| arrival_iata | IATA code for the arrival airport |
| arrival_icao | ICAO code for the arrival airport |
| airline_iata  | Airline IATA code  |
| airline_icao  | Airline ICAO code  |
| flight_number  | Use this filter to track individual flights based on their flight number |

------

## 200 OK Response Example

```
{
  "status": {
    "message": "Success"
  },
  "results": {
    "weekday": "3",
    "departure": {
      "iataCode": "lgw",
      "icaoCode": "egkk",
      "terminal": "s",
      "gate": "2",
      "scheduledTime": "17:45"
    },
    "arrival": {
      "iataCode": "dub",
      "icaoCode": "eidw",
      "terminal": "1",
      "gate": "02",
      "scheduledTime": "19:00"
    },
    "aircraft": {
      "modelCode": "b738",
      "modelText": "boeing 737-8as"
    },
    "airline": {
      "name": "ryanair",
      "iataCode": "fr",
      "icaoCode": "ryr"
    },
    "flight": {
      "number": "113",
      "iataNumber": "fr113",
      "icaoNumber": "ryr113"
    }
  }
} 
```

-------


## Full Documentation

Please visit our [website]( https://aviyair.com/documentation/).

-------

## Most Popular Use Cases

These are the most common use cases for the Future Flight Schedules API but there are no limitations regarding how the API can be useful for you. If you have any concerns about the Terms and Conditions for the future flight schedule data, you may visit the hyperlink below or contact us to ask about it.

-	Travel planning websites and apps where users can select the most desired flight routes for themselves and plan a single or multiple-leg trip.
- 	Flight booking platforms: Users can pick a date and a departure or an arrival airport and see all available flights to choose from. We also have an Autocomplete API with access to the Future Flight Schedules data, so you can display full airport and city names if you’d like.
-	Analysis of the operational efficiency based on the upcoming traffic for that airport or airline and building data-driven solutions to increase this
- 	Airport operation and staff planning and improvements based on air traffic data per terminal or the whole airport
- 	Route efficiency comparison

---------

## License

[Terms and Conditions of Use](https://aviyair.com/terms-and-conditions/) apply. If you have any questions or concerns about your use case of the Future Flight Schedules API, please [contact us](https://aviyair.com/contact-aviyair/). 

--------

## How to Access

The API key to access future flight schedule data is possible by creating an API subscription. The subscriptions do not require any commitments. It is possible to cancel anytime or make changes to your subscription level.

[View the prices and get an API key here.](https://aviyair.com/pricing-subscription-plans/)
