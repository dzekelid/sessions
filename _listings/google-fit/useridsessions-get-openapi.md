---
swagger: "2.0"
x-collection-name: Google Fit
x-complete: 0
info:
  title: Google Fit API Get Sessions
  description: Lists sessions previously created.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /fitness/v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{userId}/sessions:
    get:
      summary: Get Sessions
      description: Lists sessions previously created.
      operationId: fitness.users.sessions.list
      x-api-path-slug: useridsessions-get
      parameters:
      - in: query
        name: endTime
        description: An RFC3339 timestamp
      - in: query
        name: includeDeleted
        description: If true, deleted sessions will be returned
      - in: query
        name: pageToken
        description: The continuation token, which is used to page through large result
          sets
      - in: query
        name: startTime
        description: An RFC3339 timestamp
      - in: path
        name: userId
        description: List sessions for the person identified
      responses:
        200:
          description: OK
      tags:
      - Session
  /{userId}/sessions/{sessionId}:
    delete:
      summary: Delete Session
      description: Deletes a session specified by the given session ID.
      operationId: fitness.users.sessions.delete
      x-api-path-slug: useridsessionssessionid-delete
      parameters:
      - in: query
        name: currentTimeMillis
        description: The clients current time in milliseconds since epoch
      - in: path
        name: sessionId
        description: The ID of the session to be deleted
      - in: path
        name: userId
        description: Delete a session for the person identified
      responses:
        200:
          description: OK
      tags:
      - Session
    put:
      summary: Update Session
      description: Updates or insert a given session.
      operationId: fitness.users.sessions.update
      x-api-path-slug: useridsessionssessionid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: currentTimeMillis
        description: The clients current time in milliseconds since epoch
      - in: path
        name: sessionId
        description: The ID of the session to be created
      - in: path
        name: userId
        description: Create sessions for the person identified
      responses:
        200:
          description: OK
      tags:
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