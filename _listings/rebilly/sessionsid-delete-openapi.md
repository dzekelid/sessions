---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Delete a Session
  description: Delete a Session with predefined identifier string
  termsOfService: https://www.rebilly.com/terms/
  contact:
    name: Rebilly API Support
    url: https://www.rebilly.com/contact/
    email: integrations@rebilly.com
  version: "2.1"
host: api.rebilly.com
basePath: /v2.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    get:
      summary: Retrieve a list of sessions
      description: Retrieve a list of sessions
      operationId: retrieve-a-list-of-sessions
      x-api-path-slug: sessions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Sessions
    post:
      summary: Create a session
      description: Create a session
      operationId: create-a-session
      x-api-path-slug: sessions-post
      parameters:
      - in: body
        name: body
        description: Sessions resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Session
  /sessions/{id}:
    delete:
      summary: Delete a Session
      description: Delete a Session with predefined identifier string
      operationId: delete-a-session-with-predefined-identifier-string
      x-api-path-slug: sessionsid-delete
      responses:
        200:
          description: OK
      tags:
      - Session
    get:
      summary: Retrieve a Session
      description: Retrieve a Session with specified identifier string
      operationId: retrieve-a-session-with-specified-identifier-string
      x-api-path-slug: sessionsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Session
    put:
      summary: Create or update a Session with predefined ID
      description: Create or update a Session with predefined identifier string
      operationId: create-or-update-a-session-with-predefined-identifier-string
      x-api-path-slug: sessionsid-put
      parameters:
      - in: body
        name: body
        description: Session resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Session
      - Predefined
      - ID
  /signin:
    post:
      summary: Create a session with email and password
      description: Create a session with email and password
      operationId: create-a-session-with-email-and-password
      x-api-path-slug: signin-post
      parameters:
      - in: body
        name: body
        description: Signin resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Session
      - Email
      - Password
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