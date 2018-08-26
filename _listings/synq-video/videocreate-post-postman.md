{
  "info": {
    "name": "SYNQ Video Create a new video, optionally setting some metadata fields.",
    "_postman_id": "f8c50fac-47af-4227-b7c4-41ab929196ae",
    "description": "Create a new video, optionally setting some metadata fields. You may optionally set some of the metadata associated with the video. Only fields inside the \"userdata\" field can be set.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Video",
      "item": [
        {
          "id": "37192098-b3d6-492a-bf2d-cb6d36494cb5",
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
              "id": "0a81ff95-43f2-40b1-9869-1524f4277063"
            }
          ]
        }
      ]
    }
  ]
}