---
swagger: "2.0"
x-collection-name: Entertainment Express
x-complete: 0
info:
  title: Entertainment Express Stations are not tied to lineups, therefore no channel
    numbers will be present in the response, unlike most other listing operations.
  description: Get listings for a given station.
  version: "2.0"
host: ee.iva-api.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /TvMedia/stations/{StationID}:
    get:
      summary: ""
      description: Gets station details by ID.
      operationId: GetTvMediaStation
      x-api-path-slug: tvmediastationsstationid-get
      parameters:
      - in: path
        name: StationID
        description: Station ID
      - in: query
        name: TvMediaApiKey
        description: API Key supplied by TvMedia
      responses:
        200:
          description: OK
      tags:
      - TvMedia
      - Stations
      - StationID
  /TvMedia/stations/{StationID}/listings:
    get:
      summary: Stations are not tied to lineups, therefore no channel numbers will
        be present in the response, unlike most other listing operations.
      description: Get listings for a given station.
      operationId: GetTvMediaListingsByStation
      x-api-path-slug: tvmediastationsstationidlistings-get
      parameters:
      - in: query
        name: AdultContent
        description: Defaults to 1 (allowed)
      - in: query
        name: Channel
        description: Include only channel(s) with this number, single or array values
          accepted
      - in: query
        name: DescriptiveVideoOnly
        description: Only displays listings which are flagged as being broadcast with
          Descriptive Video
      - in: query
        name: Detail
        description: Set level of detail for response
      - in: query
        name: DisplayArtwork
        description: Displays the Artwork information
      - in: query
        name: End
        description: UTC end time in ISO8601
      - in: query
        name: EndChan
        description: Highest channel
      - in: query
        name: ExcludeChan
        description: Exclude channels by number, single or array values accepted
      - in: query
        name: ExcludeShowType
        description: Exclude only these show type ID(s), array or single values accepted
      - in: query
        name: ExcludeStation
        description: Filter out station IDs; array or single value accepted
      - in: query
        name: Id
        description: ListingID, array or single values accepted
      - in: query
        name: League
        description: Get only sports listings in the given league ID(s)
      - in: query
        name: LiveOnly
        description: Only displays live listings
      - in: query
        name: NewShowsOnly
        description: Get new shows only
      - in: query
        name: NotYetStarted
        description: Only displays listings which are starting on or after the given
          start time
      - in: query
        name: Search
        description: 'search value: can be a show, episode, movie, team, league, person,
          etc'
      - in: query
        name: ShowType
        description: Include only these show type ID(s), array or single values accepted
      - in: query
        name: SportEventsOnly
        description: Get sporting events only
      - in: query
        name: SportType
        description: Get only sports listings of type sportTypeID
      - in: query
        name: Start
        description: UTC start time in ISO8601
      - in: query
        name: StartChan
        description: Lowest channel
      - in: query
        name: Station
        description: Filter by station ID
      - in: path
        name: StationID
        description: Station ID
      - in: query
        name: Team
        description: Filter by teams playing by name(teams
      - in: query
        name: TimeZone
        description: Set a timezone or time offset for listing times (listDateTime
          property)
      - in: query
        name: TvMediaApiKey
        description: API Key supplied by TvMedia
      responses:
        200:
          description: OK
      tags:
      - TvMedia
      - Stations
      - StationID
      - Listings
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