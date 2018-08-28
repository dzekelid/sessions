{
  "info": {
    "name": "Respoke REST API App Auth Sessions",
    "_postman_id": "12076e65-13ee-40c6-81af-1600c5f28337",
    "description": "Your users authenticate to Respoke using an App-Token obtained when they POST your tokenId to [base]/appauthsessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Admin",
      "item": [
        {
          "id": "d94fbba8-1986-4ea7-be77-36e70cd1ea04",
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
              "id": "5a54d228-54c8-457f-bb2a-3899b8cd7fae"
            }
          ]
        }
      ]
    },
    {
      "name": "Adminsessions",
      "item": [
        {
          "id": "9853d39e-b7ac-4025-b204-5d7c8d303a36",
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
              "id": "8e1ee215-8266-4977-8c83-620f9bfb4b77"
            }
          ]
        }
      ]
    },
    {
      "name": "Appauthsessions",
      "item": [
        {
          "id": "7b3ac9cc-a1e8-4f56-a29a-42a1d72d649b",
          "name": "postAppauthsessions",
          "request": {
            "url": "http://api.respoke.io/v1/appauthsessions/?App-Token=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Your users authenticate to Respoke using an App-Token obtained when they POST your tokenId to [base]/appauthsessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad47b49c-dc00-4e07-a291-39806f0b1252"
            }
          ]
        }
      ]
    }
  ]
}