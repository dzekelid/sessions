{
  "info": {
    "name": "Azure Logic Apps API Sessions List By Integration Accounts",
    "_postman_id": "bd1d9164-f919-44b6-8388-246da53bfa40",
    "description": "Gets a list of integration account sessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "sessions integration accounts",
      "item": [
        {
          "id": "2c1647ae-01d5-4ad4-b33c-ddfd3c324473",
          "name": "Sessions_ListByIntegrationAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Logic/integrationAccounts/:integrationAccountName/sessions"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$top",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
            "description": "Gets a list of integration account sessions"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2ff8308-aaea-4a6c-9f97-2627a913f16e"
            }
          ]
        }
      ]
    }
  ]
}