{
  "info": {
    "name": "Instructure Canvas Polls API Close an opened poll session",
    "_postman_id": "18ccd2e7-7d6a-4654-b301-60c5f217f90e",
    "description": "Close an opened poll session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Polls",
      "item": [
        {
          "id": "7a6ed275-dd19-4585-a766-6fc4c422458b",
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
              "id": "c381a899-72e9-40a4-a70f-f42e60bf2008"
            }
          ]
        },
        {
          "id": "93465f91-88c6-4d84-bea4-bfd09832e905",
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
              "id": "c82fd553-7c01-4892-85cd-7b9264c7602c"
            }
          ]
        },
        {
          "id": "4afb256b-5124-4346-b739-449869dad79c",
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
              "id": "2808598d-4eb4-43d1-adb4-a338bd5e903f"
            }
          ]
        },
        {
          "id": "970c5e85-dbd4-4b2c-85ae-1160d3789b89",
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
              "id": "f817e0a9-c516-4987-ac41-deef945b5a30"
            }
          ]
        },
        {
          "id": "226ef49b-70df-4674-9fc1-471110949722",
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
              "id": "59ecbebf-5d9f-4604-9376-6c5c15b98cbf"
            }
          ]
        },
        {
          "id": "008bb603-8dd2-450a-b716-af7fb116b94f",
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
              "id": "c6794ff7-1755-4ca0-a3ef-e76ca2b16dcd"
            }
          ]
        },
        {
          "id": "32b75bf6-eea5-47ea-9691-c83d2493a58d",
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
              "id": "427d2f06-e70f-4d1c-ada2-fd9dfab988c4"
            }
          ]
        },
        {
          "id": "beb33b66-a87d-480e-9fdd-7842f26c6c84",
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
              "id": "9bfb89e6-47f6-432b-951f-834093c1b4c7"
            }
          ]
        },
        {
          "id": "aa29e208-7563-4fd6-9b43-0bb38130c670",
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
              "id": "17914934-6500-4181-9a1b-938dec558e28"
            }
          ]
        },
        {
          "id": "5f4d08f2-1302-41fb-9596-746fd2659abb",
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
              "id": "5fa30039-8a75-4dee-b3a3-bb8f34501815"
            }
          ]
        },
        {
          "id": "ef2a35b2-785a-4cb0-b8d4-8885fa1231ff",
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
              "id": "b32168c9-1863-44ea-8e25-aad8a5c0cbf7"
            }
          ]
        },
        {
          "id": "24c99989-147e-4e8b-b4b6-765a7da68105",
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
              "id": "c29eedd4-f796-4719-be02-cc5eb23519ba"
            }
          ]
        },
        {
          "id": "89299f60-6ccd-4d2c-8374-42cec049c42e",
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
              "id": "6e4323dd-dbe4-444c-9864-c12f208a760b"
            }
          ]
        },
        {
          "id": "211a93de-b6eb-48c1-bb1e-5e2d2a388ae8",
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
              "id": "4318dc83-5497-4141-8a7c-b89278654e33"
            }
          ]
        },
        {
          "id": "ebd4e3ea-6826-4d93-88fe-e289bf98ce24",
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
              "id": "cae4a701-0fac-4004-9644-fcfd4e2471ba"
            }
          ]
        },
        {
          "id": "442b353a-81e6-4c0d-ba4f-a46a7e749578",
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
              "id": "db716521-6ca3-4fbe-916d-d960404588e5"
            }
          ]
        }
      ]
    }
  ]
}