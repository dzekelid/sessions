---
name: Google Cloud Spanner
x-slug: google-cloud-spanner
description: 'Cloud Spanner is the first and only relational database service that
  is both strongly consistent and horizontally scalable. With Cloud Spanner you enjoy
  all the traditional benefits of a relational database: ACID transactions, relational
  schemas (and schema changes without downtime), SQL queries, high performance, and
  high availability. But unlike any other relational database service, Cloud Spanner
  scales horizontally, to hundreds or thousands of servers, so it can handle the highest
  of transactional workloads. With automatic scaling, synchronous data replication,
  and node redundancy, Cloud Spanner delivers up to 99.999% (five 9s) of availability
  for your mission critical applications. In fact, Google&rsquo;s internal Spanner
  service has been handling millions of queries per second from many Google services
  for years.'
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Sessions
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/apis.md
specificationVersion: "0.14"
apis:
- name: Cloud Spanner - Create Session
  x-api-slug: v1databasesessions-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1databasesessions-post-openapi.md
- name: Cloud Spanner - End Session
  x-api-slug: v1name-delete
  description: Ends a session, releasing server resources associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-delete-openapi.md
- name: Cloud Spanner - Get Session
  x-api-slug: v1name-get
  description: |-
    Gets a session. Returns `NOT_FOUND` if the session does not exist.
    This is mainly useful for determining whether a session is still
    alive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-get-openapi.md
- name: Cloud Spanner - Create Session
  x-api-slug: v1databasesessions-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1databasesessions-post-openapi.md
- name: Cloud Spanner - End Session
  x-api-slug: v1name-delete
  description: Ends a session, releasing server resources associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-delete-openapi.md
- name: Cloud Spanner - Get Session
  x-api-slug: v1name-get
  description: |-
    Gets a session. Returns `NOT_FOUND` if the session does not exist.
    This is mainly useful for determining whether a session is still
    alive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-get-openapi.md
- name: Cloud Spanner - Get Session
  x-api-slug: v1name-get
  description: |-
    Gets a session. Returns `NOT_FOUND` if the session does not exist.
    This is mainly useful for determining whether a session is still
    alive.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-get-openapi.md
- name: Cloud Spanner - End Session
  x-api-slug: v1name-delete
  description: Ends a session, releasing server resources associated with it.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1name-delete-openapi.md
- name: Cloud Spanner - Create Session
  x-api-slug: v1databasesessions-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-spanner-global-scale-consistency_2x.png
  humanURL: https://cloud.google.com/spanner/
  baseURL: ://spanner.googleapis.com//
  tags: Google APIs, Stack Network, API Service Provider, API Provider, Databases,
    Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/google-cloud-spanner/v1databasesessions-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.cloud.source.repositories.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.cloud.spanner.stack.network
- type: x-change-log
  url: https://cloud.google.com/spanner/docs/release-notes
- type: x-code
  url: https://cloud.google.com/spanner/docs/reference/libraries
- type: x-command-line-interfaces
  url: https://cloud.google.com/spanner/docs/gcloud-spanner
- type: x-concepts
  url: https://cloud.google.com/spanner/docs/concepts
- type: x-documentation
  url: https://cloud.google.com/spanner/docs/
- type: x-getting-started
  url: https://cloud.google.com/spanner/docs/quickstart-console
- type: x-guide
  url: https://cloud.google.com/spanner/docs/how-to
- type: x-pricing
  url: https://cloud.google.com/spanner/pricing
- type: x-rate-limits
  url: https://cloud.google.com/spanner/docs/limits
- type: x-schema
  url: https://cloud.google.com/spanner/docs/information-schema
- type: x-service-level-agreements
  url: https://cloud.google.com/spanner/sla
- type: x-support
  url: https://cloud.google.com/spanner/docs/support
- type: x-website
  url: https://cloud.google.com/spanner/
- type: x-white-papers
  url: https://cloud.google.com/spanner/docs/whitepapers
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---