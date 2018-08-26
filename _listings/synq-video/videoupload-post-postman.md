{
  "info": {
    "name": "SYNQ Video Return parameters needed for uploading a video file.",
    "_postman_id": "6904a002-3526-4516-a1eb-3b5938a69eaf",
    "description": "Return parameters needed for uploading a video file to Amazon Simple Storage Service. See http://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-post-example.html as well as the language-specific code-examples.\n#### *Example request*\n```shell\ncurl -s https://api.synq.fm/v1/video/upload \\\n  -F api_key=${SYNQ_API_KEY} \\\n  -F video_id=2d81c30ce62f4dfdb501dbca96c7ae56\n```\n\n#### *Example response*\n```json\n{\n  \"action\": \"https://synqfm.s3.amazonaws.com/\",\n  \"AWSAccessKeyId\": \"AKIAIP77Y7MMX3ITZMFA\",\n  \"Content-Type\": \"video/mp4\",\n  \"Policy\": \"eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19\",\n  \"Signature\": \"ysqDemlKXKr6hKzVFP0hCGgf/cs=\",\n  \"acl\": \"public-read\",\n  \"key\": \"projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4\"\n}\n```\n\nTo upload the file, you can then make a multipart POST request to the URL in `action`, and for all the other parameters returned, set them as form parameters.\n\nGiven the parameters above, you would upload a file `test.mp4` using cURL like this:\n\n```shell\ncurl -s https://synqfm.s3.amazonaws.com/ \\\n  -F AWSAccessKeyId=\"AKIAIP77Y7MMX3ITZMFA\" \\\n  -F Content-Type=\"video/mp4\" \\\n  -F Policy=\"eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19\" \\\n  -F Signature=\"ysqDemlKXKr6hKzVFP0hCGgf/cs=\" \\\n  -F acl=\"public-read\" \\\n  -F key=\"projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4\" \\\n  -F file=\"@my_video_file.mp4\"\n```",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Video",
      "item": [
        {
          "id": "7c6c6a31-dbea-40e5-ab45-5340973e35bc",
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
              "id": "b3cc316b-3119-45cb-9bae-872b5078b8d4"
            }
          ]
        },
        {
          "id": "1ca71973-2d76-4e5d-b32c-3a98b4bc6908",
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
              "id": "f6ec3cc1-1fcf-4d20-ac7c-a514afda4e0b"
            }
          ]
        },
        {
          "id": "0d4ec87e-1ff1-49f5-961d-98b3097bb649",
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
              "id": "0645177d-6af9-4efc-8d3d-11afe9c612cd"
            }
          ]
        },
        {
          "id": "481abb00-08fd-469a-9de5-dd83e5f2d493",
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
              "id": "39200f14-0661-4d09-9207-954d837d6479"
            }
          ]
        },
        {
          "id": "69a155c9-007f-4388-ac6a-e1cddabff5ca",
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
              "id": "82bf8df7-2572-4fca-9d8a-43367b6d643f"
            }
          ]
        },
        {
          "id": "f17ec7bf-8563-4437-a5b7-746a32c75e97",
          "name": "upload",
          "request": {
            "url": "http://api.synq.fm/v1/video/upload",
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
                  "description": "The ID of the video you are going to upload into"
                }
              ]
            },
            "description": "Return parameters needed for uploading a video file to Amazon Simple Storage Service. See http://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-post-example.html as well as the language-specific code-examples.\n#### *Example request*\n```shell\ncurl -s https://api.synq.fm/v1/video/upload \\\n  -F api_key=${SYNQ_API_KEY} \\\n  -F video_id=2d81c30ce62f4dfdb501dbca96c7ae56\n```\n\n#### *Example response*\n```json\n{\n  \"action\": \"https://synqfm.s3.amazonaws.com/\",\n  \"AWSAccessKeyId\": \"AKIAIP77Y7MMX3ITZMFA\",\n  \"Content-Type\": \"video/mp4\",\n  \"Policy\": \"eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19\",\n  \"Signature\": \"ysqDemlKXKr6hKzVFP0hCGgf/cs=\",\n  \"acl\": \"public-read\",\n  \"key\": \"projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4\"\n}\n```\n\nTo upload the file, you can then make a multipart POST request to the URL in `action`, and for all the other parameters returned, set them as form parameters.\n\nGiven the parameters above, you would upload a file `test.mp4` using cURL like this:\n\n```shell\ncurl -s https://synqfm.s3.amazonaws.com/ \\\n  -F AWSAccessKeyId=\"AKIAIP77Y7MMX3ITZMFA\" \\\n  -F Content-Type=\"video/mp4\" \\\n  -F Policy=\"eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19\" \\\n  -F Signature=\"ysqDemlKXKr6hKzVFP0hCGgf/cs=\" \\\n  -F acl=\"public-read\" \\\n  -F key=\"projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4\" \\\n  -F file=\"@my_video_file.mp4\"\n```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e7c5b0a5-d62b-4ec9-b2e4-415947888957"
            }
          ]
        }
      ]
    }
  ]
}