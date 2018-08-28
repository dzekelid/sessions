---
swagger: "2.0"
x-collection-name: Google Adsense
x-complete: 0
info:
  title: Google Adsense API Create Session
  version: 1.0.0
  description: Create an association session for initiating an association with an
    AdSense user.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /associationsessions/start:
    get:
      summary: Create Session
      description: Create an association session for initiating an association with
        an AdSense user.
      operationId: adsensehost.associationsessions.start
      x-api-path-slug: associationsessionsstart-get
      parameters:
      - in: query
        name: productCode
        description: Products to associate with the user
      - in: query
        name: userLocale
        description: The preferred locale of the user
      - in: query
        name: websiteLocale
        description: The locale of the users hosted website
      - in: query
        name: websiteUrl
        description: The URL of the users hosted website
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Session
  /associationsessions/verify:
    get:
      summary: Verify Session
      description: Verify an association session after the association callback returns
        from AdSense signup.
      operationId: adsensehost.associationsessions.verify
      x-api-path-slug: associationsessionsverify-get
      parameters:
      - in: query
        name: token
        description: The token returned to the association callback URL
      responses:
        200:
          description: OK
      tags:
      - Advertising
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