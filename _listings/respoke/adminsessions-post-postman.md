{
  "info": {
    "name": "Respoke REST API Admin Sessions",
    "_postman_id": "ce620be2-9780-4af2-968e-e499ae0d6799",
    "description": "Log in with the account username and password. Get an Admin-Token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Admin",
      "item": [
        {
          "id": "4af28069-e2df-4692-8440-cf2a02c03b2f",
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
              "id": "097455f8-adaa-48c0-a79c-aea0707a7e8c"
            }
          ]
        }
      ]
    }
  ]
}