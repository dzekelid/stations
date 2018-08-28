swagger: "2.0"
x-collection-name: Netatmo
x-complete: 1
info:
  title: Netatmo
  description: we-develop-groundbreaking-intuitive-and-beautifullydesigned-connected-consumer-electronics--truly-smart-our-innovative-products-provide-a-seamless-experience-that-helps-users-create-a-safer-healthier-and-more-comfortable-home---we-carefully-design-the-mechanics-electronics-and-embedded-software-of-all-our-products-to-the-highest-standards--our-mobile-and-web-applications-are-designed-to-be-simple-to-operate-yet-deliver-a-rich-user-experience-
  termsOfService: https://dev.netatmo.com/dev/resources/legal/introduction
  contact:
    name: Netatmo
    email: contact-api@netatmo.com
  version: 1.1.1
host: api.netatmo.net
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /getstationsdata:
    get:
      summary: Get Getstationsdata
      description: The method getstationsdata Returns data from a user Weather Stations
        (measures and device specific data).
      operationId: getstationsdata
      x-api-path-slug: getstationsdata-get
      parameters:
      - in: query
        name: device_id
        description: Id of the device you want to retrieve information of
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Stations