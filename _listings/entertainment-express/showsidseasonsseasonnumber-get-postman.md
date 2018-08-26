{
  "info": {
    "name": "Entertainment Express Get Season by ShowId and Season Number.",
    "_postman_id": "90a19dd7-d933-446d-98e2-155c3a188cc8",
    "description": "Depreciated. Use GetSeasonBySeasonNumber instead.  Requires a valid ShowId and Season Number.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "eaf34847-8eb0-43b1-b459-dd384094c9c9",
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
              "id": "f570834f-c547-4f7d-abb9-7aadbbe7b22f"
            }
          ]
        },
        {
          "id": "016db472-ac9e-46be-8179-dc9c38eb7ab9",
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
              "id": "71f8661a-ff61-451e-a11d-f54c2d0da06c"
            }
          ]
        }
      ]
    },
    {
      "name": "Charts",
      "item": [
        {
          "id": "e5552e2d-65f0-447b-9bfc-9c6057a6dad5",
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
              "id": "b854be71-2e46-4614-8617-160d0f85246f"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "ebd17dd2-0889-4691-85c4-f3c320ac5c25",
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
              "id": "fd8f2c8a-33e2-4107-ab99-2223ec970565"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "7739ed39-ecde-4883-8cd9-6ce8c665b579",
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
              "id": "e2055810-52c1-4b74-9f8d-b0cfdc7c1473"
            }
          ]
        },
        {
          "id": "3e7a6c0e-4bde-40bb-9653-6f9f592e991f",
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
              "id": "fa691b03-36fe-47ff-ac84-06643f5740bd"
            }
          ]
        },
        {
          "id": "077bc996-34bc-4a29-9f44-8c31b8dc2af8",
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
              "id": "91a547c8-4429-4fcb-9d54-fce357d9773b"
            }
          ]
        },
        {
          "id": "c61baf44-5483-4158-950d-dd589affded7",
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
              "id": "3bb8ef90-4f64-4927-89e2-a450e471a224"
            }
          ]
        },
        {
          "id": "53c8daee-6555-412b-831d-5174b9d05d2e",
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
              "id": "74c386f1-a011-44b9-85e4-53f713153dab"
            }
          ]
        },
        {
          "id": "2ce5d899-5cc8-498a-ab44-ade3ac55961c",
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
              "id": "22b8417f-1535-4e00-9704-a9b789e7fbb4"
            }
          ]
        },
        {
          "id": "305784ba-0975-413a-bbc1-6bedaaf590b8",
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
              "id": "28dafbac-a2fc-4e4f-be49-117f208bc54f"
            }
          ]
        },
        {
          "id": "112a07c8-876e-467b-bca8-1478b967eddf",
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
              "id": "ea67aa0e-f951-4746-9f0b-bccbb16d4fba"
            }
          ]
        },
        {
          "id": "b06981bc-1f14-41ac-afe7-cd63d71d1e66",
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
              "id": "bbe5b15c-22a2-491e-99b4-d15e5f743848"
            }
          ]
        },
        {
          "id": "ffe82eed-3f1a-44ac-b81f-978f98d316e5",
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
              "id": "597bfdaf-e2a6-4d9f-a00c-3da17493a775"
            }
          ]
        },
        {
          "id": "a15e97e8-a7e9-478f-a50f-5007ca3cac3e",
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
              "id": "1007b2e6-a702-4d70-bff9-b96577e1680c"
            }
          ]
        },
        {
          "id": "3edd98d8-86d3-42ee-8105-9215d5682c7f",
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
              "id": "f7ea1679-7fbd-4c85-9da8-35d98c0fbe47"
            }
          ]
        },
        {
          "id": "b2a1f2d3-d952-4127-908b-17cf7537e4cc",
          "name": "GetSeasonBySeasonNumber",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Shows/:Id/Seasons/:SeasonNumber"
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
                },
                {
                  "id": "SeasonNumber",
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
            "description": "Depreciated. Use GetSeasonBySeasonNumber instead.  Requires a valid ShowId and Season Number."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8f3af8d-a211-49a6-834f-9520a6a116dd"
            }
          ]
        }
      ]
    }
  ]
}