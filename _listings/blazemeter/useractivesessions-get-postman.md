{
  "info": {
    "name": "Blazemeter Get User Active Sessions",
    "_postman_id": "36566c59-8053-4440-b750-fa2a34276848",
    "description": "Get user active sessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Monitoring",
      "item": [
        {
          "id": "33085be3-41f0-4117-9b5c-0d4af61ab568",
          "name": "active_sessions",
          "request": {
            "url": "http://a.blazemeter.com/api/v4/user/active/sessions",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get user active sessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fadcfecf-8af9-4e9d-b248-6ddd298c99ee"
            }
          ]
        }
      ]
    }
  ]
}