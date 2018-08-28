---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Futures Get Delayed Futures By Session
  description: Returns delayed quotes for multiple future contracts by exchange session.
  version: 1.0.0
host: www.xignite.com
basePath: xFutures.json/XigniteFutures
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetDelayedFutureBySession:
    get:
      summary: Get Delayed Future By Session
      description: Returns a delayed quote for a future contract by exchange session.
      operationId: postGetdelayedfuturebysession
      x-api-path-slug: getdelayedfuturebysession-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Delayed
      - Future
      - By
      - Session
  /GetAllDelayedFuturesBySession:
    get:
      summary: Get All Delayed Futures By Session
      description: Returns delayed quotes for all contracts for a commodity by exchange
        session.
      operationId: postGetalldelayedfuturesbysession
      x-api-path-slug: getalldelayedfuturesbysession-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Delayed
      - Futures
      - By
      - Session
  /GetDelayedFuturesBySession:
    get:
      summary: Get Delayed Futures By Session
      description: Returns delayed quotes for multiple future contracts by exchange
        session.
      operationId: postGetdelayedfuturesbysession
      x-api-path-slug: getdelayedfuturesbysession-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Delayed
      - Futures
      - By
      - Session
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