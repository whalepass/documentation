---
sidebar_position: 4
---
# Incrementing A Player's Experience Points (HARDCODE)

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

This table outlines the token types and body fields required for API requests, their locations, formats, and where to find or provide the necessary values.

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns                            |
| Path Field   | playerId         | { "playerId": "string" }             | You can find in response                                            |
| Body Field   | gameId           | { "gameId": "string" }               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|
| Body Field   | additionalExp    | { "additionalExp": Int }             | Provided by the user                                                |


Request:
```http
POST https://api.whalepass.gg/players/{playerId}/progress/exp
{
  "gameId": "string",
  "additionalExp": 0
}
```

> Expected response: 200 OK



| ⚠️ Warning                                                         |
|--------------------------------------------------------------------|
|This endpoint doesn't accept **battlepassId** in the request body anymore. It will work for the ACTIVE battlepass of the game in the request body. To test specific DRAFT Battlepass, add X-Battlepass-Id header to request|

