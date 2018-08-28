---
swagger: "2.0"
x-collection-name: EhrScape
x-complete: 0
info:
  title: Ehr Scape Electronic Health Record APIs Pings an OpenEhr session.
  description: Pings an openehr session..
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: rest.ehrscape.com
basePath: /rest/v1
paths:
  /session:
    delete:
      summary: Closes an OpenEhr session.
      description: Closes an openehr session..
      operationId: close
      x-api-path-slug: session-delete
      parameters:
      - in: header
        name: Ehr-Session
        description: The ID of the session to close
      - in: query
        name: sessionId
        description: The ID of the session to close
      responses:
        200:
          description: OK
      tags:
      - Session
    post:
      summary: Creates a new OpenEhr session.
      description: Creates a new openehr session..
      operationId: login
      x-api-path-slug: session-post
      parameters:
      - in: query
        name: password
        description: Password
      - in: query
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Session
    put:
      summary: Pings an OpenEhr session.
      description: Pings an openehr session..
      operationId: ping
      x-api-path-slug: session-put
      parameters:
      - in: header
        name: Ehr-Session
        description: The ID of the session to ping
      - in: query
        name: sessionId
        description: The ID of the session to ping
      responses:
        200:
          description: OK
      tags:
      - Session
  /session/ehr/{ehrId}:
    put:
      summary: Sets the EHR on the session.
      description: Sets the ehr on the session..
      operationId: useEhr
      x-api-path-slug: sessionehrehrid-put
      parameters:
      - in: header
        name: Ehr-Session
        description: The ID of the session to set the EHR on
      - in: path
        name: ehrId
        description: The ID of the EHR to set on the session
      - in: query
        name: sessionId
        description: The ID of the session to set the EHR on
      responses:
        200:
          description: OK
      tags:
      - Session
      - Ehr
      - EhrId
  /session/ehr/{subjectNamespace}/{subjectId}:
    put:
      summary: Sets the EHR on the session (via subject namespace and ID).
      description: Sets the ehr on the session (via subject namespace and id)..
      operationId: findAndUseEhr
      x-api-path-slug: sessionehrsubjectnamespacesubjectid-put
      parameters:
      - in: header
        name: Ehr-Session
        description: The ID of the session to set the EHR on
      - in: query
        name: sessionId
        description: The ID of the session to set the EHR on
      - in: path
        name: subjectId
        description: The subject ID
      - in: path
        name: subjectNamespace
        description: The namespace where the subject ID lives
      responses:
        200:
          description: OK
      tags:
      - Session
      - Ehr
      - SubjectNamespace
      - SubjectId
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