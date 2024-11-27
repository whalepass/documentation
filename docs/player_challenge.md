---
sidebar_position: 6
---
# Completing A Challenge For A Player

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns                            |
| Path Field   | playerId         | { "playerId": "string" }             | You can find in response                                            |
| Body Field   | gameId           | { "gameId": "string" }               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|
| Body Field   | challengeId      | { "challengeId": "string" }          | https://dashboard.whalepass.gg/campaigns                            |

Request:
```http
POST https://api.whalepass.gg/players/{playerId}/progress/challenge
{
  "gameId": "string",
  "challengeId": "string"
}
```

> Expected response: 200 OK



| ⚠️ Warning                                                         |
|--------------------------------------------------------------------|
|This endpoint doesn't accept battlepassId in the request body anymore. It will work for the ACTIVE Battlepass of the game in the request body. To test specific DRAFT Battlepass, add X-Battlepass-Id header to request|

