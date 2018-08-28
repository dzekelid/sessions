{
  "info": {
    "name": "AWS AppStream 2.0 API Expire Session",
    "_postman_id": "3df1919d-2c7c-4f9b-b1de-daca3211b33c",
    "description": "This operation immediately stops a streaming session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Fleet",
      "item": [
        {
          "id": "df7d2288-3fc0-49ad-a245-a7fe0d88cedb",
          "name": "AssociateFleet",
          "request": {
            "url": "http://example.com/api/?Action=AssociateFleet?FleetName=FleetName&StackName=StackName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Associate a fleet to a stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c92a632c-7b75-4368-a9c7-7dff832640dc"
            }
          ]
        },
        {
          "id": "3da9e6c3-4c3d-459f-8afb-88f955238f84",
          "name": "CreateFleet",
          "request": {
            "url": "http://example.com/api/?Action=CreateFleet?ComputeCapacity=ComputeCapacity&Description=Description&DisconnectTimeoutInSeconds=DisconnectTimeoutInSeconds&DisplayName=DisplayName&ImageName=ImageName&InstanceType=InstanceType&MaxUserDurationInSeconds=MaxUserDurationInSeconds&Name=Name&VpcConfig=VpcConfig",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new fleet."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f67eb84d-fc46-469f-913c-224665cd5fe0"
            }
          ]
        },
        {
          "id": "261c03fe-4a82-4f0b-9e05-8c64a2c145d0",
          "name": "CreateStack",
          "request": {
            "url": "http://example.com/api/?Action=CreateStack?Description=Description&DisplayName=DisplayName&Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Create a new stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55f1d7af-74ee-476b-9f89-7c8f7e1f18fe"
            }
          ]
        },
        {
          "id": "5650c2bb-5779-4d62-beb9-2c06e21cf5b9",
          "name": "DeleteFleet",
          "request": {
            "url": "http://example.com/api/?Action=DeleteFleet?Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a fleet."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50a5a2f8-c183-40dd-8eb2-3df418b1c037"
            }
          ]
        },
        {
          "id": "6449714f-920a-4f19-8722-d75739cf1d79",
          "name": "DescribeFleets",
          "request": {
            "url": "http://example.com/api/?Action=DescribeFleets?Names=Names&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "If fleet names are provided, this operation describes the specified fleets;\n            otherwise, all the fleets in the account are described."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f328b687-5c8e-408a-8fc6-211e15558d78"
            }
          ]
        },
        {
          "id": "3ff1560b-ca86-4a22-a1bf-16e578866c1d",
          "name": "DisassociateFleet",
          "request": {
            "url": "http://example.com/api/?Action=DisassociateFleet?FleetName=FleetName&StackName=StackName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Disassociates a fleet from a stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ea97aac-c33c-4bfe-8e47-883cc2eab3e8"
            }
          ]
        }
      ]
    },
    {
      "name": "URL",
      "item": [
        {
          "id": "4320e8b3-8b83-4513-b8b3-d5528032b325",
          "name": "CreateStreamingURL",
          "request": {
            "url": "http://example.com/api/?Action=CreateStreamingURL?ApplicationId=ApplicationId&FleetName=FleetName&SessionContext=SessionContext&StackName=StackName&UserId=UserId&Validity=Validity",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a URL to start an AppStream 2."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "763e4073-8864-4dd3-804b-828b9d1cca2f"
            }
          ]
        }
      ]
    },
    {
      "name": "Stack",
      "item": [
        {
          "id": "7a6583e3-9f33-47b4-8e53-bac140b6262a",
          "name": "DeleteStack",
          "request": {
            "url": "http://example.com/api/?Action=DeleteStack?Name=Name",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the stack."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13da1e91-ce6f-44b5-82f9-61622d988918"
            }
          ]
        }
      ]
    },
    {
      "name": "Images",
      "item": [
        {
          "id": "1ea1ac03-688c-4379-9ca1-0d22a3d67963",
          "name": "DescribeImages",
          "request": {
            "url": "http://example.com/api/?Action=DescribeImages?Names=Names",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the images."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52670ac9-9a18-4e79-9b90-18a5c22fe856"
            }
          ]
        }
      ]
    },
    {
      "name": "Sessions",
      "item": [
        {
          "id": "41cee6a4-1b02-48c4-880b-3dd61f2612b2",
          "name": "DescribeSessions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeSessions?FleetName=FleetName&Limit=Limit&NextToken=NextToken&StackName=StackName&UserId=UserId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes the streaming sessions for a stack and a fleet."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "159c0d37-1a90-4a2f-b89b-8e0592a7f3b5"
            }
          ]
        }
      ]
    },
    {
      "name": "Stacks",
      "item": [
        {
          "id": "c7d14813-62dc-41a2-aea8-b3bc3adb2279",
          "name": "DescribeStacks",
          "request": {
            "url": "http://example.com/api/?Action=DescribeStacks?Names=Names&NextToken=NextToken",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "If stack names are not provided, this operation describes the specified stacks;\n            otherwise, all stacks in the account are described."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0d4024b8-3122-45b3-acd1-022e1d5a3df3"
            }
          ]
        }
      ]
    },
    {
      "name": "Session",
      "item": [
        {
          "id": "497bfb33-00b3-45c5-a451-08e6f78fd685",
          "name": "ExpireSession",
          "request": {
            "url": "http://example.com/api/?Action=ExpireSession?SessionId=SessionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This operation immediately stops a streaming session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11fed343-4ec3-4863-a180-f8a36aeef5cf"
            }
          ]
        }
      ]
    }
  ]
}