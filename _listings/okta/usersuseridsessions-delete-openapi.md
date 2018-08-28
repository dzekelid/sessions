---
swagger: "2.0"
x-collection-name: Okta
x-complete: 0
info:
  title: Okta Clear User Sessions
  description: Clear user sessions.
  version: 1.0.0
host: example.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{userId}/sessions:
    delete:
      summary: Clear User Sessions
      description: Clear user sessions.
      operationId: deleteUsersUserSessions
      x-api-path-slug: usersuseridsessions-delete
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: userId
      responses:
        200:
          description: OK
      tags:
      - Clear
      - User
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