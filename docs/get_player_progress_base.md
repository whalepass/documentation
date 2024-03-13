---
sidebar_position: 11
---
# Getting Player's Base Progress 

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

Unlike https://www.whalepass.gg/documentation/get_player_progress, 
This endpoint returns a lean response where you can get users basic progress elements like currentExp and lastCompletedLevel

To test a specific DRAFT Battlepass, add X-Battlepass-Id header to request

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
