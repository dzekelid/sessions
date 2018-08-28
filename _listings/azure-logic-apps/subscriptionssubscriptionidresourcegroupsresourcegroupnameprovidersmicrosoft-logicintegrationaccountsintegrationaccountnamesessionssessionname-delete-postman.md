{
  "info": {
    "name": "Azure Logic Apps API Sessions Delete",
    "_postman_id": "60363694-397a-4c44-9329-fe781d3301d3",
    "description": "Deletes an integration account session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "sessions",
      "item": [
        {
          "id": "2b288d22-46e8-471c-a055-0e058f6f13c4",
          "name": "Sessions_Delete",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an integration account session"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8467ac0e-381d-4c69-82d1-cb15cb802ff4"
            }
          ]
        }
      ]
    }
  ]
}