---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 0
info:
  title: Mattermost API Revoke a user session
  description: |-
    Revokes a user session from the provided user id and session id strings.
    ##### Permissions
    Must be logged in as the user being updated or have the `edit_other_users` permission.
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{user_id}/sessions:
    get:
      summary: Get user's sessions
      description: |-
        Get a list of sessions by providing the user GUID. Sensitive information will be sanitized out.
        ##### Permissions
        Must be logged in as the user being updated or have the `edit_other_users` permission.
      operationId: get-a-list-of-sessions-by-providing-the-user-guid-sensitive-information-will-be-sanitized-out-permis
      x-api-path-slug: usersuser-idsessions-get
      parameters:
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Users
      - Sessions
  /users/{user_id}/sessions/revoke:
    post:
      summary: Revoke a user session
      description: |-
        Revokes a user session from the provided user id and session id strings.
        ##### Permissions
        Must be logged in as the user being updated or have the `edit_other_users` permission.
      operationId: revokes-a-user-session-from-the-provided-user-id-and-session-id-strings-permissionsmust-be-logged-in
      x-api-path-slug: usersuser-idsessionsrevoke-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - User
      - Session
  /users/{user_id}/sessions/revoke/all:
    post:
      summary: Revoke all active sessions for a user
      description: |-
        Revokes all user sessions from the provided user id and session id strings.
        ##### Permissions
        Must be logged in as the user being updated or have the `edit_other_users` permission.
        __Minimum server version__: 4.4
      operationId: revokes-all-user-sessions-from-the-provided-user-id-and-session-id-strings-permissionsmust-be-logged
      x-api-path-slug: usersuser-idsessionsrevokeall-post
      parameters:
      - in: path
        name: user_id
        description: User GUID
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - ""
      - Active
      - Sessionsa
      - User
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