---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToAssist Remote Support Get All Sessions
  description: "This method retrieves detailed information about all current or previous
    support sessions (either attended or unattended) for a specified date range. Information
    about sessions that are complete may only be available for a limited period of
    time after the end of the session (currently, the information is available for
    at least 30 days). The session must have been hosted from an account or company
    that the authenticated user has access to.\n\n  Request Parameters                    \n
    \                     \n    field        data type      description    \n    sessionType
    \       string      The type of the session. Must be set to SCREEN_SHARING.    \n\n\n
    \ Response Parameters                    \n                      \n    field        data
    type      description    \n    totalNumSessions        number      The number
    of sessions returned.    \n    For Each Session                    \n    sessionStartToken
    \       number      A numeric value used to start the session.    \n    customerJoinUrl
    \       string      A URL that can be sent to a customer to join the session.
    \   \n    sessionId        number      The unique ID of this session.    \n    sessionType
    \       string      For these sessions, always screen_sharing.    \n    partnerObject
    \        number      The ID of the object in the partner system that is associated
    with this session.    \n    partnerObjectUrl        string      The URL for the
    expert to view the associated partnerObject.    \n    status        string      The
    current state of the session; it can be: \n\nwaiting = Waiting for the customer
    to join the session.\nactive = Customer has joined and session is currently active.\ncomplete
    = Session has ended after the customer joined.\nabandoned = Session has ended
    without any customer joining.\nnotStarted = Session was created but never started
    by the expert.\n  \n    startedAt        ISO 8061 format*      The time that the
    session started.    \n    customerJoinedAt        ISO 8061 format*      The time
    that the customer joined the session.    \n    endedAt        ISO 8061 format*
    \     The time that the session ended.    \n    expertName        string      The
    human-readable name of the first technician in the support session.    \n    expertEmail
    \       string      Email id of the first expert in the session.    \n    expertUserKey
    \       string      Unique ID of the first expert in the session in the G2A system.
    \   \n    customerName        string      The human-readable name of the customer
    in the support session.    \n    customerEmail        string      The email address
    of the customer in the support session.    \n    accountKey        number      The
    unique GoToAssist system ID of the account the support session was hosted from.
    \   \n    sessionRecordingUrl        number      The URL where the technician
    can view a recording of the session within the GoToAssist web application (only
    available if the technician has opted to record support sessions (link is external))
    \   \n                      \n* ISO 8601 format reference"
  version: 1.0.0
host: api.getgo.com
basePath: /G2A/rest/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    get:
      summary: Get All Sessions
      description: "This method retrieves detailed information about all current or
        previous support sessions (either attended or unattended) for a specified
        date range. Information about sessions that are complete may only be available
        for a limited period of time after the end of the session (currently, the
        information is available for at least 30 days). The session must have been
        hosted from an account or company that the authenticated user has access to.\n\n
        \ Request Parameters                    \n                      \n    field
        \       data type      description    \n    sessionType        string      The
        type of the session. Must be set to SCREEN_SHARING.    \n\n\n  Response Parameters
        \                   \n                      \n    field        data type      description
        \   \n    totalNumSessions        number      The number of sessions returned.
        \   \n    For Each Session                    \n    sessionStartToken        number
        \     A numeric value used to start the session.    \n    customerJoinUrl
        \       string      A URL that can be sent to a customer to join the session.
        \   \n    sessionId        number      The unique ID of this session.    \n
        \   sessionType        string      For these sessions, always screen_sharing.
        \   \n    partnerObject         number      The ID of the object in the partner
        system that is associated with this session.    \n    partnerObjectUrl        string
        \     The URL for the expert to view the associated partnerObject.    \n    status
        \       string      The current state of the session; it can be: \n\nwaiting
        = Waiting for the customer to join the session.\nactive = Customer has joined
        and session is currently active.\ncomplete = Session has ended after the customer
        joined.\nabandoned = Session has ended without any customer joining.\nnotStarted
        = Session was created but never started by the expert.\n  \n    startedAt
        \       ISO 8061 format*      The time that the session started.    \n    customerJoinedAt
        \       ISO 8061 format*      The time that the customer joined the session.
        \   \n    endedAt        ISO 8061 format*      The time that the session ended.
        \   \n    expertName        string      The human-readable name of the first
        technician in the support session.    \n    expertEmail        string      Email
        id of the first expert in the session.    \n    expertUserKey        string
        \     Unique ID of the first expert in the session in the G2A system.    \n
        \   customerName        string      The human-readable name of the customer
        in the support session.    \n    customerEmail        string      The email
        address of the customer in the support session.    \n    accountKey        number
        \     The unique GoToAssist system ID of the account the support session was
        hosted from.    \n    sessionRecordingUrl        number      The URL where
        the technician can view a recording of the session within the GoToAssist web
        application (only available if the technician has opted to record support
        sessions (link is external))    \n                      \n* ISO 8601 format
        reference"
      operationId: SessionsGet
      x-api-path-slug: sessions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: fromTime
      - in: query
        name: sessionType
      - in: query
        name: toTime
      responses:
        200:
          description: OK
      tags:
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