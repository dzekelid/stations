swagger: "2.0"
x-collection-name: HERE
x-complete: 1
info:
  title: Weather API
  description: the-here-weather-api-provides-weather-forecasts-and-reports-on-current-weather-conditions-provides-information-on-severe-weather-alerts-provides-information-about-when-the-sun-and-moon-rise-and-set-and-the-phase-of-the-moonthis-example-set-works-with-version-1-2-4-or-higheradditional-information-can-be-found-on-developer-here-comhttpsdeveloper-here-comrestapisdocumentationweather
  version: 1.0.0
host: weather.cit.api.here.com
basePath: /weather/1.0
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
  /metarouter/rest/boardservice/v1/multiboard/by_stopids.json:
    get:
      summary: All Next Departures for a list of Stations
      description: "*Request a list of all next departure times and destinations for
        a give list of stations.*\n\nAll next departures for a list of stations can
        be requested using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json`
        and specifying a `time` and `stopIds.`  \nThe maximum numbers of nearby stations
        and number of departures per station can be restricted by using the `max_stn`
        and `max` parameters, respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language
        of the response\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
        **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an app_code
        and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes
        Base64 URL-safe encoded string used for the authentication of the client application.
        \   You must include an app_code and app_code with every request.\n\n* **max**
        \ `text`\n \\- The  maximum number of next departures per station to be included
        in the response.     The default value is 40.    \n\n* **max_stn**  `text`\n
        \\-  The maximum number of stations for which departures are required.     The
        default value is 40.    \n\n* **stopIds**  `text`\n \\- Specifies a list of
        stopIds separated by comma. Each stopId must contain\n at least 6 characters
        and must not exceed a maximum of 1000 characters."
      operationId: MetarouterRestBoardserviceV1MultiboardByStopidsJsonGet
      x-api-path-slug: metarouterrestboardservicev1multiboardby-stopids-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: max
      - in: query
        name: max_stn
      - in: query
        name: stopIds
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - All
      - Next
      - Departuresa
      - List
      - Of
      - Stations
  /metarouter/rest/boardservice/v2/stationboard.json:
    get:
      summary: Next Nearby Departures from a Station
      description: "*Request a list of next departure times and destinations of a
        particular station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
        and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be
        obtained from making a prior call to one of the station search (by name or
        by geo-coordinates) endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of
        the response\n\n* **stnId**  `number`\n \\- Station Id.  The format of a station
        Id is 123456789#100. Only the first 9-digits are mandatory and if the full
        Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **time**
        \ `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **strict**  `enum`\n
        \\- When `strict=1` the board will include only departures from the given
        station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**
        \ `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication
        of the client application.    You must include an app_code and app_code with
        every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an app_code and app_code with every request."
      operationId: MetarouterRestBoardserviceV2StationboardJsonGet
      x-api-path-slug: metarouterrestboardservicev2stationboard-json-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: lang
      - in: query
        name: stnId
      - in: query
        name: strict
      - in: query
        name: time
      responses:
        200:
          description: OK
      tags:
      - Next
      - Nearby
      - Departures
      - From
      - Station