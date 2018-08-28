swagger: "2.0"
x-collection-name: Tropo
x-complete: 1
info:
  title: Tropo
  description: tropo-is-a-cloud-communications-api-and-platform-for-building-scalable-voice-and-sms-applications-
  version: v1
host: api.tropo.com
basePath: /v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    post:
      summary: Post Sessions
      description: Post sessions.
      operationId: postSessions
      x-api-path-slug: sessions-post
      parameters:
      - in: query
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Sessions