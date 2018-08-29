---
swagger: "2.0"
x-collection-name: YouTube
x-complete: 0
info:
  title: Youtube Add Watermarks Unset
  description: Deletes a channel's watermark image.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: 1.0.0
host: www.googleapis.com
basePath: /youtube/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /watermarks/set:
    post:
      summary: Add Watermarks Set
      description: Uploads a watermark image to YouTube and sets it for a channel.
      operationId: postWatermarksSet
      x-api-path-slug: watermarksset-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: channelId
        description: The channelId parameter specifies the YouTube channel ID for
          which the watermark is being provided
      - in: query
        name: onBehalfOfContentOwner
        description: 'Note: This parameter is intended exclusively for YouTube content
          partners'
      responses:
        200:
          description: OK
      tags:
      - Watermarks
      - Set
  /watermarks/unset:
    post:
      summary: Add Watermarks Unset
      description: Deletes a channel's watermark image.
      operationId: postWatermarksUnset
      x-api-path-slug: watermarksunset-post
      parameters:
      - in: query
        name: channelId
        description: The channelId parameter specifies the YouTube channel ID for
          which the watermark is being unset
      - in: query
        name: onBehalfOfContentOwner
        description: 'Note: This parameter is intended exclusively for YouTube content
          partners'
      responses:
        200:
          description: OK
      tags:
      - Watermarks
      - Unset
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---