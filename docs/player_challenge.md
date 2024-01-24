---
sidebar_position: 6
---
# Completing A Challenge For A Player

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

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

