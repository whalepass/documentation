---
sidebar_position: 11
---
# Getting Player's Base Progress 

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

Unlike https://www.whalepass.gg/documentation/get_player_progress, 
This endpoint returns a lean response where you can get users basic progress elements like currentExp and lastCompletedLevel

To test a specific DRAFT Battlepass, add X-Battlepass-Id header to request

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns                            |
| Request Param   | playerId         | \{ "playerId": "string" \}             | You can find in response                                            |
| Request Param   | gameId           | \{ "gameId": "string" \}               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|

Request:
```http
GET https://api.whalepass.gg/players/{playerId}/progress/base?gameId={gameId}
```

Expected Response:
```http
{
  "playerId": "string",
  "externalPlayerId": "string",
  "gameId": "string",
  "battlepassId": "string",
  "currentExp": 0,
  "lastCompletedLevel": 0
}
```
