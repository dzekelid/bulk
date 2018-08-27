swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/documentgeneration/bulkgrouplistcommunication:
    post:
      summary: Generates a bulk communication pack out to multiple clients in a list.
      description: Generates a bulk communication pack out to multiple clients in
        a list..
      operationId: DocumentGeneration_BulkGroupListCommunicationBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationbulkgrouplistcommunication-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Bulk
      - Communication
      - Pack
      - Out
      - To
      - Multiple
      - Clients
      - In
      - List
  /api/documentgeneration/bulkinterestrolecommunication:
    post:
      summary: Generates a bulk communication pack out to multiple clients with interest
        roles.
      description: Generates a bulk communication pack out to multiple clients with
        interest roles..
      operationId: DocumentGeneration_BulkInterestRoleCommunicationBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationbulkinterestrolecommunication-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Bulk
      - Communication
      - Pack
      - Out
      - To
      - Multiple
      - Clients
      - Interest
      - Roles
  /api/documentgeneration/bulkpropertyownercommunication:
    post:
      summary: "Generates a bulk communication pack out to multiple vendors of properties.\r\nThis
        will ignore the target type set, as the document could only ever find the
        vendor as the contact item, so it always defaults\r\nto a target type of vendor/owner"
      description: "Generates a bulk communication pack out to multiple vendors of
        properties.\r\nthis will ignore the target type set, as the document could
        only ever find the vendor as the contact item, so it always defaults\r\nto
        a target type of vendor/owner."
      operationId: DocumentGeneration_BulkPropertyVendorCommunicationBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationbulkpropertyownercommunication-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Bulk
      - Communication
      - Pack
      - Out
      - To
      - Multiple
      - Vendors
      - Of
      - Properties
      - This
      - Will
      - Ignore
      - Target
      - Type
      - Set
      - ""
      - As
      - Document
      - Could
      - Only
      - Ever
      - Find
      - Vendor
      - As
      - Contact
      - Item
      - ""
      - So
      - It
      - Always
      - "Defaults\r\nTo"
      - Target
      - Type
      - Of
      - Vendor
      - Owner
  /api/group/archivegroups:
    post:
      summary: Archive groups in bulk
      description: Archive groups in bulk.
      operationId: Group_ArchiveGroupsBydeleteCommand
      x-api-path-slug: apigrouparchivegroups-post
      parameters:
      - in: body
        name: deleteCommand
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Archive
      - Groups
      - In
      - Bulk
  /api/role/pausesearchingroles:
    post:
      summary: Pauses searching roles in bulk (by Id)
      description: Pauses searching roles in bulk (by id).
      operationId: Role_PauseSearchingRolesBysearchingRoleIds
      x-api-path-slug: apirolepausesearchingroles-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: searchingRoleIds
        description: Ids of the searching roles to pause
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Pauses
      - Searching
      - Roles
      - In
      - Bulk
      - (by
      - Id)
  /api/role/unpausesearchingroles:
    post:
      summary: UnPauses searching roles in bulk (by Id)
      description: Unpauses searching roles in bulk (by id).
      operationId: Role_UnPauseSearchingRolesBysearchingRoleIds
      x-api-path-slug: apiroleunpausesearchingroles-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: searchingRoleIds
        description: Ids of the searching roles to pause
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - UnPauses
      - Searching
      - Roles
      - In
      - Bulk
      - (by
      - Id)