---
name: SYNQ Video
x-slug: synq-video
description: White glove ingest service for VOD and Cable operators. Say goodbye to
  infinite mail threads on metadata outputs, file transfer solutions and debugging.
  We take care of video ingestion with our central repository for VOD content. Assets
  are easily accessible for distributors through our API with the outputs you expect.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
x-kinRank: "7"
x-alexaRank: "0"
tags: SYNQ Video
created: "2018-08-31"
modified: "2018-08-31"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/apis.md
specificationVersion: "0.14"
apis:
- name: SYNQ Video - Create a new video, optionally setting some metadata fields.
  x-api-slug: videocreate-post
  description: Create a new video, optionally setting some metadata fields. You may
    optionally set some of the metadata associated with the video. Only fields inside
    the "userdata" field can be set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videocreate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videocreate-post-openapi.md
- name: SYNQ Video - Return details about a video.
  x-api-slug: videodetails-post
  description: Return details about a video. You may optionally request that only
    some of the metadata fields are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videodetails-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videodetails-post-openapi.md
- name: SYNQ Video - Perform a JavaScript query to return video objects matching any
    desired criteria.
  x-api-slug: videoquery-post
  description: Find videos matching any criteria, by running a JavaScript function
    over each video object. A detailed tutorial on how to use this functionality is
    available on the [documentation page](https://www.synq.fm/queries-video-api/).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoquery-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoquery-post-openapi.md
- name: SYNQ Video - Returns urls for streaming.
  x-api-slug: videostream-post
  description: Returns a stream url that you can stream to from your broadcasting
    software, and a playback url people can use to watch the stream.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videostream-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videostream-post-openapi.md
- name: SYNQ Video - Update a video's metadata.
  x-api-slug: videoupdate-post
  description: Update a video's metadata through JavaScript code. Only fields inside
    the "userdata" object can be set.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoupdate-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoupdate-post-openapi.md
- name: SYNQ Video - Return parameters needed for uploading a video file.
  x-api-slug: videoupload-post
  description: |-
    Return parameters needed for uploading a video file to Amazon Simple Storage Service. See http://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-post-example.html as well as the language-specific code-examples.
    #### *Example request*
    ```shell
    curl -s https://api.synq.fm/v1/video/upload \
      -F api_key=${SYNQ_API_KEY} \
      -F video_id=2d81c30ce62f4dfdb501dbca96c7ae56
    ```

    #### *Example response*
    ```json
    {
      "action": "https://synqfm.s3.amazonaws.com/",
      "AWSAccessKeyId": "AKIAIP77Y7MMX3ITZMFA",
      "Content-Type": "video/mp4",
      "Policy": "eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19",
      "Signature": "ysqDemlKXKr6hKzVFP0hCGgf/cs=",
      "acl": "public-read",
      "key": "projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4"
    }
    ```

    To upload the file, you can then make a multipart POST request to the URL in `action`, and for all the other parameters returned, set them as form parameters.

    Given the parameters above, you would upload a file `test.mp4` using cURL like this:

    ```shell
    curl -s https://synqfm.s3.amazonaws.com/ \
      -F AWSAccessKeyId="AKIAIP77Y7MMX3ITZMFA" \
      -F Content-Type="video/mp4" \
      -F Policy="eyJleHBpcmF0aW9uIiA6ICIyMDE2LTA0LTIyVDE5OjAyOjI2LjE3MloiLCAiY29uZGl0aW9ucyIgOiBbeyJidWNrZXQiIDogInN5bnFmbSJ9LCB7ImFjbCIgOiAicHVibGljLXJlYWQifSwgWyJzdGFydHMtd2l0aCIsICIka2V5IiwgInByb2plY3RzLzZlLzYzLzZlNjNiNzUyYTE4NTRkZGU4ODViNWNjNDcyZWRmNTY5L3VwbG9hZHMvdmlkZW9zLzJkLzgxLzJkODFjMzBjZTYyZjRkZmRiNTAxZGJjYTk2YzdhZTU2Lm1wNCJdLCBbInN0YXJ0cy13aXRoIiwgIiRDb250ZW50LVR5cGUiLCAidmlkZW8vbXA0Il0sIFsiY29udGVudC1sZW5ndGgtcmFuZ2UiLCAwLCAxMDk5NTExNjI3Nzc2XV19" \
      -F Signature="ysqDemlKXKr6hKzVFP0hCGgf/cs=" \
      -F acl="public-read" \
      -F key="projects/6e/63/6e63b752a1854dde885b5cc472edf569/uploads/videos/2d/81/2d81c30ce62f4dfdb501dbca96c7ae56.mp4" \
      -F file="@my_video_file.mp4"
    ```
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoupload-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videoupload-post-openapi.md
- name: SYNQ Video - Return embeddable url to an uploader widget
  x-api-slug: videouploader-post
  description: Returns an embeddable url, that contains an uploader widget that allows
    you to easily upload any mp4. Great way to simplify the uploading process for
    end users.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/synq-video-logo.png
  humanURL: https://www.synq.fm
  baseURL: https://api.synq.fm//v1
  tags: Videos, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videouploader-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/synq-video/master/_listings/synq-video/videouploader-post-openapi.md
x-common:
- type: x-website
  url: https://www.synq.fm
- type: x-api-gallery
  url: http://swagger.api.gallery.streamdata.io
- type: x-api-stack
  url: http://synq.video.stack.network
- type: x-blog
  url: https://blog.synq.fm/
- type: x-github
  url: https://github.com/SYNQfm
- type: x-twitter
  url: https://twitter.com/synqfm
- type: x-website
  url: http://synq.fm
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---