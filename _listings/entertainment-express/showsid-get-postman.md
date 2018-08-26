{
  "info": {
    "name": "Entertainment Express Get Show by Show ID.",
    "_postman_id": "43479613-1994-4c31-b53b-9b3aaa84de1d",
    "description": "By default the API will only return basic title information. Additional objects can be included by passing the object in the Includes parameter.  \n\n\n`Subscriptions with \"Limited\" data will only be able to include basic title information, Videos, EpisodicVideos, and SeasonVideos.`",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "f1f798e8-a00b-46e4-bc5c-9c13ad49b32b",
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
              "id": "b4fa2d10-9e0e-474c-a0c0-c9ad8f1901bc"
            }
          ]
        },
        {
          "id": "42297731-4ac6-4715-bd90-ce8bddb27e0e",
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
              "id": "78de90d9-6289-4ab5-8f8d-5638c2719518"
            }
          ]
        }
      ]
    },
    {
      "name": "Charts",
      "item": [
        {
          "id": "7263d309-465b-49a5-85d6-1e04d1b89c00",
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
              "id": "51bd6a23-cc6a-4b99-914d-b89be5f22b89"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "93db81ef-7b76-4e8c-8df5-40e709172fa0",
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
              "id": "3c6b1fb4-540b-4cbf-9501-4b3c83913110"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "b146efcf-4765-4241-b0ac-88ee4ed76867",
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
              "id": "66775651-0a06-4ef3-9f48-efe5079475b9"
            }
          ]
        },
        {
          "id": "20bf025f-0acd-4df9-ba08-49b736b35925",
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
              "id": "829158aa-5c9c-41cf-a5ca-b58ea7a83818"
            }
          ]
        },
        {
          "id": "6b0f9b47-e6ae-4127-bcfc-8a02e5c0f0d9",
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
              "id": "0fa316cc-b517-4c8d-b505-6d6fe8217d0a"
            }
          ]
        },
        {
          "id": "9046f90b-29ba-45b0-b66e-2ab026246694",
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
              "id": "d2ae26d2-cf94-4f55-aa7e-478aa2d91e72"
            }
          ]
        },
        {
          "id": "727bef97-de4e-4c43-bee9-1ff612aef2e2",
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
              "id": "a660efed-e175-40e6-a5df-a6e1f8d08dc8"
            }
          ]
        },
        {
          "id": "cd65be9e-122c-4158-9e84-67c16e5d8904",
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
              "id": "9c1e6f56-bc54-4f76-a378-f248a2f6a84d"
            }
          ]
        },
        {
          "id": "f0ea3e43-c3a0-4020-90f0-9571ff8d2a0b",
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
              "id": "500b1af6-61a0-4094-9175-6cfda57764bc"
            }
          ]
        },
        {
          "id": "2d30dc8b-53a7-4356-9eae-85987f467bdf",
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
              "id": "7b83980e-a45a-4e08-afc0-efd914a9cfb3"
            }
          ]
        },
        {
          "id": "8a4a0034-c29c-4120-a03b-88621f289b9b",
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
              "id": "33b9c829-e87d-415c-8f0b-01652a389eff"
            }
          ]
        },
        {
          "id": "77e59e40-28cc-44c2-932e-a2ce4cc9b1fc",
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
              "id": "63573576-9e32-43b2-a594-b51bdb755f03"
            }
          ]
        },
        {
          "id": "0d9b1f09-d730-46bf-a8aa-c7e5d2ca5d01",
          "name": "GetShowGenres",
          "request": {
            "url": "http://ee.iva-api.com/Shows/ShowGenres",
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
            "description": "Returns a list of all the show genres used in the IVA database."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a179943-9601-447c-b69f-0c52bded9199"
            }
          ]
        },
        {
          "id": "656fcca4-94a0-4a9a-bb62-0df6370ee8c1",
          "name": "GetShow",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Shows/:Id"
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
            "description": "By default the API will only return basic title information. Additional objects can be included by passing the object in the Includes parameter.  \n\n\n`Subscriptions with \"Limited\" data will only be able to include basic title information, Videos, EpisodicVideos, and SeasonVideos.`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "af5ef530-4b65-4463-b38a-e37344f23ab8"
            }
          ]
        }
      ]
    }
  ]
}