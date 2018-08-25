---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 1
info:
  title: Transport for London Unified
  description: our-unified-api-brings-together-data-across-all-modes-of-transport-into-a-single-restful-api--this-api-provides-access-to-the-most-highly-requested-realtime-and-status-infomation-across-all-the-modes-of-transport-in-a-single-and-consistent-way--access-to-the-developer-documentation-is-available-at-httpsapi-tfl-gov-uk
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Line/{ids}/Arrivals/{stopPointId}:
    get:
      summary: Line s  Arrivals stop Point Id
      description: Get the list of arrival predictions for given line ids based at
        the given stop.
      operationId: Line_Arrivals
      x-api-path-slug: lineidsarrivalsstoppointid-get
      parameters:
      - in: query
        name: destinationStationId
        description: Optional
      - in: query
        name: direction
        description: Optional
      - in: path
        name: ids
        description: A comma-separated list of line ids e
      - in: path
        name: stopPointId
        description: Optional
      responses:
        200:
          description: OK
      tags:
      - Line
      - S
      - ""
      - Arrivals
      - Stop
      - Point
      - Id
  /Mode/{mode}/Arrivals:
    get:
      summary: Mode mode  Arrivals
      description: Gets the next arrival predictions for all stops of a given mode.
      operationId: Mode_Arrivals
      x-api-path-slug: modemodearrivals-get
      parameters:
      - in: query
        name: count
        description: A number of arrivals to return for each stop, -1 to return all
          available
      - in: path
        name: mode
        description: A mode name e
      responses:
        200:
          description: OK
      tags:
      - Mode
      - Mode
      - ""
      - Arrivals
  /StopPoint/{id}/Arrivals:
    get:
      summary: Stop Point  Arrivals
      description: Gets the list of arrival predictions for the given stop point id.
      operationId: StopPoint_Arrivals
      x-api-path-slug: stoppointidarrivals-get
      parameters:
      - in: path
        name: id
        description: A StopPoint id (station naptan code e
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Point
      - ""
      - Arrivals
  /Vehicle/{ids}/Arrivals:
    get:
      summary: Vehicle s  Arrivals
      description: Gets the predictions for a given list of vehicle id's..
      operationId: Vehicle_Get
      x-api-path-slug: vehicleidsarrivals-get
      parameters:
      - in: path
        name: ids
        description: A comma-separated list of vehicle ids e
      responses:
        200:
          description: OK
      tags:
      - Vehicle
      - S
      - ""
      - Arrivals
  /Line/{ids}/Arrivals:
    get:
      summary: Line s  Arrivals
      description: Get the list of arrival predictions for given line ids based at
        the given stop.
      operationId: ""
      x-api-path-slug: lineidsarrivals-get
      parameters:
      - in: path
        name: ids
        description: A comma-separated list of line ids e
      - in: query
        name: stopPointId
        description: Id of stop to get arrival predictions for (station naptan code
          e
      responses:
        200:
          description: OK
      tags:
      - Line
      - S
      - ""
      - Arrivals
---