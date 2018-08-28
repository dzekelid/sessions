swagger: "2.0"
x-collection-name: Google Adsense
x-complete: 1
info:
  title: Google Adsense Merged API
  version: 1.0.0
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