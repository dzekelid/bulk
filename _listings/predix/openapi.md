swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
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