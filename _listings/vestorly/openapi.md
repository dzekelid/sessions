swagger: "2.0"
x-collection-name: Vestorly
x-complete: 1
info:
  title: Vestorly
  description: vestorly-developers-api
  termsOfService: http://www.vestorly.com/terms/
  contact:
    name: Vestorly Team
  version: 1.0.0
host: staging.vestorly.com
basePath: /api/v2
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
      description: Login To Vestorly Platform
      operationId: login
      x-api-path-slug: sessions-post
      parameters:
      - in: query
        name: password
        description: Password in Vestorly Platform
      - in: query
        name: username
        description: Username in the vestorly platform
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/{id}:
    delete:
      summary: Delete Sessions
      description: Logout of the vestorly platform
      operationId: logout
      x-api-path-slug: sessionsid-delete
      parameters:
      - in: path
        name: id
        description: ID of pet to session
      - in: query
        name: vestorly-auth
        description: Authenication token
      - in: query
        name: vestorly_auth
        description: Authenication token
      responses:
        200:
          description: OK
      tags:
      - Sessions