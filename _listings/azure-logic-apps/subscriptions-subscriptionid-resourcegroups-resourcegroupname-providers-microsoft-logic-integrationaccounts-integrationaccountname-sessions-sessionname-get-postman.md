{
  "info": {
    "name": "Azure Logic Apps API Sessions Get",
    "_postman_id": "716bfbb0-a7af-4afb-9a14-b0806db8d7af",
    "description": "Gets an integration account session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "sessions",
      "item": [
        {
          "id": "149d134c-4742-43bb-bb9b-e27cb977bcf2",
          "name": "Sessions_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Logic/integrationAccounts/:integrationAccountName/sessions/:sessionName"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "integrationAccountName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sessionName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets an integration account session"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89a33b17-ffa4-48a1-b1b7-3a07bd36d68b"
            }
          ]
        }
      ]
    }
  ]
}