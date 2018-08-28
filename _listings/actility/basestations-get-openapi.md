---
swagger: "2.0"
x-collection-name: Actility
x-complete: 0
info:
  title: ThingPark DX Core API Base stations retrieval
  description: Retrieves a list of base stations existing within authorized scopes.
    Note that in case of an OPERATOR scope, only supplier-owned base stations are
    returned.
  version: 1.0.0
host: dx-api.thingpark.com
basePath: /core/v141/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /baseStations:
    get:
      summary: Base stations retrieval
      description: Retrieves a list of base stations existing within authorized scopes.
        Note that in case of an OPERATOR scope, only supplier-owned base stations
        are returned.
      operationId: retrieves-a-list-of-base-stations-existing-within-authorized-scopes-note-that-in-case-of-an-operator
      x-api-path-slug: basestations-get
      parameters:
      - in: query
        name: baseStationId
        description: Id of the base station to search for
      - in: query
        name: commercialDetails
        description: Indicates to also retrieve commercial information along each
          base station
      - in: query
        name: connectionState
        description: Connection state of the base stations to search for
      - in: query
        name: healthState
        description: Health state of the base stations to search for
      - in: query
        name: pageIndex
        description: If set, enables pagination and returns only the 100 base stations
          in the specified page
      - in: query
        name: statistics
        description: Indicates to also retrieve usage statistic information along
          each base station
      responses:
        200:
          description: OK
      tags:
      - Base
      - Stations
      - Retrieval
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---