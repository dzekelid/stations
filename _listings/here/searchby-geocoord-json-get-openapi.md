---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Public Transit API Find Stations Nearby
  description: "*Request a list of public transit stations within a given geo-location.*\n\nTo
    find the nearest stations use the `search/by_geocoord.json` endpoint specifying
    a center point using the `x` and `y` parameters and a search radius in meters
    using the `radius` parameter. `Max` value can also be used to restrict the number
    of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The latitude
    of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\-
    The longitude of the center point of your search.    e.g. `13.377`\n\n* **radius**
    \ `number`\n \\- Specifies a radius in meters when combined with the geo-coordinates
    defines the area of the search. The default value is 500m.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum
    number of stations/stops included in the response. \n          The default value
    is 5. The minimum value is 1 and the maximum value is not limited."
  version: 1.0.0
host: cit.transit.api.here.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/by_name.json:
    get:
      summary: Find Stations by Name
      description: "*Request a list of public transit stations based on name*\n\nA
        station search request can be made using the `search/by_name.json` endpoint
        and adding the `name` parameter. The focal point of the search is defined
        using the `x` and `y` parameters. The number of results can be further restricted
        by `max `and the `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The
        longitude of the center point of your search.    e.g. `13.377`\n\n* **y**
        \ `number`\n \\- The latitude of the center point of your search.    e.g.
        `52.515`\n\n* **name**  `text`\n \\- Specifies the name or a part of the name
        of the station to search for and can be one word, multiple words or partial
        word separated by either comma or space.\n\n* **app_id**  `text`\n \\- A 20
        bytes Base64 URL-safe encoded string used for the authentication of the client
        application.    You must include an app_code and app_code with every request.\n\n*
        **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used
        for the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the
        maximum number of stations/stops included in the response.\n  The minimum
        value is 1 and the maximum value is not limited.\n  The default value is 5.
        \    \n\n* **method**  `enum`\n \\- Specifies if the matching method is *fuzzy*
        or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy - search for stations
        with the name having similar sounding and/or similar spelling to the names
        requested\n    * strict - search for stations with the name exactly matching
        the names requested or contains it as its part.\n\n   Valid values are : `fuzzy`,
        `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when
        combined with a center point defines the area of the search. The minimum value
        is 0 and the maximum value is not limited.\n  The default value is 20000km."
      operationId: SearchByNameJsonGet
      x-api-path-slug: searchby-name-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: max
      - in: query
        name: method
      - in: query
        name: name
      - in: query
        name: radius
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - By
      - Name
  /search/by_stopids.json:
    get:
      summary: Find Stations by ID
      description: "*Request details of a specific transit station based on a previous
        request*\n\nStation details are requested using the `search/by_stopids.json`
        endpoint and appending a comma delimited list of `stop-ids` to the request
        URL. Usually, the request to this endpoint will be called after making a station
        search request, to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**
        \ `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId
        must contain at least 6 characters and must not exceed a maximum of 1000 characters.
        \    The format of a station Id is 123456789#100. Only the first 9-digits
        are mandatory and if the full Id is to be used, the `#` character must be
        encoded as `%23`.      \n\n* **lang**  `text`\n \\- A language of the response.
        \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used
        for the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request."
      operationId: SearchByStopidsJsonGet
      x-api-path-slug: searchby-stopids-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: stopIds
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - By
      - ID
  /search/by_geocoord.json:
    get:
      summary: Find Stations Nearby
      description: "*Request a list of public transit stations within a given geo-location.*\n\nTo
        find the nearest stations use the `search/by_geocoord.json` endpoint specifying
        a center point using the `x` and `y` parameters and a search radius in meters
        using the `radius` parameter. `Max` value can also be used to restrict the
        number of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The
        latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n
        \\- The longitude of the center point of your search.    e.g. `13.377`\n\n*
        **radius**  `number`\n \\- Specifies a radius in meters when combined with
        the geo-coordinates defines the area of the search. The default value is 500m.\n\n*
        **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **max**
        \ `number`\n \\- Specifies the maximum number of stations/stops included in
        the response. \n          The default value is 5. The minimum value is 1 and
        the maximum value is not limited."
      operationId: SearchByGeocoordJsonGet
      x-api-path-slug: searchby-geocoord-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: max
      - in: query
        name: radius
      - in: query
        name: x
      - in: query
        name: "y"
      responses:
        200:
          description: OK
      tags:
      - Find
      - Stations
      - Nearby
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