{
  "info": {
    "name": "Instructure Canvas Polls API Update a single poll session",
    "_postman_id": "58555359-ddc8-4f9f-83cb-092c558c342e",
    "description": "Update a single poll session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Polls",
      "item": [
        {
          "id": "efa8a178-1d7f-492b-bb75-965b6ee389d6",
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
              "id": "121b3005-e00f-47e9-bafa-4d08f5fb2ff4"
            }
          ]
        },
        {
          "id": "590f2f5e-2997-4bb1-8a8a-56f721a145f6",
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
              "id": "81392fd8-1c97-4740-8fed-a72b92f314ad"
            }
          ]
        },
        {
          "id": "08a2714a-724a-4cf3-b5f3-7de35820a8da",
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
              "id": "240cbfce-218d-4912-a573-3b993b41760c"
            }
          ]
        },
        {
          "id": "22625bda-3955-4b90-a596-44114db02c00",
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
              "id": "8dc9e8af-b914-4078-a220-40a99c2be95f"
            }
          ]
        },
        {
          "id": "9fa82211-df2c-43a8-8d5b-ad6a936e5475",
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
              "id": "0dbd3c48-ced6-454f-a7c0-82b8d9cfc27b"
            }
          ]
        },
        {
          "id": "baaf183d-e783-4031-8c46-a68afd166959",
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
              "id": "38c595a2-6b94-4f80-93b8-c9d29dd6a4c0"
            }
          ]
        },
        {
          "id": "dbde8f1b-7914-4453-a5c6-9e0bd1afd0d6",
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
              "id": "df96bebb-69ca-4a1d-9d86-14cda6e1b7b6"
            }
          ]
        },
        {
          "id": "24d898e6-2eaf-4e55-9783-5ce8213adb29",
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
              "id": "5e876e49-f514-471c-917d-195be86126f2"
            }
          ]
        },
        {
          "id": "2d6597c9-5dae-4d58-939d-2a83dc6d5f67",
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
              "id": "96be8314-dd65-4e7a-8b9e-8d07175050bf"
            }
          ]
        },
        {
          "id": "9831552d-a7d5-470b-8c85-5a932e24234d",
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
              "id": "143ccf1c-6b93-4e97-b954-b2cb2618d0c4"
            }
          ]
        },
        {
          "id": "30106de8-0082-46bc-a8ef-f758abd4ccfb",
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
              "id": "0d431202-020f-46b0-9574-09b787b37bcd"
            }
          ]
        },
        {
          "id": "9f07bf43-d457-4153-9c91-2d7f9857b307",
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
              "id": "867c6f22-8577-4bef-bc50-3ff142d7eec1"
            }
          ]
        },
        {
          "id": "c3641f03-1652-41c3-a6b6-c607d59ae331",
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
              "id": "f5588ac2-6eeb-48d5-a040-2049f92a35ce"
            }
          ]
        },
        {
          "id": "5c39eff8-30e2-41db-9fa7-ece760ca95ff",
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
              "id": "cbf59f74-3a8e-4415-b076-a67d949f420c"
            }
          ]
        },
        {
          "id": "4b3a7610-dd4d-4e01-9f8e-0c632ed16d44",
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
              "id": "5de9d2c2-4a9b-48d7-b2a1-44a263c9bfa1"
            }
          ]
        }
      ]
    }
  ]
}