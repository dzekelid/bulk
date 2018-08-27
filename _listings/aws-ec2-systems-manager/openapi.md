swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 1
info:
  title: AWS EC2 Systems Manager API
  version: 1.0.0
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