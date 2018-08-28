---
swagger: "2.0"
x-collection-name: Washington Metropolitan Area Transit Authority
x-complete: 0
info:
  title: WMATA Real-Time Rail Predictions JSON - Next Trains
  description: "Description\r\n\r\nReturns next train arrival information for one
    or more stations. Will return\r\nan empty set of results when no predictions are
    available. Use All for the StationCodes parameter to return predictions for\r\nall
    stations.\r\n\r\nFor terminal stations (e.g.: Greenbelt, Shady Grove, etc.), predictions
    may\r\nbe displayed twice.\r\n\r\nSome stations have two platforms (e.g.: Gallery
    Place, Fort Totten, L'Enfant\r\nPlaza, and Metro Center). To retrieve complete
    predictions for these stations,\r\nbe sure to pass in both StationCodes.\r\n\r\nFor
    trains with no passengers, the DestinationName will be No Passenger.\r\n\r\nNext
    train arrival information is refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nTrains\r\n\r\n\r\nArray
    containing train prediction information (AIMPredictionTrainInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nAIMPredictionTrainInfo\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCar\r\n\r\nNumber
    of cars on a train, usually 6 or 8, but might also\r\nreturn - or NULL.\r\n\r\n\r\n\r\nDestination\r\n\r\nAbbreviated
    version of the final destination for a train. This\r\nis similar to what is displayed
    on the signs at stations.\r\n\r\n\r\n\r\nDestinationCode\r\n\r\nDestination station
    code. Can be NULL. Use this value in other\r\nrail-related APIs to retrieve data
    about a station.\r\n\r\n\r\n\r\nDestinationName\r\n\r\nWhen DestinationCode is
    populated, this is the full name of the\r\ndestination station, as shown on the
    WMATA website.\r\n\r\n\r\n\r\nGroup\r\n\r\nDenotes the track this train is on,
    but does not necessarily\r\nequate to Track 1 or Track 2. With the exception of
    terminal\r\nstations, predictions at the same station with different Group\r\nvalues
    refer to trains on different tracks.\r\n\r\n\r\n\r\nLine\r\n\r\nTwo-letter abbreviation
    for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV). May also be blank or No for\r\ntrains
    with no passengers.\r\n\r\n\r\n\r\nLocationCode\r\n\r\nStation code for where
    the train is arriving. Useful when\r\npassing in All as the StationCodes\r\nparameter.
    Use this value in other rail-related APIs to retrieve\r\ndata about a station.\r\n\r\n\r\n\r\nLocationName\r\n\r\nFull
    name of the station where the train is arriving. Useful\r\nwhen passing in All
    as the\r\nStationCodes parameter.\r\n\r\n\r\n\r\nMin\r\n\r\nMinutes until arrival.
    Can be a numeric value, ARR (arriving), BRD (boarding), ---, or empty."
  version: 1.0.0
host: api.wmata.com
basePath: /StationPrediction.svc
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /json/jStationParking:
    get:
      summary: JSON - Parking Information
      description: |-
        Description

        Returns parking information at a station based on a given StationCode. Omit
        the StationCode to return parking information for all stations.

        If a station has no parking, the StationsParking element will contain no
        child elements.

        Response Elements




        Element

        Description





        StationsParking


        Array containing station parking information (StationParking).






        StationParking
        Elements





        Code

        Station code. Useful when returning parking information for all
        stations. Use this value in other rail-related APIs to retrieve
        data about a station.



        Notes

        When not NULL, provides additional parking resources such as
        nearby lots.



        AllDayParking


        Structure describing all-day
        parking options.




        ShortTermParking


        Structure describing short-term
        parking options.






        AllDayParking
        Elements





        TotalCount

        Number of all-day parking spots available at a station.



        RiderCost

        All-day cost per day (weekday) for Metro riders. NULL when no all-day
        spots are available. For most stations, this value is identical to
        the NonRiderCost.

        For cases where the NonRiderCost is different, the lower cost per
        day requires a valid rail trip using a SmarTrip&reg; card
        originating from a station other than the one where the patron
        parked. To receive this lower rate, patrons must pay for their
        parking with the same SmarTrip&reg; card used to enter/exit
        Metrorail, and must exit the parking lot within two hours of
        exiting Metrorail.



        NonRiderCost

        All-day cost per day (weekday) for non-Metro riders. NULL when no all-day
        spots are available.





        ShortTermParking Elements





        SaturdayRiderCost

        Similar to RiderCost, except denoting Saturday prices.



        SaturdayNonRiderCost

        Similar to NonRiderCost, except denoting Saturday prices.



        TotalCount

        Number of short-term parking spots available at a station
        (parking meters).



        Notes

        Misc. information relating to short-term parking. NULL when no
        short-term spots are available.
      operationId: getJsonJstationparking
      x-api-path-slug: jsonjstationparking-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Parking
  /json/jStationEntrances:
    get:
      summary: JSON - Station Entrances
      description: "Description\r\n\r\nReturns a list of nearby station entrances
        based on latitude, longitude, and\r\nradius (meters). Omit search parameters
        to return all station entrances.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nEntrances\r\n\r\n\r\nArray
        containing detailed information about station entrances\r\n(StationEntrance).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationEntrance
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDescription\r\n\r\nAdditional information
        for the entrance, if available.\r\nCurrently available data usually shows
        the same value as the Name\r\nelement.\r\n\r\n\r\n\r\nID\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nName
        of the entrance (usually the station name and nearest\r\nintersection).\r\n\r\n\r\n\r\nStationCode1\r\n\r\nThe
        station code associated with this entrance. Use this value\r\nin other rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\nStationCode2\r\n\r\nFor
        stations containing multiple platforms (e.g.: Gallery\r\nPlace, Fort Totten,
        L'Enfant Plaza, and Metro Center), the other\r\nstation code."
      operationId: getJsonJstationentrances
      x-api-path-slug: jsonjstationentrances-get
      parameters:
      - in: query
        name: Lat
        description: Center point Latitude, required if Longitude and Radius are specified
      - in: query
        name: Lon
        description: Center point Longitude, required if Latitude and Radius are specified
      - in: query
        name: Radius
        description: Radius (meters) to include in the search area, required if Latitude
          and Longitude are specified
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Entrances
  /json/jStationInfo:
    get:
      summary: JSON - Station Information
      description: "Description\r\n\r\nReturns station location and address information
        based on a given\r\nStationCode.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure
        describing address information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code.
        Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getJsonJstationinfo
      x-api-path-slug: jsonjstationinfo-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /json/jStations:
    get:
      summary: JSON - Station List
      description: "Description\r\n\r\nReturns a list of station location and address
        information based on a given\r\nLineCode. Omit the LineCode to return all
        stations. The response is an array of\r\nobjects identical to those returned
        in the Station Information method.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStations\r\n\r\n\r\nArray
        containing station information (Station).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStation
        Elements\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure describing address
        information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code. Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getJsonJstations
      x-api-path-slug: jsonjstations-get
      parameters:
      - in: query
        name: LineCode
        description: Two-letter line code abbreviation:RD - RedYL - YellowGR - GreenBL
          - BlueOR - OrangeSV - Silver
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /json/jStationTimes:
    get:
      summary: JSON - Station Timings
      description: "Description\r\n\r\nReturns opening and scheduled first/last train
        times based on a given\r\nStationCode. Omit the StationCode to return timing
        information for all\r\nstations.\r\n\r\nNote that for stations with multiple
        platforms (e.g.: Metro Center, L'Enfant\r\nPlaza, etc.), a distinct call is
        required for each StationCode to retrieve the\r\nfull set of train times at
        such stations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationTimes\r\n\r\n\r\nArray
        containing station timing information (StationTime).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationTime\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation
        code for this station. Use this value in other\r\nrail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name of the station.\r\n\r\n\r\n\r\n*Day
        Elements\r\n\r\n\r\nContainer elements containing timing information based
        on\r\nday of the week.\r\n\r\n\r\n\r\n\r\n\r\n\r\nMonday/Tuesday/Wednesday/etc.\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nOpeningTime\r\n\r\nStation
        opening time. Format is HH:mm.\r\n\r\n\r\n\r\nFirstTrains\r\n\r\n\r\nStructure
        containing first train\r\ninformation.\r\n\r\n\r\n\r\n\r\nLastTrains\r\n\r\n\r\nStructure
        containing last train\r\ninformation.\r\n\r\n\r\n\r\n\r\n\r\n\r\nFirstTrains
        Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nFirst train leaves the station
        at this time. Format is\r\nHH:mm.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation
        code for the train's destination. Use this value in\r\nother rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\n\r\n\r\nLastTrains Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nLast
        train leaves the station at this time. Format is HH:mm.\r\nNote that when
        the time is AM, it signifies the next day. For\r\nexample, a value of 02:30
        under a Saturday element means the last\r\ntrain leaves on Sunday at 2:30
        AM.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation code for the train's
        destination. Use this value in\r\nother rail-related APIs to retrieve data
        about a station."
      operationId: getJsonJstationtimes
      x-api-path-slug: jsonjstationtimes-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Times
  /json/jSrcStationToDstStationInfo:
    get:
      summary: JSON - Station to Station Information
      description: "Description\r\n\r\nReturns a distance, fare information, and estimated
        travel time between any\r\ntwo stations, including those on different lines.
        Omit both parameters to\r\nretrieve data for all stations.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfos\r\n\r\n\r\nArray
        containing station to station information (StationToStationInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfo
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCompositeMiles\r\n\r\nDistance in miles from
        the source to destination station.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nDestination
        station code. Use this value in other rail-related\r\nAPIs to retrieve data
        about a station.\r\n\r\n\r\n\r\nRailFare\r\n\r\n\r\nStructure containing fare
        information.\r\n\r\n\r\n\r\n\r\nRailTime\r\n\r\nEstimated travel time (schedule
        time) in minutes between the source and\r\ndestination station. This is not
        correlated to minutes (Min) in Real-Time Rail Predictions.\r\n\r\n\r\n\r\nSourceStation\r\n\r\nOrigin
        station code. Use this value in other rail-related APIs\r\nto retrieve data
        about a station.\r\n\r\n\r\n\r\n\r\n\r\nRailFare Elements\r\n\r\n\r\n\r\n\r\n\r\nOffPeakTime\r\n\r\nFare
        during off-peak times (times other than the ones described\r\nbelow).\r\n\r\n\r\n\r\nPeakTime\r\n\r\nFare
        during peak times (weekdays from opening to 9:30 AM and\r\n3-7 PM, and weekends
        from midnight to closing).\r\n\r\n\r\n\r\nSeniorDisabled\r\n\r\n\r\nReduced
        fare for senior citizens or\r\npeople with disabilities."
      operationId: getJsonJsrcstationtodststationinfo
      x-api-path-slug: jsonjsrcstationtodststationinfo-get
      parameters:
      - in: query
        name: FromStationCode
        description: Station code for the origin station
      - in: query
        name: ToStationCode
        description: Station code for the destination station
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /StationParking:
    get:
      summary: XML - Parking Information
      description: |-
        Description

        Returns parking information at a station based on a given StationCode. Omit
        the StationCode to return parking information for all stations.

        If a station has no parking, the StationsParking element will contain no
        child elements.

        Response Elements




        Element

        Description





        StationsParking


        Array containing station parking information (StationParking).






        StationParking
        Elements





        Code

        Station code. Useful when returning parking information for all
        stations. Use this value in other rail-related APIs to retrieve
        data about a station.



        Notes

        When not NULL, provides additional parking resources such as
        nearby lots.



        AllDayParking


        Structure describing all-day
        parking options.




        ShortTermParking


        Structure describing short-term
        parking options.






        AllDayParking
        Elements





        TotalCount

        Number of all-day parking spots available at a station.



        RiderCost

        All-day cost per day (weekday) for Metro riders. NULL when no all-day
        spots are available. For most stations, this value is identical to
        the NonRiderCost.

        For cases where the NonRiderCost is different, the lower cost per
        day requires a valid rail trip using a SmarTrip&reg; card
        originating from a station other than the one where the patron
        parked. To receive this lower rate, patrons must pay for their
        parking with the same SmarTrip&reg; card used to enter/exit
        Metrorail, and must exit the parking lot within two hours of
        exiting Metrorail.



        NonRiderCost

        All-day cost per day (weekday) for non-Metro riders. NULL when no all-day
        spots are available.





        ShortTermParking Elements





        SaturdayRiderCost

        Similar to RiderCost, except denoting Saturday prices.



        SaturdayNonRiderCost

        Similar to NonRiderCost, except denoting Saturday prices.



        TotalCount

        Number of short-term parking spots available at a station
        (parking meters).



        Notes

        Misc. information relating to short-term parking. NULL when no
        short-term spots are available.
      operationId: getStationparking
      x-api-path-slug: stationparking-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Parking
  /StationEntrances:
    get:
      summary: XML - Station Entrances
      description: "Description\r\n\r\nReturns a list of nearby station entrances
        based on latitude, longitude, and\r\nradius (meters). Omit search parameters
        to return all station entrances.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nEntrances\r\n\r\n\r\nArray
        containing detailed information about station entrances\r\n(StationEntrance).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationEntrance
        Elements\r\n\r\n\r\n\r\n\r\n\r\nDescription\r\n\r\nAdditional information
        for the entrance, if available.\r\nCurrently available data usually shows
        the same value as the Name\r\nelement.\r\n\r\n\r\n\r\nID\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nName
        of the entrance (usually the station name and nearest\r\nintersection).\r\n\r\n\r\n\r\nStationCode1\r\n\r\nThe
        station code associated with this entrance. Use this value\r\nin other rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\nStationCode2\r\n\r\nFor
        stations containing multiple platforms (e.g.: Gallery\r\nPlace, Fort Totten,
        L'Enfant Plaza, and Metro Center), the other\r\nstation code."
      operationId: getStationentrances
      x-api-path-slug: stationentrances-get
      parameters:
      - in: query
        name: Lat
        description: Center point Latitude, required if Longitude and Radius are specified
      - in: query
        name: Lon
        description: Center point Longitude, required if Latitude and Radius are specified
      - in: query
        name: Radius
        description: Radius (meters) to include in the search area, required if Latitude
          and Longitude are specified
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Entrances
  /StationInfo:
    get:
      summary: XML - Station Information
      description: "Description\r\n\r\nReturns station location and address information
        based on a given\r\nStationCode.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure
        describing address information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code.
        Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getStationinfo
      x-api-path-slug: stationinfo-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /Stations:
    get:
      summary: XML - Station List
      description: "Description\r\n\r\nReturns a list of station location and address
        information based on a given\r\nLineCode. Omit the LineCode to return all
        stations. The response is an array of\r\nobjects identical to those returned
        in the Station Information method.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStations\r\n\r\n\r\nArray
        containing station information (Station).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStation
        Elements\r\n\r\n\r\n\r\n\r\n\r\nAddress\r\n\r\n\r\nStructure describing address
        information.\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation code. Repeated from input.\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLineCode1\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV) served by this
        station.\r\n\r\n\r\n\r\nLineCode2\r\n\r\nAdditional line served by this station.
        This is often the case\r\nwhen stations have multiple platforms (e.g.: Gallery
        Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center).\r\n\r\n\r\n\r\nLineCode3\r\n\r\nSimilar
        to function as LineCodeX.\r\n\r\n\r\n\r\nLineCode4\r\n\r\nSimilar to function
        as LineCodeX. Currently not in use.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStation
        name.\r\n\r\n\r\n\r\nStationTogether1\r\n\r\nFor stations with multiple platforms
        (e.g.: Gallery Place, Fort\r\nTotten, L'Enfant Plaza, and Metro Center), the
        additional\r\nStationCode will be listed here.\r\n\r\n\r\n\r\nStationTogether2\r\n\r\nSimilar
        in function to StationTogether2. Currently not in\r\nuse.\r\n\r\n\r\n\r\n\r\n\r\nAddress
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCity\r\n\r\nCity.\r\n\r\n\r\n\r\nState\r\n\r\nState
        (abbreviated).\r\n\r\n\r\n\r\nStreet\r\n\r\nStreet address (for GPS use).\r\n\r\n\r\n\r\nZip\r\n\r\nZip
        code."
      operationId: getStations
      x-api-path-slug: stations-get
      parameters:
      - in: query
        name: LineCode
        description: Two-letter line code abbreviation:RD - RedYL - YellowGR - GreenBL
          - BlueOR - OrangeSV - Silver
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /StationTimes:
    get:
      summary: XML - Station Timings
      description: "Description\r\n\r\nReturns opening and scheduled first/last train
        times based on a given\r\nStationCode. Omit the StationCode to return timing
        information for all\r\nstations.\r\n\r\nNote that for stations with multiple
        platforms (e.g.: Metro Center, L'Enfant\r\nPlaza, etc.), a distinct call is
        required for each StationCode to retrieve the\r\nfull set of train times at
        such stations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationTimes\r\n\r\n\r\nArray
        containing station timing information (StationTime).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationTime\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCode\r\n\r\nStation
        code for this station. Use this value in other\r\nrail-related APIs to retrieve
        data about a station.\r\n\r\n\r\n\r\nStationName\r\n\r\nFull name of the station.\r\n\r\n\r\n\r\n*Day
        Elements\r\n\r\n\r\nContainer elements containing timing information based
        on\r\nday of the week.\r\n\r\n\r\n\r\n\r\n\r\n\r\nMonday/Tuesday/Wednesday/etc.\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nOpeningTime\r\n\r\nStation
        opening time. Format is HH:mm.\r\n\r\n\r\n\r\nFirstTrains\r\n\r\n\r\nStructure
        containing first train\r\ninformation.\r\n\r\n\r\n\r\n\r\nLastTrains\r\n\r\n\r\nStructure
        containing last train\r\ninformation.\r\n\r\n\r\n\r\n\r\n\r\n\r\nFirstTrains
        Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nFirst train leaves the station
        at this time. Format is\r\nHH:mm.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation
        code for the train's destination. Use this value in\r\nother rail-related
        APIs to retrieve data about a station.\r\n\r\n\r\n\r\n\r\n\r\nLastTrains Elements\r\n\r\n\r\n\r\n\r\n\r\nTime\r\n\r\nLast
        train leaves the station at this time. Format is HH:mm.\r\nNote that when
        the time is AM, it signifies the next day. For\r\nexample, a value of 02:30
        under a Saturday element means the last\r\ntrain leaves on Sunday at 2:30
        AM.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nStation code for the train's
        destination. Use this value in\r\nother rail-related APIs to retrieve data
        about a station."
      operationId: getStationtimes
      x-api-path-slug: stationtimes-get
      parameters:
      - in: query
        name: StationCode
        description: Station code
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
      - Times
  /SrcStationToDstStationInfo:
    get:
      summary: XML - Station to Station Information
      description: "Description\r\n\r\nReturns a distance, fare information, and estimated
        travel time between any\r\ntwo stations, including those on different lines.
        Omit both parameters to\r\nretrieve data for all stations.\r\n\r\nResponse
        Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfos\r\n\r\n\r\nArray
        containing station to station information (StationToStationInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStationToStationInfo
        Elements\r\n\r\n\r\n\r\n\r\n\r\nCompositeMiles\r\n\r\nDistance in miles from
        the source to destination station.\r\n\r\n\r\n\r\nDestinationStation\r\n\r\nDestination
        station code. Use this value in other rail-related\r\nAPIs to retrieve data
        about a station.\r\n\r\n\r\n\r\nRailFare\r\n\r\n\r\nStructure containing fare
        information.\r\n\r\n\r\n\r\n\r\nRailTime\r\n\r\nEstimated travel time (schedule
        time) in minutes between the source and destination station. This is not correlated
        to minutes (Min) in Real-Time Rail Predictions.\r\n\r\n\r\n\r\nSourceStation\r\n\r\nOrigin
        station code. Use this value in other rail-related APIs\r\nto retrieve data
        about a station.\r\n\r\n\r\n\r\n\r\n\r\nRailFare Elements\r\n\r\n\r\n\r\n\r\n\r\nOffPeakTime\r\n\r\nFare
        during off-peak times (times other than the ones described\r\nbelow).\r\n\r\n\r\n\r\nPeakTime\r\n\r\nFare
        during peak times (weekdays from opening to 9:30 AM and\r\n3-7 PM, and weekends
        from midnight to closing).\r\n\r\n\r\n\r\nSeniorDisabled\r\n\r\n\r\nReduced
        fare for senior citizens or\r\npeople with disabilities."
      operationId: getSrcstationtodststationinfo
      x-api-path-slug: srcstationtodststationinfo-get
      parameters:
      - in: query
        name: FromStationCode
        description: Station code for the origin station
      - in: query
        name: ToStationCode
        description: Station code for the destination station
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Stations
  /json/GetPrediction/{StationCodes}:
    get:
      summary: JSON - Next Trains
      description: "Description\r\n\r\nReturns next train arrival information for
        one or more stations. Will return\r\nan empty set of results when no predictions
        are available. Use All for the StationCodes parameter to return predictions
        for\r\nall stations.\r\n\r\nFor terminal stations (e.g.: Greenbelt, Shady
        Grove, etc.), predictions may\r\nbe displayed twice.\r\n\r\nSome stations
        have two platforms (e.g.: Gallery Place, Fort Totten, L'Enfant\r\nPlaza, and
        Metro Center). To retrieve complete predictions for these stations,\r\nbe
        sure to pass in both StationCodes.\r\n\r\nFor trains with no passengers, the
        DestinationName will be No Passenger.\r\n\r\nNext train arrival information
        is refreshed once every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nTrains\r\n\r\n\r\nArray
        containing train prediction information (AIMPredictionTrainInfo).\r\n\r\n\r\n\r\n\r\n\r\n\r\nAIMPredictionTrainInfo\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nCar\r\n\r\nNumber
        of cars on a train, usually 6 or 8, but might also\r\nreturn - or NULL.\r\n\r\n\r\n\r\nDestination\r\n\r\nAbbreviated
        version of the final destination for a train. This\r\nis similar to what is
        displayed on the signs at stations.\r\n\r\n\r\n\r\nDestinationCode\r\n\r\nDestination
        station code. Can be NULL. Use this value in other\r\nrail-related APIs to
        retrieve data about a station.\r\n\r\n\r\n\r\nDestinationName\r\n\r\nWhen
        DestinationCode is populated, this is the full name of the\r\ndestination
        station, as shown on the WMATA website.\r\n\r\n\r\n\r\nGroup\r\n\r\nDenotes
        the track this train is on, but does not necessarily\r\nequate to Track 1
        or Track 2. With the exception of terminal\r\nstations, predictions at the
        same station with different Group\r\nvalues refer to trains on different tracks.\r\n\r\n\r\n\r\nLine\r\n\r\nTwo-letter
        abbreviation for the line (e.g.: RD, BL, YL, OR, GR,\r\nor SV). May also be
        blank or No for\r\ntrains with no passengers.\r\n\r\n\r\n\r\nLocationCode\r\n\r\nStation
        code for where the train is arriving. Useful when\r\npassing in All as the
        StationCodes\r\nparameter. Use this value in other rail-related APIs to retrieve\r\ndata
        about a station.\r\n\r\n\r\n\r\nLocationName\r\n\r\nFull name of the station
        where the train is arriving. Useful\r\nwhen passing in All as the\r\nStationCodes
        parameter.\r\n\r\n\r\n\r\nMin\r\n\r\nMinutes until arrival. Can be a numeric
        value, ARR (arriving), BRD (boarding), ---, or empty."
      operationId: getJsonGetpredictionStationcodes
      x-api-path-slug: jsongetpredictionstationcodes-get
      parameters:
      - in: path
        name: StationCodes
        description: Comma-separated list of station codes
      responses:
        200:
          description: OK
      tags:
      - Transit
      - Rail
      - Prediction
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