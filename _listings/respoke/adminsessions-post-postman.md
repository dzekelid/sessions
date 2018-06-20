{
  "info": {
    "name": "Respoke REST API Permissions",
    "_postman_id": "e9aa280b-4880-4946-a799-b4511c69654a",
    "description": "Full API permissions are obtained by POSTing your username and password to [base]/adminsessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Admin",
      "item": [
        {
          "id": "c17d2447-086c-4b43-92dd-fe4b19d4c623",
          "name": "postAdminSessions",
          "request": {
            "url": "http://api.respoke.io/v1/admin-sessions/?password=%7B%7D&username=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Log in with the account username and password. Get an Admin-Token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e4d5dac5-fa0c-438a-84e0-3f46af2d1bb5"
            }
          ]
        }
      ]
    },
    {
      "name": "Adminsessions",
      "item": [
        {
          "id": "47c0c5ab-1b62-4b63-9996-83b779e91529",
          "name": "postAdminsessions",
          "request": {
            "url": "http://api.respoke.io/v1/adminsessions/?password=%7B%7D&username=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Full API permissions are obtained by POSTing your username and password to [base]/adminsessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7442e2e-d3ae-4921-99e7-452d064b8e5c"
            }
          ]
        }
      ]
    }
  ]
}