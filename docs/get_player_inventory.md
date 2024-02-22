---
sidebar_position: 8
---
# Getting Player's Inventory

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

This endpoint returns player's inventory for a game

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
      "amount": 0
    }
  ]
}
```
