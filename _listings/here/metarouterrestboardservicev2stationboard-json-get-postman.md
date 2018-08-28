{
  "info": {
    "name": "HERE Public Transit API Next Nearby Departures from a Station",
    "_postman_id": "4e5f473f-24f3-4723-a235-7815013e1577",
    "description": "*Request a list of next departure times and destinations of a particular station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json` and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained from making a prior call to one of the station search (by name or by geo-coordinates) endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**  `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **strict**  `enum`\n \\- When `strict=1` the board will include only departures from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "All",
      "item": [
        {
          "id": "f1aa82d9-85bb-490a-bea4-3d68ce0de48f",
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
              "id": "14ca1794-b52b-419b-b5d0-ece7d572dfa0"
            }
          ]
        }
      ]
    },
    {
      "name": "Next",
      "item": [
        {
          "id": "d9da883e-d53d-4d48-8b9b-b233f23706c1",
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
              "id": "8ee91d55-5a21-4c0d-a629-e043cceffa57"
            }
          ]
        }
      ]
    }
  ]
}