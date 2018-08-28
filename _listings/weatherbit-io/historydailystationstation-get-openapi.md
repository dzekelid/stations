---
swagger: "2.0"
x-collection-name: Weatherbit.io
x-complete: 0
info:
  title: Weatherbit Get History Daily Station Station
  description: Returns Historical Observations - Given a station ID. **(LIMIT 1 day
    for Low Volume plans. LIMIT 7 days for Basic/Developer. LIMIT 30 days for Advanced/Advanced+/Enterprise)**
  version: 2.0.0
host: api.weatherbit.io
basePath: /v2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /current?stations={stations}:
    get:
      summary: Get Current Stations Stations
      description: '**(Advanced/Advanced+/Enterprise plans only)** Returns a group
        of Current Observations - Given a list of Station Call IDs.'
      operationId: advancedadvancedenterprise-plans-only-returns-a-group-of-current-observations--given-a-list-of-stati
      x-api-path-slug: currentstationsstations-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: path
        name: stations
        description: Comma separated list of Station Call IDs
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Current
      - Stations
      - Stations
  /bulk/history/daily?station={station}:
    get:
      summary: Get Bulk History Daily Station
      description: Returns Historical Observations - Given a station ID.
      operationId: returns-historical-observations--given-a-station-id
      x-api-path-slug: bulkhistorydailystationstation-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: station
        description: Station ID
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Bulk
      - History
      - Daily
      - Station
      - Station
  /bulk/history/hourly?station={station}:
    get:
      summary: Get Bulk History Hourly Station
      description: Returns Historical Observations - Given a station ID.
      operationId: returns-historical-observations--given-a-station-id
      x-api-path-slug: bulkhistoryhourlystationstation-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: station
        description: Station ID
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Bulk
      - History
      - Hourly
      - Station
      - Station
  /current?station={station}:
    get:
      summary: Get Current Station Station
      description: Returns a Current Observation - Given a station ID.
      operationId: returns-a-current-observation--given-a-station-id
      x-api-path-slug: currentstationstation-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: path
        name: station
        description: Station Call ID
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Current
      - Station
      - Station
  /history/daily?station={station}:
    get:
      summary: Get History Daily Station Station
      description: Returns Historical Observations - Given a station ID. **(LIMIT
        1 day for Low Volume plans. LIMIT 7 days for Basic/Developer. LIMIT 30 days
        for Advanced/Advanced+/Enterprise)**
      operationId: returns-historical-observations--given-a-station-id-limit-1-day-for-low-volume-plans-limit-7-days-fo
      x-api-path-slug: historydailystationstation-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: station
        description: Station ID
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - History
      - Daily
      - Station
      - Station
  /history/hourly?station={station}:
    get:
      summary: Get History Hourly Station Station
      description: Returns Historical Observations - Given a station ID. **(LIMIT
        1 day for Low Volume plans. LIMIT 7 days for Basic/Developer. LIMIT 30 days
        for Advanced/Advanced+/Enterprise)**
      operationId: returns-historical-observations--given-a-station-id-limit-1-day-for-low-volume-plans-limit-7-days-fo
      x-api-path-slug: historyhourlystationstation-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: station
        description: Station ID
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - History
      - Hourly
      - Station
      - Station
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