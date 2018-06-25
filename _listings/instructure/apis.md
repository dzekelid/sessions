---
name: Instructure
x-slug: instructure
description: Instructure makes software that makes smarter people. Products include
  Canvas LMS, Bridge and Canvas Network.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
x-kinRank: "8"
x-alexaRank: "367"
tags: Sessions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/apis.md
specificationVersion: "0.14"
apis:
- name: Instructure Canvas Polls API List poll sessions for a poll
  x-api-slug: instructure-canvas-polls-api
  description: List poll sessions for a poll.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions
  tags: Polls,Poll,Id,Poll,Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessions-get-openapi.md
- name: Instructure Canvas Polls API Create a single poll session
  x-api-slug: instructure-canvas-polls-api
  description: Create a single poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions
  tags: Polls,Poll,Id,Poll,Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessions-post-openapi.md
- name: Instructure Canvas Polls API Delete a poll session
  x-api-slug: instructure-canvas-polls-api
  description: Delete a poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/id
  tags: Polls,Poll,Id,Poll,Sessions,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-delete-openapi.md
- name: Instructure Canvas Polls API Get the results for a single poll session
  x-api-slug: instructure-canvas-polls-api
  description: Get the results for a single poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/id
  tags: Polls,Poll,Id,Poll,Sessions,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-get-openapi.md
- name: Instructure Canvas Polls API Update a single poll session
  x-api-slug: instructure-canvas-polls-api
  description: Update a single poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/id
  tags: Polls,Poll,Id,Poll,Sessions,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsid-put-openapi.md
- name: Instructure Canvas Polls API Close an opened poll session
  x-api-slug: instructure-canvas-polls-api
  description: Close an opened poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/id/close
  tags: Polls,Poll,Id,Poll,Sessions,Id,Close
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsidclose-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsidclose-get-openapi.md
- name: Instructure Canvas Polls API Open a poll session
  x-api-slug: instructure-canvas-polls-api
  description: Open a poll session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/id/open
  tags: Polls,Poll,Id,Poll,Sessions,Id,Open
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsidopen-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionsidopen-get-openapi.md
- name: Instructure Canvas Polls API Create a single poll submission
  x-api-slug: instructure-canvas-polls-api
  description: Create a single poll submission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/poll_session_id/poll_submissions
  tags: Polls,Poll,Id,Poll,Sessions,Poll,Session,Id,Poll,Submissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionspoll-session-idpoll-submissions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionspoll-session-idpoll-submissions-post-openapi.md
- name: Instructure Canvas Polls API Get a single poll submission
  x-api-slug: instructure-canvas-polls-api
  description: Get a single poll submission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//polls/{poll_id}/poll_sessions/poll_session_id/poll_submissions/{id}
  tags: Polls,Poll,Id,Poll,Sessions,Poll,Session,Id,Poll,Submissions,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionspoll-session-idpoll-submissionsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/pollspoll-idpoll-sessionspoll-session-idpoll-submissionsid-get-openapi.md
- name: Instructure Canvas Polls API List closed poll sessions
  x-api-slug: instructure-canvas-polls-api
  description: List closed poll sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//poll_sessions/closed
  tags: Poll,Sessions,Closed
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/poll-sessionsclosed-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/poll-sessionsclosed-get-openapi.md
- name: Instructure Canvas Polls API List opened poll sessions
  x-api-slug: instructure-canvas-polls-api
  description: List opened poll sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//poll_sessions/opened
  tags: Poll,Sessions,Opened
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/poll-sessionsopened-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/poll-sessionsopened-get-openapi.md
- name: Instructure Canvas Polls API
  x-api-slug: instructure-canvas-polls-api
  description: Instructure makes software that makes smarter people. Products include
    Canvas LMS, Bridge and Canvas Network.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/instructure/openapi.md
x-common:
- type: x-blog
  url: http://blog.instructure.com
- type: x-blog-rss
  url: http://voice.instructure.com/CMS/UI/Modules/BizBlogger/rss.aspx?tabid=772438&moduleid=1638884&maxcount=25&t=415c2e5d197a4d6f7cdcc81385b677f1
- type: x-crunchbase
  url: https://crunchbase.com/organization/instructure
- type: x-crunchbase
  url: http://www.crunchbase.com/company/instructure
- type: x-email
  url: info@instructure.com
- type: x-email
  url: jobs@instructure.com
- type: x-email
  url: privacy@instructure.com
- type: x-email
  url: legal@instructure.com
- type: x-github
  url: https://github.com/instructure
- type: x-twitter
  url: https://twitter.com/instructure
- type: x-website
  url: http://instructure.com
- type: x-website
  url: https://canvas.instructure.com/doc/api/index.html
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---