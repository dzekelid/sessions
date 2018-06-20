---
swagger: "2.0"
x-collection-name: BlazeMeter
x-complete: 1
info:
  title: Blazemeter API Explorer
  description: live-api-documentation
  version: 1.0.0
host: a.blazemeter.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/active/sessions:
    get:
      summary: Get User Active Sessions
      description: Get user active sessions.
      operationId: active_sessions
      x-api-path-slug: useractivesessions-get
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - User
      - Active
      - Sessions
---