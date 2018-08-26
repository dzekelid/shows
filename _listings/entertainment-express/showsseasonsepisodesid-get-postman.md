{
  "info": {
    "name": "Entertainment Express Returns an Episode object for a requested Episode ID.",
    "_postman_id": "9034d19a-82d3-4469-a272-79cb215728f3",
    "description": "Returns the episode details for a specific episode ID.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Changes",
      "item": [
        {
          "id": "b30b17d3-07ad-43ab-a3aa-21447e19ee2e",
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
              "id": "037b1959-e8bf-4af4-a83e-f4c7694ab66c"
            }
          ]
        },
        {
          "id": "ae7504d3-02e1-4006-a0aa-4111d54120b9",
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
              "id": "89560f73-1f74-4572-b9ae-040ec24e233e"
            }
          ]
        }
      ]
    },
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "2ac4a6c2-7d23-4756-80f3-35d1d49a4c5b",
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
              "id": "fe1f5468-3c7d-4e21-8c34-07d093a781c0"
            }
          ]
        }
      ]
    },
    {
      "name": "Shows",
      "item": [
        {
          "id": "2eb1bc86-7dfc-4c52-90fe-17a34aa3a96b",
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
              "id": "755aabc8-2570-4cd4-9392-d8d7e90dbe31"
            }
          ]
        }
      ]
    }
  ]
}