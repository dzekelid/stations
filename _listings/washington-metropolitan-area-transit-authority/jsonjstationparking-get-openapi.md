---
swagger: "2.0"
x-collection-name: Washington Metropolitan Area Transit Authority
x-complete: 0
info:
  title: WMATA Rail Station Information JSON - Parking Information
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
  version: 1.0.0
host: api.wmata.com
basePath: /Rail.svc
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