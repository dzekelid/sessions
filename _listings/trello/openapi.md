swagger: "2.0"
x-collection-name: Trello
x-complete: 1
info:
  title: Trello
  description: this-document-describes-the-rest-api-of-trello-as-published-by-trello-com---a-hrefhttpstrello-comdocsindex-html-target-blankofficial-documentationa--a-hrefhttpstrello-comdocsapi-target-blankthe-html-pages-that-were-scraped-in-order-to-generate-this-specification-a
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
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
      operationId: addSessions
      x-api-path-slug: sessions-post
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/socket:
    get:
      summary: Get Sessions Socket
      description: Get sessions socket.
      operationId: getSessionsSocket
      x-api-path-slug: sessionssocket-get
      parameters:
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Socket
  /sessions/{idSession}:
    put:
      summary: Put Sessions
      description: Put sessions.
      operationId: updateSessionsByIdSession
      x-api-path-slug: sessionsidsession-put
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idSession
        description: idSession
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
  /sessions/{idSession}/status:
    put:
      summary: Put Sessions Status
      description: Put sessions status.
      operationId: updateSessionsStatusByIdSession
      x-api-path-slug: sessionsidsessionstatus-put
      parameters:
      - in: body
        name: body
        description: Attributes of Sessions Status to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idSession
        description: idSession
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Status