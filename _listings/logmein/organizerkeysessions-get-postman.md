{
  "info": {
    "name": "GoToWebinar Get organizer sessions",
    "_postman_id": "fcc83c6d-983a-4af5-8a96-ccb546358a8f",
    "description": "Get organizer sessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizer",
      "item": [
        {
          "id": "787dd5be-eecc-4494-9232-8eb29b14dc2e",
          "name": "SessionsByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/sessions"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "toTime",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "organizerKey",
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
            "description": "Get organizer sessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6982d925-f107-49db-8a41-c732b0502f7a"
            }
          ]
        }
      ]
    }
  ]
}