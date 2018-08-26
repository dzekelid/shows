---
swagger: "2.0"
x-collection-name: Spreaker
x-complete: 1
info:
  title: Spreaker API
  version: v1
host: api.spreaker.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/{query}:
    get:
      summary: Search users, shows and episodes
      description: Search users, shows and episodes
      operationId: getSearchQuery
      x-api-path-slug: searchquery-get
      parameters:
      - in: path
        name: query
        description: Search query
      responses:
        200:
          description: OK
      tags:
      - Podcasts
      - Search
      - Users
      - ""
      - Shows
      - Episodes
  /show/search/{query}:
    get:
      summary: Search Shows
      description: This API allows to find shows.
      operationId: getShowSearchQuery
      x-api-path-slug: showsearchquery-get
      parameters:
      - in: path
        name: query
        description: Search query
      responses:
        200:
          description: OK
      tags:
      - Podcasts
      - Search
      - Shows
  /user/{user_id}/shows/author:
    get:
      summary: GEt Shows By Author
      description: ""
      operationId: getUserUserShowsAuthor
      x-api-path-slug: useruser-idshowsauthor-get
      parameters:
      - in: path
        name: user_id
        description: The user id
      responses:
        200:
          description: OK
      tags:
      - Podcasts
      - GEt
      - Shows
      - Author
  /user/{user_id}/shows/fan:
    get:
      summary: Get Favorite Shows
      description: Retrieves the list of shows whose authors are followed by <user_id>.
      operationId: getUserUserShowsFan
      x-api-path-slug: useruser-idshowsfan-get
      parameters:
      - in: query
        name: latest_episode
        description: True (1) to enable the export of the latest episode
      - in: path
        name: user_id
        description: The user id
      responses:
        200:
          description: OK
      tags:
      - Podcasts
      - Favorite
      - Shows
---