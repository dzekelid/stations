{
  "info": {
    "name": "Weatherbit Get Current Station Station",
    "_postman_id": "4ca8960e-bd05-4775-813b-6da1baeb081f",
    "description": "Returns a Current Observation - Given a station ID.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "weather",
      "item": [
        {
          "id": "f17536c7-4b1f-4163-ae6c-a54a1e599108",
          "name": "returns-a-current-observation--given-a-station-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.weatherbit.io",
              "path": [
                "v2.0",
                "current?station=:station"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "lang",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "units",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "station",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a Current Observation - Given a station ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34c8c0ff-5cf0-4ace-868c-55fbfb1abdc9"
            }
          ]
        }
      ]
    }
  ]
}