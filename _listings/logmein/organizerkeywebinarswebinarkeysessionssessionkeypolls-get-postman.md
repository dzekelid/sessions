{
  "info": {
    "name": "GoToWebinar Get session polls",
    "_postman_id": "693c0cdb-7b3e-4e22-acbc-67b87f37b1cf",
    "description": "Get session polls.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Session",
      "item": [
        {
          "id": "13918dc3-6f38-4342-a006-a6c44fef5f61",
          "name": "WebinarsSessionsSessionKeyPollsByOrganizerKeyAndWebinarKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/webinars/:webinarKey/sessions/:sessionKey/polls"
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
            "description": "Get session polls."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ee5d5e8-fbf8-45f8-b816-7da124ea211e"
            }
          ]
        }
      ]
    }
  ]
}