{
  "info": {
    "name": "HERE Public Transit API Find Stations by ID",
    "_postman_id": "13fcd5ec-d0ad-478c-928d-4cb5276fe6e2",
    "description": "*Request details of a specific transit station based on a previous request*\n\nStation details are requested using the `search/by_stopids.json` endpoint and appending a comma delimited list of `stop-ids` to the request URL. Usually, the request to this endpoint will be called after making a station search request, to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**  `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must contain at least 6 characters and must not exceed a maximum of 1000 characters.     The format of a station Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **lang**  `text`\n \\- A language of the response. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "898ba7d8-e244-4a8e-a4cc-a14dcfd46605",
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
              "id": "30043b44-a82b-4fa6-9067-d42aaafbd840"
            }
          ]
        },
        {
          "id": "3a87bd64-dc54-42fd-b3b8-da53a94b166c",
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
              "id": "3cf61541-a8d8-41d7-bce2-58ae76a1d5f9"
            }
          ]
        }
      ]
    }
  ]
}