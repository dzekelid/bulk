---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Bulk get users
  description: Returns details of users specified in a list of usernames or keys.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=). Users with permission to access Jira can call
    this method, but empty search results are returned.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/issue/properties/{propertyKey}:
    put:
      summary: Bulk set issue property
      description: |-
        Allows to set a property for all issues identified by a given filter. Only entities the user has permissions to edit will be updated.

        Currently the following filters are available:

        *   **entityIds** \- A list of issues to update. Only issues with ids from this list will be considered for updating. This is an optional filter, if not provided, then any editable issue that matches all other filters will be updated.
        *   **currentValue** \- If provided, then only issues with the property currently set to that value will be updated.
        *   **hasProperty** \- If true, then only existing properties will be updated. If false, then only issues that do not have any value associated with this property will be updated. If omitted, the property will be set on all issues, regardless of whether it previously existed or not.

        If more than one filter is given, then they are all joined with the logical "and", that is: only issues that satisfy all filters are updated. If no filters are provided at all, then the property will be updated on _all_ issues editable by the caller (i.e. issues in projects with the EDIT_ISSUES permission).

        If an invalid combination of filters is provided, an error will be returned by the API. For example, specifying the current value and "hasProperty" to "false" would never match any issues (as it would mean: update this property if the current value is something, oh, but only if there is no value at all) and is therefore not allowed.

        This method is [asynchronous](#async), meaning that it will not return the results immediately, instead creating a task to perform the requested update operation (unless preliminary validation, e.g. of the provided filter, fails).

        The operation is transactional: either all eligible issues are updated, or none (if there are any errors).
      operationId: com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkSetIssueProperty_put
      x-api-path-slug: api2issuepropertiespropertykey-put
      parameters:
      - in: path
        name: propertyKey
        description: The key of the property to update
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Set
      - Issue
      - Property
    delete:
      summary: Bulk delete issue property
      description: Allows to delete a property from all issues identified by a given
        filter. Only entities the user has permissions to edit will be updated. See
        the [issue property bulk set endpoint documentation](#api-api-2-issue-properties-propertyKey-put)
        for more details.
      operationId: com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkDeleteIssueProperty_delete
      x-api-path-slug: api2issuepropertiespropertykey-delete
      parameters:
      - in: path
        name: propertyKey
        description: The key of the property to delete
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Delete
      - Issue
      - Property
  /api/2/user/bulk:
    get:
      summary: Bulk get users
      description: Returns details of users specified in a list of usernames or keys.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=). Users with permission to access Jira can
        call this method, but empty search results are returned.
      operationId: com.atlassian.jira.rest.v2.user.UserBulkResource.bulkGetUsers_get
      x-api-path-slug: api2userbulk-get
      parameters:
      - in: query
        name: key
        description: Comma-separated list of user keys
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: Comma-separated list of usernames
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Get
      - Users
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