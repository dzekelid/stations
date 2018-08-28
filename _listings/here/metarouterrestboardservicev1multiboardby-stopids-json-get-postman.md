{
  "info": {
    "name": "HERE Public Transit API All Next Departures for a list of Stations",
    "_postman_id": "49213584-95cc-4231-b1b6-cfc17c7a6a9c",
    "description": "*Request a list of all next departure times and destinations for a give list of stations.*\n\nAll next departures for a list of stations can be requested using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json` and specifying a `time` and `stopIds.`  \nThe maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.     The default value is 40.    \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required.     The default value is 40.    \n\n* **stopIds**  `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must contain\n at least 6 characters and must not exceed a maximum of 1000 characters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "c9d5ad10-0ab0-4679-88ed-b9df15b53ca9",
          "name": "SearchByNameJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_name.json?app_code=%7B%7D&app_id=%7B%7D&max=%7B%7D&method=%7B%7D&name=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of public transit stations based on name*\n\nA station search request can be made using the `search/by_name.json` endpoint and adding the `name` parameter. The focal point of the search is defined using the `x` and `y` parameters. The number of results can be further restricted by `max `and the `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **name**  `text`\n \\- Specifies the name or a part of the name of the station to search for and can be one word, multiple words or partial word separated by either comma or space.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum number of stations/stops included in the response.\n  The minimum value is 1 and the maximum value is not limited.\n  The default value is 5.     \n\n* **method**  `enum`\n \\- Specifies if the matching method is *fuzzy* or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy - search for stations with the name having similar sounding and/or similar spelling to the names requested\n    * strict - search for stations with the name exactly matching the names requested or contains it as its part.\n\n   Valid values are : `fuzzy`, `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with a center point defines the area of the search. The minimum value is 0 and the maximum value is not limited.\n  The default value is 20000km."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "99ddc384-98b2-443f-b7be-259211519a3d"
            }
          ]
        },
        {
          "id": "a928312c-e785-4ea3-92ef-c792f9b37966",
          "name": "SearchByStopidsJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_stopids.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&stopIds=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request details of a specific transit station based on a previous request*\n\nStation details are requested using the `search/by_stopids.json` endpoint and appending a comma delimited list of `stop-ids` to the request URL. Usually, the request to this endpoint will be called after making a station search request, to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**  `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must contain at least 6 characters and must not exceed a maximum of 1000 characters.     The format of a station Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **lang**  `text`\n \\- A language of the response. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4b20472e-5616-45dc-8c50-487e0c87ede2"
            }
          ]
        },
        {
          "id": "526b9d5b-14d8-469d-b1af-2cff676dd425",
          "name": "SearchByGeocoordJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_geocoord.json?app_code=%7B%7D&app_id=%7B%7D&max=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of public transit stations within a given geo-location.*\n\nTo find the nearest stations use the `search/by_geocoord.json` endpoint specifying a center point using the `x` and `y` parameters and a search radius in meters using the `radius` parameter. `Max` value can also be used to restrict the number of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with the geo-coordinates defines the area of the search. The default value is 500m.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum number of stations/stops included in the response. \n          The default value is 5. The minimum value is 1 and the maximum value is not limited."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5677c02f-9f58-46d2-ba07-6c9ae3a8ef3b"
            }
          ]
        },
        {
          "id": "a96858b9-68ae-42f1-8a3d-10b71d322d90",
          "name": "CoverageV1CityJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/city.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of transit operators available in cities nearby*\n\nCity coverage can be found using the `coverage/v1/city.json` endpoint. The `x` and `y` parameters specify the location of the search.\n  The response also includes the number of transit lines and transit stops available for each city.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with a center point defines the area of the search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8905ebe-37d3-449f-91a9-c25910a83aa9"
            }
          ]
        }
      ]
    },
    {
      "name": "Avoid",
      "item": [
        {
          "id": "a990bf60-f974-4833-bd98-39c38ad7c51a",
          "name": "MetarouterRestRouteserviceV2RouteJsonGet8",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/routeservice/v2/route.json?app_code=%7B%7D&app_id=%7B%7D&changes=%7B%7D&destX=%7B%7D&destY=%7B%7D&routing=%7B%7D&startX=%7B%7D&startY=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a direct public transit route excluding changes and transfers*\n\nPublic transit routes can be requested using the `metarouter/rest/routeservice/v2/route.json` endpoint. The `changes `parameter is used to indicate the number of changes or transfers desired. \n\n\n\n* **startX**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`\n\n* **destX**  `number`\n \\- The longitude of the destination point of your journey.    e.g. `13.377`\n\n* **destY**  `number`\n \\- The latitude of the destination point of your journey.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **routing**  `enum`\n \\- Type of routing response required.  tt: time-table routing, i.e. route response will show scheduled arrival/departure times of the transit at the stations.  sr: simple (or estimated) routing, i.e. route response will only show \nthe transit journey but without scheduled arrival/departure times.  all: for both estimated and time-table routing.  Default: tt  \n\n    Valid values are : `tt`, `sr`, `all`\n\n* **changes**  `enum`\n \\- Maximum number of changes or transfers. \n                Valid values: 0-6 or -1. Default: -1 (any number of transfers permitted).\n\n    >**NOTE:** In areas where this parameter is not supported the route response will show an attribute `sup_changes=0` in the `Connections` node.\n\n    Valid values are : `-1`, `0`, `1`, `2`, `3`, `4`, `5`, `6`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c501dbbd-b893-4830-9aa2-d61aa0f8ade2"
            }
          ]
        }
      ]
    },
    {
      "name": "Reachability",
      "item": [
        {
          "id": "96e88677-e833-4550-a629-26bf13311c8a",
          "name": "IsochroneV1SearchJsonGet2",
          "request": {
            "url": "http://cit.transit.api.here.com/isochrone/v1/search.json?app_code=%7B%7D&app_id=%7B%7D&max_dur=%7B%7D&time=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of the public transit stations that can be reached in a given time*\n\nTo find the stations reachable in a specified time use the `isochrone/v1/search.json` endpoint specifying a center point using the `x` and `y` parameters and a maximum total duration in minutes using the `max_dur `parameter.\n  \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the journeys, in minutes.   Minimum = 5, Maximum = 90.    The default duration is 15 minutes.    \n\n* **y**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`  \n\n* **x**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`    \n\n* **time**  `text`\n \\- Specifies the time in ISO 8601 (for example, 2015-10-18T06:36:40)\n        format. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b115c7c-2ab8-4c29-8316-6ebf424317cb"
            }
          ]
        }
      ]
    },
    {
      "name": "All",
      "item": [
        {
          "id": "0f7a3135-d974-47c1-8440-136f473fd394",
          "name": "MetarouterRestBoardserviceV1MultiboardJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/boardservice/v1/multiboard.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&max=%7B%7D&max_stn=%7B%7D&prod=%7B%7D&startX=%7B%7D&startY=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of all next departure times and destinations from a location.*\n\nAll next departures information can be requested using the `metarouter/rest/boardservice/v1/multiboard.json` and specifying a `time` and `coordinates. `The maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n  <b>NOTE:</b> This API has been deprecated and replaced with 2 new endpoints. Please see \n  <b><i>All Next Departures from a Location </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for more details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **startX**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.    The default value is 40.  \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required. The default value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains  \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined  \n  The default is 1111111111111111, meaning all supported transit types are permitted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06339b03-7b8b-40d5-aee4-3b250393dad5"
            }
          ]
        },
        {
          "id": "597fdd25-1ca6-4451-a017-9fb1881ea279",
          "name": "MetarouterRestBoardserviceV1MultiboardByStopidsJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/boardservice/v1/multiboard/by_stopids.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&max=%7B%7D&max_stn=%7B%7D&stopIds=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of all next departure times and destinations for a give list of stations.*\n\nAll next departures for a list of stations can be requested using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json` and specifying a `time` and `stopIds.`  \nThe maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.     The default value is 40.    \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required.     The default value is 40.    \n\n* **stopIds**  `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must contain\n at least 6 characters and must not exceed a maximum of 1000 characters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90ef8496-a36e-4a80-9cd9-a6fccc7b278d"
            }
          ]
        }
      ]
    },
    {
      "name": "Transit",
      "item": [
        {
          "id": "ffc4aadd-b3f4-4791-a3fe-93dca4f710e2",
          "name": "CoverageV1NearbyJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/nearby.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&details=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of transit operators and station coverage nearby*\n\nOperator coverage is requested using the `coverage/v1/nearby.json` endpoint specifying the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5976104c-f445-4e75-af4a-f7ddde8a20dc"
            }
          ]
        },
        {
          "id": "5aaca723-350f-4b82-b989-5a1244366af4",
          "name": "CoverageV1SearchJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/search.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&details=%7B%7D&lang=%7B%7D&max=%7B%7D&q=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of transit operator coverage within a specified city*\n\nA list of operators working within a city is requested using the `coverage/v1/search.json` endpoint. The city is specified using the  `q` parameter.\n\n\n\n* **q**  `text`\n \\- The name or a part of the name of the city to search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Maximum number of results to be returned. Default is null.\n\n* **details**  `enum`\n \\- With this value set to 1, the list of supported operators and population of the city is returned.   When the value is set to 0, only the list of matching city names will be returned.  Default value = 1\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.      \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **lang**  `text`\n \\- The language of the response. The value complies with the ISO 639-1 standard and defaults to <i>en</i>."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "da04905e-c8f7-4358-a613-5aefeb4fe1dc"
            }
          ]
        }
      ]
    },
    {
      "name": "Next",
      "item": [
        {
          "id": "41b88142-258e-49f4-afdb-617043292cce",
          "name": "MetarouterRestBoardserviceV2StationboardJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/boardservice/v2/stationboard.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&stnId=%7B%7D&strict=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of next departure times and destinations of a particular station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json` and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained from making a prior call to one of the station search (by name or by geo-coordinates) endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**  `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **strict**  `enum`\n \\- When `strict=1` the board will include only departures from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f401c17-b645-4f2f-941e-d1078353a9a5"
            }
          ]
        }
      ]
    }
  ]
}