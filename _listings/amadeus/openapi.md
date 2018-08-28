swagger: "2.0"
x-collection-name: Amadeus
x-complete: 1
info:
  title: Amadeus
  description: amadeus-api-is-a-toolkit-designed-for-travel-agencies-who-want-to-develop-their-own-travel-products-rather-than-using-offtheshelf-solutions--with-this-tool-you-can-build-your-very-own-customised-applications-that-link-in-a-stable-and-secure-dialogue-with-our-global-distribution-system-gds-
  contact:
    name: Amadeus Innovation and Research
    url: https://sandbox.amadeus.com
  version: 1.0.0
host: api.sandbox.amadeus.com
basePath: /v1.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rail-stations/autocomplete:
    get:
      summary: Get Rail Stations Autocomplete
      description: |-
        Given the start of any word in a rail station's official name, as a term, this API provides the full name and rail station ID of a rail station for use in searches. The response provides an array of up to 20 possible matches, sorted by passenger traffic, in a JQuery Autocomplete compatible format.

        The value returned is the UIC station code. The label returned is always in UTF-8 format, with the station's official name (which is often in the native language). Agglomeration station codes may also be returned.

        Note that only French and Italian rail stations are supported by the Rail Station Autocomplete API
      operationId: getRailStationsAutocomplete
      x-api-path-slug: railstationsautocomplete-get
      parameters:
      - in: query
        name: term
        description: Search term that should represent some part of a station name
      responses:
        200:
          description: OK
      tags:
      - Rail
      - Stations
      - Autocomplete
  /rail-station/{id}:
    get:
      summary: Get Rail Station
      description: Get rail station
      operationId: getRailStation
      x-api-path-slug: railstationid-get
      parameters:
      - in: path
        name: id
        description: Station ID for which further information is required
      responses:
        200:
          description: OK
      tags:
      - Rail
      - Station