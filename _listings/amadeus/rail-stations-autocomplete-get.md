---
swagger: "2.0"
info:
  title: Amadeus
  description: Amadeus API is a toolkit designed for travel agencies who want to develop
    their own travel products rather than using off-the-shelf solutions. With this
    tool, you can build your very own customised applications that link in a stable
    and secure dialogue with our Global Distribution System (GDS).
  contact:
    name: Amadeus Innovation and Research
    url: https://sandbox.amadeus.com
  version: 1.0.0
host: api.sandbox.amadeus.com
basePath: /v1.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rail-stations/autocomplete:
    get:
      summary: Get Rail Stations Autocomplete
      description: Given the start of any word in a rail station's official name,
        as a term, this API provides the full name and rail station ID of a rail station
        for use in searches
      operationId: getRailStationsAutocomplete
      parameters:
      - in: query
        name: term
        description: Search term that should represent some part of a station name
      responses:
        200:
          description: OK
      tags:
      - rail
      - stations
      - autocomplete
definitions:
  Address:
    properties:
      city:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      line1:
        description: This is a default description.
        type: get
      postal_code:
        description: This is a default description.
        type: get
      region:
        description: This is a default description.
        type: get
  AffiliateFlightSearchPrice:
    properties:
      currency:
        description: This is a default description.
        type: get
      total_price:
        description: This is a default description.
        type: get
  AffiliatePayout:
    properties: []
  AffiliateSearchMeta:
    properties: []
  AffiliateSearchResponse:
    properties:
      results:
        description: This is a default description.
        type: get
  AffiliateSearchResult:
    properties:
      airline:
        description: This is a default description.
        type: get
      deep_link:
        description: This is a default description.
        type: get
  Airport:
    properties:
      airport:
        description: This is a default description.
        type: get
      terminal:
        description: This is a default description.
        type: get
  AirportAutocompleteResponse:
    properties:
      label:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  AirportInformation:
    properties:
      aircraft_movements:
        description: This is a default description.
        type: get
      city_code:
        description: This is a default description.
        type: get
      city_name:
        description: This is a default description.
        type: get
      code:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      timezone:
        description: This is a default description.
        type: get
  Amenity:
    properties:
      amenity:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      ota_code:
        description: This is a default description.
        type: get
  Amount:
    properties:
      amount:
        description: This is a default description.
        type: get
      currency:
        description: This is a default description.
        type: get
  Award:
    properties:
      provider:
        description: This is a default description.
        type: get
      rating:
        description: This is a default description.
        type: get
  CarReservation:
    properties:
      drop_off:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      origin:
        description: This is a default description.
        type: get
      pick_up:
        description: This is a default description.
        type: get
      traveler_ids:
        description: This is a default description.
        type: get
  CarReservationBookingInfo:
    properties:
      reservation_code:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
  CarSearchResponse:
    properties:
      results:
        description: This is a default description.
        type: get
  CarSearchResult:
    properties:
      airport:
        description: This is a default description.
        type: get
      cars:
        description: This is a default description.
        type: get
  CarrierInfo:
    properties:
      name:
        description: This is a default description.
        type: get
  CityInformation:
    properties:
      code:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      currency:
        description: This is a default description.
        type: get
      geonames_ID:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      timezone:
        description: This is a default description.
        type: get
  Company:
    properties:
      company_code:
        description: This is a default description.
        type: get
      company_name:
        description: This is a default description.
        type: get
  Contact:
    properties:
      detail:
        description: This is a default description.
        type: get
      purpose:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  Error:
    properties:
      message:
        description: This is a default description.
        type: get
      more_info:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
  ExtensiveTrainSearchResponse:
    properties:
      results:
        description: This is a default description.
        type: get
  ExtensiveTrainSearchResult:
    properties:
      itineraries:
        description: This is a default description.
        type: get
  ExtremeSearchResponse:
    properties:
      currency:
        description: This is a default description.
        type: get
      origin:
        description: This is a default description.
        type: get
      results:
        description: This is a default description.
        type: get
  ExtremeSearchResult:
    properties:
      airline:
        description: This is a default description.
        type: get
      departure_date:
        description: This is a default description.
        type: get
      destination:
        description: This is a default description.
        type: get
      price:
        description: This is a default description.
        type: get
      return_date:
        description: This is a default description.
        type: get
  Fare:
    properties:
      tax:
        description: This is a default description.
        type: get
      total_fare:
        description: This is a default description.
        type: get
  FareRestrictions:
    properties:
      change_penalties:
        description: This is a default description.
        type: get
      refundable:
        description: This is a default description.
        type: get
  Fees:
    properties:
      creditcard_fees:
        description: This is a default description.
        type: get
      service_fees:
        description: This is a default description.
        type: get
  FlightReservationBookingInfo:
    properties:
      airline_record_locator:
        description: This is a default description.
        type: get
      booking_code:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
      travel_class:
        description: This is a default description.
        type: get
  FlightReservationBound:
    properties:
      flights:
        description: This is a default description.
        type: get
  FlightReservationSegment:
    properties:
      arrives_at:
        description: This is a default description.
        type: get
      departs_at:
        description: This is a default description.
        type: get
      flight_number:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      marketing_airline:
        description: This is a default description.
        type: get
      operating_airline:
        description: This is a default description.
        type: get
      traveler_ids:
        description: This is a default description.
        type: get
  FlightSearchBookingInfo:
    properties:
      booking_code:
        description: This is a default description.
        type: get
      cabin_code:
        description: This is a default description.
        type: get
      fare_basis:
        description: This is a default description.
        type: get
      fare_family:
        description: This is a default description.
        type: get
      seats_remaining:
        description: This is a default description.
        type: get
      travel_class:
        description: This is a default description.
        type: get
  FlightSearchBound:
    properties:
      duration:
        description: This is a default description.
        type: get
      flights:
        description: This is a default description.
        type: get
  FlightSearchItinerary:
    properties: []
  FlightSearchPrice:
    properties:
      total_price:
        description: This is a default description.
        type: get
  FlightSearchSegment:
    properties:
      aircraft:
        description: This is a default description.
        type: get
      arrives_at:
        description: This is a default description.
        type: get
      departs_at:
        description: This is a default description.
        type: get
      flight_number:
        description: This is a default description.
        type: get
      marketing_airline:
        description: This is a default description.
        type: get
      operating_airline:
        description: This is a default description.
        type: get
  FlightTicket:
    properties:
      flight_bounds:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      traveler_ids:
        description: This is a default description.
        type: get
  FlightTrafficSearchResult:
    properties:
      destination:
        description: This is a default description.
        type: get
      flights:
        description: This is a default description.
        type: get
      period:
        description: This is a default description.
        type: get
      travelers:
        description: This is a default description.
        type: get
  FrequentTravelerCard:
    properties:
      card_number:
        description: This is a default description.
        type: get
      company_code:
        description: This is a default description.
        type: get
      issuer_type:
        description: This is a default description.
        type: get
  Geolocation:
    properties:
      google_maps_link:
        description: This is a default description.
        type: get
      latitude:
        description: This is a default description.
        type: get
      longitude:
        description: This is a default description.
        type: get
  HotelPropertyResponse:
    properties:
      amenities:
        description: This is a default description.
        type: get
      awards:
        description: This is a default description.
        type: get
      contacts:
        description: This is a default description.
        type: get
      images:
        description: This is a default description.
        type: get
      property_code:
        description: This is a default description.
        type: get
      property_name:
        description: This is a default description.
        type: get
      rooms:
        description: This is a default description.
        type: get
  HotelReservation:
    properties:
      check_in:
        description: This is a default description.
        type: get
      check_out:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      property_code:
        description: This is a default description.
        type: get
      property_name:
        description: This is a default description.
        type: get
      traveler_ids:
        description: This is a default description.
        type: get
  HotelReservationBookingInfo:
    properties:
      reservation_code:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
  HotelRoom:
    properties:
      booking_code:
        description: This is a default description.
        type: get
      descriptions:
        description: This is a default description.
        type: get
      rate_plan_code:
        description: This is a default description.
        type: get
      rate_type_code:
        description: This is a default description.
        type: get
      rates:
        description: This is a default description.
        type: get
      room_type_code:
        description: This is a default description.
        type: get
  HotelSearchResponse:
    properties:
      results:
        description: This is a default description.
        type: get
  Image:
    properties:
      category:
        description: This is a default description.
        type: get
      height:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
  ImageSize:
    properties: []
  Infant:
    properties:
      date_of_birth:
        description: This is a default description.
        type: get
      first_name:
        description: This is a default description.
        type: get
      last_name:
        description: This is a default description.
        type: get
  Link:
    properties:
      href:
        description: This is a default description.
        type: get
  LocationResponse:
    properties:
      airports:
        description: This is a default description.
        type: get
  Logos:
    properties:
      medium:
        description: This is a default description.
        type: get
      small:
        description: This is a default description.
        type: get
  LowFareSearchResponse:
    properties:
      currency:
        description: This is a default description.
        type: get
      results:
        description: This is a default description.
        type: get
  LowFareSearchResult:
    properties:
      itineraries:
        description: This is a default description.
        type: get
  Message:
    properties:
      message:
        description: This is a default description.
        type: get
      severity:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  NearestAirport:
    properties:
      aircraft_movements:
        description: This is a default description.
        type: get
      airport:
        description: This is a default description.
        type: get
      airport_name:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      city_name:
        description: This is a default description.
        type: get
      distance:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      timezone:
        description: This is a default description.
        type: get
  OtherReservation:
    properties:
      date:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      location:
        description: This is a default description.
        type: get
      traveler_ids:
        description: This is a default description.
        type: get
  OtherReservationBookingInfo:
    properties:
      status:
        description: This is a default description.
        type: get
  PeriodRate:
    properties:
      currency:
        description: This is a default description.
        type: get
      end_date:
        description: This is a default description.
        type: get
      price:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
  PointOfInterestCity:
    properties:
      geoname_id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      total_points_of_interest:
        description: This is a default description.
        type: get
  PointOfInterestDetails:
    properties:
      description:
        description: This is a default description.
        type: get
      short_description:
        description: This is a default description.
        type: get
      wiki_page_link:
        description: This is a default description.
        type: get
  PointOfInterestResult:
    properties:
      categories:
        description: This is a default description.
        type: get
      contextual_images:
        description: This is a default description.
        type: get
      geoname_id:
        description: This is a default description.
        type: get
      grades:
        description: This is a default description.
        type: get
      main_image:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      walk_time:
        description: This is a default description.
        type: get
  PointsOfInterestResponse:
    properties:
      points_of_interest:
        description: This is a default description.
        type: get
  RailService:
    properties:
      destination_station_id:
        description: This is a default description.
        type: get
      services:
        description: This is a default description.
        type: get
  RailStationAutocompleteResponse:
    properties:
      label:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  RailStationResponse:
    properties:
      country:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      short_name:
        description: This is a default description.
        type: get
      traffic:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  Rate:
    properties:
      type:
        description: This is a default description.
        type: get
  Reservation:
    properties:
      cars:
        description: This is a default description.
        type: get
      hotels:
        description: This is a default description.
        type: get
      others:
        description: This is a default description.
        type: get
      unticketed_flights:
        description: This is a default description.
        type: get
  RestrictedRate:
    properties:
      rate_code:
        description: This is a default description.
        type: get
      rate_name:
        description: This is a default description.
        type: get
      restrictions:
        description: This is a default description.
        type: get
  RoomInfo:
    properties:
      bed_type:
        description: This is a default description.
        type: get
      number_of_beds:
        description: This is a default description.
        type: get
      room_type:
        description: This is a default description.
        type: get
  Station:
    properties:
      station_code:
        description: This is a default description.
        type: get
      station_name:
        description: This is a default description.
        type: get
  TopDestinationsSearchResponse:
    properties:
      origin:
        description: This is a default description.
        type: get
      period:
        description: This is a default description.
        type: get
      results:
        description: This is a default description.
        type: get
  TopDestinationsSearchResult:
    properties:
      destination:
        description: This is a default description.
        type: get
      flights:
        description: This is a default description.
        type: get
      travelers:
        description: This is a default description.
        type: get
  TopSearchesSearchResponse:
    properties:
      destination:
        description: This is a default description.
        type: get
      market:
        description: This is a default description.
        type: get
      origin:
        description: This is a default description.
        type: get
      period:
        description: This is a default description.
        type: get
      results:
        description: This is a default description.
        type: get
  TopSearchesSearchResult:
    properties:
      destination:
        description: This is a default description.
        type: get
      searches:
        description: This is a default description.
        type: get
      searches_prior_year:
        description: This is a default description.
        type: get
  TrainScheduleSearchResponse:
    properties:
      results:
        description: This is a default description.
        type: get
  TrainScheduleSearchResult:
    properties:
      date:
        description: This is a default description.
        type: get
      origin_station_id:
        description: This is a default description.
        type: get
      services:
        description: This is a default description.
        type: get
  TrainSearchItinerary:
    properties:
      trains:
        description: This is a default description.
        type: get
  TrainSearchPricing:
    properties:
      accomodation:
        description: This is a default description.
        type: get
      booking_code:
        description: This is a default description.
        type: get
      service_class:
        description: This is a default description.
        type: get
  TrainSearchSegment:
    properties:
      arrives_at:
        description: This is a default description.
        type: get
      departs_at:
        description: This is a default description.
        type: get
      marketing_company:
        description: This is a default description.
        type: get
      operating_company:
        description: This is a default description.
        type: get
      prices:
        description: This is a default description.
        type: get
      train_number:
        description: This is a default description.
        type: get
      train_type:
        description: This is a default description.
        type: get
  TravelRecordHeader:
    properties:
      creation_office_id:
        description: This is a default description.
        type: get
      owner_office_id:
        description: This is a default description.
        type: get
  TravelRecordResponse:
    properties:
      messages:
        description: This is a default description.
        type: get
      record_locator:
        description: This is a default description.
        type: get
      travelers:
        description: This is a default description.
        type: get
  Traveler:
    properties:
      contacts:
        description: This is a default description.
        type: get
      date_of_birth:
        description: This is a default description.
        type: get
      first_name:
        description: This is a default description.
        type: get
      frequent_traveler_cards:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      last_name:
        description: This is a default description.
        type: get
      traveler_type:
        description: This is a default description.
        type: get
  Vehicle:
    properties:
      images:
        description: This is a default description.
        type: get
      rates:
        description: This is a default description.
        type: get
  VehicleInfo:
    properties:
      acriss_code:
        description: This is a default description.
        type: get
      air_conditioning:
        description: This is a default description.
        type: get
      category:
        description: This is a default description.
        type: get
      fuel:
        description: This is a default description.
        type: get
      transmission:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
x-collection-name: Amadeus
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