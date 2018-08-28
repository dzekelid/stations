{
  "info": {
    "name": "Weatherbit Get Current Stations Stations",
    "_postman_id": "aa069ca7-cbd3-4c99-9099-45109041679b",
    "description": "**(Advanced/Advanced+/Enterprise plans only)** Returns a group of Current Observations - Given a list of Station Call IDs.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "weather",
      "item": [
        {
          "id": "0bb8ce42-1c5b-4cd8-bec1-874e875f521d",
          "name": "advancedadvancedenterprise-plans-only-returns-a-group-of-current-observations--given-a-list-of-stati",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.weatherbit.io",
              "path": [
                "v2.0",
                "current?stations=:stations"
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
                  "id": "stations",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "**(Advanced/Advanced+/Enterprise plans only)** Returns a group of Current Observations - Given a list of Station Call IDs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7eaea914-185d-4688-9f7b-30405bce319e"
            }
          ]
        }
      ]
    }
  ]
}