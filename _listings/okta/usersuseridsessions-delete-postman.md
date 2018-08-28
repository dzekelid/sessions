{
  "info": {
    "name": "Okta Clear User Sessions",
    "_postman_id": "f0bf18a1-ff0f-4ed8-8ee8-77a969d4ebae",
    "description": "Clear user sessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Clear",
      "item": [
        {
          "id": "259cd7cb-f00c-4180-a6af-1ed8d28fd979",
          "name": "deleteUsersUserSessions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v1",
                "users/:userId/sessions"
              ],
              "variable": [
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
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
            "description": "Clear user sessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58b21fc3-192f-4a2b-835b-d6560c1fb8b2"
            }
          ]
        }
      ]
    }
  ]
}