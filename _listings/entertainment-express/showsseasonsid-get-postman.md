{
  "info": {
    "name": "Entertainment Express Get Season by SeasonId.",
    "_postman_id": "21a76a27-cee0-444e-8cbe-bf59ae32482c",
    "description": "Use with a SeasonId to return details for a season including any video asset data.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "050c51f2-0bf4-48ba-b0a4-b2645641e31a",
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
              "id": "37548ba2-21d2-4eb7-9eea-948570d72008"
            }
          ]
        },
        {
          "id": "9057bdf1-05a5-41f4-a16d-68c397ba9831",
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
              "id": "544eeed3-f1e4-4324-9e21-e06911bb38e6"
            }
          ]
        }
      ]
    },
    {
      "name": "Charts",
      "item": [
        {
          "id": "81ec757f-dffd-4a55-ab81-ae24c3cac032",
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
              "id": "4509c597-0b23-4d40-a7e0-5dac0e9c2a9a"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "ac15770c-0430-4a42-8983-c2890ce99a78",
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
              "id": "2f049ed2-d60a-466a-a445-6d220b940f9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "6aa53264-3c04-4add-af09-a3b93751cc70",
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
              "id": "2ac993ba-bf1a-41e9-a89b-b2b6abf3bc13"
            }
          ]
        },
        {
          "id": "5150fec9-0022-48bc-8034-2da03e0d74fa",
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
              "id": "fa27110f-d193-4be6-a8fe-f4ccb60ce93e"
            }
          ]
        },
        {
          "id": "9b2b4b92-9be2-4fee-b9e2-b44aa8ca7c22",
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
              "id": "3022f05b-7d99-411b-afcd-c391f6c3e2c7"
            }
          ]
        },
        {
          "id": "19c832bd-953d-4296-9344-3329b15e2c81",
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
              "id": "da7fd7a3-b945-4001-ac06-943bf6387c19"
            }
          ]
        },
        {
          "id": "4f9048ac-1b65-4ad8-97b3-cbd662a821b0",
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
              "id": "3ee56e1d-1079-49ac-bf9d-92b6c8ca1915"
            }
          ]
        },
        {
          "id": "8b869262-ee1c-45dc-997c-051e5cb1dd83",
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
              "id": "f72a3d2f-8425-4c23-8175-9bb35482b348"
            }
          ]
        },
        {
          "id": "65170262-543a-4711-85c9-fbe65a327d07",
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
              "id": "d16f02e1-e392-465b-a35c-20d9e385be8d"
            }
          ]
        },
        {
          "id": "4eee7751-9ad5-4ee7-9bd8-57d7fe261eeb",
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
              "id": "0be1bd57-9835-42f0-b47f-b959fb99454d"
            }
          ]
        },
        {
          "id": "4eeade10-cfdc-47a3-ad7b-34967a41d7c9",
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
              "id": "dcf929ef-1602-465d-9214-52e98c8dd866"
            }
          ]
        }
      ]
    }
  ]
}