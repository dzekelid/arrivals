---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Mode mode  Arrivals
  description: Gets the next arrival predictions for all stops of a given mode.
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