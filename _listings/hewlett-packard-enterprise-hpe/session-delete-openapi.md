---
swagger: "2.0"
x-collection-name: Hewlett Packard Enterprise (HPE)
x-complete: 0
info:
  title: HPE OneSphere API Delete Session
  description: Deletes cached data and tokens for the current session.
  termsOfService: http://www.hpe.com/onesphere
  contact:
    name: HPE OneSphere API team
    url: http://www.hpe.com/onesphere
  version: 1.0.0
host: deic02-hpe.hpeonesphere.com
basePath: /rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /session:
    delete:
      summary: Delete Session
      description: Deletes cached data and tokens for the current session.
      operationId: DeleteSession
      x-api-path-slug: session-delete
      responses:
        200:
          description: OK
      tags:
      - Session
    get:
      summary: Get Session
      description: Gets information for the current user.
      operationId: ReadSession
      x-api-path-slug: session-get
      parameters:
      - in: query
        name: view
        description: 'Return related resources:  * `full` - Include the related `user`'
      responses:
        200:
          description: OK
      tags:
      - Session
    post:
      summary: Post Session
      description: |-
        Authenticates a local user and generates an authorization token. This
        token should be used in subsequent HTTP requests as part of
        the "Authorization" header. For example:

        `Authorization: "Bearer <token>"`
      operationId: CreateSession
      x-api-path-slug: session-post
      parameters:
      - in: body
        name: credentials
        description: UserName and Password
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Session
  /session/idp:
    get:
      summary: Get Session P
      description: |-
        **Not implemented**

        Gets the Identity Provider login URL for a userName.
      operationId: ReadSessionIdp
      x-api-path-slug: sessionidp-get
      parameters:
      - in: query
        name: userName
        description: User Name of the User for which login context is needed
      responses:
        200:
          description: OK
      tags:
      - Session
      - P
  /session/sso:
    get:
      summary: Get Session Sso
      description: Get the redirect URL for a configured SSO provider
      operationId: GetSSOLogin
      x-api-path-slug: sessionsso-get
      responses:
        200:
          description: OK
      tags:
      - Session
      - Sso
    post:
      summary: Post Session Sso
      description: Callback for SSO login
      operationId: callback-for-sso-login
      x-api-path-slug: sessionsso-post
      parameters:
      - in: query
        name: token
        description: The unscoped token
      responses:
        200:
          description: OK
      tags:
      - Session
      - Sso
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