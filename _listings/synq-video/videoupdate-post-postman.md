{
  "info": {
    "name": "SYNQ Video Update a video's metadata.",
    "_postman_id": "527bcc95-f084-4bd1-992d-572ef09caa8f",
    "description": "Update a video's metadata through JavaScript code. Only fields inside the \"userdata\" object can be set.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Video",
      "item": [
        {
          "id": "270e8750-9d28-42e2-9318-4564cd697cf3",
          "name": "create",
          "request": {
            "url": "http://api.synq.fm/v1/video/create",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "api_key",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "userdata",
                  "value": "{}",
                  "disabled": false,
                  "description": "Additional metadata that will be associated with the video"
                }
              ]
            },
            "description": "Create a new video, optionally setting some metadata fields. You may optionally set some of the metadata associated with the video. Only fields inside the \"userdata\" field can be set."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d5f377fc-4ee5-4068-9fe8-13329da07e23"
            }
          ]
        },
        {
          "id": "d9163c06-9561-4cd1-aa47-ce3962475792",
          "name": "details",
          "request": {
            "url": "http://api.synq.fm/v1/video/details",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "api_key",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "video_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "ID of the video to retrieve the metadata from"
                }
              ]
            },
            "description": "Return details about a video. You may optionally request that only some of the metadata fields are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0d714b6-a84d-4ee3-bc09-1710136ac7e4"
            }
          ]
        },
        {
          "id": "4cb76b51-51c7-4d45-becb-0e99f42e659e",
          "name": "query",
          "request": {
            "url": "http://api.synq.fm/v1/video/query",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "api_key",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "filter",
                  "value": "{}",
                  "disabled": false,
                  "description": "JavaScript code to be run over each video object, to determine what should be returend"
                }
              ]
            },
            "description": "Find videos matching any criteria, by running a JavaScript function over each video object. A detailed tutorial on how to use this functionality is available on the [documentation page](https://www.synq.fm/queries-video-api/)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d7bdd7e-ed62-4f6f-a808-a0393104e3a3"
            }
          ]
        },
        {
          "id": "0e9846d2-4b4b-4a6f-867c-1b57b4cab2ce",
          "name": "stream",
          "request": {
            "url": "http://api.synq.fm/v1/video/stream",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "api_key",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "video_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "The ID of the video you want to stream to"
                }
              ]
            },
            "description": "Returns a stream url that you can stream to from your broadcasting software, and a playback url people can use to watch the stream."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc9db2f2-5a38-4b29-8829-e85550ea0be1"
            }
          ]
        },
        {
          "id": "5ea4af7a-cf22-4dff-95b3-e321cbae5101",
          "name": "update",
          "request": {
            "url": "http://api.synq.fm/v1/video/update",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "api_key",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "source",
                  "value": "{}",
                  "disabled": false,
                  "description": "JavaScript code to execute on the video object"
                },
                {
                  "key": "video_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "The ID of the video whose metadata will be updated"
                }
              ]
            },
            "description": "Update a video's metadata through JavaScript code. Only fields inside the \"userdata\" object can be set."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9e4ee79-fa4e-4dea-98d8-95f2aecf8c8f"
            }
          ]
        }
      ]
    }
  ]
}