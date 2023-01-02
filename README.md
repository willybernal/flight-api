# flight-api
This project implements an API for flight information (e.g., Airports, Flights, and Airlines). Strapi was used to create and publish the API. The project also demonstrates the use of docker containers and how to run code inside them. The testing for the API was done using Postman: the collection of requests is saved inside the postman folder. Finally, code was generated in Python to send GET requests. The code is included in the vsc folder.

Collection Types:

Airline

|Field Name | Type |Required|
|-----------|------|--------|
|Name       | Text |Yes     |


Airport

|Field Name  | Type |Required|
|------------|------|--------|
|AirportCode | Text |Yes     |
|AirportName | Text |Yes     |
|Country     | Text |Yes     |
|State       | Text |Yes     |
|City        | Text |Yes     |

Flight:

|Field Name         | Type                                                                      |Required|
|-------------------|---------------------------------------------------------------------------|--------|
|FlightNumber       | Text                                                                      |Yes     |
|Airline            | Relation to Collection Type Airline. Flight has one airline.              |Yes     |
|Seats              | Integer                                                                   |Yes     |
|OriginAirport      | Relation to Collection Type Airport. Flight origin has one airport.       |Yes     |
|DestinationAirport | Relation to Collection Type Airport. Flight destination has one airport.  |Yes     |


