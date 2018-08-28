---
swagger: "2.0"
x-collection-name: SAP
x-complete: 0
info:
  title: SAP Manufacturing Network Customer APIs Updates a supplier's production option
  description: "Updates a production option proposed by the additive manufacturing
    supplier.    \nThis endpoint is used by users from the additive manufactuirng
    supplier that're not collaboration leads. The initial pricing cannot be updated."
  version: 1.0.0
host: hostname
basePath: /dim/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /collaborationRooms/{collaborationRoomId}/productionData/{productionDataId}:
    put:
      summary: Updates a supplier's production option
      description: "Updates a production option proposed by the additive manufacturing
        supplier as well as the initial pricing for this option.  \nThe login user
        must be a collaboration lead from the additive manufacturing supplier."
      operationId: updates-a-production-option-proposed-by-the-additive-manufacturing-supplier-as-well-as-the-initial-p
      x-api-path-slug: collaborationroomscollaborationroomidproductiondataproductiondataid-put
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: path
        name: productionDataId
        description: The ID of a production option
      - in: body
        name: ProductionDataUpdateRequest
        description: A request about updating a production option
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Suppliers
      - Production
      - Option
    delete:
      summary: Deletes a supplier's production option
      description: "Deletes a production option proposed by the additive manufacturing
        supplier. The initial pricing is deleted along with it.  \nThe login user
        must be from the additive manufacturing supplier."
      operationId: deletes-a-production-option-proposed-by-the-additive-manufacturing-supplier-the-initial-pricing-is-d
      x-api-path-slug: collaborationroomscollaborationroomidproductiondataproductiondataid-delete
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: path
        name: productionDataId
        description: The ID of a production option
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Suppliers
      - Production
      - Option
  /collaborationRooms/{collaborationRoomId}/productionData/{productionDataId}/basic:
    put:
      summary: Updates a supplier's production option
      description: "Updates a production option proposed by the additive manufacturing
        supplier.    \nThis endpoint is used by users from the additive manufactuirng
        supplier that're not collaboration leads. The initial pricing cannot be updated."
      operationId: updates-a-production-option-proposed-by-the-additive-manufacturing-supplier----this-endpoint-is-used
      x-api-path-slug: collaborationroomscollaborationroomidproductiondataproductiondataidbasic-put
      parameters:
      - in: body
        name: AdditionalProductionDataBasicUpdateRequest
        description: A request about updating a suppliers production option, excluding
          pricing information
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: path
        name: productionDataId
        description: The ID of a production option
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Suppliers
      - Production
      - Option
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