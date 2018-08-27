---
swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 0
info:
  title: Amazon EC2 Systems Manager API Put Inventory
  version: 1.0.0
  description: Bulk update custom inventory items on one more instance.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=PutInventory:
    get:
      summary: Put Inventory
      description: Bulk update custom inventory items on one more instance.
      operationId: putInventory
      x-api-path-slug: actionputinventory-get
      parameters:
      - in: query
        name: InstanceId
        description: One or more instance IDs where you want to add or update inventory
          items
        type: string
      - in: query
        name: Items
        description: The inventory items that you want to add or update on instances
        type: string
      responses:
        200:
          description: OK
      tags:
      - Inventory
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