{
  "info": {
    "name": "Instructure Canvas Polls API Open a poll session",
    "_postman_id": "8381095c-0f5b-494b-b25d-b8df0de38cf5",
    "description": "Open a poll session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Polls",
      "item": [
        {
          "id": "aa6a78ac-049b-4fc5-b3df-527fe6033eab",
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
              "id": "676caa40-ea0d-46ae-81a7-c7391917168e"
            }
          ]
        },
        {
          "id": "8a83a448-a673-4f4d-9fd2-f447a904c611",
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
              "id": "75a861a3-159b-4f66-9933-c21ed7e0d9fe"
            }
          ]
        },
        {
          "id": "54daa692-69a3-4846-aa92-2e4c839de848",
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
              "id": "def6b011-380c-4d85-9e4d-2c7e84e7ef56"
            }
          ]
        },
        {
          "id": "e29a1034-0169-4af6-a874-4ea4a05bcf76",
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
              "id": "cd4ded0d-e449-4a7b-9f85-0bd4960b567a"
            }
          ]
        },
        {
          "id": "53daf7b4-1964-4852-b272-ed659c5c6289",
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
              "id": "edd0f0a4-5a02-420b-881c-dac87f6698fb"
            }
          ]
        },
        {
          "id": "0c0b18d6-ce70-4e62-97ac-23a35eb3f90b",
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
              "id": "d1f12bc3-47ae-48fb-8762-fede6f31cd60"
            }
          ]
        },
        {
          "id": "172f2e9f-366e-44a8-8d44-00d709d38f22",
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
              "id": "34e17e73-317e-4f20-8e61-6cb997e72d8e"
            }
          ]
        },
        {
          "id": "b7f1f1d2-6378-452a-857e-ae02af9e4a63",
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
              "id": "d80a358e-435a-42c5-b30c-53e64c9fcda4"
            }
          ]
        },
        {
          "id": "d11f6707-1de7-4a1b-a41c-8a1c7ff3b75e",
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
              "id": "b511ce7d-24bc-45cd-a2b0-abbd2d22b36c"
            }
          ]
        },
        {
          "id": "59bd1355-8db8-4127-94b0-474dc8c4744d",
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
              "id": "eec49fec-2a84-4675-985e-8be579073b53"
            }
          ]
        },
        {
          "id": "570bac7f-8750-4f75-89d2-57837120de7e",
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
              "id": "dd2865fb-2d07-4405-a749-d568f2d1b346"
            }
          ]
        },
        {
          "id": "e98c87b6-e1c7-4747-89a9-5bce95fb7f73",
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
              "id": "00e07d1f-7c89-4022-add3-c5bf45a490cb"
            }
          ]
        },
        {
          "id": "29fe68ef-73d0-4f98-8c7e-ab16b24c80c4",
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
              "id": "66bec51c-1d79-4e45-b514-85b6019c7582"
            }
          ]
        },
        {
          "id": "4641edb7-efd2-4bdb-853f-0b2062bd8fed",
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
              "id": "ae8d9492-c43d-4775-9f12-9b849d5293b8"
            }
          ]
        },
        {
          "id": "b8d7cb12-db3b-4a5e-8101-f11879a67768",
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
              "id": "5c86550b-2707-453b-a696-bf464c153082"
            }
          ]
        },
        {
          "id": "5b0f7ec2-aa6c-4f59-9cb1-1710fbe266e1",
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
              "id": "44ec353d-246b-4705-a1d8-24fce64aea1b"
            }
          ]
        },
        {
          "id": "cbeca06f-9401-4925-8083-f51d1183645d",
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
              "id": "54e1ca88-7107-48fb-a84d-0b0cd3bfa3d6"
            }
          ]
        }
      ]
    }
  ]
}