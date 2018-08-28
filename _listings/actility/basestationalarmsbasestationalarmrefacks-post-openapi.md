---
swagger: "2.0"
x-collection-name: Actility
x-complete: 0
info:
  title: ThingPark DX Core API Base station alarm acknowledgement
  description: Acknowledges a base station alarm.
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
    post:
      summary: Base stations creation
      description: Creates a new base station.
      operationId: creates-a-new-base-station
      x-api-path-slug: basestations-post
      parameters:
      - in: body
        name: baseStation
        description: Contents of the base station to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Base
      - Stations
      - Creation
  /baseStations/{baseStationRef}:
    get:
      summary: Base station retrieval
      description: Retrieves the base station corresponding to the provided base station
        ref, if that base station is within authorized scopes.
      operationId: retrieves-the-base-station-corresponding-to-the-provided-base-station-ref-if-that-base-station-is-wi
      x-api-path-slug: basestationsbasestationref-get
      parameters:
      - in: path
        name: baseStationRef
        description: Ref of the base station to retrieve
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Retrieval
    put:
      summary: Base station update
      description: Updates the base station corresponding to the provided base station
        ref, if that base station is within authorized scopes.
      operationId: updates-the-base-station-corresponding-to-the-provided-base-station-ref-if-that-base-station-is-with
      x-api-path-slug: basestationsbasestationref-put
      parameters:
      - in: body
        name: baseStation
        description: Contents of the base station to update
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: baseStationRef
        description: Ref of the base station to update
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Update
    delete:
      summary: Base station deletion
      description: Deletes the base station corresponding to the provided base station
        ref, if that base station is within authorized scopes.
      operationId: deletes-the-base-station-corresponding-to-the-provided-base-station-ref-if-that-base-station-is-with
      x-api-path-slug: basestationsbasestationref-delete
      parameters:
      - in: path
        name: baseStationRef
        description: Ref of the base station to delete
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Deletion
  /baseStationProfiles:
    get:
      summary: Base station profiles retrieval
      description: Retrieves the list of existing base station profiles.
      operationId: retrieves-the-list-of-existing-base-station-profiles
      x-api-path-slug: basestationprofiles-get
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Profiles
      - Retrieval
  /baseStationAlarms:
    get:
      summary: Base station alarms retrieval
      description: Retrieves a list of base station alarms existing within authorized
        scopes. Note that in case of an OPERATOR scope, only supplier-owned base station
        alarms are returned.
      operationId: retrieves-a-list-of-base-station-alarms-existing-within-authorized-scopes-note-that-in-case-of-an-op
      x-api-path-slug: basestationalarms-get
      parameters:
      - in: query
        name: baseStationId
        description: Id of the base station to search alarms for
      - in: query
        name: pageIndex
        description: If set, enables pagination and returns only the 100 base station
          alarms of the specified page
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Alarms
      - Retrieval
  /baseStationAlarms/{baseStationAlarmRef}:
    get:
      summary: Base station alarm retrieval
      description: Retrieves the base station alarm corresponding to the provided
        base station alarm ref, if that base station alarm is within authorized scopes.
      operationId: retrieves-the-base-station-alarm-corresponding-to-the-provided-base-station-alarm-ref-if-that-base-s
      x-api-path-slug: basestationalarmsbasestationalarmref-get
      parameters:
      - in: path
        name: baseStationAlarmRef
        description: Ref of the base station alarm to retrieve
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Alarm
      - Retrieval
  /baseStationAlarms/{baseStationAlarmRef}/acks:
    post:
      summary: Base station alarm acknowledgement
      description: Acknowledges a base station alarm.
      operationId: acknowledges-a-base-station-alarm
      x-api-path-slug: basestationalarmsbasestationalarmrefacks-post
      parameters:
      - in: path
        name: baseStationAlarmRef
        description: Ref of the base station alarm to acknowledge
      responses:
        200:
          description: OK
      tags:
      - Base
      - Station
      - Alarm
      - Acknowledgement
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