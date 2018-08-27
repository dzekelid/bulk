---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Views Bulk create decks and cards
  version: 1.0.0
  description: Bulk create decks and cards.
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /decks/bulkCreateCardsAndDecks:
    post:
      summary: Bulk create decks and cards
      description: Bulk create decks and cards.
      operationId: postDecksBulkcreatecardsanddecks
      x-api-path-slug: decksbulkcreatecardsanddecks-post
      parameters:
      - in: body
        name: decks
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Create
      - Decks
      - Cards
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