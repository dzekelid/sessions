---
name: GoToMeeting
x-slug: gotomeeting
description: Citrix enables business mobility through the secure delivery of apps
  and data to any device on any network.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
x-kinRank: "7"
x-alexaRank: "7422"
tags: Sessions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/apis.md
specificationVersion: "0.14"
apis:
- name: Go To Assist Seeit Get details for multiple GoToAssist Seeit sessions
  x-api-slug: go-to-assist-seeit
  description: <p>This endpoint allows you to get all relevant details for mulitple
    GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The
    fields and their values in the response depend on session status and the time
    elapsed since session end; e.g. session data like snapshots or the session recording
    are only available for 72 hours.</p><p>The results will be paged, with paging
    customizable to match your requirements.</p>
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1//sessions
  tags: Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessions-get-openapi.md
- name: Go To Assist Seeit Create a GoToAssist Seeit session
  x-api-slug: go-to-assist-seeit
  description: This endpoint allows you to create a GoToAssist Seeit session. The
    session logically exists but is not started until you open the returned startUrl
    in a suitable browser.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1//sessions
  tags: Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessions-post-openapi.md
- name: Go To Assist Seeit Get details for a single GoToAssist Seeit session
  x-api-slug: go-to-assist-seeit
  description: <p>This endpoint allows you to get all relevant details for a single
    GoToAssist Seeit session. Session details are available for 90 days.</p><p>The
    fields and their values in the response depend on session status and the time
    elapsed since session end; e.g. session data like snapshots or the session recording
    are only available for 72 hours.</p>
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1//sessions/{uuid}
  tags: Sessions,Uuid
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessionsuuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/sessionsuuid-get-openapi.md
- name: Go To Assist Seeit
  x-api-slug: go-to-assist-seeit
  description: Citrix enables business mobility through the secure delivery of apps
    and data to any device on any network.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/openapi.md
- name: Go To Training Get Sessions by Date Range
  x-api-slug: go-to-training
  description: This call returns all session details over a given date range for a
    given organizer. A session is a completed training event.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest//reports/organizers/{organizerKey}/sessions
  tags: Reports,Organizers,OrganizerKey,Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/reportsorganizersorganizerkeysessions-post-openapi.md
- name: Go To Training Get Attendance Details
  x-api-slug: go-to-training
  description: This call retrieves a list of registrants from a specific completed
    training session. The response includes the registrants' email addresses, and
    if they attended, it includes the duration of each period of their attendance
    in minutes, and the times at which they joined and left. If a registrant does
    not attend, they appear at the bottom of the listing with timeInSession = 0.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest//reports/organizers/{organizerKey}/sessions/{sessionKey}/attendees
  tags: Reports,Organizers,OrganizerKey,Sessions,SessionKey,Attendees
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/reportsorganizersorganizerkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Training
  x-api-slug: go-to-training
  description: Citrix enables business mobility through the secure delivery of apps
    and data to any device on any network.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/openapi.md
- name: Go To Webinar Get organizer sessions
  x-api-slug: go-to-webinar
  description: Retrieve all completed sessions of all the webinars of a given organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/sessions
  tags: Organizers,OrganizerKey,Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeysessions-get-openapi.md
- name: Go To Webinar Get webinar sessions
  x-api-slug: go-to-webinar
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar Get webinar session
  x-api-slug: go-to-webinar
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar Get session attendees
  x-api-slug: go-to-webinar
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Attendees
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar Get attendee
  x-api-slug: go-to-webinar
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Attendees,RegistrantKey
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar Get attendee poll answers
  x-api-slug: go-to-webinar
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/polls
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Attendees,RegistrantKey,Polls
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar Get attendee questions
  x-api-slug: go-to-webinar
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/questions
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Attendees,RegistrantKey,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar Get attendee survey answers
  x-api-slug: go-to-webinar
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/surveys
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Attendees,RegistrantKey,Surveys
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar Get session performance
  x-api-slug: go-to-webinar
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/performance
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Performance
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar Get session polls
  x-api-slug: go-to-webinar
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/polls
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Polls
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar Get session questions
  x-api-slug: go-to-webinar
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/questions
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar Get session surveys
  x-api-slug: go-to-webinar
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest//organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/surveys
  tags: Organizers,OrganizerKey,Webinars,WebinarKey,Sessions,SessionKey,Surveys
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: Go To Webinar
  x-api-slug: go-to-webinar
  description: Citrix enables business mobility through the secure delivery of apps
    and data to any device on any network.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/gotomeeting/openapi.md
x-common:
- type: x-base
  url: https://api.citrixonline.com
- type: x-blog
  url: http://blogs.citrix.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/citrix-systems
- type: x-crunchbase
  url: http://www.crunchbase.com/company/citrix-systems
- type: x-developer
  url: https://developer.citrixonline.com/
- type: x-email
  url: secure@citrix.com
- type: x-email
  url: americasconsulting@citrix.com
- type: x-email
  url: poland@citrix.com
- type: x-email
  url: citrix_ru@citrix.com
- type: x-email
  url: Licensing-emea@eu.citrix.com
- type: x-email
  url: eduardo.fleites@citrix.com
- type: x-email
  url: CitrixReady@citrix.com
- type: x-email
  url: CSP@citrix.com
- type: x-email
  url: partneroperationsEMEA@eu.citrix.com
- type: x-github
  url: https://github.com/citrix
- type: x-twitter
  url: https://twitter.com/gotomeeting
- type: x-twitter
  url: https://twitter.com/citrix
- type: x-website
  url: https://citrixonline.com
- type: x-website
  url: http://citrixonline.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---