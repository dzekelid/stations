---
name: Ship Station
x-slug: ship-station
description: ShipStation is a web-based shipping solution that streamlines the order
  fulfillment process for your online business. ShipStation consolidates orders from
  over 70 ecommerce channels, creates shipping labels, packing slips, and pick lists
  in batch, communicates tracking information to your customers, provides endless
  automation, filters, and views, wireless printing, a mobile app, and a lot more.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ShipStation-stacked-blue.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Stations
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/ship-station/apis.md
specificationVersion: "0.14"
apis:
- name: Ship Station Developer Portal - Register Account
  x-api-slug: accountsregisteraccount-post
  description: "Creates a new ShipStation account and generates an apiKey and apiSecret
    to be used by the newly created account. PLEASE NOTE: This endpoint does not require
    API key and API Secret credentials.  The Authorization header can be left off.
    Use of this specific endpoint requires approval, and is meant only for direct
    partners of ShipStation. This is the only endpoint to require approval. All other
    endpoints listed in this document can be accessed by submitting proper authorization
    credentials in the header of the request. To become a direct partner of ShipStation,
    or to request more information on becoming a direct partner, we recommend reaching
    out to our Partners and Integrations team here: https://info.shipstation.com/become-a-partner-api-and-custom-store-integrations\n\nThe
    body of this request has the following attributes:\n\nName               |Data
    Type          |Description\n-------------------|-------------------|-------------------\n``firstName``
    \ | string, required | First Name\n``lastName`` | string, required | Last Name\n``email``
    | string, required | Email address. This will also be the username of the account.\n``password``
    | string, required | Password to set for account access.\n``companyName`` | string,
    optional | Name of Company.\n``addr1`` | string, optional | Company Address -
    Street 1\n``addr2`` | string, optional | Company Address - Street 2\n``city``
    | string, optional | Company Address - City\n``state`` | string, optional | Company
    Address - State \n``zip`` | string, optional | Company Address - Zip Code\n``countryCode``
    |string, optional | Company Address - Country.  Please use a 2-character country
    code.\n``phone`` | string, optional | Company Phone number."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ShipStation-stacked-blue.png
  humanURL: http://bit.ly/_ShipStation
  baseURL: https://ssapi.shipstation.com//
  tags: Shipping, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/stations/master/_listings/ship-station/accountsregisteraccount-post-openapi.md
x-common:
- type: x-website
  url: http://bit.ly/_ShipStation
- type: x-api-gallery
  url: http://server.density.api.gallery.streamdata.io
- type: x-api-stack
  url: http://ship.station.stack.network
- type: x-blog
  url: https://www.shipstation.com/blog/
- type: x-developer
  url: https://shipstation.docs.apiary.io/#
- type: x-github
  url: https://github.com/shipstation
- type: x-partners
  url: https://www.shipstation.com/partners/
- type: x-pricing
  url: https://www.shipstation.com/pricing/
- type: x-twitter
  url: https://twitter.com/ShipStation
- type: x-website
  url: http://shipstation.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---