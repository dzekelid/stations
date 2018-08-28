---
swagger: "2.0"
x-collection-name: HERE
x-complete: 0
info:
  title: HERE Public Transit API Find Stations by Name
  description: "*Request a list of public transit stations based on name*\n\nA station
    search request can be made using the `search/by_name.json` endpoint and adding
    the `name` parameter. The focal point of the search is defined using the `x` and
    `y` parameters. The number of results can be further restricted by `max `and the
    `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center
    point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude
    of the center point of your search.    e.g. `52.515`\n\n* **name**  `text`\n \\-
    Specifies the name or a part of the name of the station to search for and can
    be one word, multiple words or partial word separated by either comma or space.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **max**
    \ `number`\n \\- Specifies the maximum number of stations/stops included in the
    response.\n  The minimum value is 1 and the maximum value is not limited.\n  The
    default value is 5.     \n\n* **method**  `enum`\n \\- Specifies if the matching
    method is *fuzzy* or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy -
    search for stations with the name having similar sounding and/or similar spelling
    to the names requested\n    * strict - search for stations with the name exactly
    matching the names requested or contains it as its part.\n\n   Valid values are
    : `fuzzy`, `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters
    when combined with a center point defines the area of the search. The minimum
    value is 0 and the maximum value is not limited.\n  The default value is 20000km."
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