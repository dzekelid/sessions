---
swagger: "2.0"
x-collection-name: Google Cloud Spanner
x-complete: 0
info:
  title: Google Cloud Spanner API Get Session
  description: |-
    Gets a session. Returns `NOT_FOUND` if the session does not exist.
    This is mainly useful for determining whether a session is still
    alive.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: spanner.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{database}/sessions:
    post:
      summary: Create Session
      description: |-
        Creates a new session. A session can be used to perform
        transactions that read and/or modify data in a Cloud Spanner database.
        Sessions are meant to be reused for many consecutive
        transactions.

        Sessions can only execute one transaction at a time. To execute
        multiple concurrent read-write/write-only transactions, create
        multiple sessions. Note that standalone reads and queries use a
        transaction internally, and count toward the one transaction
        limit.

        Cloud Spanner limits the number of sessions that can exist at any given
        time; thus, it is a good idea to delete idle and/or unneeded sessions.
        Aside from explicit deletes, Cloud Spanner can delete sessions for
        which no operations are sent for more than an hour, or due to
        internal errors. If a session is deleted, requests to it
        return `NOT_FOUND`.

        Idle sessions can be kept alive by sending a trivial SQL query
        periodically, e.g., `"SELECT 1"`.
      operationId: spanner.projects.instances.databases.sessions.create
      x-api-path-slug: v1databasesessions-post
      parameters:
      - in: path
        name: database
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Session
  /v1/{name}:
    delete:
      summary: End Session
      description: Ends a session, releasing server resources associated with it.
      operationId: spanner.projects.instances.databases.sessions.delete
      x-api-path-slug: v1name-delete
      parameters:
      - in: path
        name: name
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Session
    get:
      summary: Get Session
      description: |-
        Gets a session. Returns `NOT_FOUND` if the session does not exist.
        This is mainly useful for determining whether a session is still
        alive.
      operationId: spanner.projects.instances.databases.sessions.get
      x-api-path-slug: v1name-get
      parameters:
      - in: path
        name: name
        description: Required
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