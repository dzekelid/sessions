{
  "info": {
    "name": "GoToAssist Remote Support Start Attended Session in Browser",
    "_postman_id": "4ef9ad82-e4e6-45f2-996e-4a06e7df1809",
    "description": "This method allows a partner system to launch an attended support session within a browser window. This API does not require authentication, so the technician will be prompted to enter their credentials when they run the GoToAssist Expert desktop application for the first time. Since the technician is not required to navigate to a URL, no API is implemented to create the session. Note: This method was formerly named \"Create Attended Session in browser,\" but has been renamed.\n\n  Request Parameters                    \n                      \n    field        data type      description    \n    sessionType        string      The type of session to create (only \"SCREEN_SHARING\" can be used at this time).    \n    layout*        string      The style of HTML that will be displayed when starting the session (e.g., \"iFrame\"). If this parameter is not present, then the HTML will fill the entire browser window.    \n    partnerObject*        string      The ID of object in the partner system that this session will be associated with.    \n    partnerObjectUrl*        string      The URL that may be used in the GoToAssist Expert desktop application if the technician wants to view the partner object. Note: The URL can be used in a popup window or iframe that is 600 pixels wide and 500 pixels wide. For example, a popup window could be created with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*        string      The URL that will receive a POST when the session status changes. A POST will also be made to the sessionStatusCallbackUrl when a customer joins the session and when the session ends (whether or not a customer joined). The contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID of the session is not known until the session is actually started on the endpoint. If the URL is not specified or the session is never started (e.g., if the customer cancels the installation of the GoToAssist Customer desktop application), then the callback will not be made.    \n                      \n* Optional parameters",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Start",
      "item": [
        {
          "id": "535264b3-a9b0-473b-96eb-1ccb5e69ed87",
          "name": "SessionGet",
          "request": {
            "url": "http://api.getgo.com/G2A/rest/v1/session?sessionType=%7B%7D",
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
            "description": "This method allows a partner system to launch an attended support session within a browser window. This API does not require authentication, so the technician will be prompted to enter their credentials when they run the GoToAssist Expert desktop application for the first time. Since the technician is not required to navigate to a URL, no API is implemented to create the session. Note: This method was formerly named \"Create Attended Session in browser,\" but has been renamed.\n\n  Request Parameters                    \n                      \n    field        data type      description    \n    sessionType        string      The type of session to create (only \"SCREEN_SHARING\" can be used at this time).    \n    layout*        string      The style of HTML that will be displayed when starting the session (e.g., \"iFrame\"). If this parameter is not present, then the HTML will fill the entire browser window.    \n    partnerObject*        string      The ID of object in the partner system that this session will be associated with.    \n    partnerObjectUrl*        string      The URL that may be used in the GoToAssist Expert desktop application if the technician wants to view the partner object. Note: The URL can be used in a popup window or iframe that is 600 pixels wide and 500 pixels wide. For example, a popup window could be created with HTML code as follows: Start Remote Support     \n    sessionStatusCallbackUrl*        string      The URL that will receive a POST when the session status changes. A POST will also be made to the sessionStatusCallbackUrl when a customer joins the session and when the session ends (whether or not a customer joined). The contents of the POST will be similar as the GET /v1/sessions/ API. Note: The ID of the session is not known until the session is actually started on the endpoint. If the URL is not specified or the session is never started (e.g., if the customer cancels the installation of the GoToAssist Customer desktop application), then the callback will not be made.    \n                      \n* Optional parameters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "27d1e00a-d346-41eb-836c-5a7653b0240f"
            }
          ]
        }
      ]
    }
  ]
}