---
swagger: "2.0"
x-collection-name: NPR
x-complete: 0
info:
  title: NPR Update the logged-in user's favorite station(s)
  description: Right now, only the primary station can be changed. Previously selected
    stations will not be deleted, but the new station will be moved to first in the
    array.
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