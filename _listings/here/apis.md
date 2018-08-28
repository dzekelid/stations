---
name: HERE
x-slug: here
description: HERE Technologies enables people, enterprises and cities around the world
  to harness the power of location and create innovative solutions that make our lives
  safer and more efficient. We transform information from devices, vehicles, infrastructure
  and...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
x-kinRank: "7"
x-alexaRank: "3011"
tags: Stations
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/apis.md
specificationVersion: "0.14"
apis:
- name: Public Transport API - Find Stations by Name
  x-api-slug: searchby-name-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-name-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-name-json-get-openapi.md
- name: Public Transport API - Find Stations by ID
  x-api-slug: searchby-stopids-json-get
  description: "*Request details of a specific transit station based on a previous
    request*\n\nStation details are requested using the `search/by_stopids.json` endpoint
    and appending a comma delimited list of `stop-ids` to the request URL. Usually,
    the request to this endpoint will be called after making a station search request,
    to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**  `text`\n \\- Specifies
    a list of stopIds separated by comma. Each stopId must contain at least 6 characters
    and must not exceed a maximum of 1000 characters.     The format of a station
    Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id
    is to be used, the `#` character must be encoded as `%23`.      \n\n* **lang**
    \ `text`\n \\- A language of the response. \n\n* **app_id**  `text`\n \\- A 20
    bytes Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-stopids-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-stopids-json-get-openapi.md
- name: Public Transport API - Find Stations Nearby
  x-api-slug: searchby-geocoord-json-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-geocoord-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/searchby-geocoord-json-get-openapi.md
- name: Public Transport API - All Next Departures for a list of Stations
  x-api-slug: metarouterrestboardservicev1multiboardby-stopids-json-get
  description: "*Request a list of all next departure times and destinations for a
    give list of stations.*\n\nAll next departures for a list of stations can be requested
    using the `metarouter/rest/boardservice/v1/multiboard/by_stopIds.json` and specifying
    a `time` and `stopIds.`  \nThe maximum numbers of nearby stations and number of
    departures per station can be restricted by using the `max_stn` and `max` parameters,
    respectively.\n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n*
    **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number
    of next departures per station to be included in the response.     The default
    value is 40.    \n\n* **max_stn**  `text`\n \\-  The maximum number of stations
    for which departures are required.     The default value is 40.    \n\n* **stopIds**
    \ `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must
    contain\n at least 6 characters and must not exceed a maximum of 1000 characters."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev1multiboardby-stopids-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev1multiboardby-stopids-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
- name: Public Transport API - Next Nearby Departures from a Station
  x-api-slug: metarouterrestboardservicev2stationboard-json-get
  description: "*Request a list of next departure times and destinations of a particular
    station*\n\nNext nearby departures can be requested using the `metarouter/rest/boardservice/v2/stationboard.json`
    and specifying a `time` and `stnId`.\n  \n  The station ID (stnId) can be obtained
    from making a prior call to one of the station search (by name or by geo-coordinates)
    endpoints.\n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **stnId**
    \ `number`\n \\- Station Id.  The format of a station Id is 123456789#100. Only
    the first 9-digits are mandatory and if the full Id is to be used, the `#` character
    must be encoded as `%23`.      \n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **strict**  `enum`\n \\- When `strict=1` the board will include only departures
    from the given station id.\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/here/metarouterrestboardservicev2stationboard-json-get-openapi.md
x-common:
- type: x-blog-rss
  url: https://developer.here.com/blog/feed
- type: x-github
  url: https://github.com/heremaps
- type: x-postman-collection
  url: https://github.com/heremaps/postman-collections
- type: x-api-gallery
  url: http://healthcare.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://here.stack.network
- type: x-blog
  url: https://developer.here.com/blog
- type: x-crunchbase
  url: https://crunchbase.com/organization/here-inc
- type: x-developer
  url: https://developer.here.com
- type: x-email
  url: dirk.popp@here.com
- type: x-email
  url: sebastian.kurme@here.com
- type: x-email
  url: jordan.stark@here.com
- type: x-email
  url: amy.stupavsky@here.com
- type: x-email
  url: minna.laub@here.com
- type: x-email
  url: stefanie.sirc@here.com
- type: x-email
  url: rachel.kuta@here.com
- type: x-email
  url: laurel.davis-lyons@here.com
- type: x-email
  url: linda.bradley@here.com
- type: x-email
  url: press@here.com
- type: x-twitter
  url: https://twitter.com/here
- type: x-website
  url: https://here.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---