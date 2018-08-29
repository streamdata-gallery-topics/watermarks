---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Remove Watermark on File
  description: Used to remove the watermark for a corresponding Box file.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /files/{FILE_ID}/watermark:
    get:
      summary: Get Watermark on File
      description: Used to retrieve the watermark for a corresponding Box file.
      operationId: getFileWatermark
      x-api-path-slug: filesfile-idwatermark-get
      parameters:
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Watermark
    put:
      summary: Apply Watermark on File
      description: Used to apply or update the watermark for a corresponding Box file.
        The endpoint accepts a JSON body describing the watermark to apply.
      operationId: updateFileWatermark
      x-api-path-slug: filesfile-idwatermark-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Watermark
    delete:
      summary: Remove Watermark on File
      description: Used to remove the watermark for a corresponding Box file.
      operationId: deleteFileWatermark
      x-api-path-slug: filesfile-idwatermark-delete
      parameters:
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Watermark
  /folders/{FOLDER_ID}/watermark:
    get:
      summary: Get Watermark on Folder
      description: Used to retrieve the watermark for a corresponding Box folder.
      operationId: getFolderWatermark
      x-api-path-slug: foldersfolder-idwatermark-get
      parameters:
      - in: path
        name: FOLDER_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
      - ""
      - Watermark
    put:
      summary: Apply Watermark on Folder
      description: Used to apply or update the watermark for a corresponding Box folder.
        The endpoints accepts a JSON body describing the watermark to apply.
      operationId: updateFolderWatermark
      x-api-path-slug: foldersfolder-idwatermark-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: FOLDER_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
      - ""
      - Watermark
    delete:
      summary: Remove Watermark on Folder
      description: Used to remove the watermark for a corresponding Box Folder.
      operationId: deleteFolderWatermark
      x-api-path-slug: foldersfolder-idwatermark-delete
      parameters:
      - in: path
        name: FOLDER_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
      - ""
      - Watermark
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