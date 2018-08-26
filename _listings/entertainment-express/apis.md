---
name: Entertainment Express
x-slug: entertainment-express
description: Internet Video Archive (IVA) is a leading entertainment data company
  providing metadata, images and trailers/clips, for movie and TV content. With the
  launch of its award-winning Entertainment Express APIs, clients can easily access
  everything they need to create engaging content discovery experiences. By using
  Entertainment Express, clients can also connect to other services like movie showtimes
  and ticketing, content recommendations, content availability and TV channel line-ups.
  With over a million titles, episodes and over 150,000 videos available, IVA makes
  it easy for developers to integrate all the services they need at a very affordable
  price.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Shows
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/apis.md
specificationVersion: "0.14"
apis:
- name: Entertainment Express - Returns list of unique ShowId changes greater than
    or equal to date (UTC).
  x-api-slug: changesshowshistory-get
  description: All new and updated shows from requested date and time.  When a record
    gets updated, use the ID to get the full show object and replace the data in your
    cache.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/changesshowshistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/changesshowshistory-get-openapi.md
- name: Entertainment Express - Returns list of unique ShowId and Entity changes greater
    than or equal to date (UTC).
  x-api-slug: changesshowshistorywithentity-get
  description: Returns a list of ShowId and entity of any show that has been updated.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/changesshowshistorywithentity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/changesshowshistorywithentity-get-openapi.md
- name: Entertainment Express - Returns a list of shows based on popularity.
  x-api-slug: chartsshowspopular-get
  description: Requires Skip and Take. Maximum page size is 100.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/chartsshowspopular-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/chartsshowspopular-get-openapi.md
- name: Entertainment Express - Get GoWatchItShow Availability.
  x-api-slug: gowatchitshowsidavailabilities-get
  description: Returns GoWatchIt show availability by Entertainment Show ID.  Special
    permission is required to access this endpoint. Please contact [Sales](mailto:Sales@InternetVideoArchive.com)
    for more information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/gowatchitshowsidavailabilities-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/gowatchitshowsidavailabilities-get-openapi.md
- name: Entertainment Express - Returns a paged list of all TV shows.
  x-api-slug: showsall-get
  description: "By default the API will only return basic title information. Additional
    objects can be included by passing the object in the Includes parameter. \n\n\n`Subscriptions
    with \"Limited\" data will only be able to include basic title information, Videos,
    EpisodicVideos, and SeasonVideos.`"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsall-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsall-get-openapi.md
- name: Entertainment Express - Get all AlternateIdTypes.
  x-api-slug: showsalternateidtypes-get
  description: 'Alternate Id types refer to the 3rd party ID sets IVA data has matched.  **Ex:
    IMDB**'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsalternateidtypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsalternateidtypes-get-openapi.md
- name: Entertainment Express - Perform a match to Entertainment using Title, Year,
    Cast and Director. Returns best match and score for the match.
  x-api-slug: showsmatch-get
  description: Use to match IVA show data to another data source using title, director,
    cast, etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsmatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsmatch-get-openapi.md
- name: Entertainment Express - Returns a list of Show Release Types.
  x-api-slug: showsreleasetypes-get
  description: Release types refer to the type of release and are used in the releases
    object for a show.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsreleasetypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsreleasetypes-get-openapi.md
- name: Entertainment Express - Search and discover shows.
  x-api-slug: showssearchanddiscover-get
  description: |-
    Searchable Fields: Title, AlternateTitles, Genres, Tags, Cast, Directors, Descriptions, Ratings, OriginalLanguage. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)

    Filterable Fields: Id, Title, AlternateTitles, Genres, OriginalAirDate, Year, Tags, Cast, Directors, Descriptions, HasVideo, ImageFilePath, Ratings, OriginalLanguage, Created, Modified, NumberOfSeasons, NumberOfEpisodes. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showssearchanddiscover-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showssearchanddiscover-get-openapi.md
- name: Entertainment Express - Get Season by ShowId and Season Number.
  x-api-slug: showsseason-get
  description: Use the IVA ShowId and a season number to get a season details and
    video asset data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseason-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseason-get-openapi.md
- name: Entertainment Express - Get Episode by ShowId, Season Number and Episode Number.
  x-api-slug: showsseasonsepisode-get
  description: Some use cases find it useful to be able to pass a season number and
    episode number of a known show to get the data for that exact episode.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsepisode-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsepisode-get-openapi.md
- name: Entertainment Express - Returns an Episode object for a requested Episode
    ID.
  x-api-slug: showsseasonsepisodesid-get
  description: Returns the episode details for a specific episode ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsepisodesid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsepisodesid-get-openapi.md
- name: Entertainment Express - Get Season by SeasonId.
  x-api-slug: showsseasonsid-get
  description: Use with a SeasonId to return details for a season including any video
    asset data.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsseasonsid-get-openapi.md
- name: Entertainment Express - Returns a list of Show Certifications.
  x-api-slug: showsshowcertifications-get
  description: List of Show Certifications and definitions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsshowcertifications-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsshowcertifications-get-openapi.md
- name: Entertainment Express - Get all Show Genres.
  x-api-slug: showsshowgenres-get
  description: Returns a list of all the show genres used in the IVA database.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsshowgenres-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsshowgenres-get-openapi.md
- name: Entertainment Express - Get Show by Show ID.
  x-api-slug: showsid-get
  description: "By default the API will only return basic title information. Additional
    objects can be included by passing the object in the Includes parameter.  \n\n\n`Subscriptions
    with \"Limited\" data will only be able to include basic title information, Videos,
    EpisodicVideos, and SeasonVideos.`"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsid-get-openapi.md
- name: Entertainment Express - Get Season by ShowId and Season Number.
  x-api-slug: showsidseasonsseasonnumber-get
  description: Depreciated. Use GetSeasonBySeasonNumber instead.  Requires a valid
    ShowId and Season Number.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsidseasonsseasonnumber-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsidseasonsseasonnumber-get-openapi.md
- name: Entertainment Express - Get Episode by ShowId, Season Number and Episode Number.
  x-api-slug: showsidseasonsseasonnumberepisodesepisodenumber-get
  description: Requires a valid ShowId, Season Number and Episode Number.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsidseasonsseasonnumberepisodesepisodenumber-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/showsidseasonsseasonnumberepisodesepisodenumber-get-openapi.md
- name: 'Entertainment Express - '
  x-api-slug: tvmediagenresshows-get
  description: Gets list of show genres.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/IVA-logo.png
  humanURL: https://www.internetvideoarchive.com/
  baseURL: https://ee.iva-api.com//
  tags: Celebrities, Movies, General Data, Televisions, Videos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/tvmediagenresshows-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/shows/master/_listings/entertainment-express/tvmediagenresshows-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://emuseum.api.docs.api.gallery.streamdata.io
- type: x-api-stack
  url: http://entertainment.express.stack.network
- type: x-blog
  url: https://www.internetvideoarchive.com/blog/
- type: x-developer
  url: https://developer.iva-api.com/
- type: x-pricing
  url: https://www.internetvideoarchive.com/pricing/
- type: x-website
  url: https://www.internetvideoarchive.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---