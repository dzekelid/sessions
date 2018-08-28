---
name: Coord
x-slug: coord
description: Coord is a mobility company that creates seamless mobility and self-driving
  experiences today through deep integrations. The company offers bike-share API,
  Curbs API, Tolls API, Routing API and etc.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
x-kinRank: "7"
x-alexaRank: "1035226"
tags: Sessions
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/apis.md
specificationVersion: "0.14"
apis:
- name: Parking Access API - Retrieve a location's sessions
  x-api-slug: location-idsession-get
  description: |-
    Retrieve information about all existing sessions at a location.

    On success, the response will be a list of existing sessions. At most one will still be
    active:
    ```
      [
        {
          "id":1,
          "start_time":"2018-04-12T00:14:20.292Z",
          "end_time":"2018-04-12T04:10:13.456Z",
          "user_id":"00000000-0000-0000-0000-000000000000"
        },
        {
          "id":2,
          "start_time":"2018-04-12T00:14:20.292Z",
          "user_id":"00000000-0000-0000-0000-000000000000"
        }
      ]
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-get-openapi.md
- name: Parking Access API - Retrieve a user's sessions
  x-api-slug: session-get
  description: |-
    Retrieve information about all of a user's existing sessions.

    On success, the response will be a list of existing sessions. At most one will still be
    active:
    ```
      [
        {
          "id":1,
          "start_time":"2018-04-12T00:14:20.292Z",
          "end_time":"2018-04-12T04:10:13.456Z",
          "user_id":"00000000-0000-0000-0000-000000000000"
        },
        {
          "id":2,
          "start_time":"2018-04-12T00:14:20.292Z",
          "user_id":"00000000-0000-0000-0000-000000000000"
        }
      ]
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/session-get-openapi.md
- name: Parking Access API - Create a new session
  x-api-slug: location-idsession-post
  description: |-
    Create a new session for the specified user at this location_id. Returns it with either
    the start_time set, or a follow-on token (barcode, number, etc.) that the end user must use
    to initiate the session at the location.

    On success, the response will be the newly created session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-openapi.md
- name: Parking Access API - Retrieve an existing session
  x-api-slug: location-idsessionsession-id-get
  description: |-
    Retrieve information about an existing session. This is useful to determine if/when an
    existing session has been started or ended (via external, barcode mechanism, for example).
    It may be polled to provide live feedback to an end user.

    On success, the response will be the existing session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-openapi.md
- name: Parking Access API - End a previously started session
  x-api-slug: location-idsessionsession-idend-put
  description: |-
    End a previously started session. Note that it is invalid to call this method for sessions
    where checkout is controlled physically (those returned with a `redemption_info` field).

    On success, the response will be the existing session with billing info:
    ```
      {
        "billing_info": {
          "cost": {
            "amount": 100,
            "currency": "USD"
          }
        },
        "end_time": "2018-04-12T00:17:50.161Z",
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-idend-put-openapi.md
- name: Parking Access API - Create a new session
  x-api-slug: location-idsession-post
  description: |-
    Create a new session for the specified user at this location_id. Returns it with either
    the start_time set, or a follow-on token (barcode, number, etc.) that the end user must use
    to initiate the session at the location.

    On success, the response will be the newly created session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-openapi.md
- name: Parking Access API - Retrieve an existing session
  x-api-slug: location-idsessionsession-id-get
  description: |-
    Retrieve information about an existing session. This is useful to determine if/when an
    existing session has been started or ended (via external, barcode mechanism, for example).
    It may be polled to provide live feedback to an end user.

    On success, the response will be the existing session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-openapi.md
- name: Parking Access API - End a previously started session
  x-api-slug: location-idsessionsession-idend-put
  description: |-
    End a previously started session. Note that it is invalid to call this method for sessions
    where checkout is controlled physically (those returned with a `redemption_info` field).

    On success, the response will be the existing session with billing info:
    ```
      {
        "billing_info": {
          "cost": {
            "amount": 100,
            "currency": "USD"
          }
        },
        "end_time": "2018-04-12T00:17:50.161Z",
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-idend-put-openapi.md
- name: Parking Access API - End a previously started session
  x-api-slug: location-idsessionsession-idend-put
  description: |-
    End a previously started session. Note that it is invalid to call this method for sessions
    where checkout is controlled physically (those returned with a `redemption_info` field).

    On success, the response will be the existing session with billing info:
    ```
      {
        "billing_info": {
          "cost": {
            "amount": 100,
            "currency": "USD"
          }
        },
        "end_time": "2018-04-12T00:17:50.161Z",
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-idend-put-openapi.md
- name: Parking Access API - Retrieve an existing session
  x-api-slug: location-idsessionsession-id-get
  description: |-
    Retrieve information about an existing session. This is useful to determine if/when an
    existing session has been started or ended (via external, barcode mechanism, for example).
    It may be polled to provide live feedback to an end user.

    On success, the response will be the existing session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsessionsession-id-get-openapi.md
- name: Parking Access API - Create a new session
  x-api-slug: location-idsession-post
  description: |-
    Create a new session for the specified user at this location_id. Returns it with either
    the start_time set, or a follow-on token (barcode, number, etc.) that the end user must use
    to initiate the session at the location.

    On success, the response will be the newly created session:
    ```
      {
        "id":1,
        "start_time":"2018-04-12T00:14:20.292Z",
        "user_id":"00000000-0000-0000-0000-000000000000"
      }
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/coord/location-idsession-post-openapi.md
x-common:
- type: x-blog
  url: https://medium.com/coord
- type: x-blog-rss
  url: https://medium.com/feed/coord
- type: x-openapi
  url: https://jsapi.apiary.io/apis/coordprodsearchtolls.source
- type: x-api-gallery
  url: http://convertapi.api.gallery.streamdata.io
- type: x-api-stack
  url: http://coord.stack.network
- type: x-developer
  url: https://coord.co/docs/
- type: x-pricing
  url: https://coord.co/#pricing
- type: x-twitter
  url: https://twitter.com/coordcity
- type: x-website
  url: https://coord.co
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---