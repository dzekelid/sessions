---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Polls API Create a single poll submission
  description: Create a single poll submission.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/external_tools/sessionless_launch:
    get:
      summary: Get a sessionless launch url for an external tool.
      description: Get a sessionless launch url for an external tool..
      operationId: get-a-sessionless-launch-url-for-an-external-tool
      x-api-path-slug: coursescourse-idexternal-toolssessionless-launch-get
      parameters:
      - in: query
        name: assignment_id
        description: The assignment id for an assignment launch
      - in: query
        name: id
        description: The external id of the tool to launch
      - in: query
        name: launch_type
        description: The type of launch to perform on the external tool
      - in: query
        name: url
        description: The LTI launch url for the external tool
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - External
      - Tools
      - Sessionless
      - Launch
  /polls/{poll_id}/poll_sessions:
    get:
      summary: List poll sessions for a poll
      description: List poll sessions for a poll.
      operationId: list-poll-sessions-for-a-poll
      x-api-path-slug: pollspoll-idpoll-sessions-get
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
    post:
      summary: Create a single poll session
      description: Create a single poll session.
      operationId: create-a-single-poll-session
      x-api-path-slug: pollspoll-idpoll-sessions-post
      parameters:
      - in: query
        name: poll_sessions[][course_id]
        description: The id of the course this session is associated with
      - in: query
        name: poll_sessions[][course_section_id]
        description: The id of the course section this session is associated with
      - in: query
        name: poll_sessions[][has_public_results]
        description: Whether or not results are viewable by students
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
  /polls/{poll_id}/poll_sessions/id:
    delete:
      summary: Delete a poll session
      description: Delete a poll session.
      operationId: delete-a-poll-session
      x-api-path-slug: pollspoll-idpoll-sessionsid-delete
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Id
    get:
      summary: Get the results for a single poll session
      description: Get the results for a single poll session.
      operationId: get-the-results-for-a-single-poll-session
      x-api-path-slug: pollspoll-idpoll-sessionsid-get
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Id
    put:
      summary: Update a single poll session
      description: Update a single poll session.
      operationId: update-a-single-poll-session
      x-api-path-slug: pollspoll-idpoll-sessionsid-put
      parameters:
      - in: query
        name: poll_sessions[][course_id]
        description: The id of the course this session is associated with
      - in: query
        name: poll_sessions[][course_section_id]
        description: The id of the course section this session is associated with
      - in: query
        name: poll_sessions[][has_public_results]
        description: Whether or not results are viewable by students
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Id
  /polls/{poll_id}/poll_sessions/id/close:
    get:
      summary: Close an opened poll session
      description: Close an opened poll session.
      operationId: close-an-opened-poll-session
      x-api-path-slug: pollspoll-idpoll-sessionsidclose-get
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Id
      - Close
  /polls/{poll_id}/poll_sessions/id/open:
    get:
      summary: Open a poll session
      description: Open a poll session.
      operationId: open-a-poll-session
      x-api-path-slug: pollspoll-idpoll-sessionsidopen-get
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Id
      - Open
  /polls/{poll_id}/poll_sessions/poll_session_id/poll_submissions:
    post:
      summary: Create a single poll submission
      description: Create a single poll submission.
      operationId: create-a-single-poll-submission
      x-api-path-slug: pollspoll-idpoll-sessionspoll-session-idpoll-submissions-post
      parameters:
      - in: query
        name: poll_submissions[][poll_choice_id]
        description: The chosen poll choice for this submission
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Poll
      - Session
      - Id
      - Poll
      - Submissions
  /polls/{poll_id}/poll_sessions/poll_session_id/poll_submissions/{id}:
    get:
      summary: Get a single poll submission
      description: Get a single poll submission.
      operationId: get-a-single-poll-submission
      x-api-path-slug: pollspoll-idpoll-sessionspoll-session-idpoll-submissionsid-get
      responses:
        200:
          description: OK
      tags:
      - Polls
      - Poll
      - Id
      - Poll
      - Sessions
      - Poll
      - Session
      - Id
      - Poll
      - Submissions
      - Id
  /poll_sessions/closed:
    get:
      summary: List closed poll sessions
      description: List closed poll sessions.
      operationId: list-closed-poll-sessions
      x-api-path-slug: poll-sessionsclosed-get
      responses:
        200:
          description: OK
      tags:
      - Poll
      - Sessions
      - Closed
  /poll_sessions/opened:
    get:
      summary: List opened poll sessions
      description: List opened poll sessions.
      operationId: list-opened-poll-sessions
      x-api-path-slug: poll-sessionsopened-get
      responses:
        200:
          description: OK
      tags:
      - Poll
      - Sessions
      - Opened
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