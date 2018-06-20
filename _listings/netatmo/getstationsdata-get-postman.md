{
  "info": {
    "name": "Netatmo Get Getstationsdata",
    "_postman_id": "58d81b9d-5303-415b-9f55-2e6dc09404b6",
    "description": "The method getstationsdata Returns data from a user Weather Stations (measures and device specific data).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Weather",
      "item": [
        {
          "id": "e18a6ecb-53ea-4b94-be0c-0aa1b3817c92",
          "name": "getstationsdata",
          "request": {
            "url": "http://api.netatmo.net/api/getstationsdata?device_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The method getstationsdata Returns data from a user Weather Stations (measures and device specific data)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8bfb44c-f005-4c34-a465-c2a5b477a8df"
            }
          ]
        }
      ]
    }
  ]
}