swagger: "2.0"
x-collection-name: Azure Logic Apps
x-complete: 1
info:
  title: LogicManagementClient
  description: rest-api-for-azure-logic-apps-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Logic/integrationAccounts/{integrationAccountName}/sessions/{sessionName}
  : get:
      summary: Sessions Get
      description: Gets an integration account session.
      operationId: Sessions_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-logicintegrationaccountsintegrationaccountnamesessionssessionname-get
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: path
        name: sessionName
        description: The integration account session name
      responses:
        200:
          description: OK
      tags:
      - Sessions
    put:
      summary: Sessions Create Or Update
      description: Creates or updates an integration account session.
      operationId: Sessions_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-logicintegrationaccountsintegrationaccountnamesessionssessionname-put
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: body
        name: session
        description: The integration account session
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: sessionName
        description: The integration account session name
      responses:
        200:
          description: OK
      tags:
      - Sessions
    delete:
      summary: Sessions Delete
      description: Deletes an integration account session.
      operationId: Sessions_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-logicintegrationaccountsintegrationaccountnamesessionssessionname-delete
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: path
        name: sessionName
        description: The integration account session name
      responses:
        200:
          description: OK
      tags:
      - Sessions