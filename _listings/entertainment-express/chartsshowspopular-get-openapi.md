---
swagger: "2.0"
x-collection-name: Entertainment Express
x-complete: 0
info:
  title: Entertainment Express Returns a list of shows based on popularity.
  description: Requires Skip and Take. Maximum page size is 100.
  version: "2.0"
host: ee.iva-api.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Changes/Shows/History/:
    get:
      summary: Returns list of unique ShowId changes greater than or equal to date
        (UTC).
      description: All new and updated shows from requested date and time.  When a
        record gets updated, use the ID to get the full show object and replace the
        data in your cache.
      operationId: GetShowChangeHistory
      x-api-path-slug: changesshowshistory-get
      parameters:
      - in: query
        name: Date
        description: Starting date
      - in: query
        name: Skip
        description: Offset for paging
      - in: query
        name: Take
        description: Maximum number of rows returned
      responses:
        200:
          description: OK
      tags:
      - Changes
      - Shows
      - History
  /Changes/Shows/HistoryWithEntity/:
    get:
      summary: Returns list of unique ShowId and Entity changes greater than or equal
        to date (UTC).
      description: Returns a list of ShowId and entity of any show that has been updated.
      operationId: GetShowChangeHistoryWithEntity
      x-api-path-slug: changesshowshistorywithentity-get
      parameters:
      - in: query
        name: Date
        description: Starting date
      - in: query
        name: Skip
        description: Offset for paging
      - in: query
        name: Take
        description: Maximum number of rows returned
      responses:
        200:
          description: OK
      tags:
      - Changes
      - Shows
      - HistoryWithEntity
  /Charts/Shows/Popular:
    get:
      summary: Returns a list of shows based on popularity.
      description: Requires Skip and Take. Maximum page size is 100.
      operationId: GetChartShowsPopular
      x-api-path-slug: chartsshowspopular-get
      parameters:
      - in: query
        name: Skip
        description: Skips records using for paging results
      - in: query
        name: Take
        description: Limits the total items returned
      responses:
        200:
          description: OK
      tags:
      - Charts
      - Shows
      - Popular
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