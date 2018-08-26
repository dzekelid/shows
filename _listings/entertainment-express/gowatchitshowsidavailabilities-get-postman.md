{
  "info": {
    "name": "Entertainment Express Get GoWatchItShow Availability.",
    "_postman_id": "827fdb2b-7a20-4845-b8eb-9af670b4c971",
    "description": "Returns GoWatchIt show availability by Entertainment Show ID.  Special permission is required to access this endpoint. Please contact [Sales](mailto:Sales@InternetVideoArchive.com) for more information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "GoWatchIt",
      "item": [
        {
          "id": "ce7afa1a-f7ee-447c-8e3a-2dfba96c3221",
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
              "id": "2e843536-4913-43a7-a16e-52fb40382179"
            }
          ]
        },
        {
          "id": "727b72b3-67e0-490b-a9d9-c62b758eafdd",
          "name": "GetGoWatchItMovieAvailabilities",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "GoWatchIt/Movies/:Id/Availabilities"
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
            "description": "Returns GoWatchIt movie availability by Entertainment Movie ID.  Special permission is required to access this endpoint.  Contact [Sales](mailto:Sales@InternetVideoArchive.com) for more information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "016ae9e1-2ebc-4c45-8ead-4afbcaf8bd29"
            }
          ]
        },
        {
          "id": "2ed06ac8-b037-4eb7-8d67-53283e4a2a09",
          "name": "GetGoWatchItSeasonAvailabilities",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ee.iva-api.com",
              "path": [
                "GoWatchIt/Seasons/:Id/Availabilities"
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
            "description": "Returns GoWatchIt season availability by Entertainment Season ID.  Special permission is required to access this endpoint.  Contact [Sales](mailto:Sales@InternetVideoArchive.com) for more information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c4ba61b-098a-4570-902b-883a457535b3"
            }
          ]
        },
        {
          "id": "8a0d8880-2692-4dff-bf7e-c246d8b6eae0",
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
              "id": "e366a82f-9bd3-41de-8c3f-6f046b9c455d"
            }
          ]
        }
      ]
    }
  ]
}