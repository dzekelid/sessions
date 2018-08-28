swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
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