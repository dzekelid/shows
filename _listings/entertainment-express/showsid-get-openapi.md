---
swagger: "2.0"
x-collection-name: Entertainment Express
x-complete: 0
info:
  title: Entertainment Express Get Show by Show ID.
  description: "By default the API will only return basic title information. Additional
    objects can be included by passing the object in the Includes parameter.  \n\n\n`Subscriptions
    with \"Limited\" data will only be able to include basic title information, Videos,
    EpisodicVideos, and SeasonVideos.`"
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
  /GoWatchIt/Shows/{Id}/Availabilities:
    get:
      summary: Get GoWatchItShow Availability.
      description: Returns GoWatchIt show availability by Entertainment Show ID.  Special
        permission is required to access this endpoint. Please contact [Sales](mailto:Sales@InternetVideoArchive.com)
        for more information.
      operationId: GetGoWatchItShowAvailabilities
      x-api-path-slug: gowatchitshowsidavailabilities-get
      parameters:
      - in: query
        name: ApiKey
        description: Required GoWatchIt API key
      - in: path
        name: Id
        description: Required ID of Entertainment Show
      responses:
        200:
          description: OK
      tags:
      - GoWatchIt
      - Shows
      - Id
      - Availabilities
  /Shows/All:
    get:
      summary: Returns a paged list of all TV shows.
      description: "By default the API will only return basic title information. Additional
        objects can be included by passing the object in the Includes parameter. \n\n\n`Subscriptions
        with \"Limited\" data will only be able to include basic title information,
        Videos, EpisodicVideos, and SeasonVideos.`"
      operationId: GetAllShows
      x-api-path-slug: showsall-get
      parameters:
      - in: query
        name: Includes
        description: List of additional objects to include in the show object
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
      - Shows
  /Shows/AlternateIdTypes:
    get:
      summary: Get all AlternateIdTypes.
      description: 'Alternate Id types refer to the 3rd party ID sets IVA data has
        matched.  **Ex: IMDB**'
      operationId: GetShowAlternateIdTypes
      x-api-path-slug: showsalternateidtypes-get
      responses:
        200:
          description: OK
      tags:
      - Shows
      - AlternateIdTypes
  /Shows/Match/:
    get:
      summary: Perform a match to Entertainment using Title, Year, Cast and Director.
        Returns best match and score for the match.
      description: Use to match IVA show data to another data source using title,
        director, cast, etc.
      operationId: MatchToShow
      x-api-path-slug: showsmatch-get
      parameters:
      - in: query
        name: AlternateTitles
        description: Alternate Titles of Show to be matched
      - in: query
        name: Cast
        description: Cast members of Show to be matched
      - in: query
        name: Directors
        description: Directors of Show to be matched
      - in: query
        name: StringDistance
        description: For fuzzy title match, default is 4, set to 0 for no fuzzy match
      - in: query
        name: Title
        description: Title of Show to be matched
      - in: query
        name: Year
        description: Release Year of Show to be matched
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Match
  /Shows/ReleaseTypes:
    get:
      summary: Returns a list of Show Release Types.
      description: Release types refer to the type of release and are used in the
        releases object for a show.
      operationId: GetShowReleaseTypes
      x-api-path-slug: showsreleasetypes-get
      responses:
        200:
          description: OK
      tags:
      - Shows
      - ReleaseTypes
  /Shows/SearchAndDiscover:
    get:
      summary: Search and discover shows.
      description: |-
        Searchable Fields: Title, AlternateTitles, Genres, Tags, Cast, Directors, Descriptions, Ratings, OriginalLanguage. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)

        Filterable Fields: Id, Title, AlternateTitles, Genres, OriginalAirDate, Year, Tags, Cast, Directors, Descriptions, HasVideo, ImageFilePath, Ratings, OriginalLanguage, Created, Modified, NumberOfSeasons, NumberOfEpisodes. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)
      operationId: SearchAndDiscoverShow
      x-api-path-slug: showssearchanddiscover-get
      parameters:
      - in: query
        name: Filter
        description: Expression to filter results
      - in: query
        name: IncludeTotalResultCount
        description: Includes total results in response
      - in: query
        name: OrderBy
        description: List of field names to sort results
      - in: query
        name: SearchFields
        description: List of field names to search using term
      - in: query
        name: SearchMode
        description: Specifies whether ANY or ALL of the search terms must be matched
          in order to count the item as a match
      - in: query
        name: SelectFields
        description: List of field names to be returned in the object
      - in: query
        name: Skip
        description: Skip number of results
      - in: query
        name: term
        description: Term to search for
      - in: query
        name: Top
        description: Limit results
      responses:
        200:
          description: OK
      tags:
      - Shows
      - SearchAndDiscover
  /Shows/Season/:
    get:
      summary: Get Season by ShowId and Season Number.
      description: Use the IVA ShowId and a season number to get a season details
        and video asset data.
      operationId: GetSeasonByNumber
      x-api-path-slug: showsseason-get
      parameters:
      - in: query
        name: Id
        description: Id of a Show
      - in: query
        name: SeasonNumber
        description: Number of a Season belonging to a Show
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Season
  /Shows/Seasons/Episode/:
    get:
      summary: Get Episode by ShowId, Season Number and Episode Number.
      description: Some use cases find it useful to be able to pass a season number
        and episode number of a known show to get the data for that exact episode.
      operationId: GetEpisodeByNumber
      x-api-path-slug: showsseasonsepisode-get
      parameters:
      - in: query
        name: EpisodeNumber
        description: Required EpisodeNumber
      - in: query
        name: Id
        description: Required Id of the Show
      - in: query
        name: SeasonNumber
        description: Required SeasonNumber
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Seasons
      - Episode
  /Shows/Seasons/Episodes/{Id}:
    get:
      summary: Returns an Episode object for a requested Episode ID.
      description: Returns the episode details for a specific episode ID.
      operationId: GetEpisode
      x-api-path-slug: showsseasonsepisodesid-get
      parameters:
      - in: path
        name: Id
        description: Required ID of an Episode
      - in: query
        name: Includes
        description: List of additional objects to include in the episode response
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Seasons
      - Episodes
      - Id
  /Shows/Seasons/{Id}:
    get:
      summary: Get Season by SeasonId.
      description: Use with a SeasonId to return details for a season including any
        video asset data.
      operationId: GetSeason
      x-api-path-slug: showsseasonsid-get
      parameters:
      - in: path
        name: Id
        description: Id of a Season
      - in: query
        name: Includes
        description: List of additional objects to include in the season response
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Seasons
      - Id
  /Shows/ShowCertifications:
    get:
      summary: Returns a list of Show Certifications.
      description: List of Show Certifications and definitions.
      operationId: GetShowCertifications
      x-api-path-slug: showsshowcertifications-get
      responses:
        200:
          description: OK
      tags:
      - Shows
      - ShowCertifications
  /Shows/ShowGenres:
    get:
      summary: Get all Show Genres.
      description: Returns a list of all the show genres used in the IVA database.
      operationId: GetShowGenres
      x-api-path-slug: showsshowgenres-get
      responses:
        200:
          description: OK
      tags:
      - Shows
      - ShowGenres
  /Shows/{Id}:
    get:
      summary: Get Show by Show ID.
      description: "By default the API will only return basic title information. Additional
        objects can be included by passing the object in the Includes parameter.  \n\n\n`Subscriptions
        with \"Limited\" data will only be able to include basic title information,
        Videos, EpisodicVideos, and SeasonVideos.`"
      operationId: GetShow
      x-api-path-slug: showsid-get
      parameters:
      - in: path
        name: Id
        description: Required ID of Show
      - in: query
        name: Includes
        description: List of additional objects to include in the show response
      responses:
        200:
          description: OK
      tags:
      - Shows
      - Id
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