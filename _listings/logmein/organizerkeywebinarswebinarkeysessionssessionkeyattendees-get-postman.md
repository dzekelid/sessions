{
  "info": {
    "name": "GoToWebinar Get session attendees",
    "_postman_id": "081c360e-bc15-4507-9cb9-a8ab7030368d",
    "description": "Get session attendees.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Session",
      "item": [
        {
          "id": "2ed81bef-afe8-4f83-93d4-1ec0d102ff6f",
          "name": "WebinarsSessionsSessionKeyAttendeesByOrganizerKeyAndWebinarKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/webinars/:webinarKey/sessions/:sessionKey/attendees"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sessionKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "webinarKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get session attendees."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dca5279c-df7c-4a27-ad5e-b334f2c395f6"
            }
          ]
        }
      ]
    }
  ]
}