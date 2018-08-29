swagger: "2.0"
x-collection-name: YouTube
x-complete: 1
info:
  title: YouTube
  description: youtube-allows-users-to-upload-view-rate-share-add-to-favorites-report-comment-on-videos-and-subscribe-to-other-users--it-offers-a-wide-variety-of-usergenerated-and-corporate-media-videos--available-content-includes-video-clips-tv-show-clips-music-videos-short-and-documentary-films-audio-recordings-movie-trailers-live-streams-and-other-content-such-as-video-blogging-short-original-videos-and-educational-videos--most-of-the-content-on-youtube-is-uploaded-by-individuals-but-media-corporations-including-cbs-the-bbc-vevo-and-hulu-offer-some-of-their-material-via-youtube-as-part-of-the-youtube-partnership-program--unregistered-users-can-only-watch-videos-on-the-site-while-registered-users-are-permitted-to-upload-an-unlimited-number-of-videos-and-add-comments-to-videos-
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