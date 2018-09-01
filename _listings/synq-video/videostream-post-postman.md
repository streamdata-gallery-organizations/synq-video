{
  "info": {
    "name": "SYNQ Video Returns urls for streaming.",
    "_postman_id": "b38a5ad6-862e-4777-af3c-7e5f6ff39c48",
    "description": "Returns a stream url that you can stream to from your broadcasting software, and a playback url people can use to watch the stream.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Video",
      "item": [
        {
          "id": "cbf5e98c-5477-4560-a8e5-63a9883e9f0d",
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
              "id": "15a490f6-d483-49b4-aba9-9463e6d7f5fd"
            }
          ]
        },
        {
          "id": "aca417e3-a4c3-4d7e-bf00-3c9f98671639",
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
              "id": "2fda1857-bb3e-4d5b-a25d-ac1516b8c8ff"
            }
          ]
        },
        {
          "id": "c9cc787a-57bc-40bb-8ea8-9cdaee90fcef",
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
              "id": "563eb502-0ea5-4d3d-a50e-cca4550ed86e"
            }
          ]
        },
        {
          "id": "1a1c261c-cba6-45f1-9bf8-84c6ce1f6660",
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
              "id": "484b2378-74f3-4ce0-b42f-4461b7754ddd"
            }
          ]
        }
      ]
    }
  ]
}