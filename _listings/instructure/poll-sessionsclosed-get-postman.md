{
  "info": {
    "name": "Instructure Canvas Polls API List closed poll sessions",
    "_postman_id": "42dc5298-7aa9-4139-a931-b9eef733e85a",
    "description": "List closed poll sessions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Polls",
      "item": [
        {
          "id": "51f2c198-b668-445b-981e-71d1e454b197",
          "name": "list-polls",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/polls",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List polls."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b21960a0-34df-4692-a143-91ade1ee045a"
            }
          ]
        },
        {
          "id": "efefe121-15ac-4a5e-8c10-6f0a756c5cad",
          "name": "create-a-single-poll",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/polls?polls[][description]=%7B%7D&polls[][question]=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create a single poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c91e654e-696a-4719-aa3c-32b2848298ef"
            }
          ]
        },
        {
          "id": "205496fb-40b9-4386-b1bb-0bdf3dc4cb97",
          "name": "get-a-single-poll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a single poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5828ac40-dfc0-47af-91a1-c1cb2c8ecc0d"
            }
          ]
        },
        {
          "id": "ed8b7eb5-9487-4118-bed0-b2bd0b1cd543",
          "name": "update-a-single-poll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:id"
              ],
              "query": [
                {
                  "key": "polls[][description]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "polls[][question]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Update a single poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "80577b5b-dc5a-4280-8321-9c5b8e402592"
            }
          ]
        },
        {
          "id": "6395c886-ff3a-49c8-bee7-c4ee08115466",
          "name": "delete-a-poll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86520a9a-58d8-4185-871b-a6235ea5ad27"
            }
          ]
        },
        {
          "id": "f3059b87-3107-49a7-9e74-7e02d1299107",
          "name": "list-poll-choices-in-a-poll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_choices"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List poll choices in a poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b0f0e5a2-54fe-4f6a-8b29-8d9ae3ed1b5a"
            }
          ]
        },
        {
          "id": "7e6672c3-30fb-4437-acf3-c011d697709d",
          "name": "create-a-single-poll-choice",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_choices"
              ],
              "query": [
                {
                  "key": "poll_choices[][is_correct]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_choices[][position]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_choices[][text]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create a single poll choice."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "856ea299-6696-4d94-a173-122fd759ebb3"
            }
          ]
        },
        {
          "id": "a8ba80c0-8b1c-4a79-b367-3a8615a95e30",
          "name": "get-a-single-poll-choice",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_choices/id"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a single poll choice."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4369fcfd-4826-41e1-ad8f-53f3cacfd0e0"
            }
          ]
        },
        {
          "id": "7e4ae055-f1bd-456b-9757-5c428674aaad",
          "name": "update-a-single-poll-choice",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_choices/id"
              ],
              "query": [
                {
                  "key": "poll_choices[][is_correct]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_choices[][position]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_choices[][text]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Update a single poll choice."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f8be53e-28cd-4dea-9385-b008ceacc0d4"
            }
          ]
        },
        {
          "id": "ea8dc5c0-21cc-4963-b626-c9b37f994e1d",
          "name": "delete-a-poll-choice",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_choices/id"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a poll choice."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7a02064b-eb09-42b6-8e98-89b985e07035"
            }
          ]
        },
        {
          "id": "4667b31d-aef7-435f-9a34-214325c5e36d",
          "name": "list-poll-sessions-for-a-poll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List poll sessions for a poll."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "809cd45c-da31-42e2-ba3d-bb5f4d4b3819"
            }
          ]
        },
        {
          "id": "83049b74-cd17-4aad-a9bb-ae455760410e",
          "name": "create-a-single-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions"
              ],
              "query": [
                {
                  "key": "poll_sessions[][course_id]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_sessions[][course_section_id]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_sessions[][has_public_results]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create a single poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ace5dd4d-0ad6-4c5b-a866-25ecc7537d6b"
            }
          ]
        },
        {
          "id": "c048b4da-edfe-447b-a3c3-4b3a5218d7e4",
          "name": "get-the-results-for-a-single-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/id"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the results for a single poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2c037891-e785-4b67-843e-5419d83ea345"
            }
          ]
        },
        {
          "id": "6d0d9bf0-3bd7-42c1-a90b-d769f08b7250",
          "name": "update-a-single-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/id"
              ],
              "query": [
                {
                  "key": "poll_sessions[][course_id]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_sessions[][course_section_id]",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "poll_sessions[][has_public_results]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Update a single poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc878e44-13e8-4532-b795-b76b36258a3d"
            }
          ]
        },
        {
          "id": "d309b0f4-b9f0-42b2-9d61-5fa5f5312d04",
          "name": "delete-a-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/id"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8182bbe1-36a2-4922-b5d7-6c0a15379d6b"
            }
          ]
        },
        {
          "id": "8b673210-9f88-405e-9475-29433f473cee",
          "name": "close-an-opened-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/id/close"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Close an opened poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "67ab2493-776c-4eed-9813-cd32c07fbee6"
            }
          ]
        },
        {
          "id": "96baf960-51cb-423c-a897-4ceaabfe63ba",
          "name": "open-a-poll-session",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/id/open"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Open a poll session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "99c0d728-3f35-4d9c-a090-135c935e05f7"
            }
          ]
        },
        {
          "id": "2c7be86e-2dd5-4145-a633-95ac7221f43a",
          "name": "create-a-single-poll-submission",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/poll_session_id/poll_submissions"
              ],
              "query": [
                {
                  "key": "poll_submissions[][poll_choice_id]",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create a single poll submission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59991d74-4f63-4e76-8e80-8287943f8106"
            }
          ]
        },
        {
          "id": "e4e60d40-216c-4daa-b31d-ebf72c74b052",
          "name": "get-a-single-poll-submission",
          "request": {
            "url": {
              "protocol": "http",
              "host": "canvas.instructure.com",
              "path": [
                "api",
                "v1",
                "polls/:poll_id/poll_sessions/poll_session_id/poll_submissions/:id"
              ],
              "variable": [
                {
                  "id": "poll_id",
                  "value": "poll_id",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a single poll submission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "375b7f04-6d37-4c30-98b0-67b26d8e0159"
            }
          ]
        }
      ]
    },
    {
      "name": "Poll",
      "item": [
        {
          "id": "af59fe20-f5c2-42c8-a061-d9209224a3cf",
          "name": "list-closed-poll-sessions",
          "request": {
            "url": "http://canvas.instructure.com/api/v1/poll_sessions/closed",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List closed poll sessions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0b97ff6-6479-4f92-8566-92211f857340"
            }
          ]
        }
      ]
    }
  ]
}