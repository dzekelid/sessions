---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost API Reference
  description: -api-v4-is-stable-with-the-mattermost-server-4-0-release--api-v3-was-deprecated-on-january-16th-2018-and-scheduled-for-removal-in-mattermost-v5-0--details-heretagapiv3deprecation--looking-for-the-api-v3-reference-it-has-moved-herehttpsapi-mattermost-comv3-
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
---