---
swagger: "2.0"
x-collection-name: Trello
x-complete: 0
info:
  title: Trello Put Sessions
  description: Put sessions.
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    post:
      summary: Post Sessions
      description: Post sessions.
      operationId: addSessions
      x-api-path-slug: sessions-post
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/socket:
    get:
      summary: Get Sessions Socket
      description: Get sessions socket.
      operationId: getSessionsSocket
      x-api-path-slug: sessionssocket-get
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Socket
  /sessions/{idSession}:
    put:
      summary: Put Sessions
      description: Put sessions.
      operationId: updateSessionsByIdSession
      x-api-path-slug: sessionsidsession-put
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idSession
        description: idSession
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
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