{
  "info": {
    "name": "Spreaker API Search users, shows and episodes",
    "_postman_id": "607d1b74-e28b-4ca7-8ca8-488becd5af3d",
    "description": "Search users, shows and episodes",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "ea2df7cf-67ba-45e0-8a3e-b90935d5177a",
          "name": "getSearchQuery",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.spreaker.com",
              "path": [
                "search/:query"
              ],
              "variable": [
                {
                  "id": "query",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search users, shows and episodes"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "448de371-2e76-4236-8eea-dec5f6eb98d3"
            }
          ]
        }
      ]
    }
  ]
}