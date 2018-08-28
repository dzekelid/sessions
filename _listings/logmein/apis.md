---
name: LogMeIn
x-slug: logmein
description: LogMeIn, Inc. is a provider of software as a service and cloud-based
  remote connectivity services for collaboration, IT management and customer engagement,
  founded in 2003 and based in Boston, Massachusetts.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
x-kinRank: "7"
x-alexaRank: "7271"
tags: Sessions
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/apis.md
specificationVersion: "0.14"
apis:
- name: GoToAssist Remote Support - Get All Sessions
  x-api-slug: sessions-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessions-get-openapi.md
- name: GoToAssist Remote Support - Start Screen Sharing Session
  x-api-slug: sessions-post
  description: "This method creates a new screen sharing support session (either attended
    or unattended) by generating a URL that automatically launches technicians into
    a new session when clicked. If a machineUuid request parameter is specified, an
    unattended support session will be created; if it is not specified, then an attended
    session will be created. See \"Request Parameters\" for more information. Note:
    The locale of the session start dialog will be based upon the technician\u2019s
    locale setting within GoToAssist.\n\nNote: This method was formerly named \"Create
    Attended Session,\" but has been renamed to address the fact that it now includes
    unattended support sessions as well.\n\n  Request Parameters                    \n
    \                     \n    field        data type      description    \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n    sessionType        string      The type
    of session to create (only \"SCREEN_SHARING\" can be used at this time).    \n
    \   partnerObject*        string      The ID of object in the partner system that
    this session will be associated with.    \n    partnerObjectUrl*        string
    \     The URL that may be used in the GoToAssist Expert desktop application if
    the technician wants to view the partner object. Note: The URL can be used in
    a popup window or iframe that is 600 pixels wide and 500 pixels wide. For example,
    a popup window could be created with HTML code as follows: \"Start Remote Support
    \"    \n    customerName*        string      The name of the customer that the
    session is being started for.    \n    customerEmail*        string      The email
    address of the customer that the session is being started for (if available)    \n
    \   machineUuid*        string      The machineUuid is only necessary for unattended
    support sessions. If the machineUuid is present when a screen sharing session
    is started, then the endpoint will connect to the specified unattended machine
    and an unattended support session will be started. If no machineUuid is specified,
    then an attended support session will be created. A list of machineUuid parameters
    associated with the user and company will be available through a /machines API
    in future.    \n                      \n* Optional parameters\n\nStatus Codes
    \             \n              \n    Staus Code      description    \n    200 OK
    \     The response contains the URL to start the session    \n    400 Bad Request
    \     An error occurred due to missing required parameters or portal not being
    created    \n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \n    403 Forbidden      Access denied. User doesn\u2019t have required
    roles    \n    404 Not Found      A machineUuid was specified, but the specified
    machine was not found in an account the user has access to    \n    405 Method
    Not Allowed      The method was entered incorrectly (i.e., the technician tried
    to use POST, PUT etc. instead of GET)    \n    500 Internal Server Error      An
    unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessions-post-openapi.md
- name: GoToAssist Remote Support - Start Attended Session in Browser
  x-api-slug: session-get
  description: "This method allows a partner system to launch an attended support
    session within a browser window. This API does not require authentication, so
    the technician will be prompted to enter their credentials when they run the GoToAssist
    Expert desktop application for the first time. Since the technician is not required
    to navigate to a URL, no API is implemented to create the session. Note: This
    method was formerly named \"Create Attended Session in browser,\" but has been
    renamed.\n\n  Request Parameters                    \n                      \n
    \   field        data type      description    \n    sessionType        string
    \     The type of session to create (only \"SCREEN_SHARING\" can be used at this
    time).    \n    layout*        string      The style of HTML that will be displayed
    when starting the session (e.g., \"iFrame\"). If this parameter is not present,
    then the HTML will fill the entire browser window.    \n    partnerObject*        string
    \     The ID of object in the partner system that this session will be associated
    with.    \n    partnerObjectUrl*        string      The URL that may be used in
    the GoToAssist Expert desktop application if the technician wants to view the
    partner object. Note: The URL can be used in a popup window or iframe that is
    600 pixels wide and 500 pixels wide. For example, a popup window could be created
    with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n                      \n* Optional parameters"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-openapi.md
- name: GoToAssist Remote Support - Get Screen Sharing Session Info
  x-api-slug: sessionssessionid-get
  description: "This method retrieves detailed information about a current or previous
    support session (either attended or unattended) based on the sessionID or sessionToken.
    \u201CsessionToken\u201D is returned in response of create screen-sharing session
    API. Information about sessions that are complete may only be available for a
    limited period of time after the end of the session (currently, the information
    is available for at least 30 days). The session must have been hosted from an
    account or company that the authenticated user has access to.\r\n\r\nNote: This
    method was formerly named \"Get Attended Session Info,\" but has been renamed
    to address the fact that it now includes unattended support sessions as well.\r\n\r\n
    \ Response Parameters                    \r\n                      \r\n    field
    \       data type      description    \r\n    sessionId        string      The
    unique ID of this session.    \r\n    sessionType        string      The type
    of the session; this determines what other attributes the response may contain.
    \   \r\n    status        string      \"The current state of the session; it can
    be: \r\nwaiting = Waiting for the customer to join the session.\r\nactive = Customer
    has joined and session is currently active.\r\ncomplete = Session has ended after
    the customer joined.\r\nabandoned = Session has ended without any customer joining.\r\nnotStarted
    = Session was created but never started by the expert.\"    \r\n    accountKey
    \       number      The unique GoToAssist system ID of the account the support
    session was hosted from.    \r\n    expertName        string      The human-readable
    name of the first technician in the support session.    \r\n    expertEmail        string
    \     Email id of the first expert in the session.    \r\n    expertUserKey        string
    \     Unique ID of the first expert in the session in the G2A system.    \r\n
    \   partnerObject        number      The ID of the object in the partner system
    that is associated with this session.    \r\n    partnerObjectUrl        string
    \     The URL for the expert to view the associated partnerObject.    \r\n    startedAt*
    \       ISO 8061 format*      The time that the session started.    \r\n    customerJoinedAt*
    \       ISO 8061 format*      The time that the customer joined the session.    \r\n
    \   endedAt*        ISO 8061 format*      The time that the session ended.    \r\n
    \   unattendedMachineName*        string      Name of the unattended machine the
    session is with if this is an unattended session.    \r\n    unattendedMachineUuid*
    \       string      ID of the unattended machine the session is with if this is
    an unattended session.    \r\n    accountName*        string      The human-readable
    name of the account the support session was hosted from (unattended sessions only)
    \   \r\n    customerName*        string      The human-readable name of the customer
    in the support session.    \r\n    customerEmail*        string      The email
    address of the customer in the support session.    \r\n    customerJoinUrl        string
    \     A URL that can be sent to a customer to join the session.    \r\n    notes*
    \       string      All notes that were entered by the technician in the Viewer
    during the support session    \r\n    sessionRecordingUrl*        string      The
    URL where the technician can view a recording of the session within the GoToAssist
    web application (only available if the technician has opted to record support
    sessions (link is external))    \r\n    collaborators*        array      A list
    of other users who collaborated on the support session (i.e., other technicians
    who joined the session)    \r\n                      \r\n* Parameters only listed
    if available/applicable\r\n\r\nStatus Codes              \r\n              \r\n
    \   Staus Code      description    \r\n    200 OK      The information was successfully
    retrieved    \r\n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \r\n    404 Not Found      The sessionID is not valid for the authorized
    user and the session could not be found    \r\n    405 Method Not Allowed      The
    method was entered incorrectly (i.e., the technician tried to use POST, PUT etc.
    instead of GET)    \r\n    500 Internal Server Error      An unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-openapi.md
- name: GoToAssist Remote Support - Start Screen Sharing Session
  x-api-slug: sessions-post
  description: "This method creates a new screen sharing support session (either attended
    or unattended) by generating a URL that automatically launches technicians into
    a new session when clicked. If a machineUuid request parameter is specified, an
    unattended support session will be created; if it is not specified, then an attended
    session will be created. See \"Request Parameters\" for more information. Note:
    The locale of the session start dialog will be based upon the technician\u2019s
    locale setting within GoToAssist.\n\nNote: This method was formerly named \"Create
    Attended Session,\" but has been renamed to address the fact that it now includes
    unattended support sessions as well.\n\n  Request Parameters                    \n
    \                     \n    field        data type      description    \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n    sessionType        string      The type
    of session to create (only \"SCREEN_SHARING\" can be used at this time).    \n
    \   partnerObject*        string      The ID of object in the partner system that
    this session will be associated with.    \n    partnerObjectUrl*        string
    \     The URL that may be used in the GoToAssist Expert desktop application if
    the technician wants to view the partner object. Note: The URL can be used in
    a popup window or iframe that is 600 pixels wide and 500 pixels wide. For example,
    a popup window could be created with HTML code as follows: \"Start Remote Support
    \"    \n    customerName*        string      The name of the customer that the
    session is being started for.    \n    customerEmail*        string      The email
    address of the customer that the session is being started for (if available)    \n
    \   machineUuid*        string      The machineUuid is only necessary for unattended
    support sessions. If the machineUuid is present when a screen sharing session
    is started, then the endpoint will connect to the specified unattended machine
    and an unattended support session will be started. If no machineUuid is specified,
    then an attended support session will be created. A list of machineUuid parameters
    associated with the user and company will be available through a /machines API
    in future.    \n                      \n* Optional parameters\n\nStatus Codes
    \             \n              \n    Staus Code      description    \n    200 OK
    \     The response contains the URL to start the session    \n    400 Bad Request
    \     An error occurred due to missing required parameters or portal not being
    created    \n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \n    403 Forbidden      Access denied. User doesn\u2019t have required
    roles    \n    404 Not Found      A machineUuid was specified, but the specified
    machine was not found in an account the user has access to    \n    405 Method
    Not Allowed      The method was entered incorrectly (i.e., the technician tried
    to use POST, PUT etc. instead of GET)    \n    500 Internal Server Error      An
    unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessions-post-openapi.md
- name: GoToAssist Remote Support - Start Attended Session in Browser
  x-api-slug: session-get
  description: "This method allows a partner system to launch an attended support
    session within a browser window. This API does not require authentication, so
    the technician will be prompted to enter their credentials when they run the GoToAssist
    Expert desktop application for the first time. Since the technician is not required
    to navigate to a URL, no API is implemented to create the session. Note: This
    method was formerly named \"Create Attended Session in browser,\" but has been
    renamed.\n\n  Request Parameters                    \n                      \n
    \   field        data type      description    \n    sessionType        string
    \     The type of session to create (only \"SCREEN_SHARING\" can be used at this
    time).    \n    layout*        string      The style of HTML that will be displayed
    when starting the session (e.g., \"iFrame\"). If this parameter is not present,
    then the HTML will fill the entire browser window.    \n    partnerObject*        string
    \     The ID of object in the partner system that this session will be associated
    with.    \n    partnerObjectUrl*        string      The URL that may be used in
    the GoToAssist Expert desktop application if the technician wants to view the
    partner object. Note: The URL can be used in a popup window or iframe that is
    600 pixels wide and 500 pixels wide. For example, a popup window could be created
    with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n                      \n* Optional parameters"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-openapi.md
- name: GoToAssist Remote Support - Get Screen Sharing Session Info
  x-api-slug: sessionssessionid-get
  description: "This method retrieves detailed information about a current or previous
    support session (either attended or unattended) based on the sessionID or sessionToken.
    \u201CsessionToken\u201D is returned in response of create screen-sharing session
    API. Information about sessions that are complete may only be available for a
    limited period of time after the end of the session (currently, the information
    is available for at least 30 days). The session must have been hosted from an
    account or company that the authenticated user has access to.\r\n\r\nNote: This
    method was formerly named \"Get Attended Session Info,\" but has been renamed
    to address the fact that it now includes unattended support sessions as well.\r\n\r\n
    \ Response Parameters                    \r\n                      \r\n    field
    \       data type      description    \r\n    sessionId        string      The
    unique ID of this session.    \r\n    sessionType        string      The type
    of the session; this determines what other attributes the response may contain.
    \   \r\n    status        string      \"The current state of the session; it can
    be: \r\nwaiting = Waiting for the customer to join the session.\r\nactive = Customer
    has joined and session is currently active.\r\ncomplete = Session has ended after
    the customer joined.\r\nabandoned = Session has ended without any customer joining.\r\nnotStarted
    = Session was created but never started by the expert.\"    \r\n    accountKey
    \       number      The unique GoToAssist system ID of the account the support
    session was hosted from.    \r\n    expertName        string      The human-readable
    name of the first technician in the support session.    \r\n    expertEmail        string
    \     Email id of the first expert in the session.    \r\n    expertUserKey        string
    \     Unique ID of the first expert in the session in the G2A system.    \r\n
    \   partnerObject        number      The ID of the object in the partner system
    that is associated with this session.    \r\n    partnerObjectUrl        string
    \     The URL for the expert to view the associated partnerObject.    \r\n    startedAt*
    \       ISO 8061 format*      The time that the session started.    \r\n    customerJoinedAt*
    \       ISO 8061 format*      The time that the customer joined the session.    \r\n
    \   endedAt*        ISO 8061 format*      The time that the session ended.    \r\n
    \   unattendedMachineName*        string      Name of the unattended machine the
    session is with if this is an unattended session.    \r\n    unattendedMachineUuid*
    \       string      ID of the unattended machine the session is with if this is
    an unattended session.    \r\n    accountName*        string      The human-readable
    name of the account the support session was hosted from (unattended sessions only)
    \   \r\n    customerName*        string      The human-readable name of the customer
    in the support session.    \r\n    customerEmail*        string      The email
    address of the customer in the support session.    \r\n    customerJoinUrl        string
    \     A URL that can be sent to a customer to join the session.    \r\n    notes*
    \       string      All notes that were entered by the technician in the Viewer
    during the support session    \r\n    sessionRecordingUrl*        string      The
    URL where the technician can view a recording of the session within the GoToAssist
    web application (only available if the technician has opted to record support
    sessions (link is external))    \r\n    collaborators*        array      A list
    of other users who collaborated on the support session (i.e., other technicians
    who joined the session)    \r\n                      \r\n* Parameters only listed
    if available/applicable\r\n\r\nStatus Codes              \r\n              \r\n
    \   Staus Code      description    \r\n    200 OK      The information was successfully
    retrieved    \r\n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \r\n    404 Not Found      The sessionID is not valid for the authorized
    user and the session could not be found    \r\n    405 Method Not Allowed      The
    method was entered incorrectly (i.e., the technician tried to use POST, PUT etc.
    instead of GET)    \r\n    500 Internal Server Error      An unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-openapi.md
- name: GoToAssist Remote Support - Available Recordings
  x-api-slug: archiverecordings-get
  description: "This method retrieves a list of all available recordings on the account.
    Only recordings which are available for transcoding or downloading will be returned.
    The recording IDs are always returned in the order in which the recordings were
    started (i.e., startTime order). The request must contain one or more of the following:
    accountKey, userKey or companyId. The list of recordings can be filtered by the
    request parameters listed below.\n\nNote: Session recording must be enabled on
    the account in order to use this API method. To enable session recording, log
    in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist
    Settings > Enable Session Recording check box.\n\n  Request Parameters                  \n
    \ Each request must contain one or more of the following: accountKey, userKey
    or companyId.                  \n                    \n    field      data type
    \     description    \n    accountKey      number      The account key associated
    with the recording ( available in the Get Screen Sharing Session Info (link is
    external) method response )    \n    userKey      number      The user key of
    the technician who started the recorded session (available in the Authentication
    (link is external) API method response)    \n    companyId      number      The
    companyId associated with the recording for unattended support sessions only (
    available in the Get Companies (link is external) API method response )    \n
    \   sessionType *      number      The type of session: attended (0) or unattended
    (1)    \n    fromTime *      ISO 8601 format **      The oldest sessions that
    should be retrieved (startTime must be greater than or equal to fromTime)    \n
    \   toTime *      ISO 8601 format **      The most recent sessions that should
    be retrieved (startTime must be greater than or equal to fromTime)    \n    timePeriod
    *      number      The recordings within a Time Period, starting from currentDate
    (ex: \u201DtimePeriod=30\u201D would retrieve the last 30 days\u2019 recordings)
    \   \n    archived *      number      The option to include only archived recordings,
    as follows: include only archived recordings (1) or include only non-archived
    recordings (0 or omit)    \n                    \n* Optional                    \n**
    ISO 8601 format reference                    \n                    \n  Response
    Parameters                  \n  No more than 500 recordings at a time will be
    returned for readyForTranscode or readyForDownload.                  \n                    \n
    \   field      data type      description    \n    readyForTranscode      array
    \     A list of recordingIds for recordings that are ready to be transcoded    \n
    \   readyForDownload      array      A list of recordingIds for recordings that
    are ready to be downloaded    \n                    \n                    \nStatus
    Codes                    \n                    \n    Staus Code      description
    \         \n    200 OK      Recordings retrieved successfully          \n    400
    Bad Request      Request may be malformed or property may be missing or invalid
    \         \n    403 Forbidden      Invalid authorization header or invalid userKey,
    accountKey or companyId          \n    500 Internal Server Error      Unexpected
    server error"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordings-get-openapi.md
- name: GoToAssist Remote Support - Mark Recordings as Archived
  x-api-slug: archiverecordingsarchivedrecordingids-put
  description: "This method marks a list of recordings as archived by setting their
    archived flag to \u201Ctrue.\u201D No more than 500 recordings can be marked as
    archived once.\n\nNote: Session recording must be enabled on the account in order
    to use this API method. To enable session recording, log in at https://app.gotoassist.com
    (link is external) and go to Configure > GoToAssist Settings > Enable Session
    Recording check box.\n\n  Request Parameters                    \n                      \n
    \   field        data type      description    \n    recordingIds        array
    \     A list of recordingIDs for the recordings to be archived    \n\n\nStatus
    Codes                \n                \n    Staus Code        description    \n
    \   204 No Content        Recordings have been archived    \n    400 Bad Request
    \       Request may be malformed or property may be missing or invalid    \n    403
    Forbidden        Invalid authorization header or invalid recordingIDs    \n    500
    Internal Server Error        Unexpected server error"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingsarchivedrecordingids-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingsarchivedrecordingids-put-openapi.md
- name: GoToAssist Remote Support - Transcode Recordings
  x-api-slug: archiverecordingstranscodereadyfortranscoderecordingids-post
  description: "This method requests that a list of recordings be transcoded; once
    the API passes successfully, transcoding will be initiated for each of the recordings
    in the list. A result of \u201C204\u201D will be returned, regardless of the current
    state of the recordings (i.e., even if they are already transcoded). No more than
    500 recordings can be transcoded at once.\n\nNote: Session recording must be enabled
    on the account in order to use this API method. To enable session recording, log
    in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist
    Settings > Enable Session Recording check box.\n\n  Request Parameters                    \n
    \                     \n    field        data type      description    \n    recordingIds
    \       array      A list of RecordingIds for the recordings to be transcoded
    \   \n                      \n\nStatus Codes                \n                \n
    \   Staus Code        description    \n    204 No Content        Transcoding initiated
    \   \n    400 Bad Request        Request may be malformed or property may be missing
    or invalid    \n    403 Forbidden        Invalid authorization header or invalid
    recordingIDs    \n    500 Internal Server Error        Unexpected server error"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingstranscodereadyfortranscoderecordingids-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingstranscodereadyfortranscoderecordingids-post-openapi.md
- name: GoToAssist Remote Support - Download Recordings
  x-api-slug: archiverecordingsurlsattributereadyfordownloadrecordingid-get
  description: "This method retrieves download links for a list of recordings. Each
    recording returns a link to the MP4 file, the .events file and the thumbnail.
    If a recording is not available for download then it will be omitted from the
    returned list. The archiving script may use the returned URLs to download each
    resource for the recording. The URLs will be valid for at least 48 hours. The
    URL contains a large random number so that the URL for recordings cannot be guessed.
    The response includes the recording start time to make it easier for the archiving
    script to place recordings in directories based on date. No more than 500 recordings
    can be requested at once.\n\nNote: Session recording must be enabled on the account
    in order to use this API method. To enable session recording, log in at https://app.gotoassist.com
    (link is external) and go to Configure > GoToAssist Settings > Enable Session
    Recording check box.\n\n  Response Parameters                  \n                    \n
    \   field      data type      description    \n    recordingId      number      The
    recordingId of the session recording to be downloaded    \n    recordingUrl      string
    \     The URL of MP4 recording file    \n    recordingStartTime      ISO 8601
    format*      The start time of recording    \n    eventsUrl      string      The
    URL of the events recording file    \n    thumbnailUrl      string      The URL
    of the thumbnail of recording file    \n    recordingSize      string      The
    size of the .mp4 file in bytes    \n\n* ISO 8601 format reference\n                    \nStatus
    Codes                    \n                    \n    Staus Code      description
    \         \n    200 OK      A list of URLs has been returned          \n    400
    Bad Request      Request may be malformed or property may be missing or invalid
    \         \n    403 Forbidden      Invalid authorization header or invalid recording
    Ids          \n    500 Internal Server Error      Unexpected server error"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingsurlsattributereadyfordownloadrecordingid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/archiverecordingsurlsattributereadyfordownloadrecordingid-get-openapi.md
- name: GoToAssist Remote Support - Get Screen Sharing Session Info
  x-api-slug: sessionssessionid-get
  description: "This method retrieves detailed information about a current or previous
    support session (either attended or unattended) based on the sessionID or sessionToken.
    \u201CsessionToken\u201D is returned in response of create screen-sharing session
    API. Information about sessions that are complete may only be available for a
    limited period of time after the end of the session (currently, the information
    is available for at least 30 days). The session must have been hosted from an
    account or company that the authenticated user has access to.\r\n\r\nNote: This
    method was formerly named \"Get Attended Session Info,\" but has been renamed
    to address the fact that it now includes unattended support sessions as well.\r\n\r\n
    \ Response Parameters                    \r\n                      \r\n    field
    \       data type      description    \r\n    sessionId        string      The
    unique ID of this session.    \r\n    sessionType        string      The type
    of the session; this determines what other attributes the response may contain.
    \   \r\n    status        string      \"The current state of the session; it can
    be: \r\nwaiting = Waiting for the customer to join the session.\r\nactive = Customer
    has joined and session is currently active.\r\ncomplete = Session has ended after
    the customer joined.\r\nabandoned = Session has ended without any customer joining.\r\nnotStarted
    = Session was created but never started by the expert.\"    \r\n    accountKey
    \       number      The unique GoToAssist system ID of the account the support
    session was hosted from.    \r\n    expertName        string      The human-readable
    name of the first technician in the support session.    \r\n    expertEmail        string
    \     Email id of the first expert in the session.    \r\n    expertUserKey        string
    \     Unique ID of the first expert in the session in the G2A system.    \r\n
    \   partnerObject        number      The ID of the object in the partner system
    that is associated with this session.    \r\n    partnerObjectUrl        string
    \     The URL for the expert to view the associated partnerObject.    \r\n    startedAt*
    \       ISO 8061 format*      The time that the session started.    \r\n    customerJoinedAt*
    \       ISO 8061 format*      The time that the customer joined the session.    \r\n
    \   endedAt*        ISO 8061 format*      The time that the session ended.    \r\n
    \   unattendedMachineName*        string      Name of the unattended machine the
    session is with if this is an unattended session.    \r\n    unattendedMachineUuid*
    \       string      ID of the unattended machine the session is with if this is
    an unattended session.    \r\n    accountName*        string      The human-readable
    name of the account the support session was hosted from (unattended sessions only)
    \   \r\n    customerName*        string      The human-readable name of the customer
    in the support session.    \r\n    customerEmail*        string      The email
    address of the customer in the support session.    \r\n    customerJoinUrl        string
    \     A URL that can be sent to a customer to join the session.    \r\n    notes*
    \       string      All notes that were entered by the technician in the Viewer
    during the support session    \r\n    sessionRecordingUrl*        string      The
    URL where the technician can view a recording of the session within the GoToAssist
    web application (only available if the technician has opted to record support
    sessions (link is external))    \r\n    collaborators*        array      A list
    of other users who collaborated on the support session (i.e., other technicians
    who joined the session)    \r\n                      \r\n* Parameters only listed
    if available/applicable\r\n\r\nStatus Codes              \r\n              \r\n
    \   Staus Code      description    \r\n    200 OK      The information was successfully
    retrieved    \r\n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \r\n    404 Not Found      The sessionID is not valid for the authorized
    user and the session could not be found    \r\n    405 Method Not Allowed      The
    method was entered incorrectly (i.e., the technician tried to use POST, PUT etc.
    instead of GET)    \r\n    500 Internal Server Error      An unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessionssessionid-get-openapi.md
- name: GoToAssist Remote Support - Start Attended Session in Browser
  x-api-slug: session-get
  description: "This method allows a partner system to launch an attended support
    session within a browser window. This API does not require authentication, so
    the technician will be prompted to enter their credentials when they run the GoToAssist
    Expert desktop application for the first time. Since the technician is not required
    to navigate to a URL, no API is implemented to create the session. Note: This
    method was formerly named \"Create Attended Session in browser,\" but has been
    renamed.\n\n  Request Parameters                    \n                      \n
    \   field        data type      description    \n    sessionType        string
    \     The type of session to create (only \"SCREEN_SHARING\" can be used at this
    time).    \n    layout*        string      The style of HTML that will be displayed
    when starting the session (e.g., \"iFrame\"). If this parameter is not present,
    then the HTML will fill the entire browser window.    \n    partnerObject*        string
    \     The ID of object in the partner system that this session will be associated
    with.    \n    partnerObjectUrl*        string      The URL that may be used in
    the GoToAssist Expert desktop application if the technician wants to view the
    partner object. Note: The URL can be used in a popup window or iframe that is
    600 pixels wide and 500 pixels wide. For example, a popup window could be created
    with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n                      \n* Optional parameters"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-openapi.md
- name: GoToAssist Remote Support - Start Attended Session in Browser
  x-api-slug: session-get
  description: "This method allows a partner system to launch an attended support
    session within a browser window. This API does not require authentication, so
    the technician will be prompted to enter their credentials when they run the GoToAssist
    Expert desktop application for the first time. Since the technician is not required
    to navigate to a URL, no API is implemented to create the session. Note: This
    method was formerly named \"Create Attended Session in browser,\" but has been
    renamed.\n\n  Request Parameters                    \n                      \n
    \   field        data type      description    \n    sessionType        string
    \     The type of session to create (only \"SCREEN_SHARING\" can be used at this
    time).    \n    layout*        string      The style of HTML that will be displayed
    when starting the session (e.g., \"iFrame\"). If this parameter is not present,
    then the HTML will fill the entire browser window.    \n    partnerObject*        string
    \     The ID of object in the partner system that this session will be associated
    with.    \n    partnerObjectUrl*        string      The URL that may be used in
    the GoToAssist Expert desktop application if the technician wants to view the
    partner object. Note: The URL can be used in a popup window or iframe that is
    600 pixels wide and 500 pixels wide. For example, a popup window could be created
    with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n                      \n* Optional parameters"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/session-get-openapi.md
- name: GoToAssist Remote Support - Start Screen Sharing Session
  x-api-slug: sessions-post
  description: "This method creates a new screen sharing support session (either attended
    or unattended) by generating a URL that automatically launches technicians into
    a new session when clicked. If a machineUuid request parameter is specified, an
    unattended support session will be created; if it is not specified, then an attended
    session will be created. See \"Request Parameters\" for more information. Note:
    The locale of the session start dialog will be based upon the technician\u2019s
    locale setting within GoToAssist.\n\nNote: This method was formerly named \"Create
    Attended Session,\" but has been renamed to address the fact that it now includes
    unattended support sessions as well.\n\n  Request Parameters                    \n
    \                     \n    field        data type      description    \n    sessionStatusCallbackUrl*
    \       string      The URL that will receive a POST when the session status changes.
    A POST will also be made to the sessionStatusCallbackUrl when a customer joins
    the session and when the session ends (whether or not a customer joined). The
    contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID
    of the session is not known until the session is actually started on the endpoint.
    If the URL is not specified or the session is never started (e.g., if the customer
    cancels the installation of the GoToAssist Customer desktop application), then
    the callback will not be made.    \n    sessionType        string      The type
    of session to create (only \"SCREEN_SHARING\" can be used at this time).    \n
    \   partnerObject*        string      The ID of object in the partner system that
    this session will be associated with.    \n    partnerObjectUrl*        string
    \     The URL that may be used in the GoToAssist Expert desktop application if
    the technician wants to view the partner object. Note: The URL can be used in
    a popup window or iframe that is 600 pixels wide and 500 pixels wide. For example,
    a popup window could be created with HTML code as follows: \"Start Remote Support
    \"    \n    customerName*        string      The name of the customer that the
    session is being started for.    \n    customerEmail*        string      The email
    address of the customer that the session is being started for (if available)    \n
    \   machineUuid*        string      The machineUuid is only necessary for unattended
    support sessions. If the machineUuid is present when a screen sharing session
    is started, then the endpoint will connect to the specified unattended machine
    and an unattended support session will be started. If no machineUuid is specified,
    then an attended support session will be created. A list of machineUuid parameters
    associated with the user and company will be available through a /machines API
    in future.    \n                      \n* Optional parameters\n\nStatus Codes
    \             \n              \n    Staus Code      description    \n    200 OK
    \     The response contains the URL to start the session    \n    400 Bad Request
    \     An error occurred due to missing required parameters or portal not being
    created    \n    401 Unauthorized      An authentication parameter was passed,
    but either it was invalid or the technician is not entitled with a Remote Support
    seat    \n    403 Forbidden      Access denied. User doesn\u2019t have required
    roles    \n    404 Not Found      A machineUuid was specified, but the specified
    machine was not found in an account the user has access to    \n    405 Method
    Not Allowed      The method was entered incorrectly (i.e., the technician tried
    to use POST, PUT etc. instead of GET)    \n    500 Internal Server Error      An
    unhandled error occurred"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2A/rest/v1
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/sessions-post-openapi.md
- name: GoToTraining API - Get Sessions by Training
  x-api-slug: reportsorganizersorganizerkeytrainingstrainingkey-get
  description: Get sessions by training.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2T/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/reportsorganizersorganizerkeytrainingstrainingkey-get-openapi.md
- name: GoToTraining API - Get Sessions by Date Range
  x-api-slug: reportsorganizersorganizerkeysessions-post
  description: Get sessions by date range.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2T/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/reportsorganizersorganizerkeysessions-post-openapi.md
- name: GoToWebinar API - Get performance for all webinar sessions
  x-api-slug: organizerkeywebinarswebinarkeyperformance-get
  description: Get performance for all webinar sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: GoToWebinar API - Get webinar sessions
  x-api-slug: organizerkeywebinarswebinarkeysessions-get
  description: Get webinar sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessions-get-openapi.md
- name: GoToWebinar API - Get attendees for all webinar sessions
  x-api-slug: organizerkeywebinarswebinarkeyattendees-get
  description: Get attendees for all webinar sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: GoToWebinar API - Get organizer sessions
  x-api-slug: organizerkeysessions-get
  description: Get organizer sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeysessions-get-openapi.md
- name: GoToWebinar API - Get session surveys
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Get session surveys.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: GoToWebinar API - Get session polls
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Get session polls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: GoToWebinar API - Get session questions
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Get session questions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: GoToWebinar API - Get session attendees
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Get session attendees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: GoToWebinar API - Get webinar session
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
  description: Get webinar session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: GoToWebinar API - Get session performance
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get session performance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: GoToWebinar API - Get session surveys
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Get session surveys.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: GoToWebinar API - Get session polls
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Get session polls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: GoToWebinar API - Get session questions
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Get session questions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: GoToWebinar API - Get session attendees
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Get session attendees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: GoToWebinar API - Get webinar session
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
  description: Get webinar session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: GoToWebinar API - Get session performance
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get session performance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: GoToWebinar API - Get session performance
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get session performance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: GoToWebinar API - Get session performance
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get session performance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: GoToWebinar API - Get webinar session
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
  description: Get webinar session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: GoToWebinar API - Get webinar session
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
  description: Get webinar session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: GoToWebinar API - Get session attendees
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Get session attendees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: GoToWebinar API - Get session attendees
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Get session attendees.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: GoToWebinar API - Get session questions
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Get session questions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: GoToWebinar API - Get session questions
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Get session questions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: GoToWebinar API - Get session polls
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Get session polls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: GoToWebinar API - Get session polls
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Get session polls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: GoToWebinar API - Get session surveys
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Get session surveys.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: GoToWebinar API - Get session surveys
  x-api-slug: organizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Get session surveys.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/logmein/organizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
x-common:
- type: x-github
  url: https://github.com/logmein
- type: x-openapi
  url: https://www.getpostman.com/collections/94ad52bdc3d954bad52a
- type: x-postman-collection
  url: https://www.getpostman.com/collections/00bf4391e993c3afa7b7
- type: x-postman-collection
  url: https://www.getpostman.com/collections/c35d614484f21e581775
- type: x-postman-collection
  url: https://www.getpostman.com/collections/9c6e067461f45f7faa6b
- type: x-postman-collection
  url: https://drive.google.com/open?id=16WZlBkS1i8cWSfZ3mMKOwlNP-qsE7AWy
- type: x-postman-collection
  url: https://drive.google.com/file/d/1vI11FNCKpv6WJ_70hoqPNMmPAkASiOU_/view?usp=sharing
- type: x-website
  url: http://www.LogMeInInc.com
- type: x-api-gallery
  url: http://loginradius.api.gallery.streamdata.io
- type: x-api-stack
  url: http://logmein.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/logmein
- type: x-developer
  url: https://goto-developer.logmeininc.com/
- type: x-documentation
  url: https://goto-developer.logmeininc.com/apis/apis-overview
- type: x-faq
  url: https://goto-developer.logmeininc.com/faq-page
- type: x-support
  url: https://goto-developer.logmeininc.com/api-support-request-template
- type: x-twitter
  url: https://twitter.com/LogMeIn
- type: x-website
  url: https://www.logmeininc.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---