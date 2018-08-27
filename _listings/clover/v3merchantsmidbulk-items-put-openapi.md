---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Update existing inventory items.
  version: 1.0.0
  description: This API is to going to update only the changes present in the payload.
    Not going to replace the existing inventory items. Use the POST HTTP method to
    create inventory items.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/bulk_items:
    post:
      summary: Create multiple inventory items.
      description: This API is to create multiple inventory items.  Use the PATCH
        HTTP method to update existing inventory items.
      operationId: BulkCreateInventoryItems
      x-api-path-slug: v3merchantsmidbulk-items-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Bulk
      - Items
    put:
      summary: Update existing inventory items.
      description: This API is to going to update only the changes present in the
        payload. Not going to replace the existing inventory items. Use the POST HTTP
        method to create inventory items.
      operationId: BulkPatchInventoryItems
      x-api-path-slug: v3merchantsmidbulk-items-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Bulk
      - Items
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