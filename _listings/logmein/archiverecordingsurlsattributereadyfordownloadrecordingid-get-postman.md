{
  "info": {
    "name": "GoToAssist Remote Support Download Recordings",
    "_postman_id": "7397185b-7878-4132-923f-a941b3233f62",
    "description": "This method retrieves download links for a list of recordings. Each recording returns a link to the MP4 file, the .events file and the thumbnail. If a recording is not available for download then it will be omitted from the returned list. The archiving script may use the returned URLs to download each resource for the recording. The URLs will be valid for at least 48 hours. The URL contains a large random number so that the URL for recordings cannot be guessed. The response includes the recording start time to make it easier for the archiving script to place recordings in directories based on date. No more than 500 recordings can be requested at once.\n\nNote: Session recording must be enabled on the account in order to use this API method. To enable session recording, log in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist Settings > Enable Session Recording check box.\n\n  Response Parameters                  \n                    \n    field      data type      description    \n    recordingId      number      The recordingId of the session recording to be downloaded    \n    recordingUrl      string      The URL of MP4 recording file    \n    recordingStartTime      ISO 8601 format*      The start time of recording    \n    eventsUrl      string      The URL of the events recording file    \n    thumbnailUrl      string      The URL of the thumbnail of recording file    \n    recordingSize      string      The size of the .mp4 file in bytes    \n\n* ISO 8601 format reference\n                    \nStatus Codes                    \n                    \n    Staus Code      description          \n    200 OK      A list of URLs has been returned          \n    400 Bad Request      Request may be malformed or property may be missing or invalid          \n    403 Forbidden      Invalid authorization header or invalid recording Ids          \n    500 Internal Server Error      Unexpected server error",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Available",
      "item": [
        {
          "id": "d2b996ba-30df-40d7-997d-e0d7512104ed",
          "name": "ArchiveRecordingsGet",
          "request": {
            "url": "http://api.getgo.com/G2A/rest/v1/archive/recordings?userKey=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "This method retrieves a list of all available recordings on the account. Only recordings which are available for transcoding or downloading will be returned. The recording IDs are always returned in the order in which the recordings were started (i.e., startTime order). The request must contain one or more of the following: accountKey, userKey or companyId. The list of recordings can be filtered by the request parameters listed below.\n\nNote: Session recording must be enabled on the account in order to use this API method. To enable session recording, log in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist Settings > Enable Session Recording check box.\n\n  Request Parameters                  \n  Each request must contain one or more of the following: accountKey, userKey or companyId.                  \n                    \n    field      data type      description    \n    accountKey      number      The account key associated with the recording ( available in the Get Screen Sharing Session Info (link is external) method response )    \n    userKey      number      The user key of the technician who started the recorded session (available in the Authentication (link is external) API method response)    \n    companyId      number      The companyId associated with the recording for unattended support sessions only ( available in the Get Companies (link is external) API method response )    \n    sessionType *      number      The type of session: attended (0) or unattended (1)    \n    fromTime *      ISO 8601 format **      The oldest sessions that should be retrieved (startTime must be greater than or equal to fromTime)    \n    toTime *      ISO 8601 format **      The most recent sessions that should be retrieved (startTime must be greater than or equal to fromTime)    \n    timePeriod *      number      The recordings within a Time Period, starting from currentDate (ex: ”timePeriod=30” would retrieve the last 30 days’ recordings)    \n    archived *      number      The option to include only archived recordings, as follows: include only archived recordings (1) or include only non-archived recordings (0 or omit)    \n                    \n* Optional                    \n** ISO 8601 format reference                    \n                    \n  Response Parameters                  \n  No more than 500 recordings at a time will be returned for readyForTranscode or readyForDownload.                  \n                    \n    field      data type      description    \n    readyForTranscode      array      A list of recordingIds for recordings that are ready to be transcoded    \n    readyForDownload      array      A list of recordingIds for recordings that are ready to be downloaded    \n                    \n                    \nStatus Codes                    \n                    \n    Staus Code      description          \n    200 OK      Recordings retrieved successfully          \n    400 Bad Request      Request may be malformed or property may be missing or invalid          \n    403 Forbidden      Invalid authorization header or invalid userKey, accountKey or companyId          \n    500 Internal Server Error      Unexpected server error"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0fc4d70-0608-444f-a7d8-87522d4b9dbc"
            }
          ]
        }
      ]
    },
    {
      "name": "Mark",
      "item": [
        {
          "id": "389c67e6-c01e-47ff-8798-2176443a6cb6",
          "name": "ArchiveRecordingsArchivedByRecordingIDsPut",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2A",
                "rest",
                "v1",
                "archive/recordings/archived/:recordingIDs"
              ],
              "variable": [
                {
                  "id": "recordingIDs",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
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
            "description": "This method marks a list of recordings as archived by setting their archived flag to “true.” No more than 500 recordings can be marked as archived once.\n\nNote: Session recording must be enabled on the account in order to use this API method. To enable session recording, log in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist Settings > Enable Session Recording check box.\n\n  Request Parameters                    \n                      \n    field        data type      description    \n    recordingIds        array      A list of recordingIDs for the recordings to be archived    \n\n\nStatus Codes                \n                \n    Staus Code        description    \n    204 No Content        Recordings have been archived    \n    400 Bad Request        Request may be malformed or property may be missing or invalid    \n    403 Forbidden        Invalid authorization header or invalid recordingIDs    \n    500 Internal Server Error        Unexpected server error"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d51bb413-312d-4807-ad76-68411f34cb64"
            }
          ]
        }
      ]
    },
    {
      "name": "Transcode",
      "item": [
        {
          "id": "872c814f-70ca-4f9a-badb-8d5ad0889b54",
          "name": "ArchiveRecordingsTranscodeByReadyForTranscodeRecordingIdsPost",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2A",
                "rest",
                "v1",
                "archive/recordings/transcode/:readyForTranscodeRecordingIds"
              ],
              "variable": [
                {
                  "id": "readyForTranscodeRecordingIds",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "This method requests that a list of recordings be transcoded; once the API passes successfully, transcoding will be initiated for each of the recordings in the list. A result of “204” will be returned, regardless of the current state of the recordings (i.e., even if they are already transcoded). No more than 500 recordings can be transcoded at once.\n\nNote: Session recording must be enabled on the account in order to use this API method. To enable session recording, log in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist Settings > Enable Session Recording check box.\n\n  Request Parameters                    \n                      \n    field        data type      description    \n    recordingIds        array      A list of RecordingIds for the recordings to be transcoded    \n                      \n\nStatus Codes                \n                \n    Staus Code        description    \n    204 No Content        Transcoding initiated    \n    400 Bad Request        Request may be malformed or property may be missing or invalid    \n    403 Forbidden        Invalid authorization header or invalid recordingIDs    \n    500 Internal Server Error        Unexpected server error"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "af526b72-2916-4da3-98a5-04ca68407a80"
            }
          ]
        }
      ]
    },
    {
      "name": "Download",
      "item": [
        {
          "id": "54566ae3-f7b7-4ef4-9f8c-feade74bf627",
          "name": "ArchiveRecordingsUrlsAPIGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2A",
                "rest",
                "v1",
                "archive/recordings/urls[&:attribute=:readyForDownloadRecordingId]"
              ],
              "variable": [
                {
                  "id": "attribute",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "readyForDownloadRecordingId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "This method retrieves download links for a list of recordings. Each recording returns a link to the MP4 file, the .events file and the thumbnail. If a recording is not available for download then it will be omitted from the returned list. The archiving script may use the returned URLs to download each resource for the recording. The URLs will be valid for at least 48 hours. The URL contains a large random number so that the URL for recordings cannot be guessed. The response includes the recording start time to make it easier for the archiving script to place recordings in directories based on date. No more than 500 recordings can be requested at once.\n\nNote: Session recording must be enabled on the account in order to use this API method. To enable session recording, log in at https://app.gotoassist.com (link is external) and go to Configure > GoToAssist Settings > Enable Session Recording check box.\n\n  Response Parameters                  \n                    \n    field      data type      description    \n    recordingId      number      The recordingId of the session recording to be downloaded    \n    recordingUrl      string      The URL of MP4 recording file    \n    recordingStartTime      ISO 8601 format*      The start time of recording    \n    eventsUrl      string      The URL of the events recording file    \n    thumbnailUrl      string      The URL of the thumbnail of recording file    \n    recordingSize      string      The size of the .mp4 file in bytes    \n\n* ISO 8601 format reference\n                    \nStatus Codes                    \n                    \n    Staus Code      description          \n    200 OK      A list of URLs has been returned          \n    400 Bad Request      Request may be malformed or property may be missing or invalid          \n    403 Forbidden      Invalid authorization header or invalid recording Ids          \n    500 Internal Server Error      Unexpected server error"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "216f72bd-4793-4f87-a290-916c16befd80"
            }
          ]
        }
      ]
    }
  ]
}