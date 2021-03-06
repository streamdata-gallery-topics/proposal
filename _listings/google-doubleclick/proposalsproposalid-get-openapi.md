---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Get Proposal
  version: 1.0.0
  description: Get a proposal given its id
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /privateauction/{privateAuctionId}/updateproposal:
    post:
      summary: Update Proposal
      description: Update a given private auction proposal
      operationId: adexchangebuyer.marketplaceprivateauction.updateproposal
      x-api-path-slug: privateauctionprivateauctionidupdateproposal-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: privateAuctionId
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Proposal
  /proposals/insert:
    post:
      summary: Insert Proposal
      description: Create the given list of proposals
      operationId: adexchangebuyer.proposals.insert
      x-api-path-slug: proposalsinsert-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Proposal
  /proposals/search:
    get:
      summary: Search Proposal
      description: Search for proposals using pql query
      operationId: adexchangebuyer.proposals.search
      x-api-path-slug: proposalssearch-get
      parameters:
      - in: query
        name: pqlQuery
        description: Query string to retrieve specific proposals
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Proposal
  /proposals/{proposalId}:
    get:
      summary: Get Proposal
      description: Get a proposal given its id
      operationId: adexchangebuyer.proposals.get
      x-api-path-slug: proposalsproposalid-get
      parameters:
      - in: path
        name: proposalId
        description: Id of the proposal to retrieve
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Proposal
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