{
  "info": {
    "name": "Amadeus Get Rail Station",
    "_postman_id": "28f144d7-a72b-4534-9a50-ea25f8f946eb",
    "description": "Get rail station",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Airlines",
      "item": [
        {
          "id": "374daf04-b552-47d9-bd1b-a6a470eade78",
          "name": "getAirportsAutocomplete",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/airports/autocomplete?all_airports=%7B%7D&country=%7B%7D&term=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Using the term parameter and given the start of any word in an airport's official name, a city name, or the start of an IATA code, this API provides the full name and IATA location code of the city or airport, for use in flight searches. Only major cities and civilian airports with several commercial flights per week are included by default. The response provides up to 20 possible matches, sorted by importance, in a JQuery UI Autocomplete compatible format. This sample implementation using JQuery UI may help. This API uses data from the OpenTravelData project.\n \nBy only using the country parameter, this API is also able to find all the IATA location codes associated with a country. Both term and country parameters can be used together to filter the results accordingly.          \n\nThe value returned is the IATA location code. The label returned is always in UTF-8 format, with the airport official name (which is often in the native language), in the format of English City Name (if not already included in the airport name)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8168ea2f-e60e-43ae-8a96-25a5a8977731"
            }
          ]
        },
        {
          "id": "4f917bdb-5ee0-44c3-8209-e77468380412",
          "name": "getAirportsNearestRelevant",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/airports/nearest-relevant?latitude=%7B%7D&longitude=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service gives the most relevant airports in a radius of 500 km around the given coordinates. The relevance of an airport is computed by dividing the number of airport movements (take offs and landings) by the distance from the point. This causes the relevance of an airport to increase exponentially as you approach it.\n\nTo minimize response time, all distances are computed as a great-circle distance from the provided coordinates to the airport coordinates, and thus do not take into account traffic conditions, international boundaries, mountains, water, or other elements that might make the a nearby airport hard to reach.\n\nOnly civilian airports with at least several commercial flights per week are included in the results.\n\nThe result is a list of airports sorted by decreasing relevance. It always contains the nearest airport with significant commercial traffic. You can freely download the point of reference information used by this API from the Open Travel Data project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "488038c6-1d9a-476c-adec-35c92d359e38"
            }
          ]
        },
        {
          "id": "04eadbb2-1aec-4e51-afac-f8f48e5bacc8",
          "name": "getFlightsAffiliateSearch",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/flights/affiliate-search?adults=%7B%7D&children=%7B%7D&currency=%7B%7D&departure_date=%7B%7D&destination=%7B%7D&exclude_merchants=%7B%7D&include_merchants=%7B%7D&infants=%7B%7D&max_price=%7B%7D&mobile=%7B%7D&origin=%7B%7D&return_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The Flight Affiliate Search API combines Amadeus' flight search technology with Travel Audience's Connect API partners to provide a unique flight search, where all results come with deep-links to book the flight at a partner's website. The API will let you easily provide the traveler with a path to book flights from your application.\nTravel Audience Connect partners include\n\n  CityJet, Air Europa and TAP in Western Europe,\n  Ural Airlines in Russia, \n  Avianca Brazil  and\n  JAL in East Asia\n\n\nOnly Travel Audience Connect partner airlines are searched. For an up-to-date list of routes, see the route maps on each partners respective websites above. You can earn commission using the deep links provided in the search results if you sign up for an account at connect.travelaudience.com."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "725ccdfc-1269-4e64-bb54-e2eb17e5249e"
            }
          ]
        },
        {
          "id": "0c431789-055e-4102-8abe-beb158d1caaf",
          "name": "getFlightsExtensiveSearch",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/flights/extensive-search?aggregation_mode=%7B%7D&departure_date=%7B%7D&destination=%7B%7D&direct=%7B%7D&duration=%7B%7D&max_price=%7B%7D&one-way=%7B%7D&origin=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The Extensive Flight Search allows you to find the prices of one-way or return flights between two airports over a large number of dates, and for a large variety of stay durations. The search doesn't return exact itineraries, but rather tells you the best price for a flight on a given day, for a stay of a given duration.\n\nThe search is based on our Extreme Search platform, which continually caches a large number of flight search results from a list of origin cities to a variety of destinations. Since it's a cached search, the response time is fast, but not all origin airports are available. Here is a list of the currently supported origin-destination IATA location pairs. We try to keep this list as fresh as possible for you, but be aware that it may not always be exactly up-to-date and it can change without warning.\n\nThat said, a price graph like this provides a powerful bargin shopping tool - allowing travelers with flexible itineraries to identify days on which they can get the cheapest flights to their destinations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9e2e81d1-540c-4207-b7e5-a0c115acf7ac"
            }
          ]
        },
        {
          "id": "aadfd85f-9418-4ba8-af8a-cfa232e200b9",
          "name": "getFlightsInspirationSearch",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/flights/inspiration-search?aggregation_mode=%7B%7D&departure_date=%7B%7D&destination=%7B%7D&direct=%7B%7D&duration=%7B%7D&max_price=%7B%7D&one-way=%7B%7D&origin=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The Inspiration Flight Search allows you to find the prices of one-way and return flights from an origin city without necessarily having a destination, or even a flight date, in mind. The search doesn't return a distinct set of price options, but rather, can tell you the price of flying from a given city to some destination, for a trip of a given duration, that falls within a given date range.\n\nThe search is based on our Extreme Search platform, which continually caches a large number of flight search results from a list of origin cities to a variety of destinations. Since it's a cached search, the response time is fast, but not all origin airports are available. Here is a list of the currently supported origin-destination IATA location pairs. We try to keep this list as fresh as possible for you, but be aware that it may not always be exactly up-to-date and it can change without warning.\n\nDespite this limitation don't underestimate the power of this API. Thanks to its quick response speed you can easily pair it with other APIs to provide a low fare and inspiration for any destination. For example, you can could combine it with a event search API and suggest a total price to see go and see an concert or a game in a selection of cities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "418c8fde-3564-42df-98c5-94fbe5afccec"
            }
          ]
        },
        {
          "id": "af30c646-9ef6-4a99-908d-c69eeec4c32e",
          "name": "getFlightsLowFareSearch",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/flights/low-fare-search?adults=%7B%7D&arrive_by=%7B%7D&children=%7B%7D&currency=%7B%7D&departure_date=%7B%7D&destination=%7B%7D&exclude_airlines=%7B%7D&include_airlines=%7B%7D&infants=%7B%7D&max_price=%7B%7D&nonstop=%7B%7D&number_of_results=%7B%7D&origin=%7B%7D&return_by=%7B%7D&return_date=%7B%7D&travel_class=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This is the low fare search engine Amadeus uses to retrieve the best price for flights, based on our latest Master Pricer Travel Board technology. This document describes how to make a low fare search and how to handle the returned messages.\n\nThe message is composed of multiple results for given request. A result is defined by a unique combination of price, tax, passenger type, fare type, cabin, and availability for each requested segment. \n\nA result is then composed of single or multiple itineraries. Each itinerary is composed of an outbound leg, and, if a return date was specified, an inbound leg. Each leg is composed of a list of one or more flights, that the traveller will be required to take in order to get from the origin airport to the destination airport."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2b44089e-75fa-46bf-bf4b-bea0e9ce572f"
            }
          ]
        }
      ]
    },
    {
      "name": "Cars",
      "item": [
        {
          "id": "5dd13036-aa5b-4eff-9221-8bde0001fcc1",
          "name": "getCarsSearchAirport",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/cars/search-airport?currency=%7B%7D&drop_off=%7B%7D&lang=%7B%7D&location=%7B%7D&pick_up=%7B%7D&provider=%7B%7D&rate_class=%7B%7D&rate_filter=%7B%7D&rate_plan=%7B%7D&vehicle=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "With this API you can find out the price and type of car, for all car rental providers, near a specified airport.\n\nYou can quickly see the locations of car providers near a given airport, and what cars are available to rent, and at what prices. This API is based on our car pricing service that gets live availability from car providers, and is used to power a variety of airline and travel agency websites.\n           \nResults are validated from car providers, and thus response times may take up to 10 seconds (response times are typically about 5s), and the number of concurrent calls is throttled per user to avoid flooding our provider's systems. However, this means the final result is guaranteed to be live and accurate.\n\nThe configuration of this API allows search for car rentals in the rental location where the car is picked up (at the start of the rental), is the same as the one where it will be dropped off."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "999c4b62-4ef9-4dbb-9270-c41c7e8cdbdd"
            }
          ]
        },
        {
          "id": "cc31efc3-6ba4-489e-9a8c-879c8f97dde4",
          "name": "getCarsSearchCircle",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/cars/search-circle?currency=%7B%7D&drop_off=%7B%7D&lang=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&pick_up=%7B%7D&provider=%7B%7D&radius=%7B%7D&rate_class=%7B%7D&rate_filter=%7B%7D&rate_plan=%7B%7D&vehicle=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "With this API you can find out the price and type of car, for all car rental providers, in a specified geographical location.\n\nYou can quickly see the locations of car providers near a given point, and what cars are available to rent, and at what prices. This API is based on our car pricing service that gets live availability from car providers, and is used to power a variety of airline and travel agency websites.\n           \nResults are validated from car providers, and thus response times may take up to 10 seconds (response times are typically about 5s), and the number of concurrent calls is throttled per user to avoid flooding our provider's systems. However, this means the final result is guaranteed to be live and accurate.\n\nThe configuration of this API allows search for car rentals in the rental location where the car is picked up (at the start of the rental), is the same as the one where it will be dropped off."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7fa9824-8b68-4cb7-99b2-ad6f772a4f40"
            }
          ]
        }
      ]
    },
    {
      "name": "Hotels",
      "item": [
        {
          "id": "f051cc6b-869c-4d71-8a49-f5d5e7caadeb",
          "name": "getHotelsSearchAirport",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/hotels/search-airport?all_rooms=%7B%7D&amenity=%7B%7D&chain=%7B%7D&check_in=%7B%7D&check_out=%7B%7D&currency=%7B%7D&lang=%7B%7D&location=%7B%7D&max_rate=%7B%7D&number_of_results=%7B%7D&radius=%7B%7D&show_sold_out=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A fast Hotel shopping API to see which hotels are available in a given area, on a given day and displays their lowest prices. With this API you can find out the price of the cheapest daily rate for all hotels near a given airport.\n\nThis API allows you to quickly see the locations of hotels near a given airport, and what prices in that area look like. Note that hotel images are not available to users outside of Amadeus, as we are not licensed to redistribute them. The API is based on our high-speed hotel pricing cache, which is also used to power the Amadeus Hotel Search Engine application. Results are returned very quickly, response times are generally under 2s. Our cache has great global coverage and is constantly refreshed with the latest prices."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6d25520-af99-4e2f-8c2e-9c38d60e3d5e"
            }
          ]
        },
        {
          "id": "5e859dbf-6194-4519-855b-4f2bf7bcc286",
          "name": "getHotelsSearchBox",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/hotels/search-box?all_rooms=%7B%7D&amenity=%7B%7D&chain=%7B%7D&check_in=%7B%7D&check_out=%7B%7D&currency=%7B%7D&lang=%7B%7D&max_rate=%7B%7D&north_east_corner=%7B%7D&number_of_results=%7B%7D&show_sold_out=%7B%7D&south_west_corner=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A fast Hotel shopping API to see which hotels are available in a given area, on a given day and displays their lowest prices. With this API you can find out the price of the cheapest daily rate for all hotels within a specified geographical region.\n\nThis API allows you to quickly see the hotel locations in a region, and what prices in that area look like,  as well as the check-in and check-out dates, and get a list of up to 140 properties (names, codes, image, amenities) with their locations and rates. Optional parameters such as currency and maximum rates, amenities or hotel chain codes are also available and can be used to narrow down the results. More optional parameters such as show_sold_out & rooms can be used to show sold out rooms and all available rooms.\n            \nThe API is based on our high-speed hotel pricing cache, which is also used to power the Amadeus Hotel Search Engine application. Results are returned very quickly, response times are generally under 2s. Our cache has great global coverage and is constantly refreshed with the latest prices."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3fb2a3f8-f6ab-470d-9ccd-5669912f24d0"
            }
          ]
        },
        {
          "id": "e825ee43-60f1-4955-9395-2704f4e7512d",
          "name": "getHotelsSearchCircle",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/hotels/search-circle?all_rooms=%7B%7D&amenity=%7B%7D&chain=%7B%7D&check_in=%7B%7D&check_out=%7B%7D&currency=%7B%7D&lang=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&max_rate=%7B%7D&number_of_results=%7B%7D&radius=%7B%7D&show_sold_out=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A fast Hotel shopping API to see which hotels are available in a given area, on a given day and displays their lowest prices. With this API you can find out the price of the cheapest daily rate for all hotels within a specified radius of a point.\n\nThis API allows you to quickly see the hotel locations in a region, and what prices in that area look like,  as well as the check-in and check-out dates, and get list of up to 140 properties (names, codes, image, amenities) with their locations and rates. Optional parameters such as currency and maximum rates, amenities or hotel chain codes are also available and can be used to narrow down the results. More optional parameters such as show_sold_out & rooms can be used to show sold out rooms and all available rooms. \n\nThe API is based on our high-speed hotel pricing cache, which is also used to power the Amadeus Hotel Search Engine application. Results are returned very quickly, response times are generally under 2s. Our cache has great global coverage and is constantly refreshed with the latest prices."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "219c00bc-a573-4695-a37c-8d5628921f81"
            }
          ]
        },
        {
          "id": "401c157a-1b07-4e18-b378-f9493357d913",
          "name": "getHotelsPropertyCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.sandbox.amadeus.com",
              "path": [
                "v1.2",
                "hotels/:property_code"
              ],
              "query": [
                {
                  "key": "all_rooms",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "check_in",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "check_out",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "currency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lang",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "show_sold_out",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "property_code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This API allows you to quickly see the detailed information of a single hotel, including descriptions, address, GPS location, amenities, awards, lowest priced room and all room prices and booking information. \n\nThis API gives you more information on a specific property. Optional parameters such as show_sold_out & rooms can be used to show sold out rooms and all available rooms. \n\nThe API is based on our high-speed hotel pricing cache, which is also used to power the Amadeus Hotel Search Engine application. Results are returned very quickly, response times are generally under 2s. Our cache has great global coverage and is constantly refreshed with the latest prices."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68d52bce-3f61-442e-8256-77159a5a912d"
            }
          ]
        }
      ]
    },
    {
      "name": "Location",
      "item": [
        {
          "id": "0c27317c-730d-4f2a-9aaa-fe44869729c1",
          "name": "getLocationCode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.sandbox.amadeus.com",
              "path": [
                "v1.2",
                "location/:code"
              ],
              "variable": [
                {
                  "id": "code",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This service retrieves the location information corresponding to a IATA city or airport code.\n\nWhen provided with an IATA code, the service determines whether this code could relate to a city code, an airport code or both. If the city could contain multiple airports, it will return all possible airports that correspond to that city code.\n\nThis API is based on the Amadeus supported Geobases open-source project. If you wish to make your own database with all IATA location information, in order to get faster reponses, you can download the latest raw data from their github page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4bb3ad01-0940-43cf-90ba-6974274245c6"
            }
          ]
        }
      ]
    },
    {
      "name": "Points",
      "item": [
        {
          "id": "b27eb585-01dc-462c-b879-5286ae2dd464",
          "name": "getPointsOfInterestYapqSearchCircle",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/points-of-interest/yapq-search-circle?category=%7B%7D&geonames=%7B%7D&image_size=%7B%7D&lang=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&number_of_images=%7B%7D&number_of_results=%7B%7D&radius=%7B%7D&social_media=%7B%7D&vibes=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Amadeus has partnered with YapQ to bring you point of interest APIs with the goal of offering you unbiased ratings of landmarks and tourist attractions. YapQ rates places according to their interest on social media and provides Wikipedia content and Geonames ID at a given location. \nYapQ's service indexes millions of points around the world, and provides content in 12 different languages. This allows you to ensure you catch the must-see sights at a specific YapQ supported location.\nEach point of interest comes with links to content, grading information, location and directions to help make discovering your destination easy and fun.\nThis service is still under active development, and the response format may change without warning. We'd be interested in your feedback - send us an email."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fe7b3a36-552d-4c63-b8c7-117e971c956c"
            }
          ]
        },
        {
          "id": "0016aa6a-d302-4b36-9836-8bb0532b1489",
          "name": "getPointsOfInterestYapqSearchText",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/points-of-interest/yapq-search-text?category=%7B%7D&city_name=%7B%7D&geonames=%7B%7D&image_size=%7B%7D&lang=%7B%7D&number_of_images=%7B%7D&number_of_results=%7B%7D&social_media=%7B%7D&vibes=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Amadeus has partnered with YapQ to bring you point of interest APIs with the goal of offering you unbiased ratings of landmarks and tourist attractions. YapQ rates these points according to their interest on social media and provides Wikipedia content and Geonames ID in a given city. \nYapQ's service indexes millions of points around the world, and provides content in 12 different languages. This allows you to ensure you catch the must-see sights in a YapQ supported city.\nEach point of interest comes with links to content, grading information, location and directions to help make discovering your destination easy and fun.\nThis service is still under active development, and the response format may change without warning. We'd be interested in your feedback - send us an email."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d86a73da-79c4-41e9-b06c-0a0f14c0ba64"
            }
          ]
        }
      ]
    },
    {
      "name": "Rail",
      "item": [
        {
          "id": "b4fe6b58-3964-4bd7-a52c-365a41bdff43",
          "name": "getRailStation",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.sandbox.amadeus.com",
              "path": [
                "v1.2",
                "rail-station/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get rail station"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f02e28d4-0cf5-41a7-b4fd-be6f1f7c3c21"
            }
          ]
        }
      ]
    }
  ]
}