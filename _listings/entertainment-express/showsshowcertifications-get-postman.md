{
  "info": {
    "name": "Entertainment Express Returns a list of Show Certifications.",
    "_postman_id": "8330e8c7-8a95-4079-ac26-d42db1316882",
    "description": "List of Show Certifications and definitions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "28d9a5d9-101c-41ab-b499-bad8b4030732",
          "name": "GetShowChangeHistory",
          "request": {
            "url": "http://ee.iva-api.com/Changes/Shows/History/?Date=%7B%7D&Skip=%7B%7D&Take=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "All new and updated shows from requested date and time.  When a record gets updated, use the ID to get the full show object and replace the data in your cache."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d182d53-f6b1-4f15-9372-25430f884db3"
            }
          ]
        },
        {
          "id": "a7a225d6-5cfb-482a-b02d-09152ffec711",
          "name": "GetShowChangeHistoryWithEntity",
          "request": {
            "url": "http://ee.iva-api.com/Changes/Shows/HistoryWithEntity/?Date=%7B%7D&Skip=%7B%7D&Take=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of ShowId and entity of any show that has been updated."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "63d29256-a897-4dcb-96cf-beeaf60cb1da"
            }
          ]
        }
      ]
    },
    {
      "name": "Charts",
      "item": [
        {
          "id": "cb3de37c-29af-4080-9f10-92e94f2f4566",
          "name": "GetChartShowsPopular",
          "request": {
            "url": "http://ee.iva-api.com/Charts/Shows/Popular?Skip=%7B%7D&Take=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Requires Skip and Take. Maximum page size is 100."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f910cfb4-5d6e-4df7-808d-595f68cc6f26"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "762edd40-19a4-44d6-83a9-6f542f8a8b38",
          "name": "GetGoWatchItShowAvailabilities",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "GoWatchIt/Shows/:Id/Availabilities"
              ],
              "query": [
                {
                  "key": "ApiKey",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "Id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns GoWatchIt show availability by Entertainment Show ID.  Special permission is required to access this endpoint. Please contact [Sales](mailto:Sales@InternetVideoArchive.com) for more information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "407d1f21-8a46-4b45-a85a-a4a9aaca1d4f"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "0c29c055-dc35-4299-929c-6bcc35d95753",
          "name": "GetAllShows",
          "request": {
            "url": "http://ee.iva-api.com/Shows/All?Includes=%7B%7D&Skip=%7B%7D&Take=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "By default the API will only return basic title information. Additional objects can be included by passing the object in the Includes parameter. \n\n\n`Subscriptions with \"Limited\" data will only be able to include basic title information, Videos, EpisodicVideos, and SeasonVideos.`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a73bc6a-8397-49de-bf2b-de3344287c67"
            }
          ]
        },
        {
          "id": "0f87ddab-94ce-40ec-9ba7-23349bf4bcad",
          "name": "GetShowAlternateIdTypes",
          "request": {
            "url": "http://ee.iva-api.com/Shows/AlternateIdTypes",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Alternate Id types refer to the 3rd party ID sets IVA data has matched.  **Ex: IMDB**"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c06d924-b193-4d20-bd78-508f66df4374"
            }
          ]
        },
        {
          "id": "3049b3a5-367f-4a27-94b6-7bb6039b6507",
          "name": "MatchToShow",
          "request": {
            "url": "http://ee.iva-api.com/Shows/Match/?AlternateTitles=%7B%7D&Cast=%7B%7D&Directors=%7B%7D&StringDistance=%7B%7D&Title=%7B%7D&Year=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use to match IVA show data to another data source using title, director, cast, etc."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16219f73-be1c-4788-8ea0-23cafd43dea4"
            }
          ]
        },
        {
          "id": "2ac9b485-a30e-456c-9d35-d4f03e0ee72d",
          "name": "GetShowReleaseTypes",
          "request": {
            "url": "http://ee.iva-api.com/Shows/ReleaseTypes",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Release types refer to the type of release and are used in the releases object for a show."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fc42981-c5ad-401c-bed4-6fe2014b84b3"
            }
          ]
        },
        {
          "id": "817190b5-8d19-4172-825c-211a57fdbb78",
          "name": "SearchAndDiscoverShow",
          "request": {
            "url": "http://ee.iva-api.com/Shows/SearchAndDiscover?Filter=%7B%7D&IncludeTotalResultCount=%7B%7D&OrderBy=%7B%7D&SearchFields=%7B%7D&SearchMode=%7B%7D&SelectFields=%7B%7D&Skip=%7B%7D&term=%7B%7D&Top=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Searchable Fields: Title, AlternateTitles, Genres, Tags, Cast, Directors, Descriptions, Ratings, OriginalLanguage. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)\n\nFilterable Fields: Id, Title, AlternateTitles, Genres, OriginalAirDate, Year, Tags, Cast, Directors, Descriptions, HasVideo, ImageFilePath, Ratings, OriginalLanguage, Created, Modified, NumberOfSeasons, NumberOfEpisodes. [Syntax Ref](https://docs.microsoft.com/en-us/rest/api/searchservice/simple-query-syntax-in-azure-search)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4252a392-b850-42f9-ab62-c1db5a4bcf82"
            }
          ]
        },
        {
          "id": "c52e5222-5c01-4959-aea0-e4b7531f2855",
          "name": "GetSeasonByNumber",
          "request": {
            "url": "http://ee.iva-api.com/Shows/Season/?Id=%7B%7D&SeasonNumber=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use the IVA ShowId and a season number to get a season details and video asset data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b0726251-0070-43c7-a872-370b2e81bd5d"
            }
          ]
        },
        {
          "id": "199f9ce4-324d-411f-a920-7c1f1ebe0d14",
          "name": "GetEpisodeByNumber",
          "request": {
            "url": "http://ee.iva-api.com/Shows/Seasons/Episode/?EpisodeNumber=%7B%7D&Id=%7B%7D&SeasonNumber=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Some use cases find it useful to be able to pass a season number and episode number of a known show to get the data for that exact episode."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9bac93e-5e67-4cbc-9678-a8e3122f8344"
            }
          ]
        },
        {
          "id": "f85d3bd8-9419-43b1-8cf9-56e29ffd3787",
          "name": "GetEpisode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Shows/Seasons/Episodes/:Id"
              ],
              "query": [
                {
                  "key": "Includes",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "Id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the episode details for a specific episode ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a2f9dd83-b6e2-4f14-9d9e-d09fb1891cf4"
            }
          ]
        },
        {
          "id": "f61567e0-6c76-44d1-9e47-7609e12ef6e8",
          "name": "GetSeason",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Shows/Seasons/:Id"
              ],
              "query": [
                {
                  "key": "Includes",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "Id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use with a SeasonId to return details for a season including any video asset data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9bbbdc78-a410-467c-b83b-ceafb4fe136d"
            }
          ]
        },
        {
          "id": "636f88cc-146c-4f11-8ef0-4db4e1c8f70d",
          "name": "GetShowCertifications",
          "request": {
            "url": "http://ee.iva-api.com/Shows/ShowCertifications",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List of Show Certifications and definitions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07314512-1594-4628-8197-91c8cbf8ad88"
            }
          ]
        }
      ]
    }
  ]
}