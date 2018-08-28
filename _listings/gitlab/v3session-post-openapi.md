---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Post Session
  version: 1.0.0
  description: Login to get token
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/session:
    post:
      summary: Post Session
      description: Login to get token
      operationId: postV3Session
      x-api-path-slug: v3session-post
      parameters:
      - in: formData
        name: email
        description: The email of the user
      - in: formData
        name: login
        description: The username
      - in: formData
        name: password
        description: The password of the user
      responses:
        200:
          description: OK
      tags:
      - Session
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