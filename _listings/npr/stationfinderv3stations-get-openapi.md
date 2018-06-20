---
swagger: "2.0"
x-collection-name: NPR
x-complete: 0
info:
  title: NPR List stations close to you or filter by search criteria
  description: |-
    This endpoint has two main use cases:

    - If no query parameters passed in, it returns a list of stations that are geographically closest to the calling client (based on GeoIP information)
    - If one or more query parameters are passed in, it performs a search of NPR stations that match those search criteria (not taking into account the client's physical location)

    Clients wanting to implement a 'Change Station' UI should use this endpoint to power their search. In most cases, you'll want to build a search interface that uses one of the 3 provided schemas: `lat` and `lon` (using e.g. the HTML5 Geolocation API), `city` and `state`, _or_ the generic `q` query which can accept a station name, call letters, network name, or zip code. Technically speaking, `q` can also take in either a city name or a state name, but using the `city` and `state` parameters together will yield more accurate geographic search results than `q={cityName}`.

    The `lat` and `lon` query parameters should always be passed in together (otherwise the API will return a 400 error), and if included in the query, they will take precedence over any other search criteria; that is, `lat` and `lon` will do a purely geographic search and not take into account `q`, `city` or `state`.

    Similarly, `city` and/or `state` will take precedence over (and ignore) `q`.

    If clients want to be able to offer multiple types of searches (e.g. 'Search for a station name, city or zipcode') using a *single* search input form, `q` should be used. But again, be aware that using `city` and `state` together will yield more accurate search results than `q={cityName}`.
  termsOfService: http://dev.npr.org/develop/terms-of-use
  contact:
    name: NPR One Enterprise Team
    url: http://dev.npr.org
    email: NPROneEnterprise@npr.org
  version: 1.0.0
host: api.npr.org
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /identity/v2/stations:
    put:
      summary: Update the logged-in user's favorite station(s)
      description: Right now, only the primary station can be changed. Previously
        selected stations will not be deleted, but the new station will be moved to
        first in the array.
      operationId: updateStations
      x-api-path-slug: identityv2stations-put
      parameters:
      - in: body
        name: body
        description: A JSON-serialized array of station IDs
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - Entity
      - Stations
  /stationfinder/v3/stations:
    get:
      summary: List stations close to you or filter by search criteria
      description: |-
        This endpoint has two main use cases:

        - If no query parameters passed in, it returns a list of stations that are geographically closest to the calling client (based on GeoIP information)
        - If one or more query parameters are passed in, it performs a search of NPR stations that match those search criteria (not taking into account the client's physical location)

        Clients wanting to implement a 'Change Station' UI should use this endpoint to power their search. In most cases, you'll want to build a search interface that uses one of the 3 provided schemas: `lat` and `lon` (using e.g. the HTML5 Geolocation API), `city` and `state`, _or_ the generic `q` query which can accept a station name, call letters, network name, or zip code. Technically speaking, `q` can also take in either a city name or a state name, but using the `city` and `state` parameters together will yield more accurate geographic search results than `q={cityName}`.

        The `lat` and `lon` query parameters should always be passed in together (otherwise the API will return a 400 error), and if included in the query, they will take precedence over any other search criteria; that is, `lat` and `lon` will do a purely geographic search and not take into account `q`, `city` or `state`.

        Similarly, `city` and/or `state` will take precedence over (and ignore) `q`.

        If clients want to be able to offer multiple types of searches (e.g. 'Search for a station name, city or zipcode') using a *single* search input form, `q` should be used. But again, be aware that using `city` and `state` together will yield more accurate search results than `q={cityName}`.
      operationId: searchStations
      x-api-path-slug: stationfinderv3stations-get
      parameters:
      - in: query
        name: city
        description: A city to look for stations from; intended to be paired with
          `state`
      - in: query
        name: lat
        description: A latitude value from a geographic coordinate system; only works
          if paired with `lon`
      - in: query
        name: lon
        description: A longitude value from a geographic coordinate system; only works
          if paired with `lat`
      - in: query
        name: No Name
      - in: query
        name: q
        description: Search terms to search on; can be a station name, network name,
          call letters, or zipcode
      - in: query
        name: state
        description: A state to look for stations from (using the 2-letter abbreviation);
          intended to be paired with `city`
      responses:
        200:
          description: OK
      tags:
      - News
      - Stationfinder
      - Stations
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---