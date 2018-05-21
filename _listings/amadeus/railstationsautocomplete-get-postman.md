{
  "info": {
    "name": "Amadeus Get Rail Stations Autocomplete",
    "_postman_id": "f3979aa4-11e0-4d14-9f47-09ff5421bf5b",
    "description": "Given the start of any word in a rail station's official name, as a term, this API provides the full name and rail station ID of a rail station for use in searches. The response provides an array of up to 20 possible matches, sorted by passenger traffic, in a JQuery Autocomplete compatible format.\n\nThe value returned is the UIC station code. The label returned is always in UTF-8 format, with the station's official name (which is often in the native language). Agglomeration station codes may also be returned.\n\nNote that only French and Italian rail stations are supported by the Rail Station Autocomplete API",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "rail",
      "item": [
        {
          "id": "10d6dcf8-110d-443f-b16b-3c9edd0c6d69",
          "name": "getRailStationsAutocomplete",
          "request": {
            "url": "http://api.sandbox.amadeus.com/v1.2/rail-stations/autocomplete?term=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Given the start of any word in a rail station's official name, as a term, this API provides the full name and rail station ID of a rail station for use in searches"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7d70f9de-5aaa-483d-b486-ce93639f245c"
            }
          ]
        }
      ]
    }
  ]
}