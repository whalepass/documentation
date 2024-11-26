---
sidebar_position: 9
---
# Getting Player's Inventory

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

This endpoint returns player's inventory for a game

| Token Type   | Location         | Format                               | Where To Find                              |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key     |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns   |
| Path Field   | playerId         | { "playerId": "string" }             | You can find in response                   |
| Path Field   | gameId           | { "gameId": "string" }               | https://dashboard.whalepass.gg/game-actions|

Request:
```http
GET https://api.whalepass.gg/players/{playerId}/inventory?gameId={gameId}
```

Expected Response:
```http
{
  "gameId": "string",
  "playerId": "string",
  "externalPlayerId": "string",
  "items": [
    {
      "rewardId": "string",
      "battlepassId": "string",
      "name": "string",
      "amount": 0,
      "mediaUrl": "string"
    }
  ]
}
```
