---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Get session performance
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2W/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    get:
      summary: Get details for multiple GoToAssist Seeit sessions
      description: <p>This endpoint allows you to get all relevant details for mulitple
        GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The
        fields and their values in the response depend on session status and the time
        elapsed since session end; e.g. session data like snapshots or the session
        recording are only available for 72 hours.</p><p>The results will be paged,
        with paging customizable to match your requirements.</p>
      operationId: sessions.get
      x-api-path-slug: sessions-get
      parameters:
      - in: query
        name: endTime
        description: Optional end of date range as timestamp (will be compared against
          session creation time)
      - in: query
        name: No Name
      - in: query
        name: page
        description: Optional page number
      - in: query
        name: size
        description: Optional page size
      - in: query
        name: sort
        description: Optional sort criteria, i
      - in: query
        name: startTime
        description: Optional start of date range as timestamp (will be compared against
          session creation time)
      responses:
        200:
          description: OK
      tags:
      - Sessions
    post:
      summary: Create a GoToAssist Seeit session
      description: This endpoint allows you to create a GoToAssist Seeit session.
        The session logically exists but is not started until you open the returned
        startUrl in a suitable browser.
      operationId: sessions.post
      x-api-path-slug: sessions-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/{uuid}:
    get:
      summary: Get details for a single GoToAssist Seeit session
      description: <p>This endpoint allows you to get all relevant details for a single
        GoToAssist Seeit session. Session details are available for 90 days.</p><p>The
        fields and their values in the response depend on session status and the time
        elapsed since session end; e.g. session data like snapshots or the session
        recording are only available for 72 hours.</p>
      operationId: sessions.uuid.get
      x-api-path-slug: sessionsuuid-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: uuid
        description: the uuid returned when creating the session
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Uuid
  /reports/organizers/{organizerKey}/sessions:
    post:
      summary: Get Sessions by Date Range
      description: This call returns all session details over a given date range for
        a given organizer. A session is a completed training event.
      operationId: getSessionDetailsForDateRange
      x-api-path-slug: reportsorganizersorganizerkeysessions-post
      parameters:
      - in: body
        name: body
        description: The start and end times for the time range over which to retrieve
          training sessions
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
      - Sessions
  /reports/organizers/{organizerKey}/sessions/{sessionKey}/attendees:
    get:
      summary: Get Attendance Details
      description: This call retrieves a list of registrants from a specific completed
        training session. The response includes the registrants' email addresses,
        and if they attended, it includes the duration of each period of their attendance
        in minutes, and the times at which they joined and left. If a registrant does
        not attend, they appear at the bottom of the listing with timeInSession =
        0.
      operationId: getAttendanceDetails
      x-api-path-slug: reportsorganizersorganizerkeysessionssessionkeyattendees-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: sessionKey
        description: The key of the training session
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
      - Sessions
      - SessionKey
      - Attendees
  /organizers/{organizerKey}/sessions:
    get:
      summary: Get organizer sessions
      description: Retrieve all completed sessions of all the webinars of a given
        organizer.
      operationId: getOrganizerSessions
      x-api-path-slug: organizersorganizerkeysessions-get
      parameters:
      - in: query
        name: fromTime
        description: A required start of datetime range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: toTime
        description: A required end of datetime range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Sessions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions:
    get:
      summary: Get webinar sessions
      description: Retrieves details for all past sessions of a specific webinar.
      operationId: getAllSessions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}:
    get:
      summary: Get webinar session
      description: Retrieves attendance details for a specific webinar session that
        has ended. If attendees attended the session ('registrantsAttended'), specific
        attendance details, such as attendenceTime for a registrant, will also be
        retrieved. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getWebinarSession
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees:
    get:
      summary: Get session attendees
      description: Retrieve details for all attendees of a specific webinar session.
        For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendees
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}:
    get:
      summary: Get attendee
      description: Retrieve registration details for a particular attendee of a specific
        webinar session. For technical reasons, this call cannot be executed from
        this documentation. Please use the curl command to execute it.
      operationId: getAttendee
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/polls:
    get:
      summary: Get attendee poll answers
      description: Get poll answers from a particular attendee of a specific webinar
        session. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendeePollAnswers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Polls
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/questions:
    get:
      summary: Get attendee questions
      description: Get questions asked by an attendee during a webinar session. For
        technical reasons, this call cannot be executed from this documentation. Please
        use the curl command to execute it.
      operationId: getAttendeeQuestions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Questions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/surveys:
    get:
      summary: Get attendee survey answers
      description: Retrieve survey answers from a particular attendee during a webinar
        session. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendeeSurveyAnswers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Surveys
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/performance:
    get:
      summary: Get session performance
      description: Get performance details for a session. For technical reasons, this
        call cannot be executed from this documentation. Please use the curl command
        to execute it.
      operationId: getPerformance
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Performance
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/polls:
    get:
      summary: Get session polls
      description: Retrieve all collated attendee questions and answers for polls
        from a specific webinar session. For technical reasons, this call cannot be
        executed from this documentation. Please use the curl command to execute it.
      operationId: getPolls
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Polls
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/questions:
    get:
      summary: Get session questions
      description: Retrieve questions and answers for a past webinar session. For
        technical reasons, this call cannot be executed from this documentation. Please
        use the curl command to execute it.
      operationId: getQuestions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Questions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/surveys:
    get:
      summary: Get session surveys
      description: Retrieve surveys for a past webinar session. For technical reasons,
        this call cannot be executed from this documentation. Please use the curl
        command to execute it.
      operationId: getSurveys
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Sessions
      - SessionKey
      - Surveys
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