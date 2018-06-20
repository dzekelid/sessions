---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Training Get Sessions by Date Range
  description: This call returns all session details over a given date range for a
    given organizer. A session is a completed training event.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2T/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reports/organizers/{organizerKey}/sessions:
    post:
      summary: Get Sessions by Date Range
      description: This call returns all session details over a given date range for
        a given organizer. A session is a completed training event.
      operationId: getSessionDetailsForDateRange
      x-api-path-slug: reportsorganizersorganizerkeysessions-post
      parameters:
      - in: body
        name: body
        description: The start and end times for the time range over which to retrieve
          training sessions
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
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