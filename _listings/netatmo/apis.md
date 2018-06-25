---
name: Netatmo
x-slug: netatmo
description: We develop groundbreaking, intuitive and beautifully-designed connected
  consumer electronics. Truly smart, our innovative products provide a seamless experience
  that helps users create a safer, healthier and more comfortable home. We carefully
  design the mechanics, electronics and embedded software of all our products to the
  highest standards. Our mobile and web applications are designed to be simple to
  operate, yet deliver a rich user experience.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/netatmo-logo.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Stations
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/netatmo/apis.md
specificationVersion: "0.14"
apis:
- name: Netatmo Get Getstationsdata
  x-api-slug: netatmo
  description: The method getstationsdata Returns data from a user Weather Stations
    (measures and device specific data).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/netatmo-logo.png
  humanURL: http://www.netatmo.com
  baseURL: https://api.netatmo.net//api//getstationsdata
  tags: Weather,Stations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/netatmo/getstationsdata-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/netatmo/getstationsdata-get-openapi.md
- name: Netatmo
  x-api-slug: netatmo
  description: Netatmo offers wireless thermostats and air quality measuring devices
    that can be accessed over the internet. Their Private API allows device owners
    to grant third party applications access to their devices in order to retrieve
    the data the devices have recorded. In the near future, developers will also have
    access to the Netatmo Public API, which will allow third party applications to
    retrieve data that has been marked as public by the device&#039;s owner.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/netatmo-logo.png
  humanURL: http://www.netatmo.com
  baseURL: https://api.netatmo.net//api
  tags: Stations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/netatmo/openapi.md
x-common:
- type: x-website
  url: http://www.netatmo.com
- type: x-documentation
  url: https://dev.netatmo.com/resources/technical/reference
- type: x-github
  url: https://github.com/netatmo
- type: x-twitter
  url: https://twitter.com/netatmo
- type: x-website
  url: http://netatmo.net
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---