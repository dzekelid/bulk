---
swagger: "2.0"
x-collection-name: Kaltura
x-complete: 0
info:
  title: Kaltura VPaaS Get Service Bulkupload Bulk Action List
  description: List bulk upload batch jobs
  version: 3.3.0
host: www.kaltura.com
basePath: /api_v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /service/bulkupload_bulk/action/abort:
    get:
      summary: Get Service Bulkupload Bulk Action Abort
      description: Aborts the bulk upload and all its child jobs
      operationId: bulk.abort
      x-api-path-slug: servicebulkupload-bulkactionabort-get
      parameters:
      - in: query
        name: id
        description: job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Bulkupload
      - Bulk
      - Action
      - Abort
  /service/bulkupload_bulk/action/get:
    get:
      summary: Get Service Bulkupload Bulk Action Get
      description: Get bulk upload batch job by id
      operationId: bulk.get
      x-api-path-slug: servicebulkupload-bulkactionget-get
      parameters:
      - in: query
        name: id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Bulkupload
      - Bulk
      - Action
      - Get
  /service/bulkupload_bulk/action/list:
    get:
      summary: Get Service Bulkupload Bulk Action List
      description: List bulk upload batch jobs
      operationId: bulk.list
      x-api-path-slug: servicebulkupload-bulkactionlist-get
      parameters:
      - in: query
        name: bulkUploadFilter[advancedSearch][attribute]
        description: 'Enum Type: `KalturaBaseEntryCompareAttribute`'
      - in: query
        name: bulkUploadFilter[advancedSearch][categoriesMatchOr]
      - in: query
        name: bulkUploadFilter[advancedSearch][categoryEntryStatusIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][categoryIdEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][comparison]
        description: 'Enum Type: `KalturaSearchConditionComparison`'
      - in: query
        name: bulkUploadFilter[advancedSearch][contentLike]
      - in: query
        name: bulkUploadFilter[advancedSearch][contentMultiLikeAnd]
      - in: query
        name: bulkUploadFilter[advancedSearch][contentMultiLikeOr]
      - in: query
        name: bulkUploadFilter[advancedSearch][cuePointsFreeText]
      - in: query
        name: bulkUploadFilter[advancedSearch][cuePointSubTypeEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][cuePointTypeIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][depthGreaterThanEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][distributionProfileId]
      - in: query
        name: bulkUploadFilter[advancedSearch][distributionSunStatus]
        description: 'Enum Type: `KalturaEntryDistributionSunStatus`'
      - in: query
        name: bulkUploadFilter[advancedSearch][entryDistributionFlag]
        description: 'Enum Type: `KalturaEntryDistributionFlag`'
      - in: query
        name: bulkUploadFilter[advancedSearch][entryDistributionStatus]
        description: 'Enum Type: `KalturaEntryDistributionStatus`'
      - in: query
        name: bulkUploadFilter[advancedSearch][entryDistributionValidationErrors]
        description: Comma seperated validation error types
      - in: query
        name: bulkUploadFilter[advancedSearch][extendedStatusEqual]
        description: 'Enum Type: `KalturaUserEntryExtendedStatus`'
      - in: query
        name: bulkUploadFilter[advancedSearch][extendedStatusIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][field]
      - in: query
        name: bulkUploadFilter[advancedSearch][hasEntryDistributionValidationErrors]
      - in: query
        name: bulkUploadFilter[advancedSearch][idEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][idIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][indexIdGreaterThan]
      - in: query
        name: bulkUploadFilter[advancedSearch][isQuiz]
        description: 'Enum Type: `KalturaNullableBoolean`'
      - in: query
        name: bulkUploadFilter[advancedSearch][items]
      - in: query
        name: bulkUploadFilter[advancedSearch][memberIdEq]
      - in: query
        name: bulkUploadFilter[advancedSearch][memberIdIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][memberPermissionsMatchAnd]
      - in: query
        name: bulkUploadFilter[advancedSearch][memberPermissionsMatchOr]
      - in: query
        name: bulkUploadFilter[advancedSearch][metadataProfileId]
      - in: query
        name: bulkUploadFilter[advancedSearch][noDistributionProfiles]
      - in: query
        name: bulkUploadFilter[advancedSearch][not]
      - in: query
        name: bulkUploadFilter[advancedSearch][objectType]
      - in: query
        name: bulkUploadFilter[advancedSearch][orderBy]
        description: 'Enum Type: `KalturaCategoryEntryAdvancedOrderBy`'
      - in: query
        name: bulkUploadFilter[advancedSearch][type]
        description: 'Enum Type: `KalturaSearchOperatorType`'
      - in: query
        name: bulkUploadFilter[advancedSearch][updatedAtGreaterThanOrEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][updatedAtLessThanOrEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][userIdEqual]
      - in: query
        name: bulkUploadFilter[advancedSearch][userIdIn]
      - in: query
        name: bulkUploadFilter[advancedSearch][value]
      - in: query
        name: bulkUploadFilter[advancedSearch][watermarkId]
      - in: query
        name: bulkUploadFilter[bulkUploadObjectTypeEqual]
        description: 'Enum Type: `KalturaBulkUploadObjectType`'
      - in: query
        name: bulkUploadFilter[bulkUploadObjectTypeIn]
      - in: query
        name: bulkUploadFilter[orderBy]
      - in: query
        name: bulkUploadFilter[statusEqual]
        description: 'Enum Type: `KalturaBatchJobStatus`'
      - in: query
        name: bulkUploadFilter[statusIn]
      - in: query
        name: bulkUploadFilter[uploadedOnEqual]
      - in: query
        name: bulkUploadFilter[uploadedOnGreaterThanOrEqual]
      - in: query
        name: bulkUploadFilter[uploadedOnLessThanOrEqual]
      - in: query
        name: No Name
      - in: query
        name: pager[pageIndex]
        description: The page number for which {pageSize} of objects should be retrieved
          (Default is 1)
      - in: query
        name: pager[pageSize]
        description: The number of objects to retrieve
      responses:
        200:
          description: OK
      tags:
      - Service
      - Bulkupload
      - Bulk
      - Action
      - List
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