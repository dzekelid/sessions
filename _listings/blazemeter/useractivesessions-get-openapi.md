---
swagger: "2.0"
x-collection-name: BlazeMeter
x-complete: 0
info:
  title: Blazemeter Get User Active Sessions
  description: Get user active sessions.
  version: 1.0.0
host: a.blazemeter.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/active/sessions:
    get:
      summary: Get User Active Sessions
      description: Get user active sessions.
      operationId: active_sessions
      x-api-path-slug: useractivesessions-get
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - User
      - Active
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