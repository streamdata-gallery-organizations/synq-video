{
  "info": {
    "name": "SYNQ Video Perform a JavaScript query to return video objects matching any desired criteria.",
    "_postman_id": "1f939c11-32c7-4c49-aee5-808847f31ee2",
    "description": "Find videos matching any criteria, by running a JavaScript function over each video object. A detailed tutorial on how to use this functionality is available on the [documentation page](https://www.synq.fm/queries-video-api/).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Video",
      "item": [
        {
          "id": "ccc01eb8-8dd8-4169-8edb-d75629b4f017",
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
              "id": "8b22caa7-dc31-44a9-a2f9-9de8750fff10"
            }
          ]
        },
        {
          "id": "8e7b35d5-cd61-41d8-8b2d-977f16783e1f",
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
              "id": "6cf509f6-55e1-480a-99f3-763ada6d9d43"
            }
          ]
        },
        {
          "id": "deac039e-4f0f-47f8-9d28-57199cf78271",
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
              "id": "fde6a737-24aa-4a89-a514-e109b96ddb06"
            }
          ]
        }
      ]
    }
  ]
}