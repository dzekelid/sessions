---
swagger: "2.0"
info:
  title: AWS Device Farm API Install To Remote Access Session
  version: 1.0.0
  description: Installs an application to the device in a remote access session.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=InstallToRemoteAccessSession:
    get:
      summary: ' Install To Remote Access Session '
      description: Installs an application to the device in a remote access session
      operationId: installToRemoteAccessSession
      parameters:
      - in: query
        name: appArn
        description: The Amazon Resource Name (ARN) of the app about which you are
          requesting information
        type: string
      - in: query
        name: remoteAccessSessionArn
        description: The Amazon Resource Name (ARN) of the remote access session about
          which you are requesting information
        type: string
      responses:
        200:
          description: OK
      tags:
      - remote access sessions
definitions: []
x-collection-name: AWS Device Farm
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