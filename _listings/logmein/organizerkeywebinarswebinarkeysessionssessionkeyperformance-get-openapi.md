---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToWebinar Get session performance
  description: Get session performance.
  version: 1.0.0
host: api.getgo.com
basePath: /G2W/rest/organizers
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
    post:
      summary: Start Screen Sharing Session
      description: "This method creates a new screen sharing support session (either
        attended or unattended) by generating a URL that automatically launches technicians
        into a new session when clicked. If a machineUuid request parameter is specified,
        an unattended support session will be created; if it is not specified, then
        an attended session will be created. See \"Request Parameters\" for more information.
        Note: The locale of the session start dialog will be based upon the technician\u2019s
        locale setting within GoToAssist.\n\nNote: This method was formerly named
        \"Create Attended Session,\" but has been renamed to address the fact that
        it now includes unattended support sessions as well.\n\n  Request Parameters
        \                   \n                      \n    field        data type      description
        \   \n    sessionStatusCallbackUrl*        string      The URL that will receive
        a POST when the session status changes. A POST will also be made to the sessionStatusCallbackUrl
        when a customer joins the session and when the session ends (whether or not
        a customer joined). The contents of the POST will be similar as the GET /v1/sessions/
        API. Note: The ID of the session is not known until the session is actually
        started on the endpoint. If the URL is not specified or the session is never
        started (e.g., if the customer cancels the installation of the GoToAssist
        Customer desktop application), then the callback will not be made.    \n    sessionType
        \       string      The type of session to create (only \"SCREEN_SHARING\"
        can be used at this time).    \n    partnerObject*        string      The
        ID of object in the partner system that this session will be associated with.
        \   \n    partnerObjectUrl*        string      The URL that may be used in
        the GoToAssist Expert desktop application if the technician wants to view
        the partner object. Note: The URL can be used in a popup window or iframe
        that is 600 pixels wide and 500 pixels wide. For example, a popup window could
        be created with HTML code as follows: \"Start Remote Support \"    \n    customerName*
        \       string      The name of the customer that the session is being started
        for.    \n    customerEmail*        string      The email address of the customer
        that the session is being started for (if available)    \n    machineUuid*
        \       string      The machineUuid is only necessary for unattended support
        sessions. If the machineUuid is present when a screen sharing session is started,
        then the endpoint will connect to the specified unattended machine and an
        unattended support session will be started. If no machineUuid is specified,
        then an attended support session will be created. A list of machineUuid parameters
        associated with the user and company will be available through a /machines
        API in future.    \n                      \n* Optional parameters\n\nStatus
        Codes              \n              \n    Staus Code      description    \n
        \   200 OK      The response contains the URL to start the session    \n    400
        Bad Request      An error occurred due to missing required parameters or portal
        not being created    \n    401 Unauthorized      An authentication parameter
        was passed, but either it was invalid or the technician is not entitled with
        a Remote Support seat    \n    403 Forbidden      Access denied. User doesn\u2019t
        have required roles    \n    404 Not Found      A machineUuid was specified,
        but the specified machine was not found in an account the user has access
        to    \n    405 Method Not Allowed      The method was entered incorrectly
        (i.e., the technician tried to use POST, PUT etc. instead of GET)    \n    500
        Internal Server Error      An unhandled error occurred"
      operationId: SessionsPost2
      x-api-path-slug: sessions-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Start
      - Screen
      - Sharing
      - Session
  /session:
    get:
      summary: Start Attended Session in Browser
      description: "This method allows a partner system to launch an attended support
        session within a browser window. This API does not require authentication,
        so the technician will be prompted to enter their credentials when they run
        the GoToAssist Expert desktop application for the first time. Since the technician
        is not required to navigate to a URL, no API is implemented to create the
        session. Note: This method was formerly named \"Create Attended Session in
        browser,\" but has been renamed.\n\n  Request Parameters                    \n
        \                     \n    field        data type      description    \n
        \   sessionType        string      The type of session to create (only \"SCREEN_SHARING\"
        can be used at this time).    \n    layout*        string      The style of
        HTML that will be displayed when starting the session (e.g., \"iFrame\").
        If this parameter is not present, then the HTML will fill the entire browser
        window.    \n    partnerObject*        string      The ID of object in the
        partner system that this session will be associated with.    \n    partnerObjectUrl*
        \       string      The URL that may be used in the GoToAssist Expert desktop
        application if the technician wants to view the partner object. Note: The
        URL can be used in a popup window or iframe that is 600 pixels wide and 500
        pixels wide. For example, a popup window could be created with HTML code as
        follows: Start Remote Support     \n    sessionStatusCallbackUrl*        string
        \     The URL that will receive a POST when the session status changes. A
        POST will also be made to the sessionStatusCallbackUrl when a customer joins
        the session and when the session ends (whether or not a customer joined).
        The contents of the POST will be similar as the GET /v1/sessions/ API. Note:
        The ID of the session is not known until the session is actually started on
        the endpoint. If the URL is not specified or the session is never started
        (e.g., if the customer cancels the installation of the GoToAssist Customer
        desktop application), then the callback will not be made.    \n                      \n*
        Optional parameters"
      operationId: SessionGet
      x-api-path-slug: session-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: sessionType
      responses:
        200:
          description: OK
      tags:
      - Start
      - Attended
      - Session
      - In
      - Browser
  /sessions/{sessionId}:
    get:
      summary: Get Screen Sharing Session Info
      description: "This method retrieves detailed information about a current or
        previous support session (either attended or unattended) based on the sessionID
        or sessionToken. \u201CsessionToken\u201D is returned in response of create
        screen-sharing session API. Information about sessions that are complete may
        only be available for a limited period of time after the end of the session
        (currently, the information is available for at least 30 days). The session
        must have been hosted from an account or company that the authenticated user
        has access to.\r\n\r\nNote: This method was formerly named \"Get Attended
        Session Info,\" but has been renamed to address the fact that it now includes
        unattended support sessions as well.\r\n\r\n  Response Parameters                    \r\n
        \                     \r\n    field        data type      description    \r\n
        \   sessionId        string      The unique ID of this session.    \r\n    sessionType
        \       string      The type of the session; this determines what other attributes
        the response may contain.    \r\n    status        string      \"The current
        state of the session; it can be: \r\nwaiting = Waiting for the customer to
        join the session.\r\nactive = Customer has joined and session is currently
        active.\r\ncomplete = Session has ended after the customer joined.\r\nabandoned
        = Session has ended without any customer joining.\r\nnotStarted = Session
        was created but never started by the expert.\"    \r\n    accountKey        number
        \     The unique GoToAssist system ID of the account the support session was
        hosted from.    \r\n    expertName        string      The human-readable name
        of the first technician in the support session.    \r\n    expertEmail        string
        \     Email id of the first expert in the session.    \r\n    expertUserKey
        \       string      Unique ID of the first expert in the session in the G2A
        system.    \r\n    partnerObject        number      The ID of the object in
        the partner system that is associated with this session.    \r\n    partnerObjectUrl
        \       string      The URL for the expert to view the associated partnerObject.
        \   \r\n    startedAt*        ISO 8061 format*      The time that the session
        started.    \r\n    customerJoinedAt*        ISO 8061 format*      The time
        that the customer joined the session.    \r\n    endedAt*        ISO 8061
        format*      The time that the session ended.    \r\n    unattendedMachineName*
        \       string      Name of the unattended machine the session is with if
        this is an unattended session.    \r\n    unattendedMachineUuid*        string
        \     ID of the unattended machine the session is with if this is an unattended
        session.    \r\n    accountName*        string      The human-readable name
        of the account the support session was hosted from (unattended sessions only)
        \   \r\n    customerName*        string      The human-readable name of the
        customer in the support session.    \r\n    customerEmail*        string      The
        email address of the customer in the support session.    \r\n    customerJoinUrl
        \       string      A URL that can be sent to a customer to join the session.
        \   \r\n    notes*        string      All notes that were entered by the technician
        in the Viewer during the support session    \r\n    sessionRecordingUrl*        string
        \     The URL where the technician can view a recording of the session within
        the GoToAssist web application (only available if the technician has opted
        to record support sessions (link is external))    \r\n    collaborators*        array
        \     A list of other users who collaborated on the support session (i.e.,
        other technicians who joined the session)    \r\n                      \r\n*
        Parameters only listed if available/applicable\r\n\r\nStatus Codes              \r\n
        \             \r\n    Staus Code      description    \r\n    200 OK      The
        information was successfully retrieved    \r\n    401 Unauthorized      An
        authentication parameter was passed, but either it was invalid or the technician
        is not entitled with a Remote Support seat    \r\n    404 Not Found      The
        sessionID is not valid for the authorized user and the session could not be
        found    \r\n    405 Method Not Allowed      The method was entered incorrectly
        (i.e., the technician tried to use POST, PUT etc. instead of GET)    \r\n
        \   500 Internal Server Error      An unhandled error occurred"
      operationId: SessionsBySessionIdGet2
      x-api-path-slug: sessionssessionid-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: sessionId
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Sharing
      - Session
      - Info
  /archive/recordings:
    get:
      summary: Available Recordings
      description: "This method retrieves a list of all available recordings on the
        account. Only recordings which are available for transcoding or downloading
        will be returned. The recording IDs are always returned in the order in which
        the recordings were started (i.e., startTime order). The request must contain
        one or more of the following: accountKey, userKey or companyId. The list of
        recordings can be filtered by the request parameters listed below.\n\nNote:
        Session recording must be enabled on the account in order to use this API
        method. To enable session recording, log in at https://app.gotoassist.com
        (link is external) and go to Configure > GoToAssist Settings > Enable Session
        Recording check box.\n\n  Request Parameters                  \n  Each request
        must contain one or more of the following: accountKey, userKey or companyId.
        \                 \n                    \n    field      data type      description
        \   \n    accountKey      number      The account key associated with the
        recording ( available in the Get Screen Sharing Session Info (link is external)
        method response )    \n    userKey      number      The user key of the technician
        who started the recorded session (available in the Authentication (link is
        external) API method response)    \n    companyId      number      The companyId
        associated with the recording for unattended support sessions only ( available
        in the Get Companies (link is external) API method response )    \n    sessionType
        *      number      The type of session: attended (0) or unattended (1)    \n
        \   fromTime *      ISO 8601 format **      The oldest sessions that should
        be retrieved (startTime must be greater than or equal to fromTime)    \n    toTime
        *      ISO 8601 format **      The most recent sessions that should be retrieved
        (startTime must be greater than or equal to fromTime)    \n    timePeriod
        *      number      The recordings within a Time Period, starting from currentDate
        (ex: \u201DtimePeriod=30\u201D would retrieve the last 30 days\u2019 recordings)
        \   \n    archived *      number      The option to include only archived
        recordings, as follows: include only archived recordings (1) or include only
        non-archived recordings (0 or omit)    \n                    \n* Optional
        \                   \n** ISO 8601 format reference                    \n                    \n
        \ Response Parameters                  \n  No more than 500 recordings at
        a time will be returned for readyForTranscode or readyForDownload.                  \n
        \                   \n    field      data type      description    \n    readyForTranscode
        \     array      A list of recordingIds for recordings that are ready to be
        transcoded    \n    readyForDownload      array      A list of recordingIds
        for recordings that are ready to be downloaded    \n                    \n
        \                   \nStatus Codes                    \n                    \n
        \   Staus Code      description          \n    200 OK      Recordings retrieved
        successfully          \n    400 Bad Request      Request may be malformed
        or property may be missing or invalid          \n    403 Forbidden      Invalid
        authorization header or invalid userKey, accountKey or companyId          \n
        \   500 Internal Server Error      Unexpected server error"
      operationId: ArchiveRecordingsGet
      x-api-path-slug: archiverecordings-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: userKey
      responses:
        200:
          description: OK
      tags:
      - Available
      - Recordings
  /archive/recordings/archived/{recordingIDs}:
    put:
      summary: Mark Recordings as Archived
      description: "This method marks a list of recordings as archived by setting
        their archived flag to \u201Ctrue.\u201D No more than 500 recordings can be
        marked as archived once.\n\nNote: Session recording must be enabled on the
        account in order to use this API method. To enable session recording, log
        in at https://app.gotoassist.com (link is external) and go to Configure >
        GoToAssist Settings > Enable Session Recording check box.\n\n  Request Parameters
        \                   \n                      \n    field        data type      description
        \   \n    recordingIds        array      A list of recordingIDs for the recordings
        to be archived    \n\n\nStatus Codes                \n                \n    Staus
        Code        description    \n    204 No Content        Recordings have been
        archived    \n    400 Bad Request        Request may be malformed or property
        may be missing or invalid    \n    403 Forbidden        Invalid authorization
        header or invalid recordingIDs    \n    500 Internal Server Error        Unexpected
        server error"
      operationId: ArchiveRecordingsArchivedByRecordingIDsPut
      x-api-path-slug: archiverecordingsarchivedrecordingids-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: recordingIDs
      responses:
        200:
          description: OK
      tags:
      - Mark
      - Recordings
      - As
      - Archived
  /archive/recordings/transcode/{readyForTranscodeRecordingIds}:
    post:
      summary: Transcode Recordings
      description: "This method requests that a list of recordings be transcoded;
        once the API passes successfully, transcoding will be initiated for each of
        the recordings in the list. A result of \u201C204\u201D will be returned,
        regardless of the current state of the recordings (i.e., even if they are
        already transcoded). No more than 500 recordings can be transcoded at once.\n\nNote:
        Session recording must be enabled on the account in order to use this API
        method. To enable session recording, log in at https://app.gotoassist.com
        (link is external) and go to Configure > GoToAssist Settings > Enable Session
        Recording check box.\n\n  Request Parameters                    \n                      \n
        \   field        data type      description    \n    recordingIds        array
        \     A list of RecordingIds for the recordings to be transcoded    \n                      \n\nStatus
        Codes                \n                \n    Staus Code        description
        \   \n    204 No Content        Transcoding initiated    \n    400 Bad Request
        \       Request may be malformed or property may be missing or invalid    \n
        \   403 Forbidden        Invalid authorization header or invalid recordingIDs
        \   \n    500 Internal Server Error        Unexpected server error"
      operationId: ArchiveRecordingsTranscodeByReadyForTranscodeRecordingIdsPost
      x-api-path-slug: archiverecordingstranscodereadyfortranscoderecordingids-post
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: readyForTranscodeRecordingIds
      responses:
        200:
          description: OK
      tags:
      - Transcode
      - Recordings
  /archive/recordings/urls[&{attribute}={readyForDownloadRecordingId}]:
    get:
      summary: Download Recordings
      description: "This method retrieves download links for a list of recordings.
        Each recording returns a link to the MP4 file, the .events file and the thumbnail.
        If a recording is not available for download then it will be omitted from
        the returned list. The archiving script may use the returned URLs to download
        each resource for the recording. The URLs will be valid for at least 48 hours.
        The URL contains a large random number so that the URL for recordings cannot
        be guessed. The response includes the recording start time to make it easier
        for the archiving script to place recordings in directories based on date.
        No more than 500 recordings can be requested at once.\n\nNote: Session recording
        must be enabled on the account in order to use this API method. To enable
        session recording, log in at https://app.gotoassist.com (link is external)
        and go to Configure > GoToAssist Settings > Enable Session Recording check
        box.\n\n  Response Parameters                  \n                    \n    field
        \     data type      description    \n    recordingId      number      The
        recordingId of the session recording to be downloaded    \n    recordingUrl
        \     string      The URL of MP4 recording file    \n    recordingStartTime
        \     ISO 8601 format*      The start time of recording    \n    eventsUrl
        \     string      The URL of the events recording file    \n    thumbnailUrl
        \     string      The URL of the thumbnail of recording file    \n    recordingSize
        \     string      The size of the .mp4 file in bytes    \n\n* ISO 8601 format
        reference\n                    \nStatus Codes                    \n                    \n
        \   Staus Code      description          \n    200 OK      A list of URLs
        has been returned          \n    400 Bad Request      Request may be malformed
        or property may be missing or invalid          \n    403 Forbidden      Invalid
        authorization header or invalid recording Ids          \n    500 Internal
        Server Error      Unexpected server error"
      operationId: ArchiveRecordingsUrlsAPIGet
      x-api-path-slug: archiverecordingsurlsattributereadyfordownloadrecordingid-get
      parameters:
      - in: header
        name: Accept
      - in: path
        name: attribute
      - in: header
        name: Content-Type
      - in: path
        name: readyForDownloadRecordingId
      responses:
        200:
          description: OK
      tags:
      - Download
      - Recordings
  /reports/organizers/{organizerKey}/trainings/{trainingKey}:
    get:
      summary: Get Sessions by Training
      description: Get sessions by training.
      operationId: ReportsOrganizersTrainingsByOrganizerKeyAndTrainingKeyGet
      x-api-path-slug: reportsorganizersorganizerkeytrainingstrainingkey-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: trainingKey
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - By
      - Training
  '/reports/organizers/{organizerKey}/sessions ':
    post:
      summary: Get Sessions by Date Range
      description: Get sessions by date range.
      operationId: ReportsOrganizersSessionsByOrganizerKeyPost
      x-api-path-slug: reportsorganizersorganizerkeysessions-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - By
      - Date
      - Range
  /{organizerKey}/webinars/{webinarKey}/performance:
    get:
      summary: Get performance for all webinar sessions
      description: Get performance for all webinar sessions.
      operationId: WebinarsPerformanceByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeyperformance-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Performance
      - Webinar
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/sessions:
    get:
      summary: Get webinar sessions
      description: Get webinar sessions.
      operationId: WebinarsSessionsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/attendees:
    get:
      summary: Get attendees for all webinar sessions
      description: Get attendees for all webinar sessions.
      operationId: WebinarsAttendeesByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeyattendees-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Attendees
      - Webinar
      - Sessions
  /{organizerKey}/sessions:
    get:
      summary: Get organizer sessions
      description: Get organizer sessions.
      operationId: SessionsByOrganizerKeyGet
      x-api-path-slug: organizerkeysessions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: fromTime
      - in: path
        name: organizerKey
      - in: query
        name: toTime
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/surveys:
    get:
      summary: Get session surveys
      description: Get session surveys.
      operationId: WebinarsSessionsSessionKeySurveysByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkeysurveys-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Session
      - Surveys
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/polls:
    get:
      summary: Get session polls
      description: Get session polls.
      operationId: WebinarsSessionsSessionKeyPollsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkeypolls-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Session
      - Polls
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/questions:
    get:
      summary: Get session questions
      description: Get session questions.
      operationId: WebinarsSessionsSessionKeyQuestionsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkeyquestions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Session
      - Questions
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees:
    get:
      summary: Get session attendees
      description: Get session attendees.
      operationId: WebinarsSessionsSessionKeyAttendeesByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkeyattendees-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Session
      - Attendees
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}:
    get:
      summary: Get webinar session
      description: Get webinar session.
      operationId: WebinarsSessionsSessionKeyByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Session
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/performance:
    get:
      summary: Get session performance
      description: Get session performance.
      operationId: WebinarsSessionsSessionKeyPerformanceByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkeyperformance-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Session
      - Performance
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