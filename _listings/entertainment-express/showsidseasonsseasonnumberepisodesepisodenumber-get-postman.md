{
  "info": {
    "name": "Entertainment Express Get Episode by ShowId, Season Number and Episode Number.",
    "_postman_id": "e0712da6-6bb5-41ad-ae87-65fd47d8b8b6",
    "description": "Requires a valid ShowId, Season Number and Episode Number.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "6ad2f496-342d-4f6a-93e9-614f67d26e6f",
          "name": "GetEpisodeChangeHistory",
          "request": {
            "url": "http://ee.iva-api.com/Changes/Episodes/History/?Date=%7B%7D&Skip=%7B%7D&Take=%7B%7D",
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
            "description": "For each updated episode ID, pull the full episode data for that ID and update."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e7e51037-8ef8-4f3a-8689-7518f4bff902"
            }
          ]
        },
        {
          "id": "48806644-7bf3-427e-ba3e-918537d98903",
          "name": "GetEpisodeChangeHistoryWithEntity",
          "request": {
            "url": "http://ee.iva-api.com/Changes/Episodes/HistoryWithEntity/?Date=%7B%7D&Skip=%7B%7D&Take=%7B%7D",
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
            "description": "Lists each episode ID that has changed as well as the entity in the object that changed."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e8185b6-b9c9-434d-b988-0f7071fbda97"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "9dae1588-217b-4176-86a9-251b36362842",
          "name": "GetGoWatchItEpisodeAvailabilities",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "GoWatchIt/Episodes/:Id/Availabilities"
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
            "description": "Returns GoWatchit episode availability by Entertainment Episode ID. Special permission is required to access this endpoint."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d6a92527-882b-4093-a5e8-ea4845c39fda"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "a5667c67-5cb9-48c4-ab3b-44c8a4a9145e",
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
              "id": "2aca02db-faf7-4146-b5ef-df3e096be6dd"
            }
          ]
        },
        {
          "id": "4f9add20-0791-4755-b892-be563dac5982",
          "name": "GetEpisodeByEpisodeNumber",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "Shows/:Id/Seasons/:SeasonNumber/Episodes/:EpisodeNumber"
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
                  "id": "EpisodeNumber",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Requires a valid ShowId, Season Number and Episode Number."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8bbe5cb-e10b-4f0b-b540-d5a3fa481247"
            }
          ]
        },
        {
          "id": "98b0841d-0c1e-4ae4-adcb-7ff64fa60953",
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
              "id": "5da85ede-cddf-43e8-8888-0bf28811e2de"
            }
          ]
        }
      ]
    }
  ]
}